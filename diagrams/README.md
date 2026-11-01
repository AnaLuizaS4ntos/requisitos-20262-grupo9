# 📐 Modelagem UML — Portal de Internacionalização (`requisitos-20262-grupo9`)

Esta pasta reúne todos os diagramas UML do **Projeto 4 — Portal de Internacionalização**, cobrindo tanto os entregáveis da **Atividade 1 (P1)** quanto todas as issues de modelagem da **Milestone M1 (`[US] Criar diagrama de casos de uso`, `[US] Criar diagrama de classes`, `[US] Criar diagrama de sequência`, Componentes e Implantação)**.

---

## 1. Diagrama de Casos de Uso

> Fonte PlantUML também disponível em: [diagrama-casos-de-uso.puml](diagrama-casos-de-uso.puml)

```mermaid
flowchart LR
    subgraph Atores["Atores"]
        AT01["👤 AT-01: Estudante Unifor (Outgoing)"]
        AT02["👤 AT-02: Docente / Pesquisador"]
        AT03["👤 AT-03: Estudante Internacional (Incoming)"]
        AT05["👤 AT-05: Coordenador de Curso"]
        AT04["👤 AT-04: Gestor de Conteúdo da DRI"]
        AT06["🖥️ AT-06: Autenticação Institucional"]
    end

    subgraph Portal["Sistema: Portal de Internacionalização Unifor"]
        UC01(["CDU-01: Consultar Programas de Intercâmbio e Dupla Titulação"])
        UC02(["CDU-02: Gerenciar e Publicar Conteúdos do Portal (Governança DRI)"])
        UC03(["CDU-03: Consultar Guias e Checklists de Vistos e Documentação"])
        UC04(["CDU-04: Consultar Estimativas de Despesas e Guia de Hospedagem"])
        UC05(["CDU-05: Consultar Serviços da DRI e Orientações de Aproveitamento"])
        UC06(["CDU-06: Solicitar Orientação / Atendimento à DRI"])
        UC07(["CDU-07: Gerenciar Solicitações de Orientação"])
        UC08(["CDU-08: Buscar Conteúdos e Alternar Idioma (PT/EN/ES)"])
    end

    AT01 --> UC01
    AT01 --> UC03
    AT01 --> UC04
    AT01 --> UC05
    AT01 --> UC06
    AT01 --> UC08

    AT02 --> UC01
    AT02 --> UC05
    AT02 --> UC06
    AT02 --> UC08

    AT03 --> UC03
    AT03 --> UC04
    AT03 --> UC05
    AT03 --> UC06
    AT03 --> UC08

    AT05 --> UC01
    AT05 --> UC05

    AT04 --> UC02
    AT04 --> UC07
    UC02 -.->|"<<include>>"| AT06
    UC06 -.->|"<<extend>>"| UC05
```

---

## 2. Diagrama de Classes de Domínio

> Arquivo fonte: [diagrama-classes.mmd](diagrama-classes.mmd)

```mermaid
classDiagram
    class InstituicaoParceira {
        +UUID id
        +String nome
        +String pais
        +String cidade
        +String siteOficial
        +Boolean convenioAtivo
    }

    class ProgramaMobilidade {
        +UUID id
        +String titulo
        +TipoMobilidade modalidade
        +NivelIdioma idiomaExigido
        +String duracaoSemestres
        +String preRequisitos
        +StatusPublicacao status
        +Date dataUltimaRevisao
    }

    class CursoUnifor {
        +UUID id
        +String codigoCurso
        +String nomeCurso
        +String centroAcademico
    }

    class GuiaInformativo {
        +UUID id
        +String slug
        +CategoriaGuia categoria
        +PerfilPublico publicoAlvo
        +Boolean exigeDisclaimerLegal
        +StatusPublicacao status
        +Date dataUltimaRevisao
        +Int versao
    }

    class ConteudoTraduzido {
        +UUID id
        +CodigoIdioma idioma
        +String tituloTraduzido
        +String resumo
        +String corpoMarkdown
        +Date dataTraducao
    }

    class ItemChecklistDocumento {
        +UUID id
        +String nomeDocumento
        +String descricaoOrientativa
        +Boolean obrigatorio
        +Int ordemExibicao
    }

    class EstimativaCustoDestino {
        +UUID id
        +String moedaLocal
        +Decimal faixaMoradiaMensal
        +Decimal faixaAlimentacaoMensal
        +Decimal faixaTransporteMensal
        +Decimal faixaSeguroSaude
        +String orientacaoHospedagem
        +Date dataReferenciaCotacao
    }

    class SolicitacaoOrientacao {
        +UUID id
        +String protocolo
        +String nomeSolicitante
        +String emailSolicitante
        +PerfilPublico perfilSolicitante
        +CategoriaGuia temaDuvida
        +String mensagem
        +Boolean consentimentoLGPD
        +StatusAtendimento status
        +DateTime dataCriacao
    }

    class GestorDRI {
        +UUID id
        +String matricula
        +String nome
        +String emailInstitucional
        +String cargo
    }

    class LogGovernanca {
        +UUID id
        +String acaoRealizada
        +DateTime dataHora
        +String observacaoRevisao
    }

    InstituicaoParceira "1" --> "0..*" ProgramaMobilidade : oferece
    InstituicaoParceira "1" --> "0..1" EstimativaCustoDestino : possui referencia
    ProgramaMobilidade "0..*" -- "1..*" CursoUnifor : elegivel para
    GuiaInformativo "1" *-- "1..3" ConteudoTraduzido : traduzido em (PT/EN/ES)
    ProgramaMobilidade "1" *-- "1..3" ConteudoTraduzido : traduzido em (PT/EN/ES)
    GuiaInformativo "1" *-- "0..*" ItemChecklistDocumento : contem checklist
    GestorDRI "1" --> "0..*" GuiaInformativo : publica e revisa
    GestorDRI "1" --> "0..*" ProgramaMobilidade : gerencia
    GestorDRI "1" --> "0..*" SolicitacaoOrientacao : atende
    GestorDRI "1" --> "0..*" LogGovernanca : gera auditoria
```

---

## 3. Diagrama de Sequência — Fluxo Principal (CDU-01: Consulta de Programas e Guias)

> Arquivo fonte: [diagrama-sequencia.mmd](diagrama-sequencia.mmd)

```mermaid
sequenceDiagram
    autonumber
    actor Usuario as AT-01 / AT-02 / AT-03 (Estudante ou Docente)
    participant UI as Interface Web (Portal)
    participant API as API de Catálogo e Conteúdo
    participant I18N as Serviço Multilíngue (i18n)
    participant DB as Banco de Dados (Portal DRI)

    Usuario->>UI: Acessa o Portal e seleciona idioma (PT-BR / EN / ES)
    UI->>API: GET /api/v1/programas?curso=ENG&modalidade=DUPLA_TITULACAO&lang=pt-BR
    API->>DB: Consulta programas publicados (status = PUBLICADO) e cursos elegíveis
    DB-->>API: Retorna lista de acordos e instituições parceiras
    API->>I18N: Verifica disponibilidade de tradução no idioma solicitado (RN-03)
    I18N-->>API: Retorna textos no idioma ou aplica fallback PT-BR com alerta
    API-->>UI: JSON com lista de programas, requisitos e metadados
    UI-->>Usuario: Exibe catálogo filtrado de intercâmbio e dupla titulação

    Usuario->>UI: Clica em um programa para ver Vistos, Aproveitamento e Custos
    UI->>API: GET /api/v1/programas/{id}/guias-vinculados?lang=pt-BR
    API->>DB: Busca checklist de vistos, regras de aproveitamento e estimativa de despesas
    DB-->>API: Retorna dados detalhados + dataUltimaRevisao (RN-02)
    API-->>UI: Payload completo + aviso de caráter orientativo (RN-04, RN-05)
    UI-->>Usuario: Renderiza abas (Requisitos, Visto/Checklist, Aproveitamento, Custos/Hospedagem)
```

---

## 4. Diagrama de Componentes

> Arquivo fonte: [diagrama-componentes.mmd](diagrama-componentes.mmd)

```mermaid
flowchart TB
    subgraph CamadaApresentacao["Camada de Apresentação (Frontend Web Responsivo & Acessível)"]
        UI_Publica["🌐 Portal Público (Guias, Catálogo, Busca, FAQ)"]
        UI_Admin["🛠️ Painel de Governança DRI (CMS Editorial)"]
        Mod_A11y["♿ Módulo de Acessibilidade (WCAG 2.1 AA) & Seletor i18n"]
    end

    subgraph CamadaAplicacao["Camada de Aplicação e Negócio (API Backend)"]
        Comp_Catalogo["📚 Componente de Catálogo (Intercâmbio & Dupla Titulação)"]
        Comp_Guias["🛂 Componente de Guias (Vistos, Aproveitamento, Despesas, Hospedagem)"]
        Comp_Governanca["✅ Componente de Governança Editorial & Versionamento"]
        Comp_Atendimento["📩 Componente de Solicitações de Orientação & FAQ"]
        Comp_Busca["🔍 Motor de Busca Unificada e Filtros"]
    end

    subgraph CamadaDados["Camada de Persistência"]
        DB_Relacional[("🗄️ Banco de Dados Relacional (PostgreSQL)")]
        Storage_Anexos[("📁 Repositório de Arquivos / PDFs (Modelos e Guias)")]
    end

    subgraph ServicosExternos["Sistemas Externos"]
        Auth_Unifor["🔐 Autenticação Institucional (SSO / Unifor Online)"]
        Smtp_Email["📧 Serviço de Notificação por E-mail"]
    end

    UI_Publica --> Mod_A11y
    UI_Publica --> Comp_Catalogo
    UI_Publica --> Comp_Guias
    UI_Publica --> Comp_Atendimento
    UI_Publica --> Comp_Busca

    UI_Admin --> Comp_Governanca
    UI_Admin --> Comp_Atendimento

    Comp_Governanca --> Auth_Unifor
    Comp_Atendimento --> Smtp_Email

    Comp_Catalogo --> DB_Relacional
    Comp_Guias --> DB_Relacional
    Comp_Guias --> Storage_Anexos
    Comp_Governanca --> DB_Relacional
    Comp_Atendimento --> DB_Relacional
    Comp_Busca --> DB_Relacional
```

---

## 5. Diagrama de Implantação

> Arquivo fonte: [diagrama-implantacao.mmd](diagrama-implantacao.mmd)

```mermaid
flowchart LR
    subgraph Cliente["Dispositivo do Usuário (Estudante, Docente, Gestor DRI)"]
        Browser["🌐 Navegador Web (Desktop / Mobile)\nHTTPS (TLS 1.2+)"]
    end

    subgraph InfraUnifor["Ambiente em Nuvem / Infraestrutura Institucional Unifor"]
        CDN["⚡ CDN / Reverse Proxy (WAF & Cache Estático)"]

        subgraph AppServer["Servidor de Aplicação (Container Docker)"]
            FrontendNode["🖥️ Frontend Web Server (SPA / SSR)"]
            BackendAPI["⚙️ API Backend Portal DRI"]
        end

        subgraph DataTier["Camada de Dados e Armazenamento"]
            PostgresDB[("🗄️ Servidor de Banco de Dados\nPostgreSQL (Dados + Auditoria)")]
            ObjectStorage[("📦 Object Storage\n(Documentos PDF e Imagens)")]
        end
    end

    subgraph Externos["Serviços Institucionais Externos"]
        SSOServer["🔐 Servidor de Autenticação Unifor"]
        MailServer["📧 Gateway de E-mail Institucional"]
    end

    Browser -->|"HTTPS (443)"| CDN
    CDN --> FrontendNode
    CDN --> BackendAPI
    BackendAPI -->|"TCP/SSL (5432)"| PostgresDB
    BackendAPI -->|"HTTPS API"| ObjectStorage
    BackendAPI -->|"OAuth2 / OIDC"| SSOServer
    BackendAPI -->|"SMTP / TLS"| MailServer
```
