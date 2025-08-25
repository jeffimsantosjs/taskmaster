# Overview

This is a comprehensive bakery management system (Sistema de Gestão para Confeitaria) built as a full-stack web application. The system manages a complete bakery workflow from raw materials inventory to order fulfillment, including multi-level stock control, production management, scheduled orders, and financial reporting. It handles the complex relationship between raw materials, recipes, finished products, and packaging while maintaining accurate inventory tracking throughout the production pipeline.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **React + TypeScript** single-page application using Vite as the build tool
- **Tailwind CSS + Radix UI** for styling with a comprehensive design system using CSS custom properties
- **React Hook Form + Zod** for form management and validation
- **TanStack Query** for server state management, caching, and data synchronization
- **Wouter** for client-side routing
- **Component-based architecture** with reusable UI components following shadcn/ui patterns

## Backend Architecture
- **Express.js** server with TypeScript providing RESTful API endpoints
- **Session-based authentication** using Passport.js with local strategy and bcrypt for password hashing
- **Service layer pattern** with dedicated services for production workflows and label generation
- **Storage abstraction layer** providing a clean interface between business logic and database operations

## Database Design
- **PostgreSQL** with Drizzle ORM for type-safe database operations
- **Multi-level inventory system** supporting raw materials, recipes, finished products, and packaging
- **Production workflow tracking** with separate tables for recipe production and product assembly
- **Order management** with customizable items and status tracking
- **Audit trail** through movement history tables

## Key Business Logic
- **Inventory Hierarchy**: Raw materials → Recipes → Products (with packaging)
- **Production Constraints**: Recipe production consumes raw materials; Product production consumes recipes and packaging
- **Order Lifecycle**: Orders don't affect inventory until moved to production status
- **Stock Validation**: Automatic verification before production to prevent overselling

## Authentication & Authorization
- **Role-based access control** with admin and operation user types
- **Session management** with memory store for development (configurable for production)
- **Protected routes** with automatic authentication state management

## External Dependencies

- **@neondatabase/serverless** - PostgreSQL database connection for serverless environments
- **Drizzle ORM** - Type-safe database operations and migrations
- **TanStack Query** - Server state management and caching
- **Radix UI** - Accessible component primitives for forms, dialogs, and data display
- **React Hook Form** - Form state management with validation
- **Zod** - Runtime type validation and schema definition
- **Passport.js** - Authentication middleware with local strategy
- **bcryptjs** - Password hashing and verification
- **express-session** - Session management for user authentication