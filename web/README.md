# NLW Agents - Web

Este é o front-end do projeto de Perguntas e Respostas com I.A. desenvolvido durante a **Next Level Week (NLW) Agents**, um evento online e gratuito promovido pela [Rocketseat](https://www.rocketseat.com.br/).

A aplicação consiste em um sistema onde usuários podem criar salas, fazer perguntas e interagir com respostas.

## ✨ Funcionalidades

- **Criação de Salas**: Usuários podem criar novas salas fornecendo um nome (com no mínimo 3 caracteres) e uma descrição opcional. O formulário utiliza `react-hook-form` para gerenciamento de estado e `zod` para validação.
- **Listagem de Salas**: A página inicial exibe uma lista com as salas criadas recentemente, mostrando:
  - O nome da sala.
  - Há quanto tempo foi criada (utilizando `dayjs`).
  - A quantidade de perguntas já feitas.
- **Página da Sala**: Cada sala possui uma página dedicada (`/room/:id`) onde os usuários podem visualizar as perguntas existentes e submeter novas questões.

## 🚀 Tecnologias

Este projeto foi desenvolvido com as seguintes tecnologias:

- **[React](https://react.dev/)**: Biblioteca para construção de interfaces de usuário.
- **[TypeScript](https://www.typescriptlang.org/)**: Superset do JavaScript que adiciona tipagem estática.
- **[Vite](https://vitejs.dev/)**: Ferramenta de build moderna e ultrarrápida para desenvolvimento web.
- **[Tailwind CSS](https://tailwindcss.com/)**: Framework CSS utility-first para estilização rápida.
- **[React Router DOM](https://reactrouter.com/)**: Para gerenciamento de rotas na aplicação.
- **[TanStack Query (React Query)](https://tanstack.com/query/latest)**: Para data fetching, cache e sincronização de estado com o servidor.
- **[Biome](https://biomejs.dev/)**: Ferramenta para formatação e linting de código, garantindo a consistência e qualidade.

## 💻 Como Executar

Para executar o projeto localmente, siga os passos abaixo:

1.  **Clone o repositório** (caso ainda não tenha feito):

    ```bash
    git clone https://github.com/seu-usuario/nlw-agents.git
    ```

2.  **Navegue até a pasta do projeto web:**

    ```bash
    cd nlw-agents/web
    ```

3.  **Instale as dependências:**

    ```bash
    npm install
    ```

4.  **Execute o servidor de desenvolvimento:**

    ```bash
    npm run dev
    ```

5.  Abra seu navegador e acesse `http://localhost:5173` (ou a porta indicada no seu terminal).

## 📝 Estrutura do Projeto

A estrutura de pastas do front-end está organizada da seguinte forma:

```
src/
├── components/  # Componentes reutilizáveis da UI
├── lib/         # Funções utilitárias
├── pages/       # Componentes de página (CreateRoom, Room)
├── App.tsx      # Componente principal com as rotas da aplicação
└── main.tsx     # Ponto de entrada da aplicação React
```
