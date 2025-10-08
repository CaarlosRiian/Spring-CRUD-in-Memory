# Spring-CRUD-in-Memory

Este projeto é uma API REST feita com Spring Boot que implementa um CRUD completo (Create, Read, Update, Delete) de produtos, **usando apenas a camada Controller e uma lista em memória** — sem banco de dados, com objetivo de exercitar Java Spring Boot.

---

## Como executar
1. Clone o repositório:

    ```git clone https://github.com/CaarlosRiian/Spring-CRUD-in-Memory.git```

   ```cd Spring-CRUD-in-Memory```

2. Rode o projeto:

   ```./mvnw spring-boot:run```

---

## Funcionalidades

- Listar todos os produtos (`GET /products`)
- Buscar produto por ID (`GET /products/{id}`)
- Adicionar novo produto (`POST /products`)
- Atualizar produto existente (`PUT /products/{id}`)
- Remover produto por ID (`DELETE /products/{id}`)
- Buscar produtos por nome (`GET /products/search?name=mouse`)

---

## Teste com Postman

Use o Postman para testar os endpoints:

### Adicionar produto (POST)

- **URL:** `http://localhost:8080/products`
- **Body (JSON):**
```json
{
  "name": "Mouse Gamer",
  "price": 159.90,
  "quantity": 3
}

```

### Buscar por ID (GET)

- **URL:** `http://localhost:8080/products/1`

### Atualizar produto (PUT)

- **URL:** `http://localhost:8080/products/1`
- **Body (JSON):**
```json
{
  "name": "Mouse Sem Fio",
  "price": 179.90,
  "quantity": 4
}
```

### Remover produto (DELETE)

- **URL:** `http://localhost:8080/products/1`

### Buscar por nome (GET)

- **URL:** `http://localhost:8080/products/search?name=mouse`
