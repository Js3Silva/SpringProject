# SpringProject

Projeto baseado no curso completo de Spring Boot do canal [Michelli Brito](https://www.youtube.com/watch?v=wlYvA2b1BWI&t=22s).

Este projeto é uma API RESTful desenvolvida com as últimas versões do Spring Boot 3, Spring Framework 6 e Java 17, seguindo o **Modelo de Maturidade de Richardson**. Durante a implementação, aprendi bastante sobre Spring, APIs RESTful, e como estruturar um projeto de API completa com boas práticas.

## Funcionalidades

- API RESTful completa com CRUD para gerenciamento de dados
- Arquitetura seguindo o padrão MVC e boas práticas de desenvolvimento
- Integração com banco de dados Postgres
- Documentação de endpoints com links HATEOAS
- Validação e manipulação de dados com Spring Validation
- Tratamento de erros padronizado
- Utilização de JPA e Spring Data para persistência

## Tecnologias Utilizadas

- **Java 17**
- **Spring Boot 3**
- **Spring Framework 6**
- **Postgres**
- **Spring Data JPA**
- **HATEOAS**
- **Postman** - para testes de API
- **Visual Studio Code** - como IDE

## Preparação do Ambiente

### Pré-requisitos
Para rodar este projeto localmente, você precisará do seguinte:

- **Java 17 (JDK 17)**: Certifique-se de que o JDK está instalado e configurado no PATH.
- **Postman**: Para testar e documentar os endpoints da API.
- **Postgres**: Banco de dados relacional onde os dados da aplicação são persistidos.
- **Visual Studio Code**: IDE recomendada, mas você pode utilizar a de sua preferência.

### Configuração do Banco de Dados

1. O banco de dados está configurado no **Neon** (acesso privado).
2. No arquivo `application.properties`, você pode configurar o endereço do banco Neon e as credenciais, seguindo o formato:

   ```properties
   spring.datasource.url=jdbc:postgresql://<endereco_privado_neon>:5432/springproject
   spring.datasource.username=seu_usuario
   spring.datasource.password=sua_senha
   spring.jpa.hibernate.ddl-auto=update
   spring.jpa.show-sql=true
   ```

### Executando a Aplicação

1. Clone o repositório:
   ```bash
   git clone https://github.com/Js3Silva/SpringProject.git
   cd springproject
   ```

2. Compile e execute o projeto usando sua IDE ou através do Maven:
   ```bash
   ./mvnw spring-boot:run
   ```

3. A API estará disponível em `http://localhost:8080`.

## Testando a API

Use o Postman para enviar requisições para os endpoints da API e validar seu funcionamento. Aqui estão alguns exemplos de endpoints disponíveis:

- **GET /products** - Lista todos os produtos
- **GET /products/{id}** - Retorna um produto específico pelo ID
- **POST /products** - Cria um novo produto
- **PUT /products/{id}** - Atualiza um produto existente
- **DELETE /products/{id}** - Deleta um produto

## Estrutura do Projeto

```plaintext
src
├── main
│   ├── java
│   │   └── com.example.springboot
│   │       ├── controllers       # Controladores REST
│   │       ├── dtos              # Data Transfer Objects
│   │       ├── models            # Modelos de Entidade
│   │       └── repositories      # Repositórios para acesso a dados
│   └── resources
│       ├── application.properties  # Configurações do Spring Boot
└── test                          # Testes unitários e de integração
```

## Contribuindo

Contribuições são bem-vindas! Para contribuir com este projeto:

1. Faça um fork do repositório
2. Crie uma branch para sua feature (`git checkout -b minha-feature`)
3. Commit suas mudanças (`git commit -m 'Minha nova feature'`)
4. Faça o push para a branch (`git push origin minha-feature`)
5. Abra um Pull Request

## Contato

Se tiver dúvidas ou sugestões, entre em contato:

- **Nome:** Jonathan Silva
- **Email:** [jonathansilvagw@gmail.com](mailto:jonathansilvagw@gmail.com)

---

Este projeto faz parte da minha jornada de aprendizado em Spring Boot e desenvolvimento de APIs RESTful.
