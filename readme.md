## 🏆 DevStage - Backend (API) Node.js License

### 🚀 Visão Geral

O DevStage Backend é a API responsável por gerenciar o ranqueamento de convites, autenticação de usuários e integração com o banco de dados e Redis. Ele fornece endpoints para:

🎯 Ranqueamento Dinâmico – Atualiza e retorna a posição dos usuários no ranking.
<br>
🔗 Geração de Links de Convite – Gera links exclusivos para cada usuário.
<br>
🏆 Prêmios para os Top 3 – Identifica e premia os três primeiros colocados no ranking.
<br>
🔒 Autenticação Segura – Gerencia a autenticação de usuários com JWT (JSON Web Tokens).

## ✨ Características do Projeto

✅ Banco de Dados Relacional – Utiliza PostgreSQL para armazenamento de dados.
<br>
✅ Cache com Redis – Melhora o desempenho com armazenamento em cache.
<br>
✅ Documentação da API – Integração com Swagger para documentação automática dos endpoints.
<br>
✅ Validação de Dados – Utiliza Zod para validação de esquemas.
<br>
✅ Autenticação com JWT – Segurança robusta com tokens JWT.
<br>
✅ CORS Habilitado – Permite integração segura com o frontend.

## 🛠️ Tecnologias Utilizadas

### Backend

- **Fastify** – Framework web rápido e eficiente para Node.js.

- **PostgreSQL** – Banco de dados relacional para armazenamento de dados.

- **Redis** – Armazenamento em cache para melhorar o desempenho.

- **Drizzle ORM** – ORM moderno para interação com o banco de dados.

- **Zod** – Biblioteca de validação de esquemas para TypeScript.

- **Swagger** – Documentação automática da API.

- **JWT** – Autenticação segura com JSON Web Tokens.

## 🛠️ Ferramentas de Desenvolvimento

- **TypeScript** – Adiciona tipagem estática ao JavaScript para maior segurança e produtividade.

- **Biome** – Ferramenta de formatação e linting para JavaScript/TypeScript.

- **TSX** – Executor TypeScript para desenvolvimento local.

- **Tsup** – Ferramenta de build para TypeScript.

## Como Rodar o Projeto Localmente

### Pré-requisitos

- Node.js (versão 20 ou superior)
- Docker e Docker Compose (para rodar PostgreSQL e Redis)
- npm ou yarn (gerenciadores de pacotes)

### Passos

1. Clone o repositório:
   ```bash
   git clone https://github.com/JPerrut/DevstageBackend.git
   ```
2. Acesse a pasta do projeto:
   ```bash
   cd devstage-backend
   ```
3. Crie um arquivo .env na raiz do projeto:

   ```bash
   # Server
   PORT=3333

   # Database
   DATABASE_URL="postgresql://user:password@localhost:5432/connect"

   # Redis
   REDIS_URL="redis://localhost:6379"

   # URLs
   API_URL="http://localhost:3333"
   WEB_URL="http://localhost:3000"
   Comandos Úteis
   ```

4. Crie um arquivo docker-compose.yml na raiz do projeto:

   ```bash
   services:
   connect-pg:
       image: bitnami/postgresql:latest
       ports:
       - '5432:5432'
       environment:
       - POSTGRES_USER=user
       - POSTGRES_PASSWORD=password
       - POSTGRES_DB=connect

   connect-redis:
       image: bitnami/redis:latest
       environment:
       - ALLOW_EMPTY_PASSWORD=yes
       ports:
       - "6379:6379"
   ```

5. Instale as dependências:
   ```bash
   npm install
   ```
6. Inicie os contêineres do Docker (PostgreSQL e Redis):
   ```bash
   docker compose up -d
   ```
7. Gere as migrações do banco de dados:
   ```bash
   npm run db:generate
   ```
8. Aplique as migrações:
   ```bash
   npm run db:migrate
   ```
9. Inicie o servidor de desenvolvimento:
   ```bash
   npm run dev
   ```
10. Acesse a API no navegador:
    ```bash
    http://localhost:3333/docs
    ```

## 🤝 Contribuição

### Contribuições são bem-vindas! Siga os passos abaixo:

1. Faça um fork do projeto.
2. Crie uma branch para sua feature (`git checkout -b feature/nova-feature`).
3. Commit suas mudanças (`git commit -m 'Adiciona nova feature'`).
4. Faça push para a branch (`git push origin feature/nova-feature`).
5. Abra um Pull Request.

## 📄 Licença

Este projeto está licenciado sob a <a href="https://opensource.org/license/mit">MIT License</a>.

## 📞 Contato

### Se tiver dúvidas ou sugestões, entre em contato:

Nome: João Perrut <br>
Email: joaoperrutc@gmail.com <br>
Linkedin: https://www.linkedin.com/in/perrut/
