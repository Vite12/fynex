# Overview

This is a Discord bot website built with React, Express.js, and PostgreSQL. The application appears to be for "Fynex," a Discord bot that specializes in chat rewards, giveaways, and community engagement features. The project follows a modern full-stack architecture with a React frontend, Express backend, and uses Drizzle ORM for database operations.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **React 18** with TypeScript for the client-side application
- **Vite** as the build tool and development server for fast builds and hot module replacement
- **Wouter** for lightweight client-side routing instead of React Router
- **TanStack Query** for server state management and data fetching
- **Tailwind CSS** with **shadcn/ui** components for styling and UI components
- **Radix UI** primitives for accessible, unstyled UI components

The frontend is structured as a single-page application with component-based architecture. The main pages include a home page showcasing the Discord bot's features, with sections for hero content, features, about information, and call-to-action areas.

## Backend Architecture
- **Express.js** server with TypeScript for the REST API
- **ESM modules** (type: "module") for modern JavaScript module support
- **Middleware-based** request processing with custom logging and error handling
- **Vite integration** in development mode for seamless full-stack development
- **Static file serving** for production builds

The server is designed to handle API routes with the `/api` prefix and includes middleware for JSON parsing, URL encoding, and request logging.

## Database Layer
- **PostgreSQL** as the primary database
- **Drizzle ORM** for type-safe database operations and schema management
- **Neon Database** integration via `@neondatabase/serverless` for serverless PostgreSQL
- **Schema-first approach** with shared types between frontend and backend
- **Migration system** using Drizzle Kit for database schema changes

The database schema includes a users table with basic authentication fields (username, password) and uses UUIDs for primary keys.

## State Management
- **In-memory storage** implementation as a fallback/development option
- **Storage interface pattern** allowing easy switching between different storage backends
- **Shared type definitions** between client and server for consistent data structures

## Development Tools
- **TypeScript** throughout the stack for type safety
- **ESBuild** for production builds and bundling
- **Path aliases** for clean imports (`@/`, `@shared/`, `@assets/`)
- **Hot reload** and development tooling integration

## Authentication & Session Management
- **PostgreSQL session storage** using `connect-pg-simple` for session persistence
- **Cookie-based sessions** for user authentication
- **Zod schemas** for runtime type validation using `drizzle-zod`

The architecture supports both development and production environments with different configurations for database connections, static file serving, and build processes.

# External Dependencies

## Database Services
- **Neon Database** - Serverless PostgreSQL database hosting
- **PostgreSQL** - Primary database system using the `postgresql` dialect

## UI/UX Libraries
- **Radix UI** - Comprehensive collection of accessible, unstyled UI primitives
- **shadcn/ui** - Pre-built component library built on top of Radix UI
- **Tailwind CSS** - Utility-first CSS framework for styling
- **Lucide React** - Icon library for consistent iconography

## Development Tools
- **Vite** - Frontend build tool and development server
- **Drizzle Kit** - Database migration and schema management tool
- **TypeScript** - Static type checking and enhanced developer experience

## Runtime Libraries
- **TanStack Query** - Server state management and caching
- **React Hook Form** - Form state management and validation
- **date-fns** - Date manipulation and formatting utilities
- **clsx** & **tailwind-merge** - Conditional CSS class management

## Discord Integration
The application is designed to integrate with Discord's OAuth2 API and bot systems, though specific Discord SDK dependencies are not yet implemented in the current codebase.

## Session & Storage
- **connect-pg-simple** - PostgreSQL-backed session store for Express
- **Embla Carousel** - Carousel/slider components for the frontend

The project is configured to work seamlessly in both development (with Vite's dev server) and production environments, with proper build pipelines and deployment configurations.