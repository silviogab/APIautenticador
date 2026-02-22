# APIautenticador

Uma **API REST de autenticação** desenvolvida em **Java com Spring Boot**, responsável por gerenciar o registro e login de usuários — retornando tokens JWT para acesso seguro.

##  Tecnologias

- Java  
- Spring Boot  
- Spring Security (JWT)  
- Maven  MYsql
- Banco de dados 
- JWT para autenticação e autorização  

##  Funcionalidades

✔ Registro de usuários  
✔ Login com validação de credenciais  
✔ Geração de token JWT para sessões autenticadas  
✔ Endpoints REST seguros  


## Dependências Principais


- `spring-boot-starter-web`  
- `spring-boot-starter-security`  
- `spring-boot-starter-data-jpa`  
- `jjwt` 
- Driver do banco de dados (MySQL/PostgreSQL/etc)



##  Endpoints

| Método | Endpoint           | Acesso                 |<br>
|--------|-------------------|------------------------|<br>
| POST   | `/auth/register`   | Público                |<br>
| POST   | `/auth/login`      | Público                |<br>
| GET    | `/users`           | Seguro (token JWT)     |<br>
| GET    | `/profile`         | Seguro (token JWT)     |<br>


##  Configuração

### 1) Banco de Dados

No arquivo `src/main/resources/application.properties` você deve configurar:
spring.datasource.url=jdbc:mysql://localhost:3306/seubanco
spring.datasource.username=usuario
spring.datasource.password=senha
spring.jpa.hibernate.ddl-auto=update

### 2) JWT Secret

Defina um valor secreto para gerar os tokens:

jwt.secret=SEU_SEGREDO_AQUI

🧪 Testando

Use **Postman** ou **Insomnia**:

1. POST `/auth/register` — criar usuário  
2. POST `/auth/login` — gerar token JWT  
3. Copie o token e coloque no header:  
   `Authorization: Bearer <SEU_TOKEN>`


   
jwt.expiration=86400000



No arquivo `src/main/resources/application.properties` você deve configurar:
