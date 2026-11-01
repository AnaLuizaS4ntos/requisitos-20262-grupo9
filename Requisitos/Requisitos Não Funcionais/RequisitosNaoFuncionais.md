# Especificação de Requisitos Não Funcionais — Portal de Internacionalização

> Documento elaborado conforme o template oficial para registrar os Requisitos Não Funcionais (RNF) do **Portal de Internacionalização da Unifor (`requisitos-20262-grupo9`)**, com critérios objetivos, verificáveis e rastreáveis.

## Histórico de Versões

| Data | Versão | Descrição | Autor |
| --- | --- | --- | --- |
| 29/10/2026 | 1.0 | Especificação inicial dos Requisitos Não Funcionais do Portal de Internacionalização | Grupo 9 |

---

## 1. Requisitos de Produto

### 1.1. Eficiência de Desempenho

#### 1.1.1. Comportamento temporal
- **RNF-01 — Tempo de carregamento de páginas e guias:** As páginas públicas de guias informativos (intercâmbio, dupla titulação, vistos, aproveitamento, despesas e hospedagem) devem carregar seu conteúdo principal (*Largest Contentful Paint — LCP*) em no máximo **2,5 segundos** em conexões banda larga ou 4G padrão (mínimo de 10 Mbps).
- **RNF-02 — Tempo de resposta de busca e filtros:** A busca unificada por palavra-chave e a filtragem do catálogo de universidades parceiras (`RF-01`, `RF-02`) devem retornar os resultados em até **2,0 segundos** para até 95% das requisições.

#### 1.1.2. Capacidade
- **RNF-03 — Usuários simultâneos:** O portal deve suportar pelo menos **500 usuários simultâneos** em períodos de pico (como abertura de editais de intercâmbio e semanas de orientação internacional) sem degradação superior a 20% no tempo de resposta.

#### 1.1.3. Uso de recursos
- **RNF-04 — Otimização de mídia:** Imagens, ícones e documentos anexos (como modelos de *Learning Agreement* em PDF) devem ser otimizados para que o peso total de carregamento inicial de uma página não ultrapasse **2 MB**.

---

### 1.2. Flexibilidade (Portabilidade)

#### 1.2.1. Escalabilidade
- **RNF-05 — Crescimento de catálogo e idiomas:** A arquitetura do banco de dados e de conteúdo deve permitir a adição de novos países, instituições conveniadas e novos idiomas sem necessidade de alteração estrutural no código-fonte.

#### 1.2.2. Adaptabilidade (Responsividade Mobile-First)
- **RNF-06 — Layout responsivo multiplataforma:** Todas as telas públicas do portal devem adaptar-se automaticamente a resoluções mobile (a partir de `360px` de largura), tablets (`768px`) e desktops (`1280px+`), sem perda de funcionalidade ou barra de rolagem horizontal indevida.

#### 1.2.3. Instalabilidade
- Não se aplica ao usuário final (aplicação web acessível diretamente via navegador, sem necessidade de instalação local).

#### 1.2.4. Substituibilidade
- Não se aplica nesta fase do projeto.

---

### 1.3. Confiabilidade

#### 1.3.1. Maturidade
- **RNF-07 — Tratamento de links e páginas inexistentes:** O portal não deve exibir erros técnicos brutos (stack traces) ao usuário final, apresentando página amigável de erro `404` com atalho para a busca global e página inicial.

#### 1.3.2. Disponibilidade
- **RNF-08 — Disponibilidade contínua (24/7):** Por atender estudantes no Brasil e no exterior em diferentes fusos horários, o portal deve apresentar disponibilidade mínima de **99,5%** ao mês.

#### 1.3.3. Tolerância a falhas
- **RNF-09 — Fallback de idioma:** Caso um guia específico ainda não possua tradução publicada para o idioma selecionado pelo usuário (Inglês ou Espanhol), o sistema deve continuar operando normalmente, exibindo o conteúdo no idioma padrão (`PT-BR`) acompanhado de um aviso informativo no topo da página (`RN-03`).

#### 1.3.4. Recuperabilidade
- **RNF-10 — Backup e histórico de versões de conteúdo:** O banco de dados de conteúdos da DRI deve possuir rotina de backup diário automatizado e manter histórico das últimas versões publicadas de cada guia, permitindo restauração em até **4 horas** (*RTO*) em caso de falha ou publicação incorreta.

---

### 1.4. Segurança

#### 1.4.1. Confidencialidade
- **RNF-11 — Comunicação criptografada:** Todo o tráfego de dados entre o navegador do usuário e o servidor do portal deve ocorrer exclusivamente sob protocolo seguro **HTTPS (TLS 1.2 ou superior)**.

#### 1.4.2. Integridade
- **RNF-12 — Controle de acesso baseado em papéis (RBAC):** Apenas usuários autenticados com perfil autorizado da equipe da DRI (`AT-04`) podem criar, editar, aprovar ou excluir conteúdos no painel administrativo (`RF-10`). Usuários públicos possuem permissão estritamente de leitura nos guias.

#### 1.4.3. Não repúdio
- **RNF-13 — Log de auditoria editorial (Governança):** Toda criação, edição, publicação ou arquivamento de conteúdo no painel da DRI deve registrar log de auditoria contendo identificador do usuário responsável, data/hora (timestamp) e ação realizada.

#### 1.4.4. Autenticidade (Autenticação)
- **RNF-14 — Autenticação administrativa:** O acesso ao painel de governança da DRI deve exigir autenticação segura (preferencialmente integrada ao login institucional da Unifor) com expiração automática de sessão após **30 minutos** de inatividade.

#### 1.4.5. Resistência
- **RNF-15 — Proteção em formulários públicos:** O formulário de solicitação de orientação/contato (`RF-08`) deve implementar validação de entrada contra injeção de scripts (*XSS / SQL Injection*) e mecanismo anti-spam (*CAPTCHA* ou limitação de taxa de envio por IP).

---

### 1.5. Privacidade (Conformidade LGPD)

#### 1.5.1. Licitude e Finalidade
- **RNF-16 — Consentimento e finalidade na coleta de dados:** No formulário de solicitação de atendimento à DRI (`RF-08`), o sistema deve informar explicitamente a finalidade do tratamento dos dados e exigir a marcação de ciência/consentimento em conformidade com a **LGPD (Lei nº 13.709/2018)**.

#### 1.5.2. Necessidade (Minimização de Dados)
- **RNF-17 — Coleta mínima de dados pessoais:** A navegação nos guias do portal deve ser livre de cadastro obrigatório. Nos pedidos de orientação à DRI, devem ser solicitados apenas os dados estritamente necessários ao atendimento (nome, e-mail de contato, vínculo/curso e descrição da dúvida).

---

### 1.6. Capacidade de Interação (UX, Usabilidade, Acessibilidade e Multilíngue)

#### 1.6.1. Reconhecimento de adequação e Organização da Informação
- **RNF-18 — Arquitetura da informação orientada a perfil e jornada:** A página inicial deve apresentar trilhas claras por perfil (*Estudante Unifor*, *International Student*, *Docente*) e pelos 7 eixos do escopo (Intercâmbio, Dupla Titulação, Vistos/Documentação, Aproveitamento de Disciplinas, Despesas/Hospedagem, Serviços/Contatos DRI).

#### 1.6.2. Facilidade de aprendizado (*Learnability*) e Operabilidade
- **RNF-19 — Regra dos 3 cliques:** Qualquer guia informativo principal ou contato da DRI deve poder ser alcançado em no máximo **3 cliques** a partir da página inicial.

#### 1.6.3. Internacionalização e Suporte Multilíngue (i18n)
- **RNF-20 — Suporte nativo a múltiplos idiomas:** A interface do portal (menus, botões, filtros, rótulos e mensagens de sistema) e os conteúdos editoriais devem suportar no mínimo **Português (`pt-BR`)**, **Inglês (`en`)** e **Espanhol (`es`)**, com seletor de idioma persistente durante a sessão.

#### 1.6.4. Inclusividade e Acessibilidade Digital
- **RNF-21 — Conformidade com WCAG 2.1 Nível AA:** O portal deve cumprir os critérios de acessibilidade **WCAG 2.1 Nível AA**, garantindo:
  1. Contraste mínimo de **4.5:1** para textos normais e modo de **Alto Contraste** selecionável;
  2. Controle para aumento/redução do tamanho da fonte em até **200%** sem quebra de layout;
  3. Navegação completa via teclado (`Tab`, `Shift+Tab`, `Enter`, `Esc`) com foco visual nítido;
  4. Atributos `alt` descritivos em imagens e rótulos semânticos (`ARIA` / HTML5) compatíveis com leitores de tela (NVDA, VoiceOver).

---

### 1.7. Manutenibilidade

- **RNF-22 — Autonomia editorial (CMS):** A atualização de textos, perguntas frequentes, valores estimados de despesas e listas de universidades parceiras deve ser realizada integralmente pelo painel de governança da DRI, sem exigir intervenção da equipe de desenvolvimento ou novo deploy de código.

---

### 1.8. Compatibilidade

- **RNF-23 — Compatibilidade entre navegadores (*Cross-Browser*):** O portal deve funcionar corretamente nas duas últimas versões estáveis dos navegadores **Google Chrome, Mozilla Firefox, Microsoft Edge e Apple Safari** (desktop e mobile).

---

### 1.9. Segurança Operacional (*Safety*)

- Não se aplica (sistema de informação web sem controle de dispositivos físicos críticos).

---

### 1.10. Adequação Funcional

- **RNF-24 — Rastreabilidade temporal das orientações:** Todo guia informativo deve exibir de forma visível a **data da última revisão** e o setor responsável (DRI), garantindo transparência ao estudante e ao docente sobre a atualidade da informação.

---

## 2. Requisitos Externos

### 2.1. Ético
- **RNF-25 — Transparência e imparcialidade:** As orientações sobre estimativas de despesas e opções de hospedagem devem ter caráter educativo e institucional, sem favorecimento comercial indevido a fornecedores privados não conveniados.

### 2.2. Regulatório e Legislativo
- **RNF-26 — Conformidade legal (LGPD e Marco Civil da Internet):** O sistema deve operar em conformidade com a Lei nº 13.709/2018 (LGPD) e com as normas acadêmicas vigentes da Universidade de Fortaleza sobre mobilidade estudantil e aproveitamento de estudos.

---

## 3. Requisitos Organizacionais

### 3.1. Ambientais e Operacionais
- **RNF-27 — Padronização visual institucional:** A interface do portal deve seguir a identidade visual oficial da Universidade de Fortaleza (paleta de cores institucional em tons de azul e branco, tipografia legível e brasão/marca oficial).

### 3.2. Desenvolvimento
- **RNF-28 — Padronização de artefatos e versionamento:** Toda a documentação de requisitos, modelos UML e protótipos deve ser mantida versionada no repositório GitHub do grupo (`requisitos-20262-grupo9`) com rastreabilidade às issues das sprints.

---

## 4. Checklist de Validação do Artefato (RNF)

### 4.1. Estrutura e escopo
- [x] O documento possui histórico de versões preenchido.
- [x] O escopo da solução está claro no documento.
- [x] Há requisitos registrados nas seções aplicáveis (produto, externos e organizacionais).
- [x] Requisitos não aplicáveis estão explicitamente marcados como "Não se aplica".

### 4.2. Qualidade dos requisitos
- [x] Cada requisito está escrito de forma objetiva e verificável.
- [x] Cada requisito possui critério mensurável (tempo em segundos, percentual de disponibilidade, nível WCAG, idiomas suportados).
- [x] Não há requisito ambíguo com termos vagos sem métrica.
- [x] Requisitos duplicados ou conflitantes foram eliminados.

### 4.3. Conformidade e rastreabilidade
- [x] Requisitos regulatórios/legais relevantes (LGPD, WCAG) foram registrados.
- [x] Requisitos de privacidade e segurança foram contemplados.
- [x] Os requisitos estão alinhados com a Visão da Demanda, Glossário e Casos de Uso.
- [x] Existe rastreabilidade dos requisitos para as questões da Proposta 4 (acessibilidade, organização da informação, multilíngue e governança).

### 4.4. Prontidão para uso
- [x] Os requisitos podem ser usados como base para prototipação, implementação e testes.
- [x] Há insumos suficientes para criar critérios de aceitação.
- [x] O documento foi revisado pela equipe do Grupo 9.
- [x] A versão está pronta para entrega no Milestone M1.
