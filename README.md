# NLW Connect Java - Rocketseat

## 📈 Projeto Desenvolvido

Durante o intensivo de tecnologia, foi desenvolvido um sistema de inscrições em eventos, onde os usuários podem se inscrever, gerar links de indicação e acompanhar um ranking de indicações.

## 🚀 Tecnologias

Foram utilizadas as seguintes tecnologias:

- **Java 17**
- **Spring Boot 3.4.2**
- **Maven**

### Dependências utilizadas:

- Spring Web
- Spring Boot DevTools
- Spring Data JPA
- MySQL Driver

## 💡 Estrutura do Projeto

O projeto segue a organização tradicional do Spring Boot, adotando a separação de responsabilidades.

**Padrão em camadas**: Model, Controller, Service, Repository, Padrão DTO.

### Diagrama Entidade-Relacionamento:

![Diagrama ER](https://github.com/user-attachments/assets/a8b8265c-bf10-465a-a984-89a6209dd913)

## ✨ Funcionalidades

- 📌 **Inscrição**: Usuários podem se inscrever em eventos informando nome e e-mail.
- 🔗 **Geração de Link de Indicação**: Cada inscrito pode gerar um link de indicação único.
- 📊 **Ranking de Indicações**: Exibe um ranking baseado no número de indicações bem-sucedidas.
- 👥 **Visualização de Indicações**: Cada usuário pode ver quantas pessoas se inscreveram usando seu link.

## 🌐 Rotas da API

### 🎟️ Eventos

- **Criar um evento**  
  **(POST)** `/events`
- **Listar todos os eventos**  
  **(GET)** `/events`
- **Obter evento por nome formatado**  
  **(GET)** `/events/{prettyName}`

### 📝 Inscrição

- **Realizar inscrição no evento**  
  **(POST)** `/subscription/{prettyName}`
- **Cadastrar usuário com id de indicação**  
  **(POST)** `/subscription/{prettyName}/ranking/{userId}`
- **Visualizar ranking de indicações de um evento**  
  **(GET)** `/subscription/{prettyName}/ranking`
- **Visualizar ranking de indicações de um usuário específico**  
  **(GET)** `/subscription/{prettyName}/ranking/{userId}`

## 💻 Como Rodar o Projeto

Para executar o projeto localmente, siga os passos abaixo:

1. Clone o repositório:

    ```bash
    git clone --branch aula3 --single-branch https://github.com/CamilleGFAlmeida/nlw-connect-java.git
    ```

2. Importe o projeto na sua IDE (Eclipse, IntelliJ, STS, Visual Studio):

    - Selecione **Import > Import Maven Projects**

3. Configure o banco de dados:

    - Edite o arquivo `application.properties` e adapte o valor de `spring.datasource.password` conforme sua configuração local.
    - No MySQL, crie o schema do banco de dados:

      ```sql
      CREATE SCHEMA db_events;
      ```

4. Inicie o servidor:

    - Execute a aplicação dentro da sua IDE ou pelo terminal com:

      ```bash
      mvn spring-boot:run
      ```

