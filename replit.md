# StrobeForge 3D NFT Creator

## Overview

StrobeForge is a 3D strobe light modeling and NFT creation platform that allows users to design custom 3D strobe light models with various visual effects and convert them into NFTs. The application combines a sophisticated 3D builder interface with NFT minting capabilities, providing both creative tools and blockchain integration.

**Current Status**: Premium 3D strobe light creation platform with working core features including shape library (4 primitive shapes), motion controls (6 types), material customization, strobe effects, adaptive animation complexity selector. Completely free model saving with auto-screenshot capture, GLB 3D files, and rich metadata in organized ZIP folders. Enhanced 5-tab interface with Model Naming tab as primary interface and smart contract integration for blockchain projects. All broken features have been removed for optimal stability and performance.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

The application follows a full-stack TypeScript architecture with a clear separation between frontend and backend components:

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **3D Rendering**: Three.js via React Three Fiber for WebGL-based 3D graphics
- **UI Components**: Radix UI components with Tailwind CSS for styling
- **State Management**: Zustand for client-side state management
- **Build Tool**: Vite for fast development and optimized builds

### Backend Architecture
- **Runtime**: Node.js with Express.js REST API
- **Database**: PostgreSQL with Drizzle ORM for type-safe database operations
- **Session Management**: In-memory storage with plans for PostgreSQL sessions
- **File Structure**: Modular route handling with middleware for logging and error handling

## Key Components

### 3D Modeling System
- **DynamicShape**: Advanced 3D geometry system supporting 18+ shape types (primitives + stylized forms)
- **StrobeBuilder**: Main 3D scene with real-time rendering and complex animation patterns
- **PrimitiveShapes**: Comprehensive geometry creation including crystal shards, alien orbs, helix rods
- **ShapeLibrary**: Organized shape selection with Basic, Geometric, and Stylized categories
- **ShapeFeatureControls**: Professional tools for duplication, mirroring, and boolean operations

### Advanced Strobe System  
- **Strobe Effects**: 5 working patterns (pulse, flash, fade, strobe, wave)
- **Motion Integration**: 6 motion types (static, rotateX/Y/Z, orbital, oscillate)
- **Adaptive Animation Complexity**: 4-level performance selector (minimal, balanced, detailed, maximum)
- **Real-time Controls**: Frequency, intensity, and pattern selection with instant visual feedback

### Performance Optimization
- **Animation Complexity Selector**: 4-tier system balancing visual quality with device performance
- **Adaptive Settings**: Auto-adjusts volumetric lighting, bloom effects, and motion smoothness
- **Performance Monitoring**: Real-time feedback on current settings and their impact
- **Device-Responsive**: Optimizes rendering based on selected complexity level

### Shape Validation & Metadata System
- **ShapeMetadata**: Comprehensive metadata for all 18 shapes with NFT compatibility info
- **ShapeValidator**: Performance validation, scaling guidelines, and export readiness checks
- **ShapeAuditPanel**: Real-time shape analysis with performance metrics and optimization suggestions
- **Export Standards**: Standardized GLB, JSON, and IPFS metadata generation for ERC-721 compatibility

### Payment Integration and Monetization
- **Stripe Payment System**: Complete integration with Stripe checkout sessions for premium features
- **Free Model Saving**: Users can save models without payment for local storage
- **Paid Export**: $2.99 charge required for model export operations only
- **Checkout Sessions**: Real-time payment processing with embedded Stripe checkout
- **Payment Success Handling**: Professional confirmation pages and status tracking
- **Secure API Integration**: Using provided Stripe test API key for payment processing
- **Session Management**: Payment status verification and completion handling
- **Revenue Model**: Freemium model with free saving and paid export functionality

### Data Management
- **Models Storage**: Handles CRUD operations for strobe light models with auto-save functionality
- **User Authentication**: Basic authentication system with session management
- **Screenshot System**: Auto-capture and base64 storage of model screenshots with rich metadata
- **Model Naming System**: Dedicated interface for naming and describing models with real-time sync
- **Metadata Integration**: Comprehensive model data including screenshot, timestamp, camera position, lighting setup
- **Free Save Operations**: Instant model saving with integrated screenshot capture and metadata embedding
- **Smart Contract Integration**: Optional contract address linking for NFT minting and blockchain features
- **IPFS Metadata Enrichment**: Automatic fetching and enrichment of collection metadata from IPFS URLs
- **IPFS Link Management**: Dedicated tab for model IPFS address management with history tracking and locking

### UI/UX System
- **Responsive Design**: Mobile-first approach with adaptive layouts
- **Dark Theme**: Cyberpunk-inspired color scheme with neon accents
- **Component Library**: Comprehensive set of reusable UI components
- **State Persistence**: Local storage for user preferences and model drafts
- **4-Tab Interface**: Name, Shape, Motion, IPFS Link tabs (removed non-functional Material and Effects tabs)
- **Model Naming System**: Dedicated naming tab with real-time model info, description fields, and smart naming suggestions
- **Auto-Screenshot Capture**: High-quality screenshot with embedded metadata on every save
- **Enhanced Save Flow**: Free saving with integrated screenshot, metadata, and visual feedback

## Data Flow

1. **Model Naming**: Users start with Name tab to title and describe their creation with real-time model info and quick naming suggestions
2. **Model Creation**: Users interact with 4 primitive shapes through organized 5-tab system
3. **Real-time Rendering**: Advanced strobe patterns with motion controls and material customization applied in real-time
4. **File Generation**: Auto-capture PNG screenshots and generate GLB 3D model files with embedded metadata
5. **State Synchronization**: Enhanced model data with screenshot and metadata flows through Zustand stores
6. **Free Save System**: Instant saving with PNG + GLB file downloads and comprehensive metadata
7. **Export System**: Paid export ($2.99) generates JSON metadata files with full technical specifications

## External Dependencies

### Core Libraries
- **@react-three/fiber**: 3D rendering engine integration
- **@react-three/drei**: Three.js helpers and components
- **@neondatabase/serverless**: PostgreSQL database driver
- **@tanstack/react-query**: Server state management and caching

### UI Framework
- **@radix-ui/***: Comprehensive headless UI component library
- **tailwindcss**: Utility-first CSS framework
- **class-variance-authority**: Type-safe component variants

### Development Tools
- **drizzle-orm**: Type-safe database ORM
- **vite**: Build tool and development server
- **tsx**: TypeScript execution for Node.js

## Deployment Strategy

### Development Environment
- **Hot Module Replacement**: Vite dev server with React Fast Refresh
- **Database Migrations**: Drizzle Kit for schema management
- **Type Checking**: Incremental TypeScript compilation

### Production Build
- **Client Bundle**: Vite production build with code splitting
- **Server Bundle**: esbuild compilation for Node.js deployment
- **Static Assets**: Support for 3D models, textures, and audio files
- **Environment Variables**: DATABASE_URL required for PostgreSQL connection

### Database Schema
- **Users Table**: Basic user authentication and profile data
- **Strobe Models Table**: 3D model properties, materials, and settings
- **NFTs Table**: NFT metadata and blockchain transaction records

The application is designed for cloud deployment with PostgreSQL database hosting, supporting both development and production environments through environment-based configuration.