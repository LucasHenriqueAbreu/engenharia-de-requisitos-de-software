# Casos de Uso

## Introdução

Casos de uso são uma técnica de descoberta e especificação de requisitos introduzida originalmente no método Objectory (JACOBSON et al., 1993), e hoje fazem parte fundamental da UML — Unified Modeling Language.

Em essência, um **caso de uso** representa uma interação típica entre **atores** (usuários ou sistemas externos) e o **sistema**, com o objetivo de alcançar um determinado resultado de valor. Cada interação pode ser descrita em termos de **fluxo principal** e **fluxos alternativos**.

## Representação e Modelagem

Casos de uso podem ser descritos textualmente ou visualmente por meio de diagramas UML. Um **diagrama de casos de uso** mostra os atores envolvidos e os diferentes usos do sistema, com elipses representando os casos de uso e figuras-palito representando os atores. As linhas de conexão indicam a participação dos atores em cada caso de uso.

Além disso, os casos de uso podem ser detalhados com descrições de cenários, incluindo:

- Fluxo principal de eventos  
- Cenários alternativos ou exceções  
- Pré-condições e pós-condições  
- Regras de negócio associadas

## Exemplos

Um exemplo prático pode ser o sistema de informações de pacientes. Os casos de uso incluem ações como:

- Registrar paciente  
- Agendar consulta  
- Ver ou editar registros  
- Gerar relatórios

Um dos casos de uso, como “Agendar consulta”, pode descrever que o médico seleciona um paciente e um horário disponível, sendo exibido o prontuário compartilhado com outros profissionais. A comunicação pode incluir chat textual, sendo que apenas um profissional edita enquanto outros acompanham.

## Vantagens

- Clareza na descrição de interações reais com o sistema  
- Excelente para comunicar funcionalidades com partes interessadas técnicas e não técnicas  
- Integração natural com diagramas UML e outras técnicas de modelagem  
- Boa base para derivação de testes e validação de requisitos

## Limitações

- Pode demandar esforço maior de documentação  
- Nem sempre aborda requisitos não funcionais ou de domínio  
- Pode ser excessivamente detalhado em ambientes ágeis ou dinâmicos

## Conclusão

Casos de uso são uma técnica poderosa para elicitar e documentar requisitos funcionais do sistema, especialmente quando se deseja compreender a interação entre usuários e sistema de forma clara e estruturada. Seu uso é especialmente recomendado em contextos com múltiplos atores e necessidades de rastreabilidade entre requisitos e funcionalidades.


## Conteúdos Relacionados

- [Aula](./aula/README.md)
- [Slides](./aula/presenter.md)