# ⚙️ Especificação de Requisitos Funcionais (RF) — Portal de Internacionalização

> Artefato referente à Issue **`[US] Levantar requisitos funcionais`** (Milestone M1 — Elicitação e UML).

## Histórico de Versões

| Data | Versão | Descrição | Autor |
| --- | --- | --- | --- |
| 29/10/2026 | 1.0 | Levantamento e especificação dos Requisitos Funcionais do Portal de Internacionalização | Grupo 9 |

---

## 1. Visão Geral

Este documento lista de forma estruturada e objetiva os **Requisitos Funcionais (RF)** do **Portal de Internacionalização da Unifor (`requisitos-20262-grupo9`)**, mantendo rastreabilidade direta com as necessidades (`NEC-`), funcionalidades da Visão da Demanda (`F-`), atores (`AT-`), Regras de Negócio (`RN-`) e Casos de Uso (`CDU-`).

---

## 2. Catálogo de Requisitos Funcionais

| ID | Requisito Funcional | Descrição Detalhada | Atores | Prioridade | Rastreabilidade (VD / RN / CDU) |
| --- | --- | --- | --- | --- | --- |
| **RF-01** | **Consultar catálogo de intercâmbio e dupla titulação** | O sistema deve permitir a consulta pública aos programas de intercâmbio acadêmico e acordos de dupla titulação vigentes na Unifor, exibindo país, cidade, instituição parceira, cursos elegíveis, nível de idioma exigido (quadro CEFR), duração em semestres e pré-requisitos acadêmicos. | `AT-01`, `AT-02`, `AT-05` | **Essencial (Alta)** | `NEC-01` · `F-01` · `RN-06` · `CDU-01` |
| **RF-02** | **Buscar e filtrar programas e conteúdos de forma unificada** | O sistema deve disponibilizar barra de busca global por palavra-chave e filtros combinados por perfil de usuário (*Estudante Outgoing*, *Estudante Incoming*, *Docente*), modalidade (*Intercâmbio* ou *Dupla Titulação*), país de destino, centro/curso da Unifor, idioma e categoria temática. | `AT-01`, `AT-02`, `AT-03`, `AT-05` | **Essencial (Alta)** | `NEC-01`, `NEC-06` · `F-07` · `CDU-01` |
| **RF-03** | **Consultar guias e checklists de vistos e documentação** | O sistema deve apresentar guias passo a passo e checklists interativos (permitindo marcar itens concluídos durante a sessão e exportar resumo) com a relação de documentos acadêmicos e consulares exigidos para passaporte, carta de aceite (*Acceptance Letter*), tradução juramentada, seguro-saúde internacional e visto estudantil por país. | `AT-01`, `AT-03` | **Essencial (Alta)** | `NEC-02` · `F-02` · `RN-04` · `CDU-01` |
| **RF-04** | **Consultar orientações de aproveitamento de disciplinas** | O sistema deve exibir as normas e o fluxo institucional para equivalência e aproveitamento de disciplinas cursadas no exterior (etapas antes do embarque, durante a mobilidade e no retorno), incluindo orientações sobre elaboração do Plano de Estudos (*Learning Agreement*), análise de ementas/carga horária pela coordenação de curso e entrega de histórico à DAE. | `AT-01`, `AT-05` | **Essencial (Alta)** | `NEC-03` · `F-03` · `RN-05` · `CDU-01` |
| **RF-05** | **Consultar estimativas de despesas e guia de hospedagem** | O sistema deve exibir faixas referenciais de custo de vida mensal por país/cidade de destino (moradia, alimentação, transporte local, seguro e material acadêmico) e orientações institucionais seguras sobre modalidades de hospedagem (*residência universitária*, *apartamento compartilhado*, *homestay*), tanto para alunos indo ao exterior quanto para estrangeiros chegando a Fortaleza. | `AT-01`, `AT-03` | **Importante (Média)** | `NEC-04` · `F-04` · `RN-04` · `CDU-01` |
| **RF-06** | **Consultar catálogo de serviços da DRI por perfil** | O sistema deve apresentar os serviços oferecidos pela Diretoria de Relações Internacionais (DRI) organizados em trilhas específicas para três perfis: **Estudante Unifor (*Outgoing*)**, **Estudante Internacional (*Incoming*)** e **Docente / Pesquisador** (cooperação internacional, recepção de professores visitantes e convênios). | `AT-01`, `AT-02`, `AT-03` | **Essencial (Alta)** | `NEC-05`, `NEC-08` · `F-05` |
| **RF-07** | **Consultar contatos oficiais e Perguntas Frequentes (FAQ)** | O sistema deve disponibilizar uma página centralizada com os canais de atendimento da DRI (endereço no campus, horário de atendimento, telefone, e-mail institucional) e um FAQ dinâmico agrupado por temas (Intercâmbio, Dupla Titulação, Vistos, Aproveitamento, Custos e Hospedagem). | `AT-01`, `AT-02`, `AT-03` | **Essencial (Alta)** | `NEC-05` · `F-06` |
| **RF-08** | **Registrar solicitação de orientação / atendimento à DRI** | O sistema deve permitir que estudantes e docentes enviem dúvidas específicas ou solicitações de orientação à DRI por meio de formulário contendo nome, e-mail, perfil do solicitante, categoria temática, mensagem e aceite de consentimento LGPD, gerando protocolo de acompanhamento. | `AT-01`, `AT-02`, `AT-03` | **Importante (Média)** | `NEC-05` · `F-06` · `RN-07`, `RN-08` |
| **RF-09** | **Alternar idioma e controles de acessibilidade visual** | O sistema deve permitir ao usuário alternar a qualquer momento o idioma de exibição da interface e dos conteúdos publicados entre **Português (`PT-BR`)**, **Inglês (`EN`)** e **Espanhol (`ES`)**, bem como acionar controles de alto contraste e ajuste de tamanho de fonte no topo da página. | `AT-01`, `AT-02`, `AT-03` | **Essencial (Alta)** | `NEC-06` · `F-08` · `RN-03` · `CDU-01` |
| **RF-10** | **Cadastrar, traduzir e publicar conteúdos (Governança DRI)** | O sistema deve prover painel administrativo restrito à equipe da DRI para criar, editar, traduzir (`PT-BR`, `EN`, `ES`), salvar como rascunho, aprovar/publicar e arquivar programas de mobilidade, guias temáticos, estimativas de despesas e itens de FAQ. | `AT-04`, `AT-06` | **Essencial (Alta)** | `NEC-07` · `F-09` · `RN-01`, `RN-03` · `CDU-02` |
| **RF-11** | **Exibir selo de atualização, versão e alertas de revisão** | O sistema deve exibir automaticamente em cada guia publicado a data da última atualização, a versão do documento e o aviso legal orientativo (*disclaimer*), além de alertar os gestores da DRI no painel administrativo quando um conteúdo completar mais de 180 dias sem revisão. | `AT-01`, `AT-04` | **Importante (Média)** | `NEC-07` · `F-09` · `RN-02`, `RN-04` · `CDU-02` |
| **RF-12** | **Gerenciar e responder solicitações de orientação da DRI** | O sistema deve permitir que a equipe da DRI liste, filtre por status (*Aberta*, *Em Atendimento*, *Concluída*) ou categoria e registre o retorno às solicitações de orientação enviadas pelos usuários através do portal. | `AT-04` | **Desejável (Baixa)** | `NEC-05`, `NEC-07` · `F-10` · `RN-08` |

---

## 3. Matriz de Rastreabilidade (Necessidades × Requisitos Funcionais × User Stories)

| Necessidade (VD) | Funcionalidade (VD) | Requisitos Funcionais | User Stories Relacionadas ([Backlog](BacklogPriorizado.md)) |
| --- | --- | --- | --- |
| `NEC-01` (Intercâmbio e Dupla Titulação) | `F-01`, `F-07` | `RF-01`, `RF-02` | `US-01`, `US-02` |
| `NEC-02` (Vistos e Documentação) | `F-02` | `RF-03` | `US-03` |
| `NEC-03` (Aproveitamento de Disciplinas) | `F-03` | `RF-04` | `US-04` |
| `NEC-04` (Despesas e Hospedagem) | `F-04` | `RF-05` | `US-08` |
| `NEC-05` (Serviços, Contatos e Atendimento DRI) | `F-05`, `F-06`, `F-10` | `RF-06`, `RF-07`, `RF-08`, `RF-12` | `US-05`, `US-10`, `US-11` |
| `NEC-06` (Acessibilidade, Busca e Multilíngue) | `F-07`, `F-08` | `RF-02`, `RF-09` | `US-02`, `US-06`, `US-09` |
| `NEC-07` (Governança de Conteúdo DRI) | `F-09`, `F-10` | `RF-10`, `RF-11`, `RF-12` | `US-07`, `US-11` |
| `NEC-08` (Serviços para Docentes) | `F-05` | `RF-06` | `US-05` |
