# Caroline Minelli Advocacia - Website Jurídico

Este é um site profissional para o escritório de advocacia Caroline Minelli Advocacia, especializado em Direito de Família e Civil. O projeto foi desenvolvido com uma arquitetura moderna utilizando TypeScript, React e Node.js.

## 🚀 Tecnologias Utilizadas

- **Frontend**: React, Tailwind CSS, Shadcn/UI, Framer Motion, Wouter.
- **Backend**: Node.js, Express.
- **Banco de Dados**: PostgreSQL com Drizzle ORM.
- **Gerenciamento de Estado**: TanStack React Query.

## 🛠️ Como Rodar Localmente

### Pré-requisitos
- Node.js (v20 ou superior)
- PostgreSQL instalado e rodando

### Passo a Passo

1. **Clonar o Repositório**
   ```bash
   git clone <url-do-repositorio>
   cd caroline-minelli-advocacia
   ```

2. **Instalar Dependências**
   ```bash
   npm install
   ```

3. **Configurar Variáveis de Ambiente**
   Crie um arquivo `.env` na raiz do projeto ou configure as variáveis no seu terminal:
   ```env
   DATABASE_URL=postgres://usuario:senha@localhost:5432/nome_do_banco
   PORT=5000
   ```

4. **Configurar o Banco de Dados**
   Execute o seguinte script SQL no seu banco de dados para criar a tabela necessária:
   ```sql
   CREATE TABLE "services" (
       "id" serial PRIMARY KEY NOT NULL,
       "title" text NOT NULL,
       "description" text NOT NULL,
       "category" text NOT NULL,
       "icon" text NOT NULL
   );
   ```

5. **Iniciar o Servidor de Desenvolvimento**
   ```bash
   npm run dev
   ```
   O site estará disponível em `http://localhost:5000`.

## 🌐 Hospedagem (Railway / Render)

Este projeto já está configurado para ser hospedado facilmente em plataformas como Railway ou Render.

### Configurações Gerais
- **Build Command**: `npm install && npm run build`
- **Start Command**: `npm run start`
- **Porta**: 5000 (ou a definida pela plataforma na variável `PORT`)
- **Healthcheck**: O servidor possui um endpoint de verificação em `/health`.

### Variáveis de Ambiente Necessárias
- `DATABASE_URL`: URL de conexão com o banco de dados PostgreSQL.
- `NODE_ENV`: Deve ser definido como `production`.

## 📁 Estrutura do Projeto

- `client/`: Código fonte do frontend (React).
- `server/`: Código fonte do backend (Express).
- `shared/`: Esquemas e tipos compartilhados entre frontend e backend.
- `migrations/`: Arquivos de migração do banco de dados.

---
Desenvolvido com foco em performance e experiência do usuário.