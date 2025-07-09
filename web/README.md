# NLW Agents - Web

Este é o front-end do projeto desenvolvido durante a **Next Level Week (NLW) Agents**, um evento online e gratuito promovido pela [Rocketseat](https://www.rocketseat.com.br/).

A aplicação consiste em um sistema de salas, permitindo que os usuários visualizem as salas disponíveis e acessem uma sala específica para interagir.

## ✨ Tecnologias

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
