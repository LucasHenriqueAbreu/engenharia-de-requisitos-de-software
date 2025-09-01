---
theme: gaia
_class: lead
paginate: true
backgroundColor: #fff
backgroundImage: url('../../../assets/background.svg')
marp: true
---

![bg left:40% 80%](../../../assets/logo.png)

# **Engenharia de Requisitos**
### Módulo 2
#### Modelos Preditivos e Ágeis
##### Prof. Lucas Henrique de Abreu

---

## Introdução aos Processos

- Processos definem como requisitos são levantados, documentados e acompanhados  
- Duas grandes abordagens: **Preditivas** e **Ágeis**  
- A escolha impacta diretamente como os requisitos são tratados  

[Fonte: Sommerville, Engenharia de Software]

---

## Modelos Preditivos

- Planejamento detalhado antes da implementação  
- Requisitos levantados no início e documentados em profundidade  
- Mudanças posteriores são difíceis e custosas  

Exemplos: **Waterfall**, **RUP**

---

## Vantagens (Preditivo)

- Previsibilidade no cronograma e orçamento  
- Documentação robusta para auditoria e contratos  
- Adequado para requisitos estáveis  

---

## Limitações (Preditivo)

- Pouca flexibilidade  
- Risco de desalinhamento se requisitos mudarem  
- Possibilidade de “software inútil” se ambiente mudar rápido  

---

## Modelos Ágeis

- Alternativa ao preditivo  
- Priorizam adaptação, colaboração e entregas frequentes  
- Requisitos como **user stories** em backlog  
- Mudanças esperadas e aceitas em ciclos curtos  

Exemplos: **Scrum**, **Kanban**, **XP**

---

## O Manifesto Ágil (2001)

1. **Indivíduos e interações** > processos e ferramentas  
2. **Software em funcionamento** > documentação abrangente  
3. **Colaboração com o cliente** > negociação de contratos  
4. **Responder a mudanças** > seguir um plano  

---

## User Stories

Formato **Connextra**:  
> Como [tipo de usuário], quero [funcionalidade], para [benefício]

Exemplo:  
- Como aluno, quero visualizar minhas notas, para acompanhar meu desempenho  
- Como cliente, quero receber notificações de entrega, para saber quando o pedido chegará  

---

## Critérios de Aceitação (Gherkin)

Estrutura:  
- **Dado que** [contexto]  
- **Quando** [ação]  
- **Então** [resultado]

Exemplo (Login):  
- Dado que estou na tela de login  
  Quando informo e-mail e senha válidos  
  Então acesso minha conta  

---

## Checklist INVEST (1/2)

- **I** – Independent 
  - **Independente:** a história deve ser autônoma, sem dependência rígida de outras.  
- **N** – Negotiable  
  - **Negociável:** deve ser um convite à conversa, não um contrato fechado. 
- **V** – Valuable
  - **Valiosa:** precisa entregar valor claro ao usuário ou negócio. 

---
## Checklist INVEST (1/2)

- **E** – Estimable
  - **Estimável:** deve ser possível estimar o esforço de implementação.  
- **S** – Small
  - **Pequena (Small):** deve caber dentro de uma iteração/sprint. 
- **T** – Testable
  - **Testável:** deve possuir critérios claros de aceitação para validação.

> Checklist para avaliar qualidade de user stories
---


## Exemplo Completo de User Story (1/4)

**User Story:**
> Como aluno, quero visualizar minhas notas no portal acadêmico, para acompanhar meu desempenho.

**Critérios de Aceitação:**
1. O sistema deve exibir todas as disciplinas matriculadas no semestre atual.  
2. Para cada disciplina, deve mostrar as notas parciais e a nota final.  

---

## Exemplo Completo de User Story (2/4)

**Critérios de Aceitação (continuação):**
3. Se o professor ainda não tiver lançado notas, deve aparecer a mensagem “Notas em lançamento”.  
4. O tempo de carregamento da tela deve ser inferior a 3 segundos.  

---

## Exemplo Completo de User Story (3/4) 

**Análise segundo INVEST:**
- **I – Independent:** não depende de outra story para ser entregue.  
- **N – Negotiable:** os detalhes da interface podem ser ajustados durante o desenvolvimento.  
- **V – Valuable:** entrega valor direto ao aluno.

---

## Exemplo Completo de User Story (4/4) 

**Análise segundo INVEST (continuação):**
- **E – Estimable:** a equipe consegue estimar esforço para implementar.  
- **S – Small:** pode ser implementada dentro de uma sprint.  
- **T – Testable:** critérios de aceitação permitem verificar se foi concluída corretamente.  

---

## Da Especificação Tradicional às Stories

| Tipo (Tradicional) | Exemplo | User Story | Critérios |
|---------------------|---------|------------|-----------|
| Funcional | “Login com e-mail e senha” | “Como usuário, quero fazer login...” | Validar credenciais, mensagem de erro |
| Não Funcional | “Tela < 2s” | Critério na story de login | Resposta em < 2s |

---

## Da Especificação Tradicional às Stories

| Tipo (Tradicional) | Exemplo | User Story | Critérios |
|---------------------|---------|------------|-----------|
| De Domínio | “Máx. 5 livros” | “Como bibliotecário, quero que o sistema aplique o...” | Bloqueio e mensagem explicativa |

---

## Comparação entre Modelos

| Aspecto | Preditivo | Ágil |
|---------|-----------|------|
| Levantamento | Completo no início | Contínuo ao longo |
| Documentação | Extensa e detalhada | Leve, apenas o necessário |
| Flexibilidade | Baixa | Alta |
| Entregas | Produto ao final | Incrementos frequentes |
| Cliente | Participação pontual | Participação constante |

---

## Foco de Cada Abordagem

- **Preditivo:** entrega do sistema completo ao final  
- **Ágil:** resolver dores do cliente de forma incremental  

---

## Estudo de Caso – Agendamento Médico

- **Preditivo:** requisitos levantados e documentados no início  
- Mudanças exigem renegociação formal  
- **Ágil:** requisitos como user stories no backlog  
- Refinados e implementados a cada sprint  

---

## Exercício em Sala

- Grupos de 3 alunos  
- Parte 1: transformar 3 requisitos preditivos em 2 user stories completas  
- Parte 2: criar 1 user story original com 3–5 critérios de aceitação  
- Apliquem o INVEST em todas  

---

## Conclusão

- Preditivo e Ágil possuem focos distintos  
- User stories conectam necessidades do usuário à implementação  
- INVEST e Gherkin ajudam a garantir clareza e testabilidade  
- Escolha depende do contexto do projeto