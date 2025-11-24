# Aplicação Web de Músicas

Uma aplicação web moderna para descobrir, buscar e organizar suas músicas favoritas em playlists personalizadas.

## 🎵 Como a Aplicação Funciona

### Funcionalidades Principais

#### 1. **Autenticação e Login**
- A aplicação começa com uma página de login
- Após autenticar-se, o usuário tem acesso às funcionalidades principais
- As rotas protegidas garantem que apenas usuários autenticados possam acessar as páginas

#### 2. **Home - Músicas Populares**
- Exibe uma grid com as músicas mais populares
- Cada música mostra:
  - Capa (thumbnail)
  - Nome da música
  - Artista
  - Gênero e ano de lançamento
- Permite adicionar músicas às suas playlists através de um botão flutuante
- Carrega dados da API **TheAudioDB** com artistas populares como Coldplay, Queen e The Beatles

#### 3. **Playlists**
- Crie e organize suas próprias playlists
- Gerencie suas playlists personalizadas
- Adicione ou remova músicas das playlists

#### 4. **Busca de Músicas**
- Busque músicas por:
  - **Nome do artista**: Encontra todos os artistas cadastrados e suas músicas
  - **Nome da música**: Procura diretamente por faixas específicas
- Resultados em tempo real com até 10 músicas por busca

### Fluxo da Aplicação

1. **Login** → Autenticação do usuário
2. **Home** → Visualizar músicas populares e adicionar às playlists
3. **Buscar Músicas** → Encontrar novas músicas por artista ou nome
4. **Playlists** → Gerenciar e organizar suas playlists personalizadas
5. **Modo Escuro/Claro** → Alternar tema conforme preferência

### Arquitetura Técnica

- **Frontend Framework**: React com TypeScript
- **Estado Global**: Redux Toolkit para gerenciar:
  - Autenticação do usuário
  - Musicas populares e de busca
  - Playlists do usuário
- **API Externa**: TheAudioDB para dados de músicas
- **UI Components**: shadcn-ui com componentes Radix UI
- **Estilos**: Tailwind CSS
- **Roteamento**: React Router para navegação entre páginas
- **Build Tool**: Vite

## 🚀 Como Executar

### Requisitos
- Node.js (recomendado: v16 ou superior)
- npm ou bun

### Instalação e Desenvolvimento

```bash
# Clone o repositório
git clone <URL_DO_REPOSITÓRIO>

# Acesse o diretório
cd aplicao-web-react-musicas

# Instale as dependências
npm install

# Inicie o servidor de desenvolvimento
npm run dev
```

A aplicação estará disponível em `http://localhost:5173`

### Build para Produção

```bash
npm run build
```

## 📦 Tecnologias Utilizadas

- **React 18** - Biblioteca para construir interfaces
- **TypeScript** - Tipagem estática para JavaScript
- **Vite** - Build tool rápido e moderno
- **Redux Toolkit** - Gerenciamento de estado
- **React Router** - Roteamento de páginas
- **Tailwind CSS** - Framework de estilos utilitários
- **shadcn-ui** - Componentes acessíveis e reutilizáveis
- **React Query** - Gerenciamento de requisições assíncronas
- **React Hook Form** - Gerenciamento de formulários
- **Sonner** - Toast notifications

## 📁 Estrutura do Projeto

```
src/
├── components/        # Componentes reutilizáveis
│   ├── ui/           # Componentes UI (shadcn-ui)
│   ├── AppSidebar.tsx
│   ├── Header.tsx
│   └── PrivateRoute.tsx
├── pages/            # Páginas da aplicação
│   ├── Home.tsx
│   ├── Login.tsx
│   ├── Playlists.tsx
│   ├── Musicas.tsx
│   └── NotFound.tsx
├── services/         # Serviços de API
│   └── audioDbApi.ts
├── store/            # Redux store e slices
│   ├── store.ts
│   └── slices/
├── contexts/         # Context API
│   └── ThemeContext.tsx
└── hooks/            # Custom hooks
```

## 🎨 Temas

A aplicação suporta modo claro e escuro, permitindo uma experiência personalizada de acordo com a preferência do usuário.
