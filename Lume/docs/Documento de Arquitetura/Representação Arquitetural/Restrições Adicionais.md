# **Restrições Adicionais**

- **Acesso:** O software será acessível pela Internet e exigirá login do usuário para a maioria das funcionalidades (cadastro e recuperação de senha serão públicos).
- **Características de Qualidade:**
    - **Segurança:** Senhas devem ser armazenadas com hashing (BCrypt). Acesso a funcionalidades deve ser controlado por roles (Spring Security). 
    - **Manutenibilidade:** O código deve seguir boas práticas (separação de camadas, nomes claros, testes automatizados) para facilitar futuras modificações.
    - **Portabilidade:** O uso de Docker visa facilitar a execução em diferentes ambientes.