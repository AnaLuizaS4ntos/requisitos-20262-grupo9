# Especificação de Requisitos Funcionais — Caso de Uso (CDU-01)

## Histórico de Versões

| Data | Versão | Descrição | Autor |
| --- | --- | --- | --- |
| 29/10/2026 | 1.0 | Especificação inicial do Caso de Uso CDU-01 (Consultar Programas e Guias de Internacionalização) | Grupo 9 |

---

## 1. Nome do Caso de Uso

**CDU-01 — Consultar Programas de Mobilidade, Dupla Titulação e Guias de Internacionalização**

## 2. Objetivo

Permitir que estudantes (da Unifor ou internacionais), docentes e coordenadores consultem, pesquisem e filtrem programas de intercâmbio acadêmico, acordos de dupla titulação e guias práticos (vistos, documentação, aproveitamento de disciplinas, despesas e hospedagem) de forma unificada e no idioma desejado.

## 3. Tipo de Caso de Uso

Concreto.

## 4. Atores

### 4.1. Primário
- `AT-01` — Estudante Unifor (*Outgoing*)
- `AT-02` — Docente / Pesquisador
- `AT-03` — Estudante / Visitante Internacional (*Incoming*)
- `AT-05` — Coordenador de Curso

### 4.2. Secundário
- Não se aplica.

## 5. Precondições

- Não exige autenticação prévia (consulta pública aberta à comunidade acadêmica e visitantes internacionais).
- Existem programas de mobilidade, acordos de dupla titulação e guias temáticos previamente publicados pela DRI (`RN-01`).

## 6. Fluxo Principal

### P1. Acessar o Portal de Internacionalização
O ator acessa a página inicial do Portal de Internacionalização, e o sistema exibe a barra de busca global, o seletor de idiomas (`PT-BR`, `EN`, `ES`), as trilhas por perfil (*Estudante Unifor*, *International Student*, *Docente*) e os atalhos para os eixos temáticos (Intercâmbio, Dupla Titulação, Vistos e Documentação, Aproveitamento de Disciplinas, Despesas e Hospedagem, Serviços e Contatos da DRI).

### P2. Selecionar trilha ou aplicar filtros de busca
O ator informa uma palavra-chave ou seleciona filtros combinados (Modalidade: Intercâmbio ou Dupla Titulação; Curso/Centro; País de destino; Idioma exigido; ou Tema do Guia) e aciona a pesquisa (`RF-01`, `RF-02`).

### P3. Apresentar resultados correspondentes
O sistema processa os critérios informados e exibe a listagem de programas/instituições parceiras e guias temáticos publicados que atendem aos filtros selecionados, destacando título, país, modalidade, cursos elegíveis e resumo.

### P4. Selecionar programa ou guia para detalhamento
O ator seleciona um dos itens retornados na listagem para visualizar suas informações completas.

### P5. Exibir detalhes estruturados do programa ou guia
O sistema exibe a página detalhada contendo:
- **P5.1.** Para acordos de Intercâmbio ou Dupla Titulação: descrição da universidade parceira, cursos elegíveis, pré-requisitos acadêmicos e de idioma (`RN-06`), duração e etapas de candidatura;
- **P5.2.** Guias vinculados em abas/seções organizadas:
  - **Vistos e Documentação:** checklist interativo de documentos necessários (`RF-03`);
  - **Aproveitamento de Disciplinas:** fluxo de equivalência curricular, *Learning Agreement* e papel da coordenação (`RF-04`, `RN-05`);
  - **Despesas e Hospedagem:** faixas estimadas de custo mensal e orientações de moradia (`RF-05`, `RN-04`);
- **P5.3.** Data da última revisão do conteúdo pela DRI, aviso de caráter orientativo (`RN-02`, `RN-04`) e atalho para o FAQ ou solicitação de orientação à DRI.

## 7. Fluxos Alternativos

### A1. Alternar idioma de visualização (no passo P1 ou P5)
- **A1.1.** O ator seleciona outro idioma (`EN` ou `ES`) no seletor do cabeçalho (`RF-09`).
- **A1.2.** O sistema recarrega os rótulos da interface e apresenta a versão traduzida do conteúdo selecionado.
- **A1.3.** Caso o guia específico ainda não possua tradução publicada naquele idioma, o sistema exibe o conteúdo no idioma padrão (`PT-BR`) com um banner informativo no topo (`RN-03`).
- **A1.4.** O fluxo retorna ao passo em que o ator se encontrava.

### A2. Nenhum resultado encontrado para os filtros aplicados (no passo P3)
- **A2.1.** O sistema identifica que nenhum programa ou guia atende simultaneamente aos filtros selecionados.
- **A2.2.** O sistema exibe mensagem clara informando que não foram encontrados registros para a combinação escolhida e apresenta o botão **"Limpar filtros"** e sugestões de temas principais.
- **A2.3.** O fluxo retorna ao passo **P2**.

### A3. Interagir com o Checklist de Documentação e Vistos (no passo P5.2)
- **A3.1.** O ator marca os documentos que já possui no checklist visual da página de Vistos e Documentação (`RF-03`).
- **A3.2.** O sistema atualiza visualmente a barra de progresso documental do estudante durante a sessão e permite imprimir ou salvar o resumo em PDF.
- **A3.3.** O caso de uso prossegue normalmente.

## 8. Fluxos de Exceção

### E1. Indisponibilidade temporária na busca do catálogo (no passo P3)
- **E1.1.** Caso ocorra falha de comunicação ao buscar os registros filtrados, o sistema exibe mensagem amigável orientando o usuário a tentar novamente em instantes e mantém visíveis os contatos diretos da DRI (`RNF-07`).

## 9. Pós-condições

- O ator visualiza as orientações oficiais atualizadas sobre mobilidade internacional, dupla titulação, vistos, aproveitamento de disciplinas, custos e hospedagem.

## 10. Requisitos Não Funcionais Específicos

- **RNF-01 / RNF-02:** Carregamento da página em até 2,5s e retorno dos filtros em até 2,0s.
- **RNF-06:** Layout responsivo adaptável a smartphones e desktops.
- **RNF-21:** Conformidade com acessibilidade WCAG 2.1 AA.

## 11. Ponto de Extensão

### PE1. Solicitar Orientação à DRI (`CDU-06`)
- Caso o ator ainda possua dúvidas específicas após ler o guia no passo **P5**, pode acionar o botão **"Falar com a DRI / Solicitar Orientação"**, estendendo o fluxo para o registro de atendimento (`RF-08`).

## 12. Frequência de Utilização

Alta (principal fluxo público de acesso ao portal por estudantes e docentes).

## 13. Interface Visual

### IV1. Página Inicial e Catálogo de Programas / Guias de Internacionalização
- **Localização:** Protótipos a serem detalhados na pasta `images/` na entrega **M2 (Trabalho P2)**.
- **Elementos previstos:** Cabeçalho com seletor de idiomas (`PT | EN | ES`) e barra de acessibilidade; barra de busca unificada; cards de trilhas por perfil; painel lateral de filtros (Curso, País, Modalidade, Idioma); visualização em abas para Requisitos, Documentação/Visto, Aproveitamento de Disciplinas e Custos/Hospedagem.

## 14. Observações

- As regras de negócio `RN-02`, `RN-03`, `RN-04`, `RN-05` e `RN-06` regem a apresentação dos dados neste caso de uso.

## 15. Referências

- [Visão da Demanda](../Elicitacao/VisaoDemanda.md) — Funcionalidades `F-01`, `F-02`, `F-03`, `F-04`, `F-07`
- [Backlog e Requisitos Funcionais](../Elicitacao/BacklogPriorizado.md) — `RF-01` a `RF-05`, `RF-09`
- [Regras de Negócio](../Especifica%C3%A7%C3%A3o%20de%20Regra%20de%20Negocio/RegrasDeNegocio.md) — `RN-02` a `RN-06`
- [Diagramas UML](../../diagrams/README.md)

---

## 16. Checklist de Validação do Artefato (CDU)

### 16.1. Estrutura mínima
- [x] Nome do caso de uso iniciado com verbo no infinitivo.
- [x] Objetivo claro, direto e com foco em um objetivo principal.
- [x] Tipo do caso de uso informado (concreto).
- [x] Atores primários identificados corretamente (`AT-01`, `AT-02`, `AT-03`, `AT-05`).
- [x] Precondições registradas.
- [x] Fluxo principal completo e coerente com o objetivo.
- [x] Fluxos alternativos e de exceção definidos.
- [x] Pós-condições registradas.
- [x] Requisitos não funcionais específicos do CDU registrados.
- [x] Pontos de extensão identificados corretamente.
- [x] Frequência de utilização estimada.

### 16.2. Qualidade da especificação
- [x] Passos escritos com linguagem simples e objetiva.
- [x] Ações descritas com verbos no presente do indicativo (3ª pessoa).
- [x] Alternância entre ação do ator e ação da solução está clara.
- [x] Não há ambiguidade.
- [x] Regras de negócio e requisitos estão referenciados.

### 16.3. Consistência e rastreabilidade
- [x] Pontos de entrada e saída dos fluxos alternativos estão explícitos.
- [x] Fluxos de exceção estão vinculados aos passos corretos da solução.
- [x] Referências internas entre passos estão corretas.
- [x] Interface visual (`IV1`) está coerente com o fluxo descrito.
- [x] Referências para Visão da Demanda, Glossário, RN e RNF estão atualizadas.

### 16.4. Revisão final
- [x] Não há contradições entre seções do artefato.
- [x] Links internos foram validados.
- [x] Documento revisado pela equipe do Grupo 9.
- [x] Artefato pronto para uso na especificação SRS e prototipação.
