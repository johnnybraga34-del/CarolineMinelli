# Caroline Minelli Advocacia - Law Firm Website

## Overview

This is a professional law firm website for Caroline Minelli Advocacia, built as a full-stack TypeScript application. The site showcases legal services in family and civil law, featuring a modern design with dark/light theme support, smooth animations, and WhatsApp integration for client communication. The application uses a React frontend with an Express backend, PostgreSQL database, and is optimized for the Replit deployment environment.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Routing**: Wouter (lightweight alternative to React Router)
- **State Management**: TanStack React Query for server state
- **Styling**: Tailwind CSS with CSS variables for theming
- **UI Components**: shadcn/ui component library (Radix UI primitives)
- **Animations**: Framer Motion for scroll reveals and transitions
- **Icons**: Lucide React
- **Build Tool**: Vite with custom plugins for Replit integration

### Backend Architecture
- **Runtime**: Node.js with Express
- **Language**: TypeScript (ESM modules)
- **API Pattern**: Simple REST endpoints defined in `shared/routes.ts`
- **Database ORM**: Drizzle ORM with PostgreSQL dialect
- **Schema Validation**: Zod with drizzle-zod integration

### Project Structure
```
├── client/           # Frontend React application
│   ├── src/
│   │   ├── components/   # React components including shadcn/ui
│   │   ├── hooks/        # Custom React hooks
│   │   ├── lib/          # Utilities and query client
│   │   └── pages/        # Page components
├── server/           # Backend Express application
│   ├── db.ts         # Database connection
│   ├── routes.ts     # API route definitions
│   ├── storage.ts    # Data access layer
│   └── index.ts      # Server entry point
├── shared/           # Shared types and schemas
│   ├── schema.ts     # Drizzle database schema
│   └── routes.ts     # API route definitions with Zod validation
└── migrations/       # Drizzle database migrations
```

### Design Patterns
- **Storage Pattern**: `IStorage` interface abstracts database operations in `server/storage.ts`
- **Type-Safe API**: Shared route definitions with Zod schemas ensure frontend/backend type consistency
- **Component Library**: shadcn/ui provides accessible, customizable components
- **Theme System**: CSS variables with dark/light mode toggle via React context

### Database Schema
Single table design focused on services:
- `services`: id, title, description, category, icon (references Lucide icon names)

Database is auto-seeded on startup with predefined legal services.

## External Dependencies

### Database
- **PostgreSQL**: Primary database accessed via `DATABASE_URL` environment variable
- **Drizzle ORM**: Schema definition and query building
- **Connection Pooling**: pg Pool for connection management

### Third-Party Services
- **WhatsApp Business**: Direct messaging link (https://wa.me/5511918231667)
- **Google Fonts**: Playfair Display and Plus Jakarta Sans font families

### Key NPM Packages
- `@tanstack/react-query`: Async state management
- `framer-motion`: Animation library
- `embla-carousel-react`: Carousel component
- `react-hook-form` + `@hookform/resolvers`: Form handling with Zod validation
- `wouter`: Client-side routing
- `drizzle-orm` + `drizzle-zod`: Database ORM and schema validation

### Build & Development
- `vite`: Frontend bundler with HMR
- `esbuild`: Server bundling for production
- `tsx`: TypeScript execution for development
- Replit-specific Vite plugins for development experience