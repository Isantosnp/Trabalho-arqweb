# 🚀 API de Autenticação e Autorização JWT (Spring Boot 3)

Este projeto é uma API REST construída com Spring Boot 3 que realiza **autenticação e autorização baseada em tokens JWT**. Ele inclui segurança com Spring Security, documentação com Swagger, persistência com JPA/H2 e testes com JUnit + JMeter.

## 🧰 Tecnologias Utilizadas

- Java 17+
- Spring Boot 3.x
- Spring Security
- JWT (com Auth0)
- Spring Data JPA
- H2 Database
- Swagger (Springdoc OpenAPI)
- JUnit 5 + Mockito
- Apache JMeter

⚙️ Como Executar
- Certifique-se de ter o Java 17+ e Maven instalados.
- Execute o projeto com:
   ./mvnw spring-boot:run

  Ou execute a classe TrabalhoApplication.java via sua IDE.

  🛠️ Configurações (application.yml)
- Porta da API: 8080
- Banco H2 em memória (jdbc:h2:mem:testdb)
- Console H2: http://localhost:8080/h2-console
- Swagger UI: http://localhost:8080/swagger-ui.html
- JWT configurado com chave secreta e tempo de expiração

👤 Usuários Criados Automaticamente
| Username | Senha      | Role  |
| -------- | ---------- | ----- |
| `admin`  | `123456`   | ADMIN |
| `user`   | `password` | USER  |
As senhas são criptografadas com BCrypt.

📚 Principais Endpoints

| Método | Endpoint         | Acesso      | Descrição                             |
| ------ | ---------------- | ----------- | ------------------------------------- |
| POST   | `/auth/login`    | Público     | Autentica o usuário e retorna um JWT  |
| POST   | `/auth/validate` | Público     | Valida um token JWT                   |
| GET    | `/api/hello`     | Autenticado | Retorna mensagem protegida            |
| GET    | `/api/admin`     | ADMIN       | Acesso exclusivo para administradores |

🧪 Executando os Testes
./mvnw test
Ou execute AuthIntegrationTests.java pela sua IDE.

📈 Testes de Carga com JMeter
Baixe e instale o Apache JMeter.
Abra o arquivo jmeter-tests/login_stress_test.jmx.
Configure o número de usuários, tempo de ramp-up e loops.
Execute o teste e observe os resultados em:
Summary Report
View Results Tree

🗂️ Estrutura do Projeto

src/
├── main/
│   ├── java/com/arquiteturaweb/trabalho/
│   │   ├── config/
│   │   ├── controller/
│   │   ├── model/
│   │   ├── repository/
│   │   ├── service/
│   │   └── TrabalhoApplication.java
│   └── resources/
│       ├── application.yml
│       ├── static/
│       └── templates/
└── test/
    └── java/com/arquiteturaweb/trabalho/
        └── AuthIntegrationTests.java
Desenvolvido como parte de um projeto acadêmico de Arquitetura Web com Spring Boot.
