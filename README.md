# Produto API - Sistema de Cadastro de Produtos

Este é um projeto de backend para o **Cadastro de Produtos** usando **Spring Boot** e **Flyway** para versionamento de banco de dados. O sistema permite a criação, leitura, atualização e exclusão (CRUD) de produtos no banco de dados.

## Funcionalidades

- Cadastro de produtos
- Edição de produtos
- Exclusão de produtos
- Listagem de produtos
- Exibição de detalhes de um produto

## Tecnologias Utilizadas

- **Spring Boot**: Framework para desenvolvimento de aplicações Java.
- **Flyway**: Ferramenta para versionamento de banco de dados.
- **JPA (Java Persistence API)**: Para mapeamento objeto-relacional e interação com o banco de dados.
- **MySQL**: Banco de dados para armazenamento dos dados dos produtos.
- **Git**: Controle de versão.

## Como Rodar o Projeto

### 1. Pré-requisitos

Certifique-se de que você tem o **Java 17** ou superior, **MySQL**, e **Maven** instalados no seu computador.

- **Java**: [Download Java](https://www.oracle.com/java/technologies/javase-jdk17-downloads.html)
- **MySQL**: [Download MySQL](https://dev.mysql.com/downloads/installer/)
- **Maven**: [Download Maven](https://maven.apache.org/download.cgi)

### 2. Clonar o Repositório

Clone este repositório para o seu computador:

bash
git clone https://github.com/srjoaovitorsouzas/produto-api.git

### 3. Configurar o Banco de Dados
Abra o XAMPP e inicie o MySQL .
Crie o banco de dados produto_dbcom o comando:
CREATE DATABASE produto_db;
Configure uma conexão com o banco de dados no arquivo src/main/resources/application.properties:
spring.datasource.url=jdbc:mysql://localhost:3306/produto_db
spring.datasource.username=root
spring.datasource.password=
spring.jpa.hibernate.ddl-auto=update

### 4. Rodar a Aplicação
Após configurar o banco de dados, você pode rodar um aplicativo com o Maven:
mvn spring-boot:run
O servidor será iniciado e estará disponível em: http://localhost:8080.

Pontos finais da API
Aqui estão os principais endpoints da API para gerenciamento de produtos:

### 1. Listar Produtos
URL :/api/produtos
Método :GET
Descrição : Lista todos os produtos cadastrados.
Exemplo de cURL:
curl -X GET http://localhost:8080/api/produtos

### 2. Cadastrar Produto
URL :/api/produtos
Método :POST
Descrição : Cadastrar um novo produto.
Corpo da Requisição (JSON):
{
  "nome": "Produto Exemplo",
  "descricao": "Descrição do produto",
  "preco": 29.99
}
Exemplo de cURL:
curl -X POST http://localhost:8080/api/produtos -H "Content-Type: application/json" -d '{"nome": "Produto Exemplo", "descricao": "Descrição do produto", "preco": 29.99}'

### 3. Detalhes de um Produto
URL :/api/produtos/{id}
Método :GET
Descrição : Veja os detalhes de um produto específico.
Exemplo de cURL:
curl -X GET http://localhost:8080/api/produtos/1

### 4. Atualizar Produto
URL :/api/produtos/{id}
Método :PUT
Descrição : Atualiza os dados de um produto.
Corpo da Requisição (JSON):
{
  "nome": "Produto Atualizado",
  "descricao": "Descrição atualizada",
  "preco": 39.99
}
Exemplo de cURL:
curl -X PUT http://localhost:8080/api/produtos/1 -H "Content-Type: application/json" -d '{"nome": "Produto Atualizado", "descricao": "Descrição atualizada", "preco": 39.99}'

### 5. Excluir produto
URL :/api/produtos/{id}
Método :DELETE
Descrição : Produto exclusivo.
Exemplo de cURL:
bater

### Copiar código
curl -X DELETE http://localhost:8080/api/produtos/1
Instruções para Testes
Você pode usar o Postman ou cURL para testar os endpoints da API. Veja os exemplos de cURL acima para testar as funcionalidades diretamente no terminal.

## Dependências do Projeto
Spring Web
Spring Data JPA 
Driver MySQL 
Flyway Migration

### Autor
João Vitor Souza Rodrigues


### Explicação do conteúdo do README.md:

1. **Descrição do projeto**: Explica o que o projeto faz e as tecnologias utilizadas.
2. **Como rodar o projeto**: Passos para clonar o repositório, configurar o banco de dados e rodar o servidor.
3. **Endereços da API**: Exemplos dos endpoints com cURL para interagir com a API (GET, POST, PUT, DELETE).
4. **Instruções de teste**: Como testar a API utilizando cURL ou Postman.
5. **Dependências do projeto**: Quais tecnologias são necessárias para rodar o projeto.
6. **Autor**: Você pode adicionar o nome de sua equipe ou de quem desenvolveu o projeto.


