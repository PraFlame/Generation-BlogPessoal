# ✍️ Blog Pessoal - Generation Brasil

![Java](https://img.shields.io/badge/Java-17-blue.svg)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.2.5-brightgreen.svg)
![MySQL](https://img.shields.io/badge/MySQL-8.0-orange.svg)
![Docker](https://img.shields.io/badge/Docker-Container-blue.svg)

Este é o repositório do **Projeto Blog Pessoal**, desenvolvido como parte do bootcamp da **Generation Brasil**. A aplicação consiste em uma API REST completa para um sistema de blog, permitindo o gerenciamento de postagens, temas de categorização e autenticação de usuários.

---

## 🎯 Funcionalidades Principais

A API oferece as seguintes funcionalidades:

-   **Autenticação e Autorização:** Cadastro e login de usuários com geração de token JWT (JSON Web Token) para controle de acesso.
-   **Gerenciamento de Postagens:** Criar, ler, atualizar e deletar (CRUD) postagens do blog.
-   **Gerenciamento de Temas:** Criar, listar, atualizar e deletar temas para categorizar as postagens.
-   **Relacionamento entre Entidades:** Postagens e temas possuem um relacionamento bidirecional (muitos-para-um).
-   **Validação de Dados:** Utilização de anotações (`@Valid`, `@NotBlank`, `@Size`) para garantir a integridade dos dados recebidos.
-   **Documentação Interativa:** Acesso à interface do Swagger UI para explorar e testar todos os endpoints disponíveis.

---

## 🛠️ Tecnologias Utilizadas

- **Java 17**
- **Spring Boot 3.x**
    - Spring Web (Endpoints REST)
    - Spring Data JPA (Persistência com Hibernate)
    - Spring Validation (Validação de dados)
    - Spring Security (Autenticação e Autorização)
    - SpringDoc OpenAPI (Geração da documentação da API com Swagger UI)
- **MySQL** (Banco de dados relacional)
- **JWT (JSON Web Token)** (Controle de sessão e autorização)
- **Maven** (Gerenciador de dependências)
- **Docker** (Containerização da aplicação)

```bash
http://localhost:8080/swagger-ui.html
```

Através da interface do Swagger UI, é possível visualizar os esquemas de requisição e resposta, bem como testar cada um dos endpoints da API diretamente pela interface gráfica.

---

## 📚 Documentação da API (Swagger)

Com a aplicação em execução, a documentação completa e interativa de todos os endpoints está disponível no seu navegador através do endereço:

## 🛑 Pré-requisitos para Execução

Antes de rodar a aplicação localmente, certifique-se de que possui:

1. **Java JDK 17** ou superior configurado no sistema.
2. Uma ferramenta de base de dados como o **MySQL Workbench** ativa.
3. Uma IDE instalada (Spring Tool Suite - STS, Eclipse, VS Code ou IntelliJ).

---

## 🚀 Como Rodar a Aplicação Localmente
   1. **Clonar este Repositório:**
   ```bash
   git clone https://github.com/crmprojetointegrador/projeto-integrador-fitness.git
   ```

2. **Configurar o Banco de Dados:**
   - No MySQL Workbench, crie uma base de dados com o nome que preferir (ex: `db_fitness_app`).
   - Configure as credenciais de acesso no arquivo `application.properties` localizado em `src/main/resources/`.

   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/db_fitness_app?useSSL=false&serverTimezone=UTC
   spring.datasource.username=root
   spring.datasource.password=sua_senha
   ```

3. **Executar a Aplicação:**
   - Importe o projeto na sua IDE como um **Projeto Maven Existente**.
   - Localize a classe principal `FitnessApplication.java` (ou similar) e execute-a como **Spring Boot App**.
  
4. **Testar a API**
   - Para acessar os endpoints autenticados, primeiro é necessário fazer login (`POST /usuarios/logar`) ou cadastrar um usuário (`POST /usuarios/cadastrar`). A requisição de login retornará um token JWT.
   - Utilize este token no cabeçalho `Authorization` das próximas requisições, no formato `Bearer <token_recebido>`.

---

## 🐳 Como Executar com Docker

O projeto possui um `Dockerfile`, permitindo sua execução em um container.

1.  **Build da Imagem:**
    ```bash
    docker build -t blog-pessoal-api .
    ```
2.  **Executar o Container:**
    ```bash
    docker run -p 8080:8080 blog-pessoal-api
    ```

---

## 👨‍💻 Autora

Desenvolvido por **Flame Souza** durante o bootcamp JAVA84 da Generation Brasil.

- **Flame Souza** - [GitHub](https://github.com/PraFlame)   [Linkedin](https://www.linkedin.com/in/souflame/)
