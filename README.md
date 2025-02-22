# Evento NLW Connect Java

## 📍 Sobre

Este projeto foi desenvolvido durante o intensivo de trilhas da Rocketseat e tem como objetivo gerenciar inscrições em eventos. Os usuários podem se inscrever, gerar links de indicação e acompanhar um ranking baseado nas indicações realizadas.

## 🚀 Tecnologias Utilizadas

O projeto foi desenvolvido com as seguintes tecnologias:

- **Java 17**
- **Spring Boot 3.4.2**
- **Maven**
- **MySQL**

### 📦 Dependências

- Spring Web
- Spring Boot DevTools
- Spring Data JPA
- MySQL Driver

## 🗂 Arquitetura do Projeto

O projeto segue a organização tradicional do Spring Boot, adotando a separação de responsabilidades para melhor manutenção e escalabilidade.

**Padrão em camadas**: Model, Controller, Service, Repository, DTO.

### 📊 Diagrama Entidade-Relacionamento

![Diagrama ER](https://github.com/user-attachments/assets/a8b8265c-bf10-465a-a984-89a6209dd913)

## ✨ Funcionalidades Principais

- 📌 **Inscrição**: Usuários podem se inscrever em eventos informando nome e e-mail.
- 🔗 **Geração de Link de Indicação**: Cada inscrito pode gerar um link de indicação único.
- 📊 **Ranking de Indicações**: Exibe um ranking baseado no número de indicações bem-sucedidas.
- 👥 **Visualização de Indicações**: Cada usuário pode ver quantas pessoas se inscreveram usando seu link.

## 🌐 Endpoints da API

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

## 💻 Como Configurar e Executar o Projeto

### 🔹 Pré-requisitos
Antes de começar, certifique-se de ter instalado:
- [Java 17](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html)
- [MySQL](https://dev.mysql.com/downloads/)
- [Maven](https://maven.apache.org/)
- Uma IDE como [IntelliJ](https://www.jetbrains.com/idea/) ou [Eclipse](https://www.eclipse.org/)

### 🔹 Passos para execução

1. **Clone o repositório**

    ```bash
    git clone --branch main --single-branch https://github.com/CamilleGFAlmeida/nlw-connect-java.git
    ```

2. **Importe o projeto na sua IDE**

    - Selecione **Import > Import Maven Projects**

3. **Configure o banco de dados**

    - Edite o arquivo `application.properties` e adapte o valor de `spring.datasource.password` conforme sua configuração local.
    - No MySQL, crie o schema do banco de dados:

      ```sql
      CREATE SCHEMA db_events;
      ```

4. **Execute a aplicação**

    - Inicie a aplicação dentro da sua IDE ou via terminal com:

      ```bash
      mvn spring-boot:run
      ```

## 🛠 Melhorias Futuras
- Implementação de autenticação para usuários
- Adição de testes unitários e de integração
- Melhorias no sistema de ranking

---

Este projeto foi desenvolvido com base no evento NLW da Rocketseat. 💜🚀

