# Overview

TasksIQ is a mobile-first task management application designed for teams with role-based access control. The system supports both administrators who can create and assign tasks, and team members who can view and manage their assigned tasks. The app features an intuitive UI flow with authentication via OTP, role-based dashboards, and real-time task management capabilities.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **Framework**: React with TypeScript using Vite for build tooling
- **Routing**: Wouter for lightweight client-side routing
- **State Management**: Zustand for auth state with persistence
- **UI Components**: Shadcn/ui components built on Radix UI primitives
- **Styling**: Tailwind CSS with custom CSS variables for theming
- **Data Fetching**: TanStack React Query for server state management

## Backend Architecture
- **Framework**: Express.js with TypeScript
- **Database**: PostgreSQL with Drizzle ORM for type-safe database operations
- **API Pattern**: RESTful endpoints with role-based access control
- **Development Setup**: Vite middleware integration for full-stack development

## Database Schema Design
- **Users Table**: Stores user information with role-based access (admin/team_member)
- **Projects Table**: Organizes tasks into projects with admin ownership
- **Tasks Table**: Core entity with status tracking (pending, accepted, in_progress, completed, cancelled)
- **Team Members Table**: Junction table for project-user relationships
- **Task Comments**: Supports task collaboration through comments
- **Notifications**: System for task-related alerts and updates

## Authentication & Authorization
- **OTP-based Authentication**: Email/phone verification without traditional passwords
- **Role-based Access Control**: Separate workflows for admins and team members
- **Session Management**: Persistent auth state with automatic role-based routing
- **Mock Implementation**: Development-friendly OTP system (fixed code: 123456)

## Mobile-First Design
- **Responsive Layout**: Optimized for mobile devices with desktop compatibility
- **Touch-Friendly UI**: Large buttons, bottom navigation, and gesture-friendly interactions
- **Progressive Web App Ready**: Structured for PWA conversion with proper viewport settings

## Development Tools
- **Type Safety**: End-to-end TypeScript with shared schema validation using Zod
- **Code Quality**: ESLint and Prettier integration (implied by setup)
- **Hot Reload**: Vite HMR for rapid development cycles
- **Error Handling**: Runtime error overlay for development debugging

# External Dependencies

## Database & ORM
- **Neon Database**: Serverless PostgreSQL database via `@neondatabase/serverless`
- **Drizzle ORM**: Type-safe database toolkit with `drizzle-orm` and `drizzle-kit`
- **PostgreSQL Session Store**: `connect-pg-simple` for session management

## UI Framework & Components
- **Radix UI**: Comprehensive primitive components for accessible UI
- **Tailwind CSS**: Utility-first CSS framework for styling
- **Lucide React**: Icon library for consistent iconography
- **Class Variance Authority**: Type-safe CSS class composition

## State Management & Data Fetching
- **TanStack React Query**: Server state management and caching
- **Zustand**: Lightweight state management for client state
- **React Hook Form**: Form management with validation
- **Zod**: Schema validation for type-safe data handling

## Development & Build Tools
- **Vite**: Fast build tool and development server
- **TypeScript**: Type safety across the entire stack
- **ESBuild**: Fast bundling for production builds
- **Replit Integration**: Development environment optimizations

## Authentication & Utilities
- **Date-fns**: Date manipulation and formatting
- **clsx & tailwind-merge**: Conditional CSS class management
- **Wouter**: Minimalist client-side routing
- **cmdk**: Command palette functionality (future feature)