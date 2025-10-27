# Justificativa

A escolha da arquitetura Cliente-Servidor é justificada pela necessidade de separar as responsabilidades da interface do usuário (React) da lógica de negócios e acesso a dados (Spring Boot). Isso permite:

- Desenvolvimento paralelo das interfaces web e da API.
- Flexibilidade para futuras interfaces (ex: um app mobile consumindo a mesma API).
- Escalabilidade independente do front-end e back-end.

A Arquitetura em Camadas no back-end foi escolhida por ser um padrão bem estabelecido no ecossistema Spring, promovendo:

- Organização clara do código.
- Separação de responsabilidades (apresentação, negócio, dados).
- Maior testabilidade (testes unitários por camada).
- Manutenibilidade.

Essa estrutura suporta os objetivos do produto de fornecer uma plataforma interativa e gerenciável para conectar usuários distintos (estudantes e investidores).