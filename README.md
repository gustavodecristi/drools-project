# Drools Basic

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

Este repositório contém um projeto básico utilizando **Drools**, uma engine de regras de negócios baseada em Java que permite separar a lógica de negócios das regras complexas do código principal da aplicação. É uma solução poderosa para sistemas que exigem alta flexibilidade na definição e execução de regras.

## Descrição

O objetivo deste projeto é fornecer um exemplo simples e funcional de como utilizar o Drools para processar regras de negócios. Ele é voltado para iniciantes que desejam aprender a integrar Drools em seus projetos Java, facilitando a implementação de um mecanismo de decisão baseado em regras.

## Funcionalidades

- Configuração básica do **Drools**.
- Exemplos de como criar e executar regras.
- Demonstração de como utilizar um *Knowledge Base* e *Sessions* no Drools.
- Execução de regras com base em fatos fornecidos pela aplicação.

## Pré-requisitos

Antes de rodar o projeto, você precisará dos seguintes pré-requisitos:

- Java 8 ou superior
- Apache Maven 3.6 ou superior
- IDE compatível com Java (por exemplo: IntelliJ IDEA, Eclipse)

## Instalação

1. Clone este repositório:
   ```bash
   git clone https://github.com/paneladev/drools-basic.git
   cd drools-basic
   ```

2. Compile o projeto usando Maven:
   ```bash
   mvn clean install
   ```

3. Execute o projeto:
   ```bash
   mvn exec:java -Dexec.mainClass="com.example.droolsbasic.App"
   ```

## Estrutura do Projeto

```bash
drools-basic/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/example/droolsbasic/  # Código-fonte principal
│   │   ├── resources/
│   │   │   └── rules/  # Regras Drools
│   └── test/
├── pom.xml  # Configurações do Maven
└── README.md
```

- **src/main/java**: Contém o código Java que interage com o Drools.
- **src/main/resources**: Contém arquivos de configuração e arquivos `.drl` (regras do Drools).

## Exemplos

Aqui está um exemplo simples de como uma regra Drools é definida:

```java
rule "Regra de exemplo"
when
    $fato : Fato(atributo == "valor")
then
    System.out.println("Regra acionada!");
end
```

Este é um exemplo básico, onde o fato é comparado com um valor e, se for verdadeiro, uma ação é executada.
