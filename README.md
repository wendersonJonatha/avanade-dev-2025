# Santander Dev Week 2023 - Java API 🚀

RESTful API da Santander Dev Week 2023 construída em **Java 17** com **Spring Boot 3**.

---

## 🔧 Principais Tecnologias  

- **Java 17:** Aproveitando a versão LTS mais recente para desempenho e produtividade.  
- **Spring Boot 3:** Framework robusto que simplifica a criação de aplicações web e serviços RESTful.  
- **Spring Data JPA:** Facilita a integração com bancos de dados SQL e simplifica a camada de persistência.  
- **OpenAPI (Swagger):** Gera uma documentação de API clara e interativa.  
- **Railway:** Plataforma prática para deploy na nuvem, com suporte a banco de dados e pipelines CI/CD.  

---

## 📌 Diagrama de Classes (Domínio da API)

```mermaid
classDiagram
  class User {
    - String name
    - Account account
    - Feature[] features
    - Card card
    - News[] news
  }

  class Account {
    - String number
    - String agency
    - Number balance
    - Number limit
  }

  class Feature {
    - String icon
    - String description
  }

  class Card {
    - String number
    - Number limit
  }

  class News {
    - String icon
    - String description
  }

  User "1" *-- "1" Account
  User "1" *-- "N" Feature
  User "1" *-- "1" Card
  User "1" *-- "N" News


