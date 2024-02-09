Este projeto é uma API desenvolvida em Node.js que permite a criação, visualização e votação em enquetes em tempo real.

------- Rotas Disponíveis: --------

--Criar Enquete--

Endpoint: POST /polls
Corpo da Requisição:

json
{
  "title": "Título da Enquete",
  "options": ["Opção 1", "Opção 2", ...]
}

--Obter Enquete--

Endpoint: GET /polls/:pollId

Retorna os detalhes da enquete com o ID especificado, incluindo título, opções e contagem de votos para cada opção.


--Votar em uma Enquete--

Endpoint: POST /polls/:pollId/votes
Corpo da Requisição:

json
{
  "pollOptionId": "ID da Opção de Enquete"
}

Registra o voto do usuário na enquete especificada pelo ID da opção de enquete fornecido. A votação é realizada apenas uma vez por sessão do usuário.


------Tecnologias Utilizadas:-----
Node.js
TypeScript
PostgreSQL
Redis
WebSockets
Prisma
Fastify
Zod

Para iniciar o servidor, execute o arquivo Server.ts. Certifique-se de ter todas as dependências instaladas e configuradas corretamente. Após iniciar o servidor, você pode interagir com a API usando as rotas mencionadas acima.

--------Projeto de estudos do evento NLW da Rocketseat------
