


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

- Baseados no **Manifesto Ágil** (2001), que valoriza indivíduos e interações, software funcionando, colaboração com o cliente e resposta a mudanças.  
- Requisitos são representados de forma simples, geralmente como **user stories**, que descrevem funcionalidades do ponto de vista do usuário.  
- Os requisitos são organizados em um **backlog de produto**, priorizados pelo valor que entregam ao cliente.  
- Mudanças são esperadas e aceitas ao longo do processo, com ciclos curtos (iterações ou sprints) que permitem adaptação rápida.  
- O foco está em entregas incrementais, feedback contínuo e melhoria constante da equipe.  

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

- Ferramenta auxiliar: **INVEST** (Independent, Negotiable, Valuable, Estimable, Small, Testable) para avaliar a qualidade de uma user story.

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

## 5. Estudo de Caso – Sistema de Agendamento Médico

- **Modelo Preditivo:** todos os requisitos são levantados e documentados antes do desenvolvimento. Mudanças posteriores exigem renegociação formal.  
- **Modelo Ágil:** requisitos são levantados em forma de user stories no backlog. A cada sprint, novos requisitos são refinados e implementados.  

## 6. Exercício em Sala

- Formem grupos de 3 alunos.  
- Escolham um sistema simples (ex.: biblioteca, rede social, app de transporte).  
- Modelem os requisitos sob duas perspectivas:  
  1. Abordagem preditiva (lista detalhada inicial).  
  2. Abordagem ágil (user stories para backlog).  
- Compare as vantagens e limitações percebidas em cada abordagem.  
- Preparem para apresentar para a turma.  

## Leitura Recomendada

- SOMMERVILLE, Ian. *Engenharia de Software*. 10ª ed. Pearson, 2019. Cap. 4 e Cap. 22.  
- PRESSMAN, Roger S.; MAXIM, Bruce R. *Engenharia de Software: Uma Abordagem Profissional*. 8ª ed. McGraw-Hill, 2016.  
- BECK, Kent et al. *Manifesto Ágil* (2001). Disponível em: [https://agilemanifesto.org/](https://agilemanifesto.org/).