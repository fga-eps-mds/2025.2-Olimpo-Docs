# **Visão de Implantação**

- **Ambiente de Desenvolvimento Local:** O software é implantado localmente utilizando **Docker Compose**.
    - O Banco de Dados **PostgreSQL (v16-alpine)** roda em um contêiner Docker (`db`).
    - A API Back-end **Spring Boot (Java 21)** roda em um segundo contêiner Docker (`app`), construído a partir de um `Dockerfile` que utiliza Maven.
    - O Cliente Web **React (Vite/Node.js v22)** roda diretamente na máquina do desenvolvedor via `npm run dev` e se conecta à API exposta pelo Docker na `localhost:8080`.
- **Ambiente de Produção:** Devido ao tempo e a proposta da disciplina, não utilizaremos nenhum ambiente de produção.