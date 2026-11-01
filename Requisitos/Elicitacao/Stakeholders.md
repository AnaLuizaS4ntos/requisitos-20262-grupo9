# 👥 Identificação e Análise de Stakeholders — Portal de Internacionalização

> Artefato referente à Issue **`[US] Identificar stakeholders`** (Milestone M1 — Elicitação e UML).

## Histórico de Versões

| Data | Versão | Descrição | Autor |
| --- | --- | --- | --- |
| 29/10/2026 | 1.0 | Identificação de stakeholders, papéis, matriz de influência e personas iniciais | Grupo 9 |

---

## 1. Catálogo de Stakeholders

| ID | Stakeholder | Categoria | Papel no Sistema | Principais Interesses e Necessidades | Nível de Influência | Nível de Interesse |
| --- | --- | --- | --- | --- | --- | --- |
| **STK-01** | **Equipe da Diretoria de Relações Internacionais (DRI)** | Solicitante / Gestor Operacional | Definir diretrizes, publicar e atualizar conteúdos, gerenciar FAQs e atender solicitações enviadas pelo portal | Reduzir retrabalho no atendimento de dúvidas repetitivas; garantir que orientações sobre intercâmbio, dupla titulação e vistos estejam centralizadas e atualizadas | **Alto** | **Alto** |
| **STK-02** | **Estudantes da Unifor (Graduação e Pós — *Outgoing*)** | Usuário Primário | Consultar programas de intercâmbio, dupla titulação, requisitos de visto, aproveitamento de disciplinas, custos, hospedagem e contatos da DRI | Encontrar informações confiáveis, organizadas por curso/país, sem precisar buscar em múltiplos documentos dispersos | **Médio** | **Alto** |
| **STK-03** | **Estudantes e Visitantes Estrangeiros (*Incoming*)** | Usuário Primário | Consultar o portal em inglês ou espanhol sobre como estudar na Unifor, visto brasileiro, moradia em Fortaleza e recepção institucional | Ter acesso a informações claras em seu idioma e suporte rápido para adaptação acadêmica e legal no Brasil | **Baixo** | **Alto** |
| **STK-04** | **Docentes e Pesquisadores da Unifor** | Usuário Primário | Consultar serviços da DRI voltados a professores, convênios internacionais vigentes e orientações para apoiar alunos orientandos | Localizar facilmente oportunidades de cooperação acadêmica e procedimentos institucionais da DRI | **Médio** | **Médio** |
| **STK-05** | **Coordenadores de Curso (Unifor)** | Parte Interessada / Usuário | Consultar regras e fluxos de equivalência/aproveitamento de disciplinas e acordos de dupla titulação do seu curso | Garantir que os alunos compreendam previamente os critérios de aproveitamento curricular antes da viagem | **Alto** | **Médio** |
| **STK-06** | **Secretaria Acadêmica / DAE** | Parte Interessada Institucional | Processar registros formais de matrícula em mobilidade e lançamento de aproveitamento de estudos no histórico | Receber documentação correta dos estudantes conforme as orientações publicadas no portal | **Médio** | **Baixo** |
| **STK-07** | **Equipe de TI e Conformidade (LGPD / Acessibilidade)** | Parte Interessada Técnica | Definir padrões de infraestrutura, segurança da informação, autenticação, acessibilidade e proteção de dados pessoais | Garantir conformidade com a LGPD, padrões visuais da Unifor e segurança do painel administrativo | **Alto** | **Médio** |
| **STK-08** | **Professor da Disciplina (Prof. Marcelo Bezerra)** | Avaliador / Sponsor Acadêmico | Avaliar a aderência metodológica da elicitação, requisitos, diagramas UML, SRS e protótipo | Clareza do problema, rastreabilidade dos artefatos e qualidade da engenharia de requisitos | **Alto** | **Alto** |

---

## 2. Matriz de Poder (Influência) x Interesse

```mermaid
quadrantChart
    title Matriz de Influencia x Interesse dos Stakeholders
    x-axis Baixo Interesse --> Alto Interesse
    y-axis Baixa Influencia --> Alta Influencia
    quadrant-1 Gerenciar de Perto (Alto Poder / Alto Interesse)
    quadrant-2 Manter Satisfeito (Alto Poder / Medio Interesse)
    quadrant-3 Monitorar (Baixo Poder / Baixo Interesse)
    quadrant-4 Manter Informado (Baixo-Medio Poder / Alto Interesse)
    "STK-01 Equipe DRI": [0.90, 0.90]
    "STK-08 Prof. Marcelo Bezerra": [0.85, 0.95]
    "STK-05 Coordenadores de Curso": [0.45, 0.75]
    "STK-07 Equipe TI / LGPD": [0.40, 0.70]
    "STK-02 Estudantes Outgoing": [0.90, 0.45]
    "STK-03 Estudantes Incoming": [0.80, 0.25]
    "STK-04 Docentes": [0.65, 0.45]
    "STK-06 Secretaria / DAE": [0.25, 0.35]
```

### Estratégia de Engajamento por Quadrante

1. **Gerenciar de Perto (`STK-01` Equipe DRI, `STK-08` Professor):** Envolver diretamente na validação do escopo, das regras de governança de conteúdo e dos protótipos a cada sprint.
2. **Manter Informado e Envolver em Testes de Usabilidade (`STK-02` Estudantes *Outgoing*, `STK-03` Estudantes *Incoming*, `STK-04` Docentes):** Realizar entrevistas de elicitação para mapear as principais dores de busca de informação e validar a navegabilidade dos wireframes/protótipos.
3. **Manter Satisfeito (`STK-05` Coordenadores de Curso, `STK-07` TI/LGPD):** Garantir que as regras de aproveitamento de disciplinas e os requisitos não funcionais (LGPD, segurança e acessibilidade) estejam contemplados na especificação.
4. **Monitorar (`STK-06` Secretaria/DAE):** Manter alinhamento quanto aos formulários e documentos referenciados nos checklists do portal.

---

## 3. Personas Contextuais (Apoio à Experiência do Usuário)

### Persona 1 — Mariana Alves (Estudante *Outgoing* de Graduação)
- **Perfil:** 21 anos, aluna do 5º semestre de Engenharia / Administração na Unifor, nível intermediário de inglês.
- **Objetivo:** Deseja fazer intercâmbio ou dupla titulação no próximo ano, mas não sabe quais universidades têm acordo com seu curso, quanto custa morar fora e se perderá semestres ao voltar.
- **Dores atuais:** Encontra informações espalhadas em PDFs antigos, tem medo de errar na documentação do visto e não sabe como funciona o aproveitamento de disciplinas.
- **O que espera do Portal:** Um guia passo a passo por etapa (antes de ir, durante e ao voltar), filtro de universidades por curso e estimativa realista de custos e hospedagem.

### Persona 2 — Carlos Eduardo (Analista de Relações Internacionais da DRI)
- **Perfil:** 34 anos, colaborador da DRI responsável pelo atendimento a alunos e atualização de informações de convênios.
- **Objetivo:** Atender estudantes e docentes com qualidade e manter os guias de mobilidade sempre atualizados em português, inglês e espanhol.
- **Dores atuais:** Responde diariamente dezenas de e-mails e atendimentos presenciais com as mesmas perguntas básicas sobre vistos, dupla titulação e contatos; depende de terceiros para atualizar páginas institucionais.
- **O que espera do Portal:** Uma área administrativa simples para atualizar guias, tabelas de instituições parceiras e FAQs com autonomia, selo de data de atualização e versão multilíngue.

### Persona 3 — Lukas Meyer (Estudante Internacional *Incoming*)
- **Perfil:** 23 anos, estudante alemão de intercâmbio recém-aceito para cursar um semestre na Unifor. Fala inglês e alemão, com pouco domínio do português.
- **Objetivo:** Saber quais documentos levar para o visto brasileiro, como encontrar hospedagem segura próxima à Unifor e a quem recorrer ao chegar em Fortaleza.
- **Dores atuais:** Tem dificuldade para navegar em páginas apenas em português e encontrar informações consolidadas para estrangeiros.
- **O que espera do Portal:** Uma trilha dedicada a *International Students* em inglês, com checklist de chegada, contatos da DRI e orientações práticas sobre Fortaleza.
