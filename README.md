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

- Endpoints disponíveis
| Método | Endpoint         | Protegido | Descrição                     |
| ------ | ---------------- | --------- | ----------------------------- |
| POST   | `/auth/login`    | ❌         | Login e geração do token JWT  |
| POST   | `/auth/validate` | ❌         | Validação manual de token     |
| GET    | `/api/hello`     | ✅         | Requer qualquer token válido  |
| GET    | `/api/admin`     | ✅ (ADMIN) | Requer token com role `ADMIN` |
