# Especificação de Regras de Negócio (RN) — Portal de Internacionalização

> Documento elaborado conforme o template oficial para registrar as Regras de Negócio do **Portal de Internacionalização da Unifor (`requisitos-20262-grupo9`)**, utilizando o padrão *Sujeito + Verbo + Objeto*.

## Histórico de Versões

| Data | Versão | Descrição | Autor |
| --- | --- | --- | --- |
| 29/10/2026 | 1.0 | Definição inicial das Regras de Negócio do Portal de Internacionalização | Grupo 9 |

---

## 1. Catálogo de Regras de Negócio

### RN-01 — Gestor da DRI aprova publicação de conteúdos no portal
- **Identificador:** `RN-01` — Gestor da DRI aprova publicação de conteúdos no portal
- **Descrição:** Nenhum guia informativo, acordo de intercâmbio/dupla titulação ou item de FAQ pode ser exibido publicamente no portal sem antes receber o status **Publicado** por um usuário autenticado com perfil de Gestor de Conteúdo da DRI (`AT-04`). Conteúdos em elaboração permanecem no estado **Rascunho** ou **Em Revisão**.
- **Origem / Fonte:** Proposta 4 — Questões para levantamento (Governança de conteúdo).
- **Artefatos Relacionados:** `F-09`, `RF-10`, `CDU-02`, `RNF-12`.

---

### RN-02 — Portal exibe data de atualização e alerta revisão periódica de conteúdos
- **Identificador:** `RN-02` — Portal exibe data de atualização e alerta revisão periódica de conteúdos
- **Descrição:** Todo conteúdo publicado no portal deve exibir ao usuário final a data da última atualização e o setor responsável (DRI). Além disso, conteúdos com mais de **180 dias (1 semestre letivo)** sem revisão devem ser sinalizados no painel administrativo da DRI com alerta de **"Revisão Semestral Pendente"**, garantindo que regras de vistos, acordos e valores estimados não fiquem defasados.
- **Origem / Fonte:** Proposta 4 — Governança de conteúdo e mitigação do risco `PQ-03`.
- **Artefatos Relacionados:** `F-09`, `RF-11`, `CDU-02`, `RNF-24`.

---

### RN-03 — Sistema aplica idioma padrão com aviso quando tradução não estiver disponível
- **Identificador:** `RN-03` — Sistema aplica idioma padrão com aviso quando tradução não estiver disponível
- **Descrição:** O portal deve priorizar a publicação de conteúdos nos três idiomas suportados (**Português `PT-BR`**, **Inglês `EN`** e **Espanhol `ES`**). O cadastro em Português (`PT-BR`) é obrigatório para toda publicação. Caso o usuário alterne para Inglês ou Espanhol em uma página cuja tradução ainda esteja em andamento, o sistema deve exibir o conteúdo no idioma padrão (`PT-BR`) acompanhado de um banner informativo no idioma escolhido indicando que a tradução oficial daquela página está em atualização pela DRI.
- **Origem / Fonte:** Proposta 4 — Questões para levantamento (Versões multilíngues).
- **Artefatos Relacionados:** `F-08`, `RF-09`, `RNF-09`, `RNF-20`, `CDU-02`.

---

### RN-04 — Guias de vistos, despesas e hospedagem exibem aviso de caráter orientativo
- **Identificador:** `RN-04` — Guias de vistos, despesas e hospedagem exibem aviso de caráter orientativo
- **Descrição:** Todas as páginas que apresentem orientações sobre obtenção de vistos, estimativas de despesas mensais e opções de hospedagem devem exibir obrigatoriamente um aviso institucional (*disclaimer*) esclarecendo que:
  1. A concessão de vistos e suas exigências legais são de competência exclusiva das embaixadas e consulados de cada país;
  2. Os valores de despesas e opções de moradia são estimativas referenciais levantadas para planejamento estudantil, cabendo ao estudante verificar contratos e condições diretamente com as instituições ou serviços no destino.
- **Origem / Fonte:** Proposta 4 — Escopo inicial e segurança jurídica institucional (`PQ-03`).
- **Artefatos Relacionados:** `F-02`, `F-04`, `RF-03`, `RF-05`, `RF-11`.

---

### RN-05 — Coordenação de curso valida equivalência para aproveitamento de disciplinas
- **Identificador:** `RN-05` — Coordenação de curso valida equivalência para aproveitamento de disciplinas
- **Descrição:** O guia e os fluxos de aproveitamento de disciplinas no portal devem explicitar que a consulta às informações e matrizes no portal **não substitui** a validação formal do Plano de Estudos (*Learning Agreement*) pela Coordenação do Curso de origem na Unifor antes do embarque, nem a entrega do Histórico Escolar e ementas autenticadas pela universidade parceira após o retorno.
- **Origem / Fonte:** Proposta 4 — Aproveitamento de disciplinas e normas acadêmicas da Unifor.
- **Artefatos Relacionados:** `F-03`, `RF-04`, `CDU-01`.

---

### RN-06 — Acordos de dupla titulação restringem elegibilidade por curso e pré-requisitos
- **Identificador:** `RN-06` — Acordos de dupla titulação restringem elegibilidade por curso e pré-requisitos
- **Descrição:** Diferentemente dos programas de intercâmbio geral, todo acordo de **Dupla Titulação** cadastrado no portal deve estar vinculado obrigatoriamente a um ou mais **cursos específicos da Unifor**, exibindo os pré-requisitos mínimos exigidos pelo convênio (percentual ou semestre mínimo cursado na Unifor, nível de proficiência no idioma conforme quadro CEFR e carga horária no destino).
- **Origem / Fonte:** Proposta 4 — Escopo inicial (Intercâmbio e Dupla Titulação).
- **Artefatos Relacionados:** `F-01`, `RF-01`, `CDU-01`.

---

### RN-07 — Usuário consente com tratamento de dados (LGPD) ao solicitar orientação à DRI
- **Identificador:** `RN-07` — Usuário consente com tratamento de dados (LGPD) ao solicitar orientação à DRI
- **Descrição:** O envio de qualquer solicitação de orientação ou dúvida pelo formulário de contato da DRI (`RF-08`) somente pode ser concluído se o usuário informar e-mail válido, selecionar seu perfil (Estudante Unifor, Estudante Internacional ou Docente) e marcar o aceite expresso da finalidade de tratamento de dados pessoais conforme a **LGPD (Lei nº 13.709/2018)**.
- **Origem / Fonte:** Observações da Proposta 2026.2 (Observância da LGPD).
- **Artefatos Relacionados:** `F-06`, `RF-08`, `RNF-16`, `RNF-17`.

---

### RN-08 — DRI classifica e direciona solicitações de atendimento por categoria e perfil
- **Identificador:** `RN-08` — DRI classifica e direciona solicitações de atendimento por categoria e perfil
- **Descrição:** Toda solicitação de orientação enviada pelo portal deve ser automaticamente classificada por **Perfil do Solicitante** (`Outgoing`, `Incoming` ou `Docente`) e **Categoria Temática** (Intercâmbio, Dupla Titulação, Vistos/Documentação, Aproveitamento de Disciplinas, Hospedagem/Custos ou Parcerias Docentes), gerando um número de protocolo único e exibindo o prazo estimado de resposta institucional da DRI.
- **Origem / Fonte:** Proposta 4 — Contatos e serviços da DRI.
- **Artefatos Relacionados:** `F-06`, `F-10`, `RF-08`, `RF-12`.

---

## 2. Checklist de Validação das Regras de Negócio

### 2.1. Estrutura mínima
- [x] Identificador único e padronizado (`RN-01` a `RN-08`).
- [x] Nome da regra no formato *sujeito + verbo + objeto*.
- [x] Descrição clara, direta e sem ambiguidades.

### 2.2. Qualidade da regra
- [x] Cada regra descreve uma decisão/comportamento principal de negócio.
- [x] Condições de aplicação (gatilho/contexto) estão explícitas.
- [x] Resultado esperado da regra está explícito.
- [x] As regras são verificáveis e testáveis.

### 2.3. Consistência e rastreabilidade
- [x] Não há conflito entre as regras definidas.
- [x] Cada regra referencia sua origem (Proposta 4 da disciplina, normas acadêmicas ou LGPD).
- [x] As regras estão alinhadas com a Visão da Demanda, CDU e RNF.

### 2.4. Prontidão
- [x] Conteúdo revisado pela equipe do Grupo 9.
- [x] Regras prontas para uso em análise, prototipação e especificação SRS.
