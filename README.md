# Movie Tracker - Full-Stack Application

**Live Demo:** [movies.am-tech.cloud](https://movies.am-tech.cloud)

## Overview

Movie Tracker is a production-grade, full-stack web application that enables users to discover, track, and analyze their movie and TV show watching habits. Built with modern technologies and best practices, this application demonstrates proficiency in end-to-end development, from database design to responsive frontend implementation.

The platform integrates real-time data from The Movie Database (TMDB) API with a custom user analytics engine, providing personalized insights and statistics based on viewing patterns.

## Key Features

### Advanced Search & Discovery
- Multi-parameter filtering system supporting genre, release year, rating range, and content type
- Person-based search enabling discovery by actors, directors, and producers
- Curated collection browsing (Marvel Cinematic Universe, DC Extended Universe, Star Wars, etc.)
- Real-time search with intelligent debouncing for optimal performance
- Six sorting algorithms (popularity, rating, release date, revenue)
- Pagination handling for large result sets

### User Analytics Dashboard
- Comprehensive viewing statistics including total watch time and average ratings
- Genre distribution visualization with preference analysis
- Rating pattern analysis revealing user tendencies
- 12-week activity trends with week-over-week comparisons
- Year-over-year growth tracking
- Top-rated content showcase
- Favorite actors identification based on viewing frequency

### Content Management
- Personal watchlist with categorization by movies and TV shows
- Watched list with 1-10 rating scale and optional commentary
- Quick-action buttons for seamless list management
- Real-time synchronization across devices

### Authentication & User Experience
- Secure JWT-based authentication system
- Guest mode for exploring the platform without registration
- Session persistence and automatic token refresh
- Mobile-first responsive design with breakpoint optimization

## Technical Implementation

### Backend Architecture
**Framework:** FastAPI (Python 3.9+)
- High-performance async request handling with motor (async MongoDB driver)
- RESTful API design with comprehensive OpenAPI documentation
- Pydantic schemas for request/response validation
- JWT token generation and verification with python-jose
- Bcrypt password hashing for security
- CORS middleware for secure cross-origin requests

**Database:** MongoDB Atlas
- Document-based schema optimized for user data and content relationships
- Indexed queries for fast lookups
- Aggregation pipelines for complex analytics calculations

**External Integration:** TMDB API
- Custom service layer for API abstraction
- Rate limiting and error handling
- Image optimization and CDN integration

### Frontend Architecture
**Core Technologies:**
- React 18 with TypeScript for type-safe component development
- Vite build tool for fast HMR and optimized production builds
- React Router v6 for client-side routing

**State Management:**
- Zustand for lightweight global state (authentication)
- TanStack React Query for server state management, caching, and background refetching
- Custom hooks for reusable logic (useDebounce)

**UI/UX:**
- Tailwind CSS for utility-first styling
- shadcn/ui component library
- Lucide React for consistent iconography
- Custom loading skeletons for perceived performance
- Smooth transitions and hover effects

**Performance Optimizations:**
- Lazy loading for route-based code splitting
- Debounced search inputs to reduce API calls
- React Query cache management for reduced network requests
- Optimized re-renders with proper memoization

### Design System
Custom dark theme featuring:
- Primary colors: Deep blue gradient (#00406c, #00253e)
- Accent: Vibrant purple (#8b5cf6) for interactive elements
- High contrast ratios for accessibility
- Consistent spacing and typography scale
- Glassmorphism effects on elevated surfaces

## API Architecture

The application exposes 20+ RESTful endpoints organized into logical domains:

**Authentication:** User registration, login, and session management
**Content Discovery:** Trending content, popular movies/TV shows, detailed information
**Advanced Search:** Multi-criteria filtering, person search, genre listings, collections
**User Data:** Watchlist management, rating system, comment storage
**Analytics:** Statistical aggregations, trend calculations, preference analysis

All endpoints are documented with interactive Swagger UI and include request/response schemas, authentication requirements, and example payloads.

## Security Measures

- Password hashing with bcrypt and secure salt generation
- JWT tokens with configurable expiration
- Input validation on all endpoints using Pydantic models
- MongoDB query injection prevention
- Environment-based configuration (no hardcoded secrets)
- CORS policy enforcement
- HTTPS enforcement in production

## Deployment & DevOps

**Production Environment:**
- VPS deployment with process management
- Environment variable configuration
- Database hosted on MongoDB Atlas with automated backups
- Frontend served with optimized static assets
- CDN integration for TMDB images

**Development Workflow:**
- TypeScript for compile-time error detection
- ESLint for code quality enforcement
- Git version control with conventional commits
- Separate development and production configurations

## Future Enhancements

### AI-Powered Recommendation Engine
Development of a hybrid recommendation system combining:
- **Content-Based Filtering:** Analyzing genre preferences, rating patterns, and actor affinities to suggest similar content
- **Collaborative Filtering:** Leveraging user behavior patterns to identify like-minded viewers and recommend their highly-rated content
- **Natural Language Processing:** Implementing semantic search to understand user intent in natural language queries
- **Sentiment Analysis:** Analyzing user comments to refine recommendation weights
- **Personalized Dashboard:** Dynamic content curation based on viewing history and predicted preferences

### Additional Planned Features
- Social features including list sharing and collaborative watchlists
- Export functionality for analytics and watchlist data
- Email notifications for new content from favorite actors/directors
- Theme customization options
- Advanced data visualizations with D3.js or Chart.js

## Technical Highlights for AI Engineering

This project demonstrates core competencies relevant to AI engineering roles:

- **Data Processing:** Aggregation pipelines for analytics mirror data preprocessing workflows
- **API Integration:** Experience consuming and processing third-party APIs, essential for LLM and ML service integration
- **Full-Stack Development:** End-to-end ownership from database to UI, crucial for deploying AI applications
- **Performance Optimization:** Caching strategies and async operations applicable to AI inference systems
- **User Analytics:** Statistical analysis and pattern recognition foundational for recommendation systems

The planned AI recommendation engine will showcase machine learning implementation, model deployment, and real-time inference in a production environment.

---

**Tech Stack Summary:** React · TypeScript · Python · FastAPI · MongoDB · TMDB API · JWT · Tailwind CSS · Zustand · React Query · Vite

**Status:** Production-ready application deployed and accessible at [movies.am-tech.cloud](https://movies.am-tech.cloud)
