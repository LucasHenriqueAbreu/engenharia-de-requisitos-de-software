# Roteiro de Aula – Casos de Uso

## 1. Introdução aos Casos de Uso

- Os **casos de uso** são uma técnica de elicitação de requisitos introduzida no método Objectory (Jacobson et al., 1993).
- Tornaram-se parte fundamental da **UML (Unified Modeling Language)**.
- Representam interações típicas entre atores (usuários ou sistemas externos) e o sistema.
- Foco principal: **funcionalidades do sistema sob a perspectiva do usuário final**.
- São eficazes na comunicação entre stakeholders e equipes técnicas.

## 2. Componentes de um Caso de Uso

- **Atores**: pessoas ou sistemas externos que interagem com o sistema.
- **Objetivo**: o que o ator deseja alcançar.
- **Fluxo principal**: sequência ideal de passos para alcançar o objetivo.
- **Fluxos alternativos**: variações ou exceções ao fluxo principal.
- **Pré-condições**: o que deve ser verdadeiro antes da execução.
- **Pós-condições**: o que será verdadeiro após a execução.

## 3. Diagramas de Casos de Uso (UML)

- Usados para representar visualmente os casos de uso e seus atores.
- **Elementos principais**:
  - Atores (figuras-palito).
  - Casos de uso (elipses).
  - Associações (linhas conectando atores a casos de uso).
  - Sistema (retângulo delimitador do escopo).
- Relações adicionais:
  - **include**: uso comum de funcionalidade.
  - **extend**: variações opcionais.

## 4. Exemplo Visual – Sistema de Pacientes

```
Recepcionista   Enfermeira     Médico(a)     Gerente
      \             |             |             |
     Registrar   Ver registro  Agendar        Gerar
     paciente     Editar       consulta       relatório
                  registro
```

(Representação textual simplificada de um diagrama do sistema MHC-PMS citado no livro)

## 5. Exemplo Textual – Caso de Uso “Agendar Consulta”

- **Atores**: Médicos
- **Objetivo**: Agendar uma consulta com um paciente
- **Fluxo Principal**:
  1. Médico acessa o sistema.
  2. Seleciona paciente e horário.
  3. O prontuário é exibido.
  4. Apenas um médico pode editar.
  5. Uma janela de mensagens é aberta.
- **Fluxos Alternativos**:
  - Outro médico já está editando.
  - O paciente está indisponível.

##### Relações de Extensão:

- **Realizar pagamento** ← extensão de "Agendar Consulta":
  - O caso de uso "Realizar pagamento" é **opcional** e **condicional**, sendo executado **apenas se** a consulta for particular.
  - Essa extensão encapsula o fluxo de pagamento, permitindo reutilização em outros contextos (ex: exames, retornos).
  - Representa uma relação **«extend»** no diagrama UML, com a condição: "Consulta particular".

**Observação:** em um diagrama de casos de uso, essa extensão é representada por uma seta tracejada com o estereótipo `«extend»`, partindo do caso de uso "Realizar pagamento" para "Agendar Consulta".

## 6. Vantagens dos Casos de Uso

- Boa compreensão de interações esperadas.
- Útil para criar cenários de teste.
- Facilita alinhamento entre áreas técnicas e não técnicas.

## 7. Limitações dos Casos de Uso

- Pouca cobertura de requisitos não funcionais e de domínio.
- Exigem esforço de documentação.
- Menor utilidade em ambientes ágeis com mudanças rápidas.
---

## Prática Guiada – Criando um Diagrama no Draw.io

Nesta parte da aula, vamos criar juntos um **diagrama de casos de uso** utilizando a ferramenta [Draw.io](https://app.diagrams.net/).

### Instruções:---

## Prática Guiada – Criando um Diagrama no Draw.io

Nesta parte da aula, vamos criar juntos um **diagrama de casos de uso** utilizando a ferramenta [Draw.io](https://app.diagrams.net/).

### Instruções:

1. Acesse [https://app.diagrams.net/](https://app.diagrams.net/)
2. Crie um novo diagrama em branco
3. Insira os seguintes elementos:
   - Atores: utilizando a forma de "figura-palito"
   - Casos de uso: representados por elipses
   - Relacione os atores aos casos de uso com linhas
4. Modele o sistema **"Agendamento de Consultas"** com pelo menos 4 casos de uso:
   - Registrar paciente
   - Agendar consulta
   - Editar prontuário
   - Gerar relatório

### Objetivo:

- Visualizar como os elementos da UML são organizados
- Discutir decisões de modelagem e refinamento do escopo

Após a criação, discutiremos os diagramas em grupo.

1. Acesse [https://app.diagrams.net/](https://app.diagrams.net/)
2. Crie um novo diagrama em branco
3. Insira os seguintes elementos:
   - Atores: utilizando a forma de "figura-palito"
   - Casos de uso: representados por elipses
   - Relacione os atores aos casos de uso com linhas
4. Modele o sistema **"Agendamento de Consultas"** com pelo menos 4 casos de uso:
   - Registrar paciente
   - Agendar consulta
   - Editar prontuário
   - Gerar relatório

### Objetivo:

- Visualizar como os elementos da UML são organizados
- Discutir decisões de modelagem e refinamento do escopo

Após a criação, discutiremos os diagramas em grupo.

## 9. Atividade em Sala

### Etapas:

- Formem grupos de 2 a 3 pessoas.
- Escolham um sistema simples. Exemplo sugerido: **Sistema de Agendamento de Consultas Médicas**.
- Realizem as seguintes tarefas:
  - Criem um **diagrama de casos de uso** (visão macro) com pelo menos 5 casos de uso:
    - Registrar paciente
    - Agendar consulta
    - Editar prontuário
    - Gerar relatório
    - Realizar pagamento
  - Desenvolvam uma **descrição textual detalhada** de um dos casos de uso, com fluxo principal e fluxos alternativos.

---

### Exemplo:

#### Caso de Uso: **Agendar Consulta**

- **Atores**: Paciente, Médico, Sistema de Agenda
- **Objetivo**: Permitir que o paciente agende uma consulta com um médico disponível

##### Fluxo Principal:
1. O paciente acessa o sistema com login e senha.
2. O sistema valida as credenciais.
3. O paciente escolhe a opção "Agendar Consulta".
4. O sistema apresenta uma lista de especialidades médicas.
5. O paciente seleciona a especialidade desejada.
6. O sistema exibe os médicos disponíveis e seus horários.
7. O paciente escolhe o médico e o horário desejado.
8. O sistema verifica se o horário ainda está disponível.
9. O sistema registra a consulta na agenda do médico.
10. O paciente recebe uma confirmação com os detalhes do agendamento.
11. O paciente realiza o pagamento da consulta (caso seja particular).

##### Fluxos Alternativos:

- **Login inválido**:
  - O sistema informa que as credenciais são inválidas e permite nova tentativa.

- **Nenhum médico disponível**:
  - O sistema informa que não há médicos disponíveis naquela especialidade e horário e sugere outras datas.

- **Horário indisponível no momento da confirmação**:
  - O sistema informa que o horário foi ocupado por outro paciente e retorna à lista de horários atualizados.

- **Paciente não seleciona nenhuma especialidade**:
  - O sistema solicita a seleção obrigatória para prosseguir.

- **Falha no pagamento**:
  - O sistema informa que houve erro no processamento do pagamento e oferece nova tentativa ou opção de agendamento sem cobrança (se aplicável).

---

### Entregáveis do grupo:

- Diagrama de casos de uso (feito no Draw.io)
- Descrição textual de um caso de uso com:
  - Atores
  - Objetivo
  - Fluxo principal numerado
  - Pelo menos dois fluxos alternativos

## 10. Leitura Recomendada

- SOMMERVILLE, Ian. *Engenharia de Software*. 10ª ed. Pearson, 2019. Capítulo 4.
- JACOBSON, Ivar. *Object-Oriented Software Engineering*. Addison-Wesley, 1993.
- WIEGERS, Karl; BEATTY, Joy. *Software Requirements*. 3ª ed. Microsoft Press, 2013.