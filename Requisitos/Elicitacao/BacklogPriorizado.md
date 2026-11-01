# 📋 Requisitos Funcionais e Backlog Priorizado — Portal de Internacionalização

> Artefato referente às Issues **`[US] Levantar requisitos funcionais`** e **`[US] Criar backlog inicial priorizado`** (Milestone M1 — Elicitação e UML).

## Histórico de Versões

| Data | Versão | Descrição | Autor |
| --- | --- | --- | --- |
| 29/10/2026 | 1.0 | Levantamento dos Requisitos Funcionais e criação do Product Backlog priorizado | Grupo 9 |

---

## 1. Catálogo de Requisitos Funcionais (RF)

| ID | Requisito Funcional | Descrição | Funcionalidade / Necessidade | Prioridade |
| --- | --- | --- | --- | --- |
| **RF-01** | **Consultar catálogo de intercâmbio e dupla titulação** | O sistema deve permitir a consulta pública aos programas de intercâmbio acadêmico e acordos de dupla titulação vigentes na Unifor, exibindo país, instituição parceira, cursos elegíveis, idioma exigido e duração. | `F-01` / `NEC-01` | Essencial |
| **RF-02** | **Filtrar e pesquisar oportunidades e conteúdos** | O sistema deve disponibilizar busca por palavra-chave e filtros combinados por perfil (Estudante *Outgoing*, Estudante *Incoming*, Docente), país de destino, centro/curso, modalidade (Intercâmbio ou Dupla Titulação) e tema. | `F-07` / `NEC-01`, `NEC-06` | Essencial |
| **RF-03** | **Exibir guias e checklists de documentação e vistos** | O sistema deve apresentar guias estruturados e checklists interativos (marcáveis na sessão do usuário) com a documentação acadêmica e consular necessária para passaporte, carta de aceite, seguro-saúde e visto por país. | `F-02` / `NEC-02` | Essencial |
| **RF-04** | **Apresentar orientações de aproveitamento de disciplinas** | O sistema deve exibir o passo a passo institucional para equivalência e aproveitamento de disciplinas cursadas no exterior, incluindo prazos, documentos necessários (*Learning Agreement*, ementas, histórico) e papel das coordenações. | `F-03` / `NEC-03` | Essencial |
| **RF-05** | **Exibir estimativas de despesas e guia de hospedagem** | O sistema deve disponibilizar informações orientativas sobre o custo de vida médio mensal nos países/cidades de destino (moradia, alimentação, transporte, seguro) e orientações seguras sobre tipos de hospedagem estudantil. | `F-04` / `NEC-04` | Importante |
| **RF-06** | **Exibir catálogo de serviços da DRI por perfil** | O sistema deve organizar e exibir os serviços oferecidos pela Diretoria de Relações Internacionais segmentados para Estudantes da Unifor, Estudantes Internacionais (*Incoming*) e Docentes/Pesquisadores. | `F-05` / `NEC-05`, `NEC-08` | Essencial |
| **RF-07** | **Disponibilizar contatos oficiais e FAQ categorizado** | O sistema deve exibir os canais oficiais de contato da DRI (localização, horário de funcionamento, e-mail, telefone) e uma seção de Perguntas Frequentes (FAQ) organizada por categorias temáticas. | `F-06` / `NEC-05` | Essencial |
| **RF-08** | **Registrar solicitação de orientação / contato com a DRI** | O sistema deve permitir que estudantes e docentes enviem dúvidas ou solicitações de agendamento de orientação para a DRI por meio de formulário estruturado com assunto, perfil e mensagem, gerando protocolo de acompanhamento. | `F-06` / `NEC-05` | Importante |
| **RF-09** | **Alternar idioma de exibição do portal** | O sistema deve permitir que o usuário alterne o idioma da interface e dos conteúdos publicados entre Português (`PT-BR`), Inglês (`EN`) e Espanhol (`ES`). | `F-08` / `NEC-06` | Essencial |
| **RF-10** | **Manter conteúdos e guias do portal (Governança DRI)** | O sistema deve permitir que gestores autenticados da DRI criem, editem, traduzam, revisem, publiquem e arquivem guias temáticos, instituições parceiras, FAQs e avisos institucionais. | `F-09` / `NEC-07` | Essencial |
| **RF-11** | **Exibir metadados de governança e atualização** | O sistema deve registrar e exibir automaticamente no rodapé de cada guia informativo a data da última atualização, a versão do conteúdo e o aviso de caráter orientativo quando aplicável. | `F-09` / `NEC-07` | Importante |
| **RF-12** | **Gerenciar solicitações de orientação no painel da DRI** | O sistema deve permitir que a equipe da DRI consulte, filtre por status (Aberta, Em Atendimento, Concluída) e responda às solicitações de orientação enviadas pelos usuários. | `F-10` / `NEC-05`, `NEC-07` | Desejável |

---

## 2. Backlog do Produto Priorizado (User Stories)

A priorização utiliza a técnica **MoSCoW** combinada ao valor de negócio para definir o **Produto Mínimo Viável (MVP)**:
- **Must Have (Essencial):** indispensável para o MVP do Portal.
- **Should Have (Importante):** agrega alto valor à experiência e entra logo após o núcleo informativo.
- **Could Have (Desejável):** evolução incremental caso haja capacidade na janela do projeto.

| ID | User Story | Critérios de Aceitação Principais | RF Vinculado | Prioridade (MoSCoW) | Valor | Entrega / Escopo |
| --- | --- | --- | --- | --- | --- | --- |
| **US-01** | **Como** estudante da Unifor, **quero** consultar as universidades parceiras de intercâmbio e dupla titulação filtrando pelo meu curso e país, **para** descobrir onde posso estudar no exterior. | 1. Permite filtrar por modalidade (Intercâmbio / Dupla Titulação), país, idioma e curso.<br>2. Exibe detalhes da instituição parceira, requisitos de idioma e vagas/período.<br>3. Exibe mensagem amigável caso não haja resultados para o filtro. | RF-01, RF-02 | **Must Have (Alta)** | Alto | MVP |
| **US-02** | **Como** estudante ou docente, **quero** pesquisar conteúdos por palavra-chave ou tema na barra de busca global, **para** encontrar rapidamente qualquer orientação no portal. | 1. Busca termos em títulos, resumos, FAQs e guias.<br>2. Permite filtrar os resultados por categoria (Vistos, Dupla Titulação, Aproveitamento, Custos, Serviços DRI). | RF-02 | **Must Have (Alta)** | Alto | MVP |
| **US-03** | **Como** estudante selecionado para mobilidade, **quero** consultar o guia e checklist de documentação e visto do país de destino, **para** preparar meus documentos sem esquecer nenhuma exigência. | 1. Apresenta lista de documentos acadêmicos e consulares por país/região.<br>2. Permite marcar itens concluídos no checklist visual.<br>3. Exibe links para órgãos oficiais (consulados/embaixadas) e aviso de caráter orientativo (`RN-04`). | RF-03 | **Must Have (Alta)** | Alto | MVP |
| **US-04** | **Como** estudante da Unifor, **quero** consultar as regras e o passo a passo de aproveitamento de disciplinas, **para** planejar meu plano de estudos (*Learning Agreement*) sem atrasar minha graduação. | 1. Exibe o fluxo completo (antes do embarque, durante e no retorno).<br>2. Disponibiliza a lista de documentos exigidos pela coordenação/DAE.<br>3. Orienta sobre equivalência de carga horária e ementas (`RN-05`). | RF-04 | **Must Have (Alta)** | Alto | MVP |
| **US-05** | **Como** estudante ou docente, **quero** acessar o catálogo de serviços, contatos e FAQ da DRI segmentado pelo meu perfil, **para** saber como a DRI pode me apoiar. | 1. Possui trilhas/abas claras para Estudante *Outgoing*, Estudante *Incoming* e Docente.<br>2. Exibe horários, endereço físico, e-mail, telefone e perguntas frequentes (FAQ). | RF-06, RF-07 | **Must Have (Alta)** | Alto | MVP |
| **US-06** | **Como** estudante internacional (*Incoming*) ou visitante estrangeiro, **quero** alternar o idioma do portal entre Português, Inglês e Espanhol, **para** compreender todas as orientações no meu idioma. | 1. Seletor de idioma visível no cabeçalho em todas as páginas.<br>2. Traduz rótulos de navegação e carrega a versão correspondente do conteúdo.<br>3. Caso um guia específico ainda não possua tradução, exibe aviso claro e versão padrão (`RN-03`). | RF-09 | **Must Have (Alta)** | Alto | MVP |
| **US-07** | **Como** gestor de conteúdo da DRI, **quero** cadastrar, editar, traduzir e publicar guias e convênios no painel administrativo, **para** manter as informações do portal sempre atualizadas e confiáveis. | 1. Acesso restrito mediante autenticação e perfil da DRI (`RN-01`).<br>2. Permite salvar como rascunho ou publicar.<br>3. Registra automaticamente data/hora da última revisão e autor (`RN-02`). | RF-10, RF-11 | **Must Have (Alta)** | Alto | MVP |
| **US-08** | **Como** estudante planejando intercâmbio, **quero** consultar estimativas de despesas mensais e orientações sobre hospedagem por destino, **para** organizar meu orçamento antes da viagem. | 1. Exibe faixas estimadas de custo (moradia, alimentação, transporte, seguro) por cidade/país.<br>2. Apresenta modalidades de hospedagem (residência universitária, apartamento compartilhado, *homestay*) e dicas de segurança.<br>3. Exibe data de referência e aviso de isenção de responsabilidade (`RN-04`). | RF-05 | **Should Have (Média)** | Alto | MVP |
| **US-09** | **Como** usuário com necessidades de acessibilidade, **quero** ajustar o contraste de cores, tamanho da fonte e navegar via teclado no portal, **para** consumir todo o conteúdo com autonomia. | 1. Barra de acessibilidade com alto contraste e controle tipográfico.<br>2. Conformidade com navegação por teclado (`Tab`) e textos alternativos em imagens (`WCAG 2.1 AA`). | RF-09 / RNF | **Should Have (Média)** | Alto | MVP |
| **US-10** | **Como** estudante ou docente, **quero** enviar uma solicitação de orientação categorizada para a DRI pelo portal, **para** esclarecer dúvidas específicas que não estão no FAQ. | 1. Formulário solicita nome, e-mail institucional, perfil, categoria da dúvida e mensagem.<br>2. Exige aceite do termo de privacidade/LGPD (`RN-07`).<br>3. Gera protocolo de confirmação para o usuário. | RF-08 | **Should Have (Média)** | Médio | Release 2 |
| **US-11** | **Como** colaborador da DRI, **quero** visualizar e responder às solicitações de orientação recebidas pelo portal, **para** organizar o fluxo de atendimento da equipe. | 1. Lista solicitações filtradas por status (Aberta, Em Atendimento, Concluída) e categoria.<br>2. Permite registrar resposta e atualizar o status do atendimento. | RF-12 | **Could Have (Baixa)** | Médio | Release 2 |
