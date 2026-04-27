# Desafio: Consulta de Vendas - Spring Boot

Projeto desenvolvido como parte do módulo de Back-end da formação da DevSuperior (Prof. Nélio Alves).

## 🚀 Tecnologias
- Java 17+
- Spring Boot
- Spring Data JPA
- Hibernate
- H2 Database
- Maven
- Postman (para testes)

## 📚 Descrição do projeto

A aplicação consiste em uma API REST para consulta de vendas, permitindo gerar:

- Relatório de vendas com filtros e paginação
- Sumário de vendas por vendedor

## 🧠 Conceitos aplicados
- Arquitetura em camadas (Controller, Service, Repository)
- Desenvolvimento de API REST com Spring Boot
- Consultas personalizadas com JPQL
- Projeção de dados em DTO
- Paginação com Spring Data (Pageable e Page)
- Relacionamento entre entidades (Many-to-One e One-to-Many)
- Manipulação de datas com LocalDate
- Tratamento de parâmetros opcionais
- Boas práticas de organização de código

## ⚙️ Funcionalidades

### 🔹 Relatório de vendas
- Filtro por data inicial, data final e nome do vendedor
- Resultado paginado
- Retorna: id, data, valor e nome do vendedor

### 🔹 Sumário de vendas
- Filtro por data inicial e final
- Retorna o total vendido por cada vendedor

## 📡 Endpoints

### 📍 Relatório de vendas

GET /sales/report

Parâmetros:
- minDate (opcional)
- maxDate (opcional)
- name (opcional)

Exemplo:
GET /sales/report?minDate=2022-05-01&maxDate=2022-05-31&name=odinson

Isso garante que, ao iniciar a aplicação, os dados já estejam disponíveis para teste.

### 📍 Sumário de vendas

GET /sales/summary

Parâmetros:
- minDate (opcional)
- maxDate (opcional)

Exemplo:
GET /sales/summary?minDate=2022-01-01&maxDate=2022-06-30

## 🧪 Testes

Os testes podem ser realizados utilizando o Postman ou qualquer ferramenta de requisições HTTP.


## ⚙️ Como executar o projeto
### 📌 Pré-requisitos
- Java 17 ou superior

## ▶️ Rodando a aplicação

- Clonar repositório
  git clone https://github.com/alinasobral/desafio-consulta-vendas.git
- Acessar a pasta do projeto desafio-consulta-vendas
-  No terminal, execute:
```bash
./mvnw spring-boot:run
```

## 🗄️ Acessando o banco H2

Após iniciar o projeto, acesse:

👉 http://localhost:8080/h2-console

🔑 Dados de conexão:
- JDBC URL: jdbc:h2:mem:testdb
- User: sa
- Password: (vazio)

## 📄 Licença

Este projeto está sob a licença MIT.

## 👩🏻‍💻 Autor

Alina Sobral