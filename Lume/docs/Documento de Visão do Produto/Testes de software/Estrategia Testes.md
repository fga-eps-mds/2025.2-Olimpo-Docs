# **Estratégia de Testes**

A estratégia de testes adotada para o sistema foi definida com o objetivo de garantir que as funcionalidades implementadas atendessem aos requisitos previstos nas User Stories, assegurando também a confiabilidade e o correto funcionamento entre as camadas da aplicação. Os testes foram planejados considerando diferentes níveis, tipos e ambientes de execução, buscando assegurar qualidade tanto em aspectos funcionais quanto não funcionais básicos.

## **Níveis de Testes Abordados:**

Foram considerados dois principais níveis de verificação:

- **Teste Unitário:**

Focado na validação de classes e métodos individuais, especialmente na camada de serviços (Services).
  - Utilização de JUnit 5 para criação dos casos de teste;
  - Uso de Mockito para simular dependências e isolar a lógica.

- **Teste de Integração:**

Realizado para garantir o correto fluxo entre as camadas da aplicação (Controller ↔ Service ↔ Repository).
  - Uso do Spring Boot Test (@SpringBootTest, @DataJpaTest);
  - Testes utilizando MockMvc para simulação de requisições HTTP.

## **Tipos de Testes Abordados:**

- **Funcionais:** Verificam se as funcionalidades implementadas estão em conformidade com os requisitos das User Stories (ex.: cadastro, login, recuperação de senha, etc.).

- **Não Funcionais (Básicos):**
    - Segurança: avaliação simples do controle de acesso (endpoints públicos x protegidos).
    - Usabilidade: observada informalmente durante testes manuais e demonstrativos.

**Ambientes de Teste:** Os testes ocorreram em ambiente local, com separação entre desenvolvimento e integração:

- **Desenvolvimento Local**: Execução de testes unitários e de integração via IDE ou linha de comando.

- **Ambiente Integrado Local**: Execução de testes manuais com back-end em Docker (docker compose up) e front-end rodando em modo de desenvolvimento (npm run dev).
    - Fluxo de versionamento: feature → developer → main.

## **Formas de Análise dos Resultados:**

A validação dos testes utiliza diferentes critérios:

- **Resultados**: análise binária (Passou / Falhou).
- **Cobertura de Testes**: relatórios de cobertura para identificar áreas críticas sem validação suficiente.
- **Revisão por Pares (Pull Requests)**: obrigatoriedade de testes associados ao código enviado.

## **Resultados Obtidos (Previstos x Realizados)**

- Para cada caso de teste, o resultado previsto é que seja "Passou", desde que o comportamento atenda ao requisito validado.
- Os resultados serão registrados no Roteiro de Testes (Seção 6.2), contendo evidências quando necessário.
- Em caso de falha:
    - o defeito é registrado,
    - o código é corrigido,
    - e o teste é reexecutado até que o resultado "Realizado" = "Previsto".