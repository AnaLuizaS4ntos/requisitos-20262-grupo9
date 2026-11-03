# Visão da Demanda (VD) — Template LAPIS

> **Versão do template:** 2.1 (proposta revisada) | **Aplicação:** processo de requisitos LAPIS, etapa de Elicitação, com refinamento nas etapas de Especificação e Validação.

> **Como usar**
>
> - Use este template para novos sistemas, evoluções, integrações ou manutenção.
> - Substitua os campos entre colchetes e remova as orientações após preencher.
> - Mantenha o documento como panorama do problema, valor, público e escopo. Ajuste a profundidade ao tamanho da demanda.
> - Especifique fluxos, precondições, exceções e critérios de aceitação das funcionalidades em casos de uso ou documentos equivalentes, vinculados na seção 7.
> - Mantenha regras compartilhadas, requisitos de qualidade detalhados, arquitetura e contratos em suas referências próprias. Não duplique seu conteúdo aqui.
> - Registre dúvidas como **A definir**, com responsável. Propostas elaboradas com apoio de IA devem ser revisadas antes de serem consideradas validadas.
> - Se uma seção não se aplicar, indique **Não se aplica** com justificativa breve. Não há quantidade mínima de personas ou diagramas.
> - As orientações de integração com o processo e com IA pertencem ao template e ao guia de elaboração; remova-as da VD preenchida.
> - Utilize o [guia LAPIS de elaboração da visão](../../Elicitacao/VisaoDemanda.md), quando este template estiver na pasta `Requisitos/Artefatos/Templates/`.
> - Mapas de histórias, diagramas de casos de uso e protótipos podem ajudar a comunicar o escopo; use-os quando agregarem clareza, sem transformar a VD em documento de arquitetura.

## Identificação e Histórico

| Campo | Informação |
| --- | --- |
| Nome e identificador da demanda | [Nome e código, se houver] |
| Tipo | [Novo sistema / evolução / integração / manutenção / outro] |
| Sistema ou produto relacionado | [Nome ou não aplicável] |
| Área solicitante | [Área] |
| Responsável pela elaboração | [Nome e papel] |
| Responsável pela validação | [Nome e papel] |
| Situação do documento | [Rascunho / em revisão / validado] |
| Versão e data | [Versão — dd/mm/aaaa] |

| Data | Versão | Descrição da alteração | Autor |
| --- | --- | --- | --- |
| [dd/mm/aaaa] | [1.0] | [Criação ou alteração realizada] | [Nome] |

## 1. Objetivo

Descreva o resultado que a demanda pretende alcançar e para quem, sem detalhar a implementação.

> [Permitir que determinado público realize uma atividade ou alcance um resultado, resolvendo uma necessidade identificada.]

## 2. Contexto, Problema e Descrição Sumária da Demanda

Apresente o contexto do negócio e um resumo da mudança pretendida. Para evoluções, indique a situação atual e a situação desejada.

- **Situação atual:** [Como a atividade é realizada hoje.]
- **Problema ou oportunidade:** [O que precisa mudar e por quê.]
- **Públicos afetados e impactos:** [Quem é afetado e quais são as consequências.]
- **Evidências disponíveis:** [Dados ou exemplos e suas fontes; identificar hipóteses.]
- **Descrição sumária da demanda:** [Síntese das capacidades propostas, sem descrever fluxos nem antecipar decisões técnicas.]

## 3. Proposta de Valor e Sucesso da Demanda

Resuma os benefícios e como avaliar o resultado global. Critérios de aceitação de funcionalidades pertencem às respectivas especificações.

| Benefício esperado | Indicador ou evidência | Resultado desejado | Como e quando avaliar |
| --- | --- | --- | --- |
| [Benefício] | [Métrica ou evidência observável; situação atual, se conhecida] | [Meta ou condição de sucesso] | [Forma e momento de avaliação] |

> Identifique estimativas como hipóteses. Se faltarem dados para uma meta, registre a necessidade de levantamento na seção 10.

## 4. Partes Interessadas

Liste quem solicita, decide, desenvolve, opera ou valida a solução, conforme aplicável.

| Parte interessada | Papel e interesse | Responsabilidade | Representante |
| --- | --- | --- | --- |
| [Área, equipe ou pessoa] | [Papel e interesse] | [Decisões ou atividades] | [Nome ou a definir] |

## 5. Usuários e Atores Externos

Descreva os perfis e sistemas que interagem com a solução. Sistemas e dispositivos são atores externos, não personas. Personas detalhadas são opcionais e podem ser referenciadas na seção 11. Crie personas apenas quando suas necessidades e características influenciarem decisões de escopo ou experiência.

| ID | Usuário, sistema ou dispositivo | Objetivo ou papel na interação | Contexto de uso relevante |
| --- | --- | --- | --- |
| AT-01 | [Perfil ou nome] | [O que realiza, solicita, fornece ou recebe] | [Ambiente e necessidades relevantes] |

## 6. Escopo e Entregas Previstas

### 6.1. Incluído na demanda

- [Capacidade ou resultado que será atendido.]

### 6.2. Fora do escopo

- [Capacidade ou responsabilidade que não será atendida nesta demanda.]

### 6.3. Evoluções futuras — opcional

- [Possibilidade futura, sem compromisso de implementação nesta demanda.]

### 6.4. Entregas e marcos — quando conhecidos

| Entrega ou marco | Resultado previsto | Data ou condição | Natureza do prazo |
| --- | --- | --- | --- |
| [Entrega] | [Resultado] | [Data, condição ou a definir] | [Obrigatório / estimado / a definir] |

## 7. Necessidades e Catálogo de Funcionalidades

Apresente apenas o resumo das capacidades. Use identificadores estáveis para vincular a visão aos documentos que detalham seu comportamento.

| ID | Necessidade | Fonte ou evidência | Públicos ou atores relacionados |
| --- | --- | --- | --- |
| NEC-01 | [Problema ou resultado necessário] | [Entrevista, observação, documento, norma ou link; a confirmar quando necessário] | [AT-01] |

| ID | Funcionalidade e resultado esperado | Necessidade | Atores (IDs) | Prioridade | Valor | Frequência | Escopo ou entrega | Especificação |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| F-01 | [Nome e descrição breve da capacidade] | NEC-01 | AT-01 | [Essencial / importante / desejável] | [Alto / médio / baixo / a definir] | [Alta / média / baixa / a definir] | [Entrega / futura / em avaliação] | [CDU-01 — link ou a elaborar] |

> **Prioridade:** essencial = necessária para cumprir o objetivo; importante = agrega valor e admite alternativa temporária; desejável = pode ser adiada sem comprometer o objetivo. **Valor** indica benefício relativo (alto, médio, baixo); **frequência** indica recorrência esperada de uso (alta, média, baixa). Não confunda prioridade, valor e frequência. Registre **A definir** quando não houver evidência suficiente.
>
> **Rastreabilidade:** fonte/evidência → `NEC-01` → `F-01` → `CDU-01` → testes (estes últimos detalhados em artefatos próprios). Na coluna Atores, use somente IDs cadastrados na seção 5; não repita suas descrições.
>
> Uma funcionalidade pode ser detalhada por um ou mais casos de uso. Registre os atores específicos, passos, alternativas, exceções, regras aplicáveis e critérios de aceitação nesses documentos. A indicação da entrega não representa situação de implementação.

## 8. Visão Geral da Solução e Impactos

Descreva brevemente os limites da solução, suas responsabilidades, as principais interações externas e os impactos conhecidos em soluções existentes. Identifique propostas ainda não confirmadas.

- **Responsabilidades da solução:** [O que ficará sob sua responsabilidade.]
- **Sistemas ou dispositivos externos:** [Quais participam e para qual finalidade.]
- **Integrações principais:** [Resumo das informações ou serviços trocados.]
- **Diagrama de contexto — opcional:** [Imagem ou referência, quando facilitar a compreensão.]
- **Arquitetura e contratos detalhados:** [Referências da seção 11 ou a elaborar.]

### 8.1. Sistemas e processos impactados

| Sistema ou processo | Impacto esperado | Responsável ou dependência | Situação |
| --- | --- | --- | --- |
| [Nome] | [Mudança esperada, apenas em alto nível] | [Área/pessoa ou a definir] | [Confirmado / hipótese / a definir] |

### 8.2. Representações visuais — opcionais

- **Mapa de histórias ou diagrama geral de casos de uso:** [Link/imagem ou não se aplica; mostre atores e principais interações, sem detalhar os fluxos.]
- **Protótipo de baixa fidelidade:** [Link/imagem ou não se aplica, se ajudar a delimitar escopo.]
- **Diagramas de componentes/implantação:** [Somente referência a documento técnico existente, quando necessário. Não são obrigatórios na VD.]

> Decisões sobre componentes internos, protocolos, formatos de mensagens e implantação devem ser detalhadas nos documentos técnicos relacionados.

## 9. Condições Gerais da Demanda

Resuma apenas condições que influenciam o escopo ou a viabilidade. Referencie definições detalhadas de regras e requisitos de qualidade.

| Tipo | Condição e impacto na demanda | Responsável ou fonte | Referência, se houver |
| --- | --- | --- | --- |
| [Premissa / restrição / dependência / qualidade / regra geral] | [Resumo da condição e impacto] | [Responsável ou fonte] | [Documento ou a definir] |

> **Premissa:** hipótese a confirmar. **Restrição:** limite conhecido. **Dependência:** recurso ou ação necessária de outra parte. Para qualidade, considere necessidades relevantes de segurança, desempenho, acessibilidade, disponibilidade ou compatibilidade, sem repetir sua especificação detalhada.

## 10. Riscos e Questões em Aberto

Registre apenas os itens relevantes para definir ou validar a visão. O acompanhamento detalhado pode ocorrer em ferramenta ou documento vinculado.

| ID | Tipo | Risco ou questão | Impacto | Próxima ação | Responsável e prazo | Situação |
| --- | --- | --- | --- | --- | --- | --- |
| PQ-01 | [Risco / dúvida / decisão pendente] | [Descrição] | [Consequência] | [Ação] | [Nome e data ou a definir] | [Aberto / resolvido / aceito] |

> Ao resolver uma questão, atualize a seção afetada e o histórico. Decisões que precisem de justificativa própria devem ser vinculadas na seção 11.

## 11. Documentos Relacionados

Vincule apenas os documentos necessários. Especificações por funcionalidade ficam na seção 7; registre aqui referências gerais ou compartilhadas.

| Documento | Conteúdo sob sua responsabilidade | Referência e situação |
| --- | --- | --- |
| [Regras de negócio compartilhadas] | [Políticas e condições comuns a vários casos de uso] | [Link / a elaborar / não aplicável] |
| [Requisitos não funcionais ou de qualidade] | [Requisitos detalhados e critérios de verificação] | [Link / a elaborar / não aplicável] |
| [Arquitetura e contratos de integração] | [Decisões técnicas e interfaces] | [Link / a elaborar / não aplicável] |
| [Glossário] | [Termos e definições do domínio] | [Link / a elaborar / não aplicável] |
| [Outros necessários] | [Finalidade] | [Link e situação] |

## 12. Validação da Visão

### 12.1. Checklist

- [ ] Objetivo, contexto e problema estão claros.
- [ ] Benefícios e condições de sucesso estão descritos, com hipóteses identificadas.
- [ ] Responsáveis por decisões e validação estão identificados.
- [ ] Usuários e atores externos relevantes estão representados.
- [ ] Escopo, exclusões e possíveis evoluções estão diferenciados.
- [ ] Necessidades têm identificadores e fontes/evidências (ou indicação de levantamento pendente).
- [ ] Funcionalidades têm identificadores, prioridades, atores por ID e vínculo com necessidades.
- [ ] Valor e frequência são tratados separadamente e estimados quando úteis, ou marcados como **A definir**.
- [ ] Cada funcionalidade tem referência à especificação ou indicação de que será elaborada.
- [ ] A visão geral da solução esclarece seus limites, interações externas e impactos em outros sistemas ou processos.
- [ ] Diagramas e protótipos foram incluídos apenas quando agregam clareza, sem detalhamento técnico indevido.
- [ ] Restrições, premissas, dependências e pendências relevantes estão registradas.
- [ ] Informações detalhadas estão nos documentos apropriados, com referências consistentes.
- [ ] O conteúdo foi revisado pelos responsáveis, inclusive quando elaborado com apoio de IA.

### 12.2. Critérios de conclusão e encaminhamento

A avaliação da VD deve indicar uma das seguintes condições, sem exigir que todos os casos de uso já estejam detalhados:

- **Apta para iniciar a especificação:** objetivos, envolvidos, limites do escopo, necessidades e catálogo inicial são suficientemente claros; pendências remanescentes estão registradas com responsáveis. Não equivale a aprovação final da VD.
- **Validada pelas partes interessadas:** responsáveis confirmaram o entendimento geral e o escopo da demanda; ressalvas aceitas são explícitas e rastreáveis.
- **Com pendências impeditivas:** há decisões ou informações ausentes que impedem estabelecer o escopo ou iniciar especificações com segurança. Registrar as pendências na seção 10, seus responsáveis e ações necessárias.

> Os estados representam condições de encaminhamento da Visão; a validação do comportamento de cada funcionalidade ocorre nas especificações correspondentes.

### 12.3. Registro da validação

| Versão | Responsável e papel | Data | Condição da VD | Resultado e ressalvas |
| --- | --- | --- | --- | --- |
| [Versão] | [Nome e papel] | [Data] | [Apta para especificação / validada / pendências impeditivas] | [Registro das decisões e pendências aceitas] |

> Validar a visão confirma o entendimento geral da demanda. As funcionalidades devem ser especificadas e validadas antes de sua implementação; a aceitação do software depende das evidências previstas nesses documentos.


---

## Orientações do template para o processo LAPIS (remover da VD preenchida)

- **Análise de Viabilidade:** fornece problema inicial, restrições e riscos conhecidos; a VD não substitui o parecer de viabilidade.
- **Elicitação:** produz a primeira VD com objetivos, atores, necessidades, funcionalidades e escopo.
- **Especificação:** utiliza os identificadores `NEC-`, `F-` e `AT-` para detalhar casos de uso, fluxos UML por cenário, regras e critérios de aceitação em documentos próprios.
- **Validação:** confirma a visão com as partes interessadas; a validação das especificações e a aceitação do software são atividades distintas.

**Orientação para IA:** identificar lacunas e inconsistências, preservar fontes e rastreabilidade, não transformar hipóteses em decisões, não inventar metas ou aprovações e não implementar comportamentos ainda não especificados. Toda proposta apoiada por IA exige revisão humana.

**Histórico do template:** versão 2.1 evolui a versão 2.0 ao separar valor e frequência, registrar a fonte das necessidades, identificar critérios de conclusão da VD, evitar duplicação de descrições de atores e distinguir orientações do modelo do documento preenchido.
