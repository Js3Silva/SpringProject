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
