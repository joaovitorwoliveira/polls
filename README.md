API de Enquetes
Este projeto é uma API desenvolvida em Node.js que permite a criação, visualização e votação em enquetes em tempo real.

Rotas Disponíveis:
Criar Enquete

Endpoint: POST /polls
Corpo da Requisição:
json
Copy code
{
  "title": "Título da Enquete",
  "options": ["Opção 1", "Opção 2", ...]
}
Cria uma nova enquete com o título fornecido e as opções especificadas.
Obter Enquete

Endpoint: GET /polls/:pollId
Retorna os detalhes da enquete com o ID especificado, incluindo título, opções e contagem de votos para cada opção.
Votar em uma Enquete

Endpoint: POST /polls/:pollId/votes
Corpo da Requisição:
json
Copy code
{
  "pollOptionId": "ID da Opção de Enquete"
}
Registra o voto do usuário na enquete especificada pelo ID da opção de enquete fornecido. A votação é realizada apenas uma vez por sessão do usuário.
Tecnologias Utilizadas:
Node.js: Plataforma de execução de código JavaScript.
TypeScript: Superset de JavaScript que adiciona tipagem estática ao código.
PostgreSQL: Sistema de gerenciamento de banco de dados relacional.
Redis: Banco de dados em memória usado para caching e armazenamento de dados temporários.
WebSockets: Protocolo que permite comunicação bidirecional e em tempo real entre o cliente e o servidor.
Prisma: ORM (Object-Relational Mapping) para interagir com o banco de dados.
Fastify: Framework web extremamente rápido e eficiente para Node.js.
Zod: Biblioteca de validação de esquemas para tipos de dados em JavaScript e TypeScript.
Para iniciar o servidor, execute o arquivo Server.ts. Certifique-se de ter todas as dependências instaladas e configuradas corretamente. Após iniciar o servidor, você pode interagir com a API usando as rotas mencionadas acima.
