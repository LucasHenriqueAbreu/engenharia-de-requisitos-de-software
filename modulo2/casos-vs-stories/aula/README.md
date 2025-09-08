


# Roteiro de Aula – Casos de Uso vs. User Stories

## 1. Introdução

- Casos de uso e user stories são duas formas de representar requisitos funcionais.  
- Ambas descrevem **o que o sistema deve fazer**, mas diferem em nível de detalhe, formalidade e contexto de aplicação.  
- Compreender essas diferenças ajuda a escolher a técnica mais adequada em cada projeto.  
- [Fonte: Sommerville, *Engenharia de Software*, 10ª ed.]

## 2. Casos de Uso

- Representação estruturada que descreve **atores** (usuários ou sistemas externos) e suas interações com o sistema.  
- Mostra **como** e **por que** o sistema é utilizado em diferentes cenários.  
- Um caso de uso é composto por:  
  - **Ator:** quem interage com o sistema.  
  - **Objetivo:** o que o ator deseja alcançar.  
  - **Fluxo principal:** sequência normal de eventos até o objetivo ser atingido.  
  - **Fluxos alternativos:** caminhos opcionais ou exceções.  
  - **Pré-condições:** condições que devem ser verdadeiras antes da execução.  
  - **Pós-condições:** resultado esperado após a execução.  
- São frequentemente documentados em **diagramas de casos de uso UML** (visão macro) acompanhados de **descrições textuais detalhadas** (visão micro).  
- Usados principalmente em metodologias tradicionais ou híbridas, mas também podem complementar abordagens ágeis quando necessário.

### Vantagens
- Oferecem visão detalhada e clara dos cenários de uso.  
- Úteis para comunicação com clientes e equipes técnicas.  
- Servem como base para derivação de casos de teste.  
- Facilitam identificar fluxos alternativos, exceções e regras de negócio.

### Limitações
- Demandam mais esforço e tempo para serem produzidos.  
- Podem gerar documentação extensa e difícil de manter em projetos dinâmicos.  
- Menos adequados para ambientes onde requisitos mudam constantemente.

### Exemplo: Sistema de Biblioteca – Caso de Uso “Emprestar Livro”  
- **Ator:** Aluno  
- **Objetivo:** Realizar o empréstimo de um livro.  
- **Pré-condições:** O aluno deve estar cadastrado e sem multas pendentes.  
- **Fluxo Principal:**  
  1. O aluno solicita o empréstimo.  
  2. O sistema verifica disponibilidade do livro.  
  3. O sistema verifica se o aluno não excedeu o limite de empréstimos.  
  4. O sistema registra o empréstimo e atualiza o catálogo.  
  5. O sistema confirma o empréstimo ao aluno.  
- **Fluxo Alternativo (Livro indisponível):**  
  1. O sistema informa indisponibilidade e sugere reserva.  
- **Pós-condição:** O empréstimo é registrado no histórico do aluno.  

## 3. User Stories

- Descrições curtas, simples e focadas no valor para o usuário.  
- Comuns em metodologias ágeis.  
- Usam o formato **Connextra**:  
  > Como [usuário], quero [funcionalidade], para [benefício].  

### Vantagens
- Escrita rápida e simples.  
- Facilita priorização e adaptação contínua.  
- Foco direto no valor para o usuário.  

### Limitações
- Pouco detalhadas sem critérios de aceitação.  
- Exigem refinamento e discussões constantes.  

Exemplo:  
- Como aluno, quero reservar um livro online, para garantir disponibilidade quando for à biblioteca.  

#### Critérios de Aceitação (Gherkin)

- **Dado que** o aluno acessa o catálogo online  
- **Quando** ele reserva um livro disponível  
- **Então** o sistema deve marcar o livro como reservado e enviar confirmação.  

## 4. Comparação entre Casos de Uso e User Stories

| Aspecto                  | Casos de Uso                      | User Stories                          |
|---------------------------|------------------------------------|---------------------------------------|
| Nível de detalhe          | Alto, descreve fluxos completos   | Baixo, descrição breve e simples      |
| Estrutura                 | Formal, atores + cenários         | Informal, linguagem natural           |
| Esforço de produção       | Maior                             | Menor                                 |
| Adequação metodológica    | Projetos tradicionais/preditivos  | Projetos ágeis/incrementais           |
| Uso em testes             | Base para testes de aceitação     | Depende de critérios de aceitação     |

## 5. Estudo de Caso – Sistema de Biblioteca Universitária

- **Caso de Uso:** “Renovar Empréstimo”  
  - Ator: Aluno  
  - Fluxo principal: aluno solicita renovação → sistema verifica prazos e multas → atualiza data de devolução.  

- **User Story equivalente:**  
  > Como aluno, quero renovar meus empréstimos online, para evitar multas e facilitar meu acesso a livros.  

- **Critérios de Aceitação:**  
  - Renovação permitida apenas se não houver multas pendentes.  
  - Renovação limitada a 2 vezes por empréstimo.  
  - Confirmação deve ser exibida ao aluno.  

## 6. Exercício em Sala – Casos de Uso vs. User Stories

- Formem grupos de **3 alunos**.  
- Escolham um sistema simples (ex.: rede social, aplicativo de transporte, sistema acadêmico).  

### Parte 1 – Criar um Caso de Uso
- Elaborem um **caso de uso completo** para uma funcionalidade do sistema.  
- Incluam ator, fluxo principal e pelo menos 1 fluxo alternativo.  

### Parte 2 – Criar a User Story correspondente
- Transformem o mesmo requisito em uma **user story**, no formato Connextra.  
- Definam **3 critérios de aceitação** usando o modelo Gherkin.  

### Apresentação
- Cada grupo deve apresentar o caso de uso e a user story equivalente.  
- Discutam vantagens e limitações de cada abordagem no contexto escolhido.  

## Leitura Recomendada

- SOMMERVILLE, Ian. *Engenharia de Software*. 10ª ed. Pearson, 2019. Cap. 4 e Cap. 14.  
- PRESSMAN, Roger S.; MAXIM, Bruce R. *Engenharia de Software: Uma Abordagem Profissional*. 8ª ed. McGraw-Hill, 2016.  
- WIEGERS, Karl; BEATTY, Joy. *Software Requirements*. 3ª ed. Microsoft Press, 2013.  
- Documentação oficial do **Gherkin** – [https://cucumber.io/docs/gherkin/](https://cucumber.io/docs/gherkin/)