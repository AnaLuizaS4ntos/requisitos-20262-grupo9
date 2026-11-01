# Especificação de Requisitos Funcionais — Caso de Uso (CDU-02)

## Histórico de Versões

| Data | Versão | Descrição | Autor |
| --- | --- | --- | --- |
| 29/10/2026 | 1.0 | Especificação inicial do Caso de Uso CDU-02 (Gerenciar e Publicar Conteúdos do Portal — Governança DRI) | Grupo 9 |

---

## 1. Nome do Caso de Uso

**CDU-02 — Gerenciar e Publicar Conteúdos do Portal (Governança DRI)**

## 2. Objetivo

Permitir que a equipe autorizada da Diretoria de Relações Internacionais (DRI) cadastre, atualize, traduza (PT-BR, EN, ES), revise e publique guias informativos, acordos de intercâmbio/dupla titulação, estimativas de despesas e itens de FAQ, garantindo a governança e a rastreabilidade de versão das informações.

## 3. Tipo de Caso de Uso

Concreto.

## 4. Atores

### 4.1. Primário
- `AT-04` — Gestor de Conteúdo da DRI

### 4.2. Secundário
- `AT-06` — Sistema de Autenticação Institucional (Unifor Online)

## 5. Precondições

- O ator `AT-04` deve estar autenticado no painel administrativo e possuir permissão de gestão vinculada à DRI (`RNF-12`, `RNF-14`).

## 6. Fluxo Principal

### P1. Acessar o Painel de Governança de Conteúdo
O Gestor da DRI (`AT-04`) acessa o painel administrativo do portal. O sistema exibe a listagem de conteúdos existentes (Guias Temáticos, Instituições Parceiras / Dupla Titulação, Serviços e FAQ), destacando o status atual (**Rascunho**, **Publicado**, **Arquivado**) e sinalizando itens com revisão semestral pendente (`RN-02`).

### P2. Iniciar criação ou edição de conteúdo
O Gestor da DRI aciona a opção **"Novo Conteúdo"** ou seleciona um conteúdo existente para **"Editar"**.

### P3. Preencher dados estruturados e versões por idioma
O Gestor da DRI preenche ou atualiza os campos obrigatórios do conteúdo no idioma base (`PT-BR`) e, opcionalmente, nas abas de tradução (`EN` e `ES`):
- **P3.1.** Categoria do conteúdo (Programa de Intercâmbio, Dupla Titulação, Guia de Visto/Documentação, Aproveitamento de Disciplinas, Despesas/Hospedagem, Serviço DRI ou FAQ);
- **P3.2.** Público-alvo relacionado (`Estudante Outgoing`, `Estudante Incoming`, `Docente`);
- **P3.3.** Cursos elegíveis, país, pré-requisitos de idioma e corpo do guia/checklist;
- **P3.4.** Links oficiais de referência e anexos (quando aplicável).

### P4. Solicitar publicação do conteúdo
O Gestor da DRI revisa a pré-visualização da página e aciona a opção **"Aprovar e Publicar"** (`RN-01`).

### P5. Validar dados e publicar com registro de governança
O sistema valida o preenchimento dos campos obrigatórios, altera o status do conteúdo para **Publicado**, atualiza automaticamente a **data da última revisão**, incrementa a versão do documento, grava o registro no log de auditoria (`RNF-13`, `RN-02`) e disponibiliza imediatamente o conteúdo para consulta pública no portal.

## 7. Fluxos Alternativos

### A1. Salvar conteúdo como Rascunho (no passo P4)
- **A1.1.** O Gestor da DRI opta por acionar **"Salvar Rascunho"** para concluir a redação ou tradução posteriormente.
- **A1.2.** O sistema armazena as alterações com o status **Rascunho**, mantendo a versão anterior (se existir) visível ao público sem publicar as edições incompletas (`RN-01`).
- **A1.3.** O caso de uso é encerrado.

### A2. Arquivar conteúdo ou convênio encerrado (no passo P1)
- **A2.1.** O Gestor da DRI seleciona um guia ou acordo de mobilidade cujo convênio expirou e aciona **"Arquivar"**.
- **A2.2.** O sistema solicita confirmação, altera o status para **Arquivado**, retira o item da listagem pública de busca e preserva seu histórico para auditoria (`RNF-10`, `RNF-13`).
- **A2.3.** O caso de uso é encerrado.

## 8. Fluxos de Exceção

### E1. Campos obrigatórios não preenchidos na publicação (no passo P5)
- **E1.1.** Caso o Gestor tente publicar um conteúdo sem preencher os campos obrigatórios no idioma padrão (`PT-BR`) ou sem vincular os cursos elegíveis em um acordo de Dupla Titulação (`RN-03`, `RN-06`), o sistema impede a publicação e destaca os campos pendentes para correção, retornando ao passo **P3**.

## 9. Pós-condições

- O conteúdo atualizado fica disponível no portal público com data de revisão atualizada e histórico de auditoria salvo.

## 10. Requisitos Não Funcionais Específicos

- **RNF-12 / RNF-13 / RNF-14:** Controle de acesso RBAC, log de auditoria e sessão autenticada.
- **RNF-22:** Autonomia editorial via CMS sem necessidade de alteração de código.

## 11. Ponto de Extensão

Não se aplica.

## 12. Frequência de Utilização

Média (atualizações semanais/mensais e revisões gerais a cada semestre letivo).

## 13. Interface Visual

### IV2. Painel Administrativo de Governança de Conteúdo (DRI)
- **Localização:** Protótipos a serem detalhados na pasta `images/` na entrega **M2 (Trabalho P2)**.
- **Elementos previstos:** Dashboard com indicadores de conteúdos publicados e alertas de revisão pendente (`> 180 dias`); editor estruturado com abas de idioma (`Português`, `English`, `Español`); botões de *Salvar Rascunho*, *Pré-visualizar* e *Publicar*.

## 14. Observações

- Garante o atendimento direto à questão de levantamento **"Governança de Conteúdo"** especificada na Proposta 4.

## 15. Referências

- [Visão da Demanda](../Elicitacao/VisaoDemanda.md) — Funcionalidade `F-09` (`NEC-07`)
- [Backlog e Requisitos Funcionais](../Elicitacao/BacklogPriorizado.md) — `RF-10`, `RF-11`
- [Regras de Negócio](../Especifica%C3%A7%C3%A3o%20de%20Regra%20de%20Negocio/RegrasDeNegocio.md) — `RN-01`, `RN-02`, `RN-03`, `RN-06`

---

## 16. Checklist de Validação do Artefato (CDU)

### 16.1. Estrutura mínima
- [x] Nome do caso de uso iniciado com verbo no infinitivo.
- [x] Objetivo claro, direto e com foco em um objetivo principal.
- [x] Tipo do caso de uso informado (concreto).
- [x] Atores primário e secundário identificados (`AT-04`, `AT-06`).
- [x] Precondições registradas.
- [x] Fluxo principal completo e coerente com o objetivo.
- [x] Fluxos alternativos e de exceção definidos.
- [x] Pós-condições registradas.
- [x] Requisitos não funcionais específicos registrados.
- [x] Pontos de extensão marcados como "Não se aplica".
- [x] Frequência de utilização estimada.

### 16.2. Qualidade da especificação
- [x] Passos escritos com linguagem simples e objetiva.
- [x] Ações descritas com verbos no presente do indicativo (3ª pessoa).
- [x] Alternância entre ação do ator e ação da solução está clara.
- [x] Não há ambiguidade.
- [x] Regras de negócio (`RN-01`, `RN-02`, `RN-03`, `RN-06`) referenciadas.

### 16.3. Consistência e rastreabilidade
- [x] Pontos de entrada e saída dos fluxos alternativos estão explícitos.
- [x] Fluxo de exceção vinculado ao passo de validação (`P5`).
- [x] Referências internas corretas.
- [x] Interface visual (`IV2`) coerente com o fluxo.
- [x] Referências para Visão da Demanda, RN e RNF atualizadas.

### 16.4. Revisão final
- [x] Não há contradições entre seções do artefato.
- [x] Links internos validados.
- [x] Documento revisado pela equipe do Grupo 9.
- [x] Artefato pronto para uso na especificação SRS e prototipação.
