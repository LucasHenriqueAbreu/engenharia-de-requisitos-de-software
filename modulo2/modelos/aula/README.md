# Roteiro de Aula – Modelos Preditivos e Ágeis

## 1. Introdução aos Processos de Engenharia de Requisitos

- Os processos de requisitos definem como os requisitos são levantados, documentados e acompanhados ao longo do ciclo de vida do software.  
- Existem duas grandes abordagens: **preditivas** e **ágeis**.  
- A escolha do modelo impacta diretamente na forma como os requisitos são tratados.  
- [Fonte: Sommerville, *Engenharia de Software*, 10ª ed.]

## 2. Modelos Preditivos

- Planejamento detalhado antes da implementação.  
- Requisitos levantados no início e documentados em profundidade.  
- Mudanças posteriores são difíceis e custosas.  

### Vantagens
- Previsibilidade no cronograma e orçamento.  
- Documentação robusta para auditoria e contratos.  
- Mais adequado para projetos com requisitos estáveis.  

### Limitações
- Pouca flexibilidade para mudanças.  
- Alto risco de desalinhamento se os requisitos mudarem.  
- Possibilidade de “software inútil” se o ambiente mudar rapidamente.  

Exemplos: **Modelo Cascata (Waterfall)**, **RUP (Rational Unified Process)**.

## 3. Modelos Ágeis

- Surgem como alternativa aos modelos preditivos, privilegiando adaptação, colaboração e entregas frequentes.  
- Requisitos são representados de forma simples, geralmente como **user stories**, que descrevem funcionalidades do ponto de vista do usuário.  
- Os requisitos são organizados em um **backlog de produto**, priorizados pelo valor que entregam ao cliente.  
- Mudanças são esperadas e aceitas ao longo do processo, com ciclos curtos (iterações ou sprints) que permitem adaptação rápida.  
- O foco está em entregas incrementais, feedback contínuo e melhoria constante da equipe.  

### O Manifesto Ágil

O Manifesto Ágil (2001) apresenta quatro valores principais:

1. **Indivíduos e interações** mais que processos e ferramentas  
2. **Software em funcionamento** mais que documentação abrangente  
3. **Colaboração com o cliente** mais que negociação de contratos  
4. **Responder a mudanças** mais que seguir um plano  

Esses valores orientam práticas como user stories, backlog, sprints e retrospectivas.

### Como construir User Stories

- Uma **user story** é uma breve descrição de funcionalidade, escrita do ponto de vista do usuário.  
- Estrutura comum (modelo *Connextra*):  
  > **Como** [tipo de usuário], **quero** [funcionalidade], **para** [benefício/valor].  

- Exemplos:
  - Como aluno, quero visualizar minhas notas no portal acadêmico, para acompanhar meu desempenho.  
  - Como cliente de e-commerce, quero receber notificações de entrega, para saber quando meu pedido chegará.  

- Boas práticas para user stories:
  - Devem ser curtas, claras e de fácil entendimento.  
  - Devem conter **critérios de aceitação**, que definem quando a story pode ser considerada concluída.  
  - Devem ser negociáveis e priorizáveis.  

#### Critérios de Aceitação e o Modelo Gherkin

Os **critérios de aceitação** definem quando uma user story pode ser considerada concluída.  
Uma forma comum de descrevê-los é usando o **modelo Gherkin**, que ajuda a estruturar cenários de forma clara e testável.

**Estrutura Gherkin:**
- **Dado que** [contexto inicial]  
- **Quando** [ação executada]  
- **Então** [resultado esperado]

**Exemplo (User Story de Login):**
> Como usuário, quero fazer login com e-mail e senha, para acessar minha conta com segurança.

Critérios de aceitação (Gherkin):
- Dado que o usuário está na tela de login  
  Quando informar um e-mail e senha válidos  
  Então deve acessar sua conta com sucesso.  

- Dado que o usuário está na tela de login  
  Quando informar credenciais inválidas  
  Então deve ver a mensagem “Usuário ou senha incorretos”.  

#### Checklist INVEST para User Stories

- **I — Independent (Independente):** a story deve ser autônoma, sem dependências rígidas para entregar valor.  
  *Ex.:* “Gerar 2ª via do boleto” não deve depender de “Cadastro de endereço” para ser entregue.
- **N — Negotiable (Negociável):** a story é um convite à conversa; detalhes são refinados no backlog refinement.  
  *Evite* tratá-la como contrato fechado.
- **V — Valuable (Valiosa):** precisa entregar valor claro ao usuário/negócio.  
  *Ex.:* “Como cliente, quero salvar meu cartão para pagar mais rápido.”
- **E — Estimable (Estimável):** a equipe consegue estimar esforço; se não, falta informação ou está grande demais.  
  *Dica:* fatie por fluxos, regras ou plataformas.
- **S — Small (Pequena):** cabe em um sprint; procure < 1/4 do sprint como referência prática.  
  *Ex.:* separar “cadastrar cartão” de “editar cartão”.
- **T — Testable (Testável):** possui critérios de aceitação verificáveis.  
  *Ex.:* “Dado que sou cliente logado… Quando salvo um cartão válido… Então devo ver a mensagem ‘Cartão salvo’ e o cartão deve aparecer na minha carteira.”

> Use o INVEST como checklist durante o *refinement* e antes de levar a história para a sprint.

### Exemplo Completo de User Story

Vamos aplicar o checklist **INVEST** em um exemplo prático de sistema acadêmico.

**User Story:**
> Como aluno, quero visualizar minhas notas no portal acadêmico, para acompanhar meu desempenho.

**Critérios de Aceitação:**
1. O sistema deve exibir todas as disciplinas matriculadas no semestre atual.  
2. Para cada disciplina, deve mostrar as notas parciais e a nota final.  
3. Se o professor ainda não tiver lançado notas, deve aparecer a mensagem “Notas em lançamento”.  
4. O tempo de carregamento da tela deve ser inferior a 3 segundos.  

**Análise segundo INVEST:**
- **I – Independent:** não depende de outra story para ser entregue.  
- **N – Negotiable:** os detalhes da interface podem ser ajustados durante o desenvolvimento.  
- **V – Valuable:** entrega valor direto ao aluno.  
- **E – Estimable:** a equipe consegue estimar esforço para implementar.  
- **S – Small:** pode ser implementada dentro de uma sprint.  
- **T – Testable:** critérios de aceitação permitem verificar se foi concluída corretamente.  

### Da Especificação Tradicional para User Stories

Uma dúvida comum é como transformar **requisitos funcionais, não funcionais e de domínio** (modelos preditivos) em **user stories e critérios de aceitação** (modelos ágeis).  
Veja exemplos comparativos:

| Tipo de Requisito (Tradicional) | Exemplo (Preditivo) | User Story (Ágil) | Critérios de Aceitação |
|---------------------------------|----------------------|-------------------|-------------------------|
| **Funcional** | “O sistema deve permitir login com e-mail e senha.” | “Como usuário, quero fazer login com e-mail e senha, para acessar minha conta com segurança.” | - O usuário deve informar e-mail e senha válidos.<br>- Caso os dados estejam incorretos, mostrar mensagem de erro. |
| **Não Funcional** | “A tela de login deve carregar em menos de 2 segundos.” | Integrado à User Story de login como critério de aceitação. | - O tempo de resposta deve ser < 2 segundos em 95% das tentativas. |
| **De Domínio** | “Máx. 5 empréstimos por usuário (política da biblioteca)” | “Como bibliotecário, quero que o sistema aplique o limite de 5 empréstimos por usuário, para cumprir a política da biblioteca.” | Bloquear acima do limite; informar quantos empréstimos restam; registrar tentativa no histórico. |

### Observação Didática

- **Requisitos funcionais** → geralmente viram **user stories**.  
- **Requisitos não funcionais** → aparecem como **critérios de aceitação** ou histórias técnicas.  
- **Requisitos de domínio** → podem virar user stories ou regras de negócio aplicadas em várias histórias.  

Essa transição ajuda a conectar a documentação tradicional (ERS) com práticas ágeis, permitindo que alunos entendam como os mesmos requisitos podem ser representados em diferentes abordagens.

---

### Vantagens
- Adaptação rápida a mudanças.  
- Entregas frequentes de valor ao cliente.  
- Maior engajamento dos stakeholders.  

### Limitações
- Documentação mínima pode gerar lacunas.  
- Exige alta colaboração dos usuários.  
- Dificuldade em projetos regulatórios ou com requisitos muito estáveis.  

Exemplos: **Scrum**, **Kanban**, **Extreme Programming (XP)**.

## 4. Comparação entre os Modelos

| Aspecto              | Preditivo                        | Ágil                               |
|-----------------------|----------------------------------|------------------------------------|
| Levantamento          | Completo, no início do projeto   | Contínuo, ao longo do projeto      |
| Documentação          | Extensa e detalhada              | Leve, apenas o necessário          |
| Flexibilidade         | Baixa                            | Alta                               |
| Entregas              | Produto ao final                 | Incrementos frequentes             |
| Participação do cliente | Pontual, em revisões            | Constante, em cada iteração        |

### Foco de cada abordagem

- **Modelo Preditivo:** o foco está em entregar o sistema completo ao final do projeto. Todo o esforço inicial é dedicado a levantar e documentar todos os requisitos para que a entrega final seja um produto fechado, com poucas mudanças ao longo do caminho.  
- **Modelo Ágil:** o foco está em resolver as principais dores do cliente de forma incremental. O sistema é construído em partes, entregando valor gradualmente, permitindo ajustes frequentes de acordo com feedback e novas necessidades identificadas.

## 5. Estudo de Caso – Sistema de Agendamento Médico

- **Modelo Preditivo:** todos os requisitos são levantados e documentados antes do desenvolvimento. Mudanças posteriores exigem renegociação formal.  
- **Modelo Ágil:** requisitos são levantados em forma de user stories no backlog. A cada sprint, novos requisitos são refinados e implementados.  

## 6. Exercício em Sala – Da Especificação Tradicional para User Stories

- Formem grupos de **3 alunos**.
- Escolham um sistema simples (ex.: biblioteca, rede social, app de transporte, agendamento médico).

### Parte 1 – Transformar requisitos preditivos em user stories
1. Elaborem uma **mini documentação preditiva** com **3 requisitos**:
   - 1 **Requisito Funcional (RF)**
   - 1 **Requisito Não Funcional (RNF)**
   - 1 **Requisito de Domínio (RD)**
2. **Transformem 2 desses requisitos** (preferencialmente 1 RF + 1 RD) em **user stories completas**, com **critérios de aceitação**.
3. Apliquem o **checklist INVEST** a cada story e registrem brevemente os pontos atendidos.

**Modelo de user story (Connextra):**  
> Como **[tipo de usuário]**, quero **[funcionalidade]**, para **[benefício/valor]**.

**Modelo de critérios de aceitação (Gherkin – opcional):**  
- Dado que **[contexto]**  
- Quando **[ação]**  
- Então **[resultado observável/mensurável]**

**Exemplo rápido (agendamento médico):**  
- Requisito (RD): “Cancelamentos só podem ocorrer até 24h antes da consulta.”  
- Story: “Como paciente, quero **cancelar minha consulta até 24h antes**, para **liberar o horário e evitar multa**.”  
- Critérios:  
  - Dado que tenho uma consulta marcada em **t < 24h**, quando tento cancelar, **então** devo ver a mensagem “Cancelamento indisponível (menos de 24h)”.  
  - Dado que tenho consulta em **t ≥ 24h**, quando cancelo, **então** devo receber **confirmação por e-mail**.  
  - O tempo de resposta do cancelamento deve ser **< 2s em 95% dos casos** (RNF incorporado como critério).

---

### Parte 2 – Criar uma user story do zero
1. Identifiquem uma **dor real do usuário** no sistema escolhido.
2. Escrevam **1 nova user story original** (não derivada dos requisitos da Parte 1), com **3–5 critérios de aceitação**.
3. Apliquem o **INVEST** e registrem a avaliação (2–3 linhas).
4. 
---

### Papéis sugeridos no grupo
- **Analista** (conduz escrita das stories)  
- **“Product Owner”** (define valor/prioridade)  
- **QA/Documentador** (escreve critérios e aplica INVEST)

## Leitura Recomendada

- SOMMERVILLE, Ian. *Engenharia de Software*. 10ª ed. Pearson, 2019. Cap. 4 e Cap. 22.  
- PRESSMAN, Roger S.; MAXIM, Bruce R. *Engenharia de Software: Uma Abordagem Profissional*. 8ª ed. McGraw-Hill, 2016.  
- BECK, Kent et al. *Manifesto Ágil* (2001). Disponível em: [https://agilemanifesto.org/](https://agilemanifesto.org/).
- Documentação oficial do **Gherkin** – [https://cucumber.io/docs/gherkin/](https://cucumber.io/docs/gherkin/)