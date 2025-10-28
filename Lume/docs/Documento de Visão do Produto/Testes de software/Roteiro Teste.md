# **Roteiro de Testes**

### **Caso de Teste 1** – Hashing de Senha no Cadastro (Service)

| Campo                 | Descrição                                                                 |
|----------------------|-----------------------------------------------------------------------------|
| Código               | TU-USR-001                                                                 |
| Nome do Teste        | Hashing de Senha no Cadastro (Service)                                     |
| Objetivo             | Verificar se a senha é hasheada antes do salvamento                        |
| Nível                | Unitário                                                                    |
| Tipo                 | Funcional                                                                   |
| Precondições         | `UserRepository` e `PasswordEncoder` mockados via Mockito                      |
| Critério de Aceite   | `encode()` chamado 1x + `save()` recebe senha hasheada                         |
| Resultado Previsto   | Passar                                                                      |
| Resultado Realizado  | A definir durante execução                                                |
| Evidências           | A definir (logs ou prints)                                                |
| Reparos Executados   | A definir                                                                 |
| Ciclos de Teste      | A definir                                                                 |


### **Caso de Teste 2** – Cadastro de Usuário (Integração)

| Campo                 | Descrição                                                                 |
|----------------------|-----------------------------------------------------------------------------|
| Código               | TI-USR-001                                                                 |
| Nome do Teste        | Cadastro de Usuário Válido (Controller API)                                |
| Objetivo             | Validar se o endpoint `POST /user` cadastra um usuário com sucesso           |
| Nível                | Integração                                                                  |
| Tipo                 | Funcional                                                                   |
| Precondições         | API rodando + banco limpo para o e-mail testado                            |
| Critério de Aceite   | HTTP `201/200` + JSON com `id` + senha hasheada salva                          |
| Resultado Previsto   | Passar                                                                      |
| Resultado Realizado  | A definir durante execução                                                |
| Evidências           | A definir (print do Postman ou terminal)                                  |
| Reparos Executados   | A definir                                                                 |
| Ciclos de Teste      | A definir                                                                 |


### **Caso de Teste 3** – Fluxo Completo de Cadastro (Sistema – Manual)

| Campo                 | Descrição                                                                 |
|----------------------|-----------------------------------------------------------------------------|
| Código               | TS-MAN-001                                                                 |
| Nome do Teste        | Fluxo Completo de Cadastro (Front + Back + DB)                              |
| Objetivo             | Validar ponta-a-ponta o cadastro pelo front-end até salvamento no banco    |
| Nível                | Sistema (Manual)                                                            |
| Tipo                 | Funcional                                                                   |
| Precondições         | Front (`npm run dev`) + Back + DB em `docker-compose` rodando                  |
| Critério de Aceite   | Formulário submetido com sucesso + usuário persistido com senha hasheada   |
| Resultado Previsto   | Passar                                                                      |
| Resultado Realizado  | A definir durante execução                                                |
| Evidências           | A definir (prints ou vídeo)                                               |
| Reparos Executados   | A definir                                                                 |
| Ciclos de Teste      | A definir                                                                 |

Nas tabelas apresentadas acima, todas as informações essenciais dos casos de teste foram registradas, incluindo código de identificação, nome do teste, objetivo, nível, tipo, precondições, registro dos resultados, reparos executados e quantidade de ciclos de teste.

No entanto, para complementar o roteiro de testes, é importante destacar que a definição de Aceito/Rejeitado de cada caso não foi incluída na tabela, mas permanece detalhada no texto descritivo de cada teste. Essa definição é fundamental, pois estabelece claramente os critérios que determinam se o teste passou ou falhou, garantindo que os resultados sejam avaliados de forma objetiva e padronizada.

Durante a execução dos testes, os campos de Resultado Realizado, Evidências e Reparos Executados serão preenchidos, permitindo um acompanhamento completo da validação do sistema Olimpo e facilitando futuras análises de qualidade e melhoria contínua.