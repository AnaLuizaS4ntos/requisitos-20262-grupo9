# 🌍 Portal de Internacionalização — Unifor (`requisitos-20262-grupo9`)

Repositório de Engenharia de Requisitos do **Grupo 9** (Semestre 2026.2), referente ao **Projeto 4 do Eixo I — Internacionalização**.

---

## 🎯 Sobre o Projeto

- **Tema:** 4. Portal de Internacionalização
- **Problema a investigar:** Como melhorar a experiência de estudantes e docentes na busca por informações e serviços de internacionalização?
- **Escopo inicial sugerido:** Portal unificado com orientações sobre intercâmbio, dupla titulação, vistos, documentação, aproveitamento de disciplinas, despesas, hospedagem, contatos e serviços da Diretoria de Relações Internacionais (DRI).
- **Questões para levantamento:** Acessibilidade, organização da informação, versões multilíngues e governança de conteúdo.

---

## 📄 Índice de Artefatos Produzidos (Milestone M1 — Trabalho P1)

### 1. Elicitação e Definição de Requisitos (`Requisitos/Elicitacao/`)
- 📘 [Documento de Visão da Demanda (VD)](Requisitos/Elicitacao/VisaoDemanda.md)
- 📖 [Glossário de Termos](Requisitos/Elicitacao/Glossario.md)
- 👥 [Identificação e Matriz de Stakeholders](Requisitos/Elicitacao/Stakeholders.md)
- 🎙️ [Roteiro e Registro de Entrevistas](Requisitos/Elicitacao/RoteiroEntrevistas.md)
- ⚙️ [Especificação de Requisitos Funcionais (RF)](Requisitos/Elicitacao/RequisitosFuncionais.md)
- 📋 [Backlog Priorizado (User Stories)](Requisitos/Elicitacao/BacklogPriorizado.md)

### 2. Especificações de Requisitos, Regras de Negócio e Casos de Uso
- 🛡️ [Especificação de Requisitos Não Funcionais (RNF)](Requisitos/Requisitos%20N%C3%A3o%20Funcionais/RequisitosNaoFuncionais.md)
- ⚖️ [Especificação de Regras de Negócio (RN)](Requisitos/Especifica%C3%A7%C3%A3o%20de%20Regra%20de%20Negocio/RegrasDeNegocio.md)
- 📝 [CDU-01 — Consultar Programas de Mobilidade, Dupla Titulação e Guias de Internacionalização](Requisitos/Especifica%C3%A7%C3%A3o%20de%20Casos%20de%20Uso/CDU-01-Consultar-Guias-Mobilidade-Dupla-Titulacao.md)
- 📝 [CDU-02 — Gerenciar e Publicar Conteúdos do Portal (Governança DRI)](Requisitos/Especifica%C3%A7%C3%A3o%20de%20Casos%20de%20Uso/CDU-02-Gerenciar-Conteudos-Portal-DRI.md)

### 3. Modelagem UML (`diagrams/`)
- 📐 [Documentação Completa dos Diagramas UML (Casos de Uso, Classes, Sequência, Componentes e Implantação)](diagrams/README.md)
  - [Fonte PlantUML — Casos de Uso](diagrams/diagrama-casos-de-uso.puml)
  - [Fonte Mermaid — Diagrama de Classes](diagrams/diagrama-classes.mmd)
  - [Fonte Mermaid — Diagrama de Sequência](diagrams/diagrama-sequencia.mmd)
  - [Fonte Mermaid — Diagrama de Componentes](diagrams/diagrama-componentes.mmd)
  - [Fonte Mermaid — Diagrama de Implantação](diagrams/diagrama-implantacao.mmd)

---

## 📂 Estrutura de Pastas do Repositório

```text
├── diagrams/                              # Diagramas UML (Casos de Uso, Classes, Sequência, Componentes, Implantação)
├── GestaoConfiguracao/                    # Artefatos de gestão de configuração, sprints e versionamento
├── images/                                # Imagens, wireframes e evidências visuais dos protótipos
├── Requisitos/                            # Artefatos de Engenharia de Requisitos
│   ├── Artefatos/
│   │   └── Templates/                     # Templates base (Visão da Demanda, Glossário, CDU, RNF, RN)
│   ├── Elicitacao/                        # Documento de Visão, Glossário, Stakeholders, Entrevistas e Backlog
│   ├── Especificação de Casos de Uso/     # Especificações de Casos de Uso (CDU) e SRS
│   ├── Especificação de Regra de Negocio/ # Regras de Negócio (RN)
│   └── Requisitos Não Funcionais/         # Requisitos Não Funcionais (RNF)
└── README.md
```
