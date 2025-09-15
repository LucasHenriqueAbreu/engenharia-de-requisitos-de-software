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
#### Casos de Uso
##### Prof. Lucas Henrique de Abreu

---

## Introdução aos Casos de Uso

- Técnica introduzida no método Objectory (Jacobson et al., 1993)  
- Parte fundamental da UML (Unified Modeling Language)  
- Representam interações entre atores e sistema  
- Foco em **funcionalidades sob a perspectiva do usuário**

---

## Objetivos de um Caso de Uso

- Identificar **atores** e **interações relevantes** com o sistema  
- Descrever fluxos principais e alternativos  
- Estabelecer pré e pós-condições  
- Apoiar modelagem, testes e validação de requisitos

---

## Componentes do Caso de Uso

- **Ator:** pessoa ou sistema externo  
- **Objetivo:** o que o ator quer realizar  
- **Fluxo Principal:** sequência ideal de passos  
- **Fluxos Alternativos:** exceções e variações  
- **Pré-condições / Pós-condições**  
- **Regras de negócio** relacionadas

---

## Diagrama de Casos de Uso (UML)

- Elementos visuais:
  - Atores (figuras-palito)
  - Casos de uso (elipses)
  - Associações (linhas)
  - Sistema (retângulo delimitador)
- Relações adicionais:
  - **include**, **extend**

---

## Fluxos Alternativos e Extensões

**Fluxos Alternativos:**
- **Login inválido:** sistema informa erro e permite nova tentativa  
- **Paciente indisponível:** sistema sugere outro horário  
- **Horário indisponível:** sistema atualiza lista de horários  
- **Pagamento falhou:** sistema solicita nova tentativa ou oferece agendamento gratuito (ex: consulta SUS)  

**Relação de Extensão:**
- O caso de uso “Realizar pagamento” é uma **extensão** (`«extend»`) de “Agendar Consulta”  
  - Executado **apenas se** a consulta for particular  

---

## Vantagens dos Casos de Uso

- Clareza na interação sistema–usuário  
- Boa comunicação com stakeholders  
- Excelente base para testes  
- Apoia rastreabilidade de requisitos

---

## Limitações dos Casos de Uso

- Pouca cobertura de requisitos não funcionais  
- Documentação pode ser extensa  
- Pode não se adaptar bem a mudanças ágeis

---

## Casos de Uso vs. Cenários

- Um caso de uso pode conter múltiplos **cenários**  
  - Ex: fluxo principal + exceções  
- Algumas abordagens tratam **cada cenário como um caso de uso**  
- Escolha depende do nível de detalhe desejado

---

## Atividade em Sala

- Formem grupos de 2 a 3 alunos  
- Escolham um sistema simples (ex: app de academia, loja virtual)  
- Criem:
  - 1 diagrama de casos de uso  
  - 1 descrição textual com fluxo principal e alternativo

---

## Leitura Recomendada

- SOMMERVILLE, Ian. *Engenharia de Software*. 10ª ed. Capítulo 4  
- JACOBSON, Ivar. *Object-Oriented Software Engineering*. Addison-Wesley  
- WIEGERS, Karl; BEATTY, Joy. *Software Requirements*. Microsoft Press  
