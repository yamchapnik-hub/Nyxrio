# Overview

This is a modern full-stack e-commerce web application for "Nyxrio," a streetwear brand. The application is built as a monorepo with a React frontend and Express.js backend, featuring a sleek dark-themed UI for showcasing urban fashion products. The app includes product browsing, shopping cart functionality, customer testimonials, brand storytelling, and newsletter subscription features.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **Framework**: React 18 with TypeScript using Vite as the build tool
- **UI Framework**: shadcn/ui components built on Radix UI primitives with Tailwind CSS for styling
- **Routing**: Wouter for client-side routing (lightweight React router alternative)
- **State Management**: TanStack Query (React Query) for server state management
- **Styling**: Tailwind CSS with custom CSS variables for theming, featuring a dark mode design with purple accent colors
- **Forms**: React Hook Form with Zod validation via @hookform/resolvers
- **Animations**: Framer Motion for component animations and transitions

## Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ES modules
- **Development**: tsx for TypeScript execution in development
- **Production Build**: esbuild for bundling the server code
- **API Design**: RESTful API structure with `/api` prefix routing
- **Middleware**: Custom logging middleware for API request tracking
- **Error Handling**: Centralized error handling with proper HTTP status codes

## Data Storage Solutions
- **Database**: PostgreSQL with Drizzle ORM for type-safe database operations
- **Database Provider**: Neon Database (serverless PostgreSQL)
- **Schema Management**: Drizzle Kit for migrations and schema management
- **Connection**: @neondatabase/serverless driver for database connectivity
- **Fallback Storage**: In-memory storage implementation for development/testing

## Database Schema
- **Products Table**: Comprehensive product catalog with pricing, categories, variants (colors/sizes), ratings, and inventory status
- **Cart Items Table**: Shopping cart persistence with product references, quantities, and variant selections
- **Schema Validation**: Zod schemas generated from Drizzle table definitions for runtime type safety

## Development and Build Setup
- **Development Server**: Concurrent Express server with Vite dev server integration
- **Hot Module Replacement**: Vite HMR for fast development iteration
- **Static Serving**: Vite-generated static assets served in production
- **TypeScript Configuration**: Shared TypeScript config across client, server, and shared modules
- **Path Aliases**: Configured path mapping for clean imports (@, @shared, @assets)

## UI Component System
- **Design System**: shadcn/ui with "new-york" style variant
- **Component Library**: Comprehensive set including forms, navigation, cards, dialogs, and data display components
- **Accessibility**: Built on Radix UI primitives ensuring WCAG compliance
- **Responsive Design**: Mobile-first approach with Tailwind's responsive utilities
- **Dark Theme**: Consistent dark mode implementation with CSS custom properties

# External Dependencies

## Database Services
- **Neon Database**: Serverless PostgreSQL hosting with connection pooling
- **Drizzle ORM**: Type-safe database toolkit with PostgreSQL support

## UI and Styling
- **Radix UI**: Unstyled, accessible UI primitives for complex components
- **Tailwind CSS**: Utility-first CSS framework with PostCSS processing
- **Lucide React**: Modern icon library for consistent iconography
- **React Icons**: Additional icon collections (Simple Icons for social media)
- **Framer Motion**: Animation library for smooth transitions and interactions

## Development Tools
- **Vite**: Fast build tool with React plugin and runtime error overlay
- **Replit Integration**: Development environment integration with cartographer plugin
- **TypeScript**: Static type checking across the entire application
- **ESBuild**: Fast JavaScript bundler for production builds

## Form and Validation
- **React Hook Form**: Performant form library with minimal re-renders
- **Zod**: Schema validation library for runtime type safety
- **@hookform/resolvers**: Integration between React Hook Form and Zod

## Data Fetching
- **TanStack Query**: Server state management with caching, background updates, and error handling
- **Fetch API**: Native browser API for HTTP requests with custom wrapper functions

## Fonts and Assets
- **Google Fonts**: Inter, DM Sans, Fira Code, Geist Mono, and Architects Daughter font families
- **Unsplash**: External image hosting for product and promotional imagery