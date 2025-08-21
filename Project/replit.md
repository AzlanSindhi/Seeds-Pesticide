# FarmBasket E-commerce Platform

## Overview

FarmBasket is a comprehensive agricultural e-commerce platform built for managing and selling agricultural products like seeds and pesticides. The application features a multi-module architecture supporting three distinct user roles: customers, administrators, and suppliers. Built with modern web technologies, it provides a full-stack solution for agricultural product management, ordering, and inventory tracking.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript using Vite as the build tool
- **UI Library**: Shadcn/ui component library with Radix UI primitives
- **Styling**: Tailwind CSS with custom CSS variables for theming
- **Routing**: Wouter for client-side routing with role-based page organization
- **State Management**: TanStack Query (React Query) for server state management
- **Forms**: React Hook Form with Zod validation

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ES modules
- **API Design**: RESTful API with organized route handlers
- **Database ORM**: Drizzle ORM with type-safe queries
- **Development**: Hot reload with Vite integration during development

### Database Design
- **Database**: PostgreSQL with connection pooling
- **Schema**: Relational design with the following core entities:
  - Users (customers, admins, suppliers)
  - Products (seeds, pesticides)
  - Orders and Order Items
  - Cart Items
- **Type Safety**: Drizzle Zod integration for runtime validation

### Module Organization
The application is organized into three distinct modules:

1. **Customer Module**: Product browsing, cart management, and order placement
2. **Admin Module**: Dashboard, product management, order tracking, and analytics
3. **Supplier Module**: Inventory management, product creation, and order fulfillment

### Authentication & Authorization
- Role-based access control with three user types (customer, admin, supplier)
- Session-based authentication (infrastructure for connect-pg-simple sessions)

### Development Workflow
- **Build Process**: Vite for frontend bundling, esbuild for backend compilation
- **Type Checking**: Shared TypeScript configuration across client, server, and shared modules
- **Database Migrations**: Drizzle Kit for schema management

## External Dependencies

### Core Framework Dependencies
- **@neondatabase/serverless**: Neon serverless PostgreSQL driver for database connectivity
- **drizzle-orm**: Type-safe ORM for database operations
- **express**: Backend web framework
- **react**: Frontend framework with TypeScript support

### UI and Styling
- **@radix-ui/\***: Comprehensive set of accessible UI primitives
- **tailwindcss**: Utility-first CSS framework
- **class-variance-authority**: Component variant management
- **lucide-react**: Icon library

### Development Tools
- **vite**: Build tool and development server
- **tsx**: TypeScript execution for development
- **@replit/vite-plugin-\***: Replit-specific development plugins

### Form and Validation
- **react-hook-form**: Form state management
- **@hookform/resolvers**: Form validation resolvers
- **zod**: Schema validation library

### Database and Storage
- **connect-pg-simple**: PostgreSQL session store
- **drizzle-zod**: Integration between Drizzle ORM and Zod validation

The architecture prioritizes type safety, developer experience, and scalability while maintaining clear separation of concerns between different user roles and system components.