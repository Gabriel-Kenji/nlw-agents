# NLW Agents - Server

Este é o backend do projeto **NLW Agents**, desenvolvido durante a 16ª edição do evento Next Level Week da [Rocketseat](https://rocketseat.com.br).

A aplicação consiste em um servidor robusto para gerenciar salas de chat e interações, utilizando um stack moderno e performático.

## ✨ Tecnologias Utilizadas

Este projeto foi construído com as seguintes tecnologias:

- **[Node.js](https://nodejs.org/en/)**
- **[Fastify](https://fastify.dev/)**: Um framework web focado em performance.
- **[TypeScript](https://www.typescriptlang.org/)**: Para tipagem estática e um desenvolvimento mais seguro.
- **[PostgreSQL](https://www.postgresql.org/)**: Como banco de dados relacional.
- **[Drizzle ORM](https://orm.drizzle.team/)**: Um ORM TypeScript-first, leve e rápido.
- **[Zod](https://zod.dev/)**: Para validação de schemas e tipos.
- **[Biome](https://biomejs.dev/)**: Para formatação e linting do código, garantindo consistência e qualidade.

## 🚀 Funcionalidades

O servidor atualmente implementa os seguintes endpoints:

- **Verificação de Saúde**: Um endpoint para verificar se a API está no ar.
- **Listagem de Salas**: Um endpoint para obter a lista de salas disponíveis.

## ⚙️ Configuração do Ambiente

Siga os passos abaixo para configurar e rodar o projeto em seu ambiente de desenvolvimento.

### Pré-requisitos

- **Node.js**: Versão 20 ou superior.
- **Gerenciador de Pacotes**: npm, Yarn ou pnpm.
- **Docker**: Para rodar uma instância do PostgreSQL facilmente (recomendado).

### 1. Clonar o Repositório

```bash
git clone https://github.com/SEU_USUARIO/nlw-agents.git
cd nlw-agents/server
```

### 2. Instalar Dependências

Use seu gerenciador de pacotes preferido para instalar todas as dependências do projeto.

```bash
npm install
```

### 3. Configurar o Banco de Dados

É recomendado usar o Docker para subir uma instância do PostgreSQL:

```bash
docker run --name nlw-agents-pg -e POSTGRES_PASSWORD=docker -e POSTGRES_DB=nlw_agents -p 5432:5432 -d postgres
```

Crie um arquivo `.env` na raiz da pasta `server` e adicione a variável de ambiente para a URL de conexão com o banco:

```env
DATABASE_URL="postgresql://docker:docker@localhost:5432/nlw_agents"
```

### 4. Migrations e Seed

Com o banco de dados rodando, aplique as migrações para criar as tabelas e, em seguida, popule o banco com dados iniciais.

```bash
# Para aplicar as migrações
npx drizzle-kit migrate

# Para popular o banco (opcional)
npx drizzle-seed
```

> **Dica**: Adicione scripts no seu `package.json` para facilitar esses comandos.

## ▶️ Executando a Aplicação

Para iniciar o servidor em modo de desenvolvimento, execute o seguinte comando:

```bash
npm run dev
```

> **Nota**: Este projeto usa `ultracite` como servidor de desenvolvimento. Certifique-se de ter um script `dev` no seu `package.json`, como: `"dev": "ultracite"`.

O servidor estará disponível em `http://localhost:3333`.

## 📝 Endpoints da API

Você pode testar os endpoints usando o arquivo `client.http` ou sua ferramenta de API preferida.

- `GET /health`
  - Retorna o status da aplicação.
- `GET /rooms`
  - Retorna a lista de salas disponíveis.
