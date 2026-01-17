# Caroline Minelli Advocacia - Website Jurídico

Este é um site profissional de alta performance para o escritório de advocacia Caroline Minelli Advocacia, focado em Direito de Família e Civil. O projeto reflete autoridade, confiança e modernidade no ambiente digital.

---

## 🏛️ Objetivo do Projeto
O principal objetivo deste site é estabelecer a presença digital da Dra. Caroline Minelli, oferecendo uma interface intuitiva para que potenciais clientes conheçam seus serviços especializados e entrem em contato diretamente via WhatsApp de forma rápida e segura.

## 🎨 Design e Cores
O design foi cuidadosamente escolhido para transmitir seriedade e acolhimento:
- **Cores Primárias**: Tons sóbrios (Preto/Branco) com suporte completo a **Modo Escuro (Dark Mode)**.
- **Destaques**: Azul profundo e detalhes metálicos para transmitir autoridade jurídica.
- **Tipografia**: Combinação de fontes serifadas para títulos (elegância) e sans-serif para leitura (clareza).

## 🚀 Tecnologias e Importância
A escolha tecnológica foi feita pensando em **SEO, Performance e Escalabilidade**:
- **React + Vite**: Carregamento ultra rápido e interface reativa.
- **Tailwind CSS**: Estilização moderna e responsiva.
- **PostgreSQL + Drizzle**: Banco de dados robusto e consultas tipadas para evitar erros.
- **Framer Motion**: Animações suaves que elevam a percepção de qualidade do site.
- **TanStack Query**: Gerenciamento de dados eficiente, garantindo que as informações estejam sempre atualizadas.

---

## 🛠️ Como Rodar Localmente

### 1. Pré-requisitos
- Node.js (v20+) e npm instalados.
- Instância do PostgreSQL rodando (Docker ou instalação local).

### 2. Instalação
```bash
npm install
```

### 3. Configuração do Banco de Dados
Crie a tabela principal utilizando o script SQL abaixo:
```sql
-- Script SQL Completo
CREATE TABLE IF NOT EXISTS "services" (
    "id" SERIAL PRIMARY KEY,
    "title" TEXT NOT NULL,
    "description" TEXT NOT NULL,
    "category" TEXT NOT NULL,
    "icon" TEXT NOT NULL
);

-- Inserção de Dados Iniciais (Semente)
INSERT INTO "services" ("title", "description", "category", "icon") VALUES 
('Guarda', 'Proteção e bem-estar dos filhos e menores.', 'Família', 'Shield'),
('Divórcio', 'Atuação em divórcios judiciais e extrajudiciais.', 'Família', 'HeartCrack'),
('Regularização de Imóvel', 'Regularização documental e usucapião.', 'Civil', 'Home'),
('Indenização', 'Ações de reparação por danos materiais e morais.', 'Civil', 'Gavel');
```

### 4. Execução
```bash
# Configure o .env com seu DATABASE_URL
npm run dev
```

---

## 🌐 Deploy e Configuração de Domínio

### 1. Hospedagem (Railway / Render)
- **Build**: `npm install && npm run build`
- **Start**: `npm run start`
- **Variáveis**: 
  - `DATABASE_URL`: Link do seu banco Postgres.
  - `NODE_ENV`: `production`.
  - `PORT`: 5000.

### 2. Configuração de Domínio (ex: carolineminelli.com.br)
Para configurar um domínio personalizado:
1. No seu provedor de domínio (Registro.br, GoDaddy, etc), acesse as configurações de DNS.
2. No painel da sua hospedagem (Railway/Render), adicione seu domínio personalizado.
3. Crie os registros DNS solicitados pela plataforma:
   - **Registro A**: Apontando para o IP da plataforma.
   - **Registro CNAME**: Apontando para o endereço fornecido pela plataforma.
4. Aguarde a propagação (pode levar até 24h) e o certificado SSL (HTTPS) será gerado automaticamente.

---
Desenvolvido para representar excelência jurídica no ambiente digital.