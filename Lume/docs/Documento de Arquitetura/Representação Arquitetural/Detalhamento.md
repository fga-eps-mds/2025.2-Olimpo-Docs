# Detalhamento

A arquitetura geral pode ser representada esquematicamente da seguinte forma:

**Componentes Principais:**

1.  **Cliente Web (React/Vite):** Responsável pela interface com o usuário (UI) e experiência do usuário (UX). Executa no navegador do usuário.
    - **Responsabilidades:** Renderizar telas, capturar entradas do usuário, fazer requisições HTTP para a API Back-end, exibir dados recebidos.
    - **Comunicação:** Utiliza o protocolo **HTTP** para enviar requisições (GET, POST, PUT, DELETE) para a API Back-end. Os dados são trocados no formato **JSON**.
2.  **API Back-end (Spring Boot/Java):** Contém a lógica de negócio principal, gerenciamento de usuários, e orquestração do acesso aos dados. Executa em um contêiner Docker.
    - **Responsabilidades:** Expor endpoints RESTful, validar dados de entrada, processar regras de negócio, interagir com o banco de dados através da camada de persistência, gerenciar autenticação e autorização.
    - **Comunicação:** Recebe requisições HTTP do Cliente Web. Comunica-se com o Banco de Dados via **JDBC** (gerenciado pelo Spring Data JPA/Hibernate).
3.  **Banco de Dados (PostgreSQL):** Armazena todos os dados persistentes da aplicação (usuários, projetos, etc.). Executa em um contêiner Docker separado.
    - **Responsabilidades:** Persistir dados, garantir integridade referencial, executar consultas SQL.
    - **Comunicação:** Recebe conexões JDBC da API Back-end.

**Tecnologias e Protocolos:**

- Front-end para Back-end: HTTP/JSON sobre TCP/IP.
- Back-end para Banco de Dados: JDBC sobre TCP/IP.
- Ambiente de Desenvolvimento: Docker Compose para gerenciar os contêineres do Back-end e Banco de Dados.