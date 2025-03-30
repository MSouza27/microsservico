# Microserviço de Pedidos - TechTaste

## Visão Geral
Este repositório contém um microserviço para gestão de pedidos, desenvolvido com **Spring Boot** e **Spring Cloud**. Ele permite o cadastro e consulta de pedidos, integrando-se a um registro de serviços via **Eureka Server** e a um **API Gateway**.

## Tecnologias Utilizadas
- Java 21
- Spring Boot
- Spring Data JPA
- Spring Cloud (Eureka Server & API Gateway)
- Hibernate
- PostgreSQL
- Docker
- OpenAPI (Swagger)

## Funcionalidades
- **Cadastro de Pedidos**: Registra um novo pedido com CPF, itens e quantidade.
- **Consulta de Pedidos**: Retorna todos os pedidos cadastrados.
- **Cálculo do Total**: O valor total do pedido é calculado com base nos itens e quantidades.
- **Gerenciamento de Status**: Os pedidos possuem status que refletem seu progresso.
- **Descoberta de Serviço**: Integração com Eureka Server para registro dinâmico.
- **Roteamento via API Gateway**: Requisições passam pelo gateway para maior segurança e controle.

## Como Executar

### 1. Clonar o Repositório
```bash
$ git clone https://github.com/techtaste/ms_pedidos.git
$ cd ms_pedidos
```

### 2. Configurar o Banco de Dados
O sistema utiliza **PostgreSQL**. Configure a URL de conexão no `application.properties`.
```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/ms_pedidos
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha
```

### 3. Executar os Containers Docker
```bash
$ docker-compose up -d
```
Isso subirá o banco de dados PostgreSQL.

### 4. Rodar a Aplicação
```bash
$ mvn spring-boot:run
```

## Endpoints Principais
- **Cadastro de Pedido:** `POST /pedidos`
- **Consulta de Pedidos:** `GET /pedidos`
- **Teste de Resposta:** `GET /pedidos/response`

## Documentação da API
A documentação interativa pode ser acessada via **Swagger UI**:
```
http://localhost:8080/swagger-ui.html
```

## Contribuição
Sinta-se à vontade para abrir issues e enviar pull requests.

