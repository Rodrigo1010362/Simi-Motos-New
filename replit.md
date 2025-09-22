# Inventory Management System for Auto Parts Store

## Overview

This is a full-stack inventory management system built for an auto parts store called "Simi Motos". The application allows users to track parts inventory, register sales, monitor stock levels, and receive alerts for low/critical stock situations. It features a modern React frontend with a clean UI built using shadcn/ui components and a Node.js/Express backend with PostgreSQL database integration.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React with TypeScript using Vite as the build tool
- **UI Library**: shadcn/ui components built on top of Radix UI primitives
- **Styling**: Tailwind CSS with CSS variables for theming support (light/dark modes)
- **State Management**: TanStack Query (React Query) for server state management
- **Routing**: Wouter for lightweight client-side routing
- **Form Handling**: React Hook Form with Zod validation resolvers

The frontend follows a component-based architecture with reusable UI components, custom hooks, and page-level components. The application uses a clean separation between presentation components and business logic.

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ES modules
- **Database ORM**: Drizzle ORM for type-safe database operations
- **Validation**: Zod schemas for request/response validation
- **Session Management**: Express sessions with PostgreSQL session store
- **Development**: Hot module replacement with Vite integration

The backend follows a RESTful API design with clear separation of concerns between routes, storage layer, and business logic. It uses an in-memory storage implementation that can be easily replaced with actual database operations.

### Data Storage
- **Database**: PostgreSQL with Neon serverless driver integration
- **ORM**: Drizzle ORM with migrations support
- **Schema**: Two main entities - Parts and Sales with proper foreign key relationships
- **Session Store**: PostgreSQL-backed session storage using connect-pg-simple

The database schema supports parts inventory with stock tracking, sales recording with automatic stock updates, and maintains referential integrity between parts and sales.

### Key Features
- **Inventory Management**: Track parts with codes, prices, current stock, and minimum stock alerts
- **Sales Processing**: Register sales with automatic stock deduction and validation
- **Stock Monitoring**: Real-time alerts for critical (0 stock) and low stock situations
- **Restocking**: Simple interface to add inventory to existing parts
- **Analytics**: Daily sales reporting with totals and transaction history

## External Dependencies

### Core Framework Dependencies
- **@neondatabase/serverless**: Serverless PostgreSQL driver for Neon database
- **drizzle-orm**: TypeScript ORM for database operations
- **drizzle-kit**: CLI tools for database migrations and schema management
- **express**: Web application framework for Node.js
- **connect-pg-simple**: PostgreSQL session store for Express sessions

### Frontend UI Components
- **@radix-ui/***: Comprehensive set of low-level UI primitives (dialogs, dropdowns, forms, etc.)
- **@tanstack/react-query**: Server state management and data fetching
- **tailwindcss**: Utility-first CSS framework
- **class-variance-authority**: Utility for creating variant-based component APIs
- **wouter**: Minimalist routing library for React

### Development Tools
- **vite**: Fast build tool and development server
- **typescript**: Static type checking
- **@replit/vite-plugin-***: Replit-specific development plugins for debugging and cartography

### Validation and Forms
- **zod**: TypeScript-first schema validation
- **react-hook-form**: Performant forms with minimal re-renders
- **@hookform/resolvers**: Validation resolvers for various schema libraries

### Utility Libraries
- **date-fns**: Modern JavaScript date utility library
- **clsx**: Utility for constructing className strings conditionally
- **nanoid**: URL-safe unique string ID generator