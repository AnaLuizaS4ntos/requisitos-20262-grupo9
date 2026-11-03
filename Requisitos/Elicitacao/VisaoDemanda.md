# Visão da Demanda (VD) — Portal de Internacionalização Unifor

> **Documento elaborado conforme o Template LAPIS v2.1.** Base documental: Proposta 4 do Eixo I (Internacionalização) do documento *Propostas de Projetos de Sistemas — Internacionalização e ENADE (Semestre 2026.2)*. As necessidades e funcionalidades descritas combinam informações da proposta acadêmica com hipóteses de elicitação identificadas para validação junto às partes interessadas (DRI, estudantes e docentes).

## Identificação e Histórico

| Campo | Informação |
| --- | --- |
| Nome e identificador da demanda | Portal de Internacionalização Unifor — `PROJ-04` (`requisitos-20262-grupo9`) |
| Tipo | Novo sistema (Portal Web Institucional) |
| Sistema ou produto relacionado | Portal Institucional Unifor / Serviços da Diretoria de Relações Internacionais (DRI) |
| Área solicitante | Diretoria / Assessoria de Relações Internacionais (DRI) — Universidade de Fortaleza (Unifor) |
| Responsável pela elaboração | Grupo 9 — Disciplina de Engenharia de Requisitos (2026.2) |
| Responsável pela validação | Professor Marcelo Bezerra de Alcântara / Representantes da DRI (a confirmar) |
| Situação do documento | Em revisão — Apta para iniciar a especificação |
| Versão e data | 1.0 — 29/10/2026 |

| Data | Versão | Descrição da alteração | Autor |
| --- | --- | --- | --- |
| 29/10/2026 | 1.0 | Elaboração inicial da Visão da Demanda para o Projeto 4 — Portal de Internacionalização | Grupo 9 |

---

## 1. Objetivo

Melhorar a experiência de **estudantes (graduação e pós-graduação), docentes e visitantes internacionais** na busca por informações, orientações práticas e serviços de internacionalização da Universidade de Fortaleza (Unifor), centralizando em um **portal unificado, acessível e multilíngue** os conteúdos sobre intercâmbio acadêmico, dupla titulação, vistos, documentação, aproveitamento de disciplinas, estimativa de despesas, hospedagem, contatos e canais de atendimento da Diretoria de Relações Internacionais (DRI).

---

## 2. Contexto, Problema e Descrição Sumária da Demanda

- **Situação atual:** As informações sobre programas de mobilidade internacional, dupla titulação, exigências documentais, aproveitamento de estudos e suporte da DRI encontram-se dispersas em diferentes páginas institucionais, editais em PDF, comunicados ou dependem de atendimento presencial/por e-mail para esclarecimento de dúvidas recorrentes *(hipótese derivada do problema proposto no documento da disciplina, a confirmar em entrevista com a DRI e alunos)*.
- **Problema ou oportunidade:** Estudantes e docentes enfrentam dificuldades para localizar informações consolidadas, atualizadas e organizadas por perfil ou etapa da jornada de internacionalização, gerando insegurança no planejamento acadêmico e financeiro e sobrecarga operacional à equipe da DRI com dúvidas repetitivas.
- **Públicos afetados e impactos:**
  - **Estudantes da Unifor (Outgoing):** dificuldade em comparar opções de intercâmbio e dupla titulação, entender equivalência de disciplinas, planejar custos/hospedagem e preparar documentação/vistos.
  - **Estudantes e pesquisadores estrangeiros (Incoming):** barreira de idioma e falta de guia centralizado para recepção, visto, moradia em Fortaleza e matrícula.
  - **Docentes:** dificuldade para localizar serviços de apoio à internacionalização docente, acordos vigentes e orientações para alunos orientandos.
  - **Equipe da DRI:** alto volume de atendimentos básicos que poderiam ser resolvidos por autoatendimento estruturado, além de dificuldade na governança e atualização rápida de conteúdos.
- **Evidências disponíveis:** Documento *Propostas de Projetos de Sistemas — Internacionalização e ENADE (2026.2)*, item *4. Portal de Internacionalização*. Métricas quantitativas de atendimento atual da DRI encontram-se **A definir** mediante entrevista.
- **Descrição sumária da demanda:** Solução web responsiva e multilíngue que organiza a jornada de internacionalização em trilhas e guias práticos (intercâmbio, dupla titulação, vistos, documentação, aproveitamento de disciplinas, despesas e hospedagem), catálogo de instituições conveniadas, FAQ inteligente, diretório de contatos/serviços da DRI com solicitação de atendimento e painel administrativo para governança e publicação de conteúdo pela equipe da DRI.

---

## 3. Proposta de Valor e Sucesso da Demanda

| Benefício esperado | Indicador ou evidência | Resultado desejado | Como e quando avaliar |
| --- | --- | --- | --- |
| Centralizar e facilitar o acesso às informações de internacionalização | Tempo e quantidade de cliques para localizar informações-chave (intercâmbio, dupla titulação, visto, aproveitamento) | Usuário localiza qualquer guia temático principal em até 3 cliques a partir da página inicial *(meta hipótese a validar)* | Teste de usabilidade com estudantes e docentes no protótipo navegável (M2) |
| Reduzir dúvidas recorrentes no atendimento da DRI | Disponibilidade de guias passo a passo, checklists documentais e FAQ categorizado | Cobertura de 100% dos tópicos essenciais previstos no escopo da DRI | Revisão do catálogo de conteúdos junto aos interessados (M1/M2) |
| Ampliar o alcance internacional e a inclusão | Suporte a múltiplos idiomas (PT-BR, EN, ES) e conformidade com diretrizes de acessibilidade | Navegação funcional em múltiplos idiomas e aprovação em checklist de acessibilidade WCAG 2.1 AA | Verificação nos protótipos e validação de requisitos não funcionais |
| Garantir atualização e confiabilidade das informações | Fluxo de governança de conteúdo com histórico de revisão e data da última atualização visível | Equipe da DRI consegue publicar, revisar e arquivar orientações com rastreabilidade | Simulação do fluxo administrativo (CDU-02) na entrega M2 |

> As metas quantitativas e linhas de base operacionais da DRI são hipóteses iniciais e estão registradas para confirmação na seção 10 (`PQ-01` a `PQ-04`).

---

## 4. Partes Interessadas

| Parte interessada | Papel e interesse | Responsabilidade | Representante |
| --- | --- | --- | --- |
| Diretoria de Relações Internacionais (DRI) | Solicitante, gestora do domínio e operadora do conteúdo | Definir regras de governança, validar informações oficiais sobre acordos, vistos e serviços, e manter o conteúdo atualizado | Equipe DRI (a definir na entrevista) |
| Estudantes de Graduação e Pós-Graduação (Unifor) | Usuários principais (perfil *Outgoing*) | Consultar orientações de intercâmbio, dupla titulação, aproveitamento de disciplinas, despesas e documentação | Representantes discentes (entrevistados) |
| Estudantes e Visitantes Internacionais (*Incoming*) | Usuários externos (perfil *Incoming*) | Consultar informações em inglês/espanhol sobre recepção, vistos para o Brasil, hospedagem e serviços da Unifor | Intercambistas / DRI (a definir) |
| Docentes e Coordenadores de Curso | Usuários e orientadores acadêmicos | Consultar serviços da DRI para docentes e regras de equivalência/aproveitamento de disciplinas | Docentes entrevistados (a definir) |
| Equipe de Projeto (Grupo 9) | Equipe de Engenharia de Requisitos | Elicitar, especificar, modelar em UML e prototipar a solução | Integrantes do Grupo 9 |
| Professor da Disciplina | Avaliador e orientador metodológico | Validar os entregáveis de requisitos, modelagem UML, SRS e protótipo | Prof. Marcelo Bezerra de Alcântara |

---

## 5. Usuários e Atores Externos

| ID | Usuário, sistema ou dispositivo | Objetivo ou papel na interação | Contexto de uso relevante |
| --- | --- | --- | --- |
| AT-01 | Estudante Unifor (*Outgoing*) | Consultar guias de intercâmbio, dupla titulação, documentação, vistos, aproveitamento de disciplinas, custos, hospedagem e acionar suporte da DRI | Acesso web via smartphone ou computador; precisa de linguagem clara e checklists práticos |
| AT-02 | Docente / Pesquisador | Consultar serviços da DRI voltados ao corpo docente, parcerias internacionais e orientações de aproveitamento acadêmico | Acesso web via computador ou dispositivo móvel |
| AT-03 | Estudante / Visitante Internacional (*Incoming*) | Consultar informações institucionais, guia de chegada, visto brasileiro, moradia e contatos da DRI em idioma estrangeiro (EN/ES) | Acesso web internacional; depende de interface multilíngue e acessível |
| AT-04 | Gestor de Conteúdo da DRI | Cadastrar, atualizar, traduzir, revisar e publicar guias, instituições parceiras, FAQs, estimativas de custo e canais de serviço | Acesso autenticado ao painel administrativo de governança do portal |
| AT-05 | Coordenador de Curso | Consultar matrizes de equivalência/aproveitamento de disciplinas e orientar alunos candidatos à mobilidade | Acesso web para consulta de regras e fluxos acadêmicos |
| AT-06 | Sistema de Autenticação Institucional (Unifor Online) | Autenticar usuários internos (equipe DRI e comunidade acadêmica, quando aplicável) | Ator externo de integração (hipótese técnica a confirmar) |

---

## 6. Escopo e Entregas Previstas

### 6.1. Incluído na demanda

- **Catálogo de Programas e Parcerias:** consulta estruturada de modalidades de intercâmbio acadêmico, programas de dupla titulação e instituições parceiras por país, área/curso e idioma.
- **Guias Passo a Passo e Checklists Documentais:** orientações detalhadas sobre vistos, documentação exigida, seguro-saúde e etapas pré e pós-embarque.
- **Guia de Aproveitamento de Disciplinas:** explicação do fluxo institucional, regras de equivalência curricular e documentos necessários (*Learning Agreement* / histórico).
- **Guia de Despesas e Hospedagem:** informações orientativas sobre custo de vida estimado por destino, taxas acadêmicas e orientações seguras sobre modalidades de hospedagem.
- **Catálogo de Serviços, Contatos e FAQ da DRI:** página centralizada com serviços oferecidos a estudantes e docentes, perguntas frequentes (FAQ), contatos oficiais e formulário/canal de solicitação de atendimento ou agendamento de orientação.
- **Recursos de Acessibilidade e Multilíngue:** alternância de idioma (Português, Inglês e Espanhol), busca unificada por palavras-chave/filtros e recursos de acessibilidade digital.
- **Painel de Governança de Conteúdo (DRI):** gerenciamento de páginas informativas, parcerias, FAQs, versão por idioma, selo de "última atualização" e controle de publicação.

### 6.2. Fora do escopo

- Processamento financeiro ou pagamento direto de taxas, passagens ou hospedagem dentro do portal.
- Emissão oficial de vistos (competência exclusiva de consulados e embaixadas) — o portal fornece apenas caráter orientativo.
- Rede social entre alunos com chat e publicação livre de anúncios de moradia por estudantes (escopo pertencente ao *Projeto 1 — Conecta Intercâmbio*).
- Gestão de currículos Lattes e indicadores de produção científica docente (escopo pertencente ao *Projeto 2*).
- Submissão e julgamento completo de inscrições em editais de bolsas (escopo pertencente ao *Projeto 3 — Gestão de Oportunidades Internacionais*, podendo o Portal exibir links/chamadas para os editais vigentes).

### 6.3. Evoluções futuras — opcional

- Chatbot assistente baseado em IA para responder dúvidas com base nos guias oficiais homologados pela DRI.
- Simulador interativo de equivalência automática de disciplinas integrado ao histórico escolar do aluno no Unifor Online.
- Integração via API com os sistemas dos Projetos 1, 2 e 3 para formar um ecossistema único de internacionalização.

### 6.4. Entregas e marcos — quando conhecidos

| Entrega ou marco | Resultado previsto | Data ou condição | Natureza do prazo |
| --- | --- | --- | --- |
| **M1 — Elicitação e UML (P1)** | Visão da Demanda, Glossário, Stakeholders, Entrevistas, RF, RNF, RN, Backlog e UML inicial | 01/11/2026 a 02/11/2026 | Obrigatório |
| **M2 — Especificação e Protótipo (P2)** | Documento SRS (IEEE 830 / Casos de Uso), Revisão de consistência UML e Protótipo navegável | 22/11/2026 a 23/11/2026 | Obrigatório |
| **M3 — Pitch Final (P3)** | Slides do Pitch (PDF), demonstração do protótipo e evolução das sprints | 29/11/2026 a 01/12/2026 | Obrigatório |

---

## 7. Necessidades e Catálogo de Funcionalidades

### 7.1. Necessidades Identificadas

| ID | Necessidade | Fonte ou evidência | Públicos ou atores relacionados |
| --- | --- | --- | --- |
| NEC-01 | Encontrar rapidamente orientações claras sobre intercâmbio tradicional e programas de dupla titulação elegíveis para o seu curso | Proposta 4 (Eixo I — Internacionalização) + Roteiro de elicitação | AT-01, AT-02, AT-05 |
| NEC-02 | Compreender a documentação exigida e os procedimentos para obtenção de visto estudantil e seguro-saúde sem omissões | Proposta 4 (Eixo I — Internacionalização) | AT-01, AT-03 |
| NEC-03 | Entender como funciona o aproveitamento de disciplinas cursadas no exterior e quais documentos submeter à coordenação | Proposta 4 (Eixo I — Internacionalização) | AT-01, AT-05 |
| NEC-04 | Planejar financeiramente a mobilidade com informações sobre despesas médias e opções seguras de hospedagem no destino | Proposta 4 (Eixo I — Internacionalização) | AT-01, AT-03 |
| NEC-05 | Localizar facilmente os serviços prestados pela DRI, contatos institucionais, horários e canais de orientação para estudantes e docentes | Proposta 4 (Eixo I — Internacionalização) | AT-01, AT-02, AT-03 |
| NEC-06 | Acessar o portal em diferentes idiomas (PT, EN, ES) e com recursos de acessibilidade digital e busca eficiente | Proposta 4 — Questões para levantamento (acessibilidade, organização e multilíngue) | AT-01, AT-02, AT-03 |
| NEC-07 | Manter as informações do portal atualizadas, revisadas e padronizadas com controle de versão e governança institucional | Proposta 4 — Questões para levantamento (governança de conteúdo) | AT-04 |
| NEC-08 | Consultar orientações específicas de serviços de internacionalização voltados ao corpo docente (parcerias, recepção de professores visitantes, apoio institucional) | Proposta 4 — Problema a investigar (experiência de estudantes e docentes) | AT-02, AT-04 |

### 7.2. Catálogo de Funcionalidades

| ID | Funcionalidade e resultado esperado | Necessidade | Atores (IDs) | Prioridade | Valor | Frequência | Escopo ou entrega | Especificação |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| F-01 | **Consultar Programas de Intercâmbio e Dupla Titulação:** explorar catálogo de universidades conveniadas e acordos de dupla titulação com filtros por país, curso, idioma e tipo de mobilidade | NEC-01 | AT-01, AT-02, AT-05 | Essencial | Alto | Alta | Entrega (MVP) | [CDU-01](../Especifica%C3%A7%C3%A3o%20de%20Casos%20de%20Uso/CDU-01-Consultar-Guias-Mobilidade-Dupla-Titulacao.md) |
| F-02 | **Consultar Guias e Checklists de Vistos e Documentação:** acessar passo a passo de documentos acadêmicos, tradução juramentada, passaporte, visto e seguro por país | NEC-02 | AT-01, AT-03 | Essencial | Alto | Alta | Entrega (MVP) | `CDU-03` — a elaborar |
| F-03 | **Consultar Orientações de Aproveitamento de Disciplinas:** visualizar fluxo de equivalência curricular, regras por centro/curso e modelos de plano de estudos (*Learning Agreement*) | NEC-03 | AT-01, AT-05 | Essencial | Alto | Média | Entrega (MVP) | [CDU-01](../Especifica%C3%A7%C3%A3o%20de%20Casos%20de%20Uso/CDU-01-Consultar-Guias-Mobilidade-Dupla-Titulacao.md) |
| F-04 | **Consultar Estimativas de Despesas e Guia de Hospedagem:** consultar faixas estimadas de custo de vida (moradia, alimentação, transporte) e orientações institucionais de hospedagem por destino | NEC-04 | AT-01, AT-03 | Importante | Alto | Média | Entrega (MVP) | `CDU-04` — a elaborar |
| F-05 | **Consultar Serviços da DRI para Docentes e Estudantes:** navegar pelo catálogo de serviços da DRI segmentado por perfil (Estudante *Outgoing*, Estudante *Incoming* e Docente) | NEC-05, NEC-08 | AT-01, AT-02, AT-03 | Essencial | Alto | Alta | Entrega (MVP) | `CDU-05` — a elaborar |
| F-06 | **Solicitar Atendimento / Orientação e Consultar Contatos da DRI:** visualizar contatos oficiais, consultar FAQ interativo e enviar solicitação de orientação/dúvida categorizada para a DRI | NEC-05 | AT-01, AT-02, AT-03, AT-04 | Importante | Médio | Média | Entrega (MVP) | `CDU-06` — a elaborar |
| F-07 | **Buscar Conteúdos de Forma Unificada e Filtrada:** pesquisar por palavra-chave, tema (visto, dupla titulação, hospedagem, aproveitamento), país ou perfil de usuário | NEC-01, NEC-06 | AT-01, AT-02, AT-03 | Essencial | Alto | Alta | Entrega (MVP) | [CDU-01](../Especifica%C3%A7%C3%A3o%20de%20Casos%20de%20Uso/CDU-01-Consultar-Guias-Mobilidade-Dupla-Titulacao.md) |
| F-08 | **Alternar Idioma e Recursos de Acessibilidade:** selecionar o idioma de exibição do portal (PT-BR, EN, ES) e utilizar controles de contraste e tamanho de fonte | NEC-06 | AT-01, AT-02, AT-03 | Essencial | Alto | Alta | Entrega (MVP) | [RNF](../Requisitos%20N%C3%A3o%20Funcionais/RequisitosNaoFuncionais.md) |
| F-09 | **Gerenciar e Publicar Conteúdos do Portal (Governança DRI):** criar, editar, traduzir, revisar, aprovar e arquivar guias, acordos, FAQs e alertas com registro de data de revisão e responsável | NEC-07 | AT-04, AT-06 | Essencial | Alto | Média | Entrega (MVP) | [CDU-02](../Especifica%C3%A7%C3%A3o%20de%20Casos%20de%20Uso/CDU-02-Gerenciar-Conteudos-Portal-DRI.md) |
| F-10 | **Gerenciar Solicitações de Orientação Recebidas:** visualizar e responder chamados de dúvidas ou pedidos de orientação enviados por estudantes e docentes pelo portal | NEC-05, NEC-07 | AT-04 | Desejável | Médio | Média | Em avaliação | `CDU-07` — a elaborar |

---

## 8. Visão Geral da Solução e Impactos

- **Responsabilidades da solução:** Apresentar informações públicas e estruturadas sobre internacionalização na Unifor; permitir busca e filtragem por perfil, país, curso e tema; disponibilizar versões em Português, Inglês e Espanhol; encaminhar solicitações de atendimento à DRI; e prover ambiente administrativo para governança editorial dos conteúdos.
- **Sistemas ou dispositivos externos:** Navegadores web (desktop e mobile), serviço de autenticação institucional (para gestores da DRI e áreas restritas, quando aplicável) e serviço de envio de notificações por e-mail.
- **Integrações principais:** Autenticação de gestores (`AT-06`) e redirecionamento/links para o Unifor Online e página oficial de Editais (quando aplicável).
- **Diagramas UML e arquitetura:** Disponíveis na pasta [diagrams/](../../diagrams/README.md).

### 8.1. Sistemas e processos impactados

| Sistema ou processo | Impacto esperado | Responsável ou dependência | Situação |
| --- | --- | --- | --- |
| Atendimento presencial e por e-mail da DRI | Redução de perguntas repetitivas devido à centralização de guias, checklists e FAQ no portal | Equipe da DRI | Hipótese a validar |
| Processo de atualização de informações sobre convênios e dupla titulação | Padronização do fluxo editorial com revisão periódica obrigatória e versão multilíngue | Equipe da DRI | Hipótese a validar |
| Portal Institucional da Unifor / Unifor Online | Inclusão de ponto de acesso direto para o Portal de Internacionalização | Equipe de TI / Comunicação Unifor | A definir |

### 8.2. Representações visuais — opcionais

- **Diagrama de Casos de Uso, Classes, Sequência, Componentes e Implantação:** Documentados em [diagrams/README.md](../../diagrams/README.md).
- **Protótipos de baixa e alta fidelidade:** Previstos para a entrega **M2 (Trabalho P2)** na pasta `images/`.

---

## 9. Condições Gerais da Demanda

| Tipo | Condição e impacto na demanda | Responsável ou fonte | Referência, se houver |
| --- | --- | --- | --- |
| **Qualidade (Acessibilidade)** | O portal deve atender às diretrizes de acessibilidade digital (WCAG 2.1 nível AA), permitindo navegação por teclado, leitores de tela e alto contraste | Proposta 4 (Questões para levantamento) | [Requisitos Não Funcionais](../Requisitos%20N%C3%A3o%20Funcionais/RequisitosNaoFuncionais.md) |
| **Qualidade (Multilíngue)** | O sistema deve suportar conteúdos em Português (PT-BR), Inglês (EN) e Espanhol (ES), mantendo fallback claro caso alguma página específica ainda esteja em tradução | Proposta 4 (Questões para levantamento) | [Requisitos Não Funcionais](../Requisitos%20N%C3%A3o%20Funcionais/RequisitosNaoFuncionais.md) e [Regras de Negócio](../Especifica%C3%A7%C3%A3o%20de%20Regra%20de%20Negocio/RegrasDeNegocio.md) |
| **Regra Geral (Governança)** | Todo conteúdo publicado deve exibir a data da última revisão e passar por aprovação de um gestor da DRI antes de ficar visível publicamente | Proposta 4 (Governança de conteúdo) | [Regras de Negócio](../Especifica%C3%A7%C3%A3o%20de%20Regra%20de%20Negocio/RegrasDeNegocio.md) |
| **Restrição Legal (LGPD)** | Eventuais dados pessoais coletados em formulários de contato/orientação devem observar a Lei Geral de Proteção de Dados (Lei nº 13.709/2018), com consentimento e finalidade explícita | Observações gerais da Proposta 2026.2 | [Requisitos Não Funcionais](../Requisitos%20N%C3%A3o%20Funcionais/RequisitosNaoFuncionais.md) |
| **Premissa** | As informações sobre vistos, custos de vida e hospedagem têm caráter estritamente orientativo e referencial, devendo o estudante confirmar exigências oficiais nos consulados | Equipe de Requisitos (Grupo 9) | [Regras de Negócio](../Especifica%C3%A7%C3%A3o%20de%20Regra%20de%20Negocio/RegrasDeNegocio.md) |

---

## 10. Riscos e Questões em Aberto

| ID | Tipo | Risco ou questão | Impacto | Próxima ação | Responsável e prazo | Situação |
| --- | --- | --- | --- | --- | --- | --- |
| PQ-01 | Dúvida de negócio | Quais idiomas, além de Português e Inglês (ex.: Espanhol, Francês), são prioritários para a DRI na primeira versão do portal? | Define escopo de tradução e regras de publicação multilíngue | Validar na entrevista com a equipe da DRI | Grupo 9 — Sprint 1 | Aberto |
| PQ-02 | Decisão pendente | Como é realizada hoje a governança de conteúdo da DRI (quem redige, quem revisa e com que frequência os acordos e guias são atualizados)? | Define os perfis de permissão no módulo de governança (`F-09`) | Aplicar roteiro de entrevista com gestor da DRI | Grupo 9 — Sprint 1 | Aberto |
| PQ-03 | Risco operacional | Desatualização de valores estimados de despesas ou regras consulares de visto, gerando expectativa incorreta no estudante | Impacto na confiabilidade da informação do portal | Exigir selo de data de atualização, aviso de isenção de responsabilidade (*disclaimer*) e alerta de revisão semestral (`RN-02`, `RN-04`) | Grupo 9 — Sprint 1 | Aceito (mitigado por RN) |
| PQ-04 | Dúvida de negócio | O guia de aproveitamento de disciplinas apresentará apenas a regra geral da Unifor ou também tabelas de equivalência prévia por curso? | Altera o detalhamento da funcionalidade `F-03` | Levantar com coordenadores de curso e DRI | Grupo 9 — Sprint 1/2 | Aberto |
| PQ-05 | Dúvida técnica | A consulta a todos os guias do portal será 100% pública (sem login) ou haverá conteúdos restritos apenas para alunos e docentes autenticados? | Define precondições dos casos de uso de consulta | Confirmar com a DRI e o professor da disciplina | Grupo 9 — Sprint 1 | Aberto |

---

## 11. Documentos Relacionados

| Documento | Conteúdo sob sua responsabilidade | Referência e situação |
| --- | --- | --- |
| **Glossário do Projeto** | Termos, siglas e definições do domínio de internacionalização acadêmica | [Glossario.md](Glossario.md) — Elaborado (v1.0) |
| **Mapeamento de Stakeholders** | Identificação, papéis, matriz de influência e personas | [Stakeholders.md](Stakeholders.md) — Elaborado (v1.0) |
| **Roteiro e Registro de Entrevistas** | Perguntas de elicitação por perfil e síntese das dores identificadas | [RoteiroEntrevistas.md](RoteiroEntrevistas.md) — Elaborado (v1.0) |
| **Requisitos Funcionais (RF)** | Catálogo detalhado de Requisitos Funcionais (`RF-01` a `RF-12`) e rastreabilidade | [RequisitosFuncionais.md](RequisitosFuncionais.md) — Elaborado (v1.0) |
| **Backlog Priorizado** | User Stories (`US-01` a `US-11`) priorizadas com critérios de aceitação | [BacklogPriorizado.md](BacklogPriorizado.md) — Elaborado (v1.0) |
| **Requisitos Não Funcionais (RNF)** | Requisitos de desempenho, acessibilidade, multilíngue, segurança e LGPD | [RequisitosNaoFuncionais.md](../Requisitos%20N%C3%A3o%20Funcionais/RequisitosNaoFuncionais.md) — Elaborado (v1.0) |
| **Regras de Negócio (RN)** | Políticas de governança de conteúdo, idioma, avisos legais e atendimento | [RegrasDeNegocio.md](../Especifica%C3%A7%C3%A3o%20de%20Regra%20de%20Negocio/RegrasDeNegocio.md) — Elaborado (v1.0) |
| **Diagramas UML** | Diagramas de Casos de Uso, Classes, Sequência, Componentes e Implantação | [diagrams/README.md](../../diagrams/README.md) — Elaborado (v1.0) |

---

## 12. Validação da Visão

### 12.1. Checklist

- [x] Objetivo, contexto e problema estão claros.
- [x] Benefícios e condições de sucesso estão descritos, com hipóteses identificadas.
- [x] Responsáveis por decisões e validação estão identificados.
- [x] Usuários e atores externos relevantes estão representados (`AT-01` a `AT-06`).
- [x] Escopo, exclusões e possíveis evoluções estão diferenciados.
- [x] Necessidades têm identificadores (`NEC-01` a `NEC-08`) e fontes/evidências.
- [x] Funcionalidades têm identificadores (`F-01` a `F-10`), prioridades, atores por ID e vínculo com necessidades.
- [x] Valor e frequência são tratados separadamente.
- [x] Cada funcionalidade tem referência à especificação ou indicação de que será elaborada.
- [x] A visão geral da solução esclarece seus limites, interações externas e impactos em outros sistemas ou processos.
- [x] Diagramas foram referenciados nos documentos apropriados.
- [x] Restrições, premissas, dependências e pendências relevantes (`PQ-01` a `PQ-05`) estão registradas.
- [x] Informações detalhadas estão nos documentos apropriados, com referências consistentes.
- [ ] O conteúdo foi revisado e homologado formalmente pelos representantes da DRI.

### 12.2. Critérios de conclusão e encaminhamento

- **Condição atual:** **Apta para iniciar a especificação** — Os objetivos, partes interessadas, limites do escopo, necessidades e catálogo inicial estão definidos com base no documento da disciplina; as questões pendentes de confirmação em entrevista (`PQ-01` a `PQ-05`) estão rastreadas com responsáveis.

### 12.3. Registro da validação

| Versão | Responsável e papel | Data | Condição da VD | Resultado e ressalvas |
| --- | --- | --- | --- | --- |
| 1.0 | Grupo 9 — Equipe de Requisitos | 29/10/2026 | Apta para iniciar a especificação | Escopo inicial estruturado para a Sprint 1 (M1); sujeito a refinamento após entrevistas com stakeholders. |
