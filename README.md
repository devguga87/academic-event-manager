# Sistema de Gestão de Participantes e Atividades para Evento Acadêmico

## Descrição

Este projeto é um sistema desenvolvido em **Java** utilizando **Spring Boot** e banco de dados **H2** para gerenciar informações dos participantes e das atividades de um evento acadêmico.

As atividades do evento podem incluir palestras, cursos, oficinas práticas, entre outras. Cada atividade possui:

- Nome
- Descrição
- Preço
- Blocos de horários (um curso pode ocorrer em vários blocos, com dia, horário de início e fim).

Para cada participante, o sistema cadastra:

- Nome
- Email

---

## Tecnologias Utilizadas

- Java
- Spring Boot
- H2 Database (banco de dados em memória para desenvolvimento e testes)
- Maven

---

## Funcionalidades

- Cadastro e gerenciamento de atividades do evento, incluindo múltiplos blocos de horário por atividade.
- Cadastro e gerenciamento dos participantes, com nome e email.
- Associação dos participantes às atividades.

---

## Como executar o projeto

1. Clone o repositório:

    ```bash
    git clone <url-do-repositorio>
    ```

2. Navegue até a pasta do projeto:

    ```bash
    cd nome-do-projeto
    ```

3. Execute o projeto com Maven:

    ```bash
    ./mvnw spring-boot:run
    ```

4. Acesse o sistema via navegador (exemplo):

    ```
    http://localhost:8080
    ```


---

## Acesso ao banco H2

O H2 Console pode ser acessado para visualizar e manipular os dados durante o desenvolvimento em:

```
http://localhost:8080/h2-console
```

- JDBC URL: `jdbc:h2:mem:testdb`
- Usuário e senha conforme configuração no `application-test.properties` 

---

## Estrutura das Entidades Principais

- **Atividade**: nome, descrição, preço, lista de blocos de horário
- **Bloco de Horário**: dia, horário de início, horário de fim
- **Participante**: nome, email