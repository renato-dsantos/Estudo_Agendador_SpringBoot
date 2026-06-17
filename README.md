Readme · MD
# 📅 Agendador de Horários — Estudo Spring Boot

Projeto desenvolvido para fins de estudo e prática com **Java** e **Spring Boot**, implementando uma API REST simples de agendamento de horários.
 
---

## 🚀 Tecnologias Utilizadas

| Tecnologia | Versão |
|---|---|
| Java | 21 |
| Spring Boot | 4.1.0 |
| Spring Data JPA | — |
| Spring Web MVC | — |
| H2 Database (em memória) | — |
| Lombok | — |
| Maven | — |
 
---

## 📋 Funcionalidades

- Cadastro de agendamentos
- Listagem de horários agendados
- Persistência com banco de dados em memória H2
- Console H2 disponível para inspeção dos dados
---

## 🗂️ Estrutura do Projeto

```
src/
└── main/
    ├── java/
    │   └── com/estudo/agendadorhorarios/
    │       ├── controller/   # Endpoints REST
    │       ├── model/        # Entidades JPA
    │       ├── repository/   # Interfaces de acesso ao banco
    │       └── service/      # Regras de negócio
    └── resources/
        └── application.properties
```
 
---

## ▶️ Como Executar

### Pré-requisitos

- Java 21 instalado
- Maven instalado (ou usar o `mvnw` incluso no projeto)
### Passos

```bash
# Clone o repositório
git clone https://github.com/renato-dsantos/Estudo_Agendador_SpringBoot.git
 
# Acesse a pasta do projeto
cd Estudo_Agendador_SpringBoot
 
# Execute com Maven Wrapper
./mvnw spring-boot:run
 
# No Windows:
mvnw.cmd spring-boot:run
```

A aplicação iniciará em `http://localhost:8080`.
 
---

## 🗄️ Console H2

Com a aplicação rodando, acesse o console do banco de dados em memória:

```
URL: http://localhost:8080/h2-console
JDBC URL: jdbc:h2:mem:testdb
Usuário: sa
Senha: (deixar em branco)
```
 
---

## 📡 Endpoints da API

> Base URL: `http://localhost:8080`

| Método | Endpoint | Descrição |
|---|---|---|
| `GET` | `/agendamentos` | Lista todos os agendamentos |
| `GET` | `/agendamentos/{id}` | Busca agendamento por ID |
| `POST` | `/agendamentos` | Cria um novo agendamento |
| `PUT` | `/agendamentos/{id}` | Atualiza um agendamento |
| `DELETE` | `/agendamentos/{id}` | Remove um agendamento |

### Exemplo de payload (POST)

```json
{
  "nome": "João Silva",
  "dataHora": "2025-07-10T14:30:00",
  "descricao": "Consulta médica"
}
```
 
---

## 🎯 Objetivo do Estudo

Este projeto foi criado para praticar:

- Criação de APIs REST com Spring Boot
- Mapeamento de entidades com JPA/Hibernate
- Uso de banco de dados em memória H2
- Boas práticas de estrutura em camadas (Controller → Service → Repository)
- Uso do Lombok para reduzir código boilerplate
---

## 👤 Autor

**Renato D. Santos**  
🔗 [github.com/renato-dsantos](https://github.com/renato-dsantos)
 
---

> Projeto de estudo — em desenvolvimento contínuo.