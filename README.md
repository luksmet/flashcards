# AI Flashcard Learning Platform

A web-based educational tool that leverages AI to streamline the creation and study of flashcards, designed to help high school students prepare for tests efficiently using proven spaced repetition methodology.

## Table of Contents

- [Project Description](#project-description)
- [Tech Stack](#tech-stack)
- [Getting Started Locally](#getting-started-locally)
- [Available Scripts](#available-scripts)
- [Project Scope](#project-scope)
- [Project Status](#project-status)
- [License](#license)

## Project Description

The AI Flashcard Learning Platform is designed to solve the problem of time-consuming manual flashcard creation that discourages students from using effective study methods like spaced repetition. 

### Key Features

- **AI-Powered Flashcard Generation**: Generate high-quality flashcards from user-provided text (150-15,000 characters)
- **Google Authentication**: Secure sign-in using Google OAuth
- **Deck Management**: Create and organize flashcards into named decks
- **Flashcard Review System**: Review, edit, accept, or reject AI-generated cards before adding them to your deck
- **Manual Card Creation**: Create flashcards manually when needed
- **Spaced Repetition Study Sessions**: Study using the proven Leitner system for optimal learning
- **Progress Tracking**: View performance summaries after study sessions

### Target Users

Primarily high school students (ages 13+) seeking an efficient way to prepare for tests by combining AI-assisted content generation with spaced repetition methodology.

## Tech Stack

### Frontend
- **Astro 5** - Fast, efficient website framework with minimal JavaScript
- **React 19** - Interactive components where needed
- **TypeScript 5** - Static typing and enhanced IDE support
- **Tailwind CSS 4** - Utility-first CSS framework for styling
- **Shadcn/ui** - Accessible React component library for UI elements

### Backend
- **Supabase** - Comprehensive backend-as-a-service solution
  - PostgreSQL database
  - Built-in user authentication
  - SDK for seamless integration
  - Open source with self-hosting options

### AI Integration
- **Openrouter.ai** - AI service providing access to multiple models
  - Support for OpenAI, Anthropic, Google, and other providers
  - Financial limits and cost optimization
  - High efficiency and flexibility

### CI/CD and Hosting
- **GitHub Actions** - Automated CI/CD pipelines
- **DigitalOcean** - Application hosting via Docker containers

## Getting Started Locally

### Prerequisites

- Node.js version 22.14.0 (specified in `.nvmrc`)
- npm or yarn package manager
- Git

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd flashcards
   ```

2. **Install Node.js version**
   ```bash
   # If using nvm
   nvm use
   # Or install Node.js 22.14.0 manually
   ```

3. **Install dependencies**
   ```bash
   npm install
   ```

4. **Set up environment variables**
   ```bash
   # Copy environment template (create if needed)
   cp .env.example .env.local
   # Configure your Supabase and Openrouter.ai credentials
   ```

5. **Start the development server**
   ```bash
   npm run dev
   ```

The application will be available at `http://localhost:4321` (default Astro port).

## Available Scripts

| Script | Description |
|--------|-------------|
| `npm run dev` | Start the development server |
| `npm run build` | Build the application for production |
| `npm run preview` | Preview the production build locally |
| `npm run astro` | Run Astro CLI commands |
| `npm run lint` | Run ESLint to check for code issues |
| `npm run lint:fix` | Run ESLint and automatically fix issues |
| `npm run format` | Format code using Prettier |

## Project Scope

### Included Features (MVP)

- **Authentication**: Google Sign-In integration
- **Deck Management**: Create and view named flashcard decks
- **AI Generation**: Generate flashcards from text input with monthly limits per user
- **Card Review**: Edit, accept, or reject AI-generated cards before saving
- **Manual Creation**: Create flashcards manually with question/answer format
- **Study Sessions**: Spaced repetition using the Leitner system
- **Progress Tracking**: Session summaries showing performance metrics

### Current Limitations

The following features are **not included** in the MVP scope:

- Custom repetition algorithms (Leitner system only)
- File imports (text input only)
- Deck sharing between users
- Native mobile applications (web-responsive only)
- Administrative UI panel
- Sub-decks, deck renaming, or deck deletion
- Bulk "Accept All" / "Reject All" actions for generated cards

### Success Metrics

- **AI Flashcard Acceptance Rate**: Target 75% (accepted cards / total generated cards)
- **AI Usage Rate**: Target 75% (AI-generated cards / total created cards)

## Project Status

🚧 **Development Phase** - MVP (Minimum Viable Product)

This project is currently in active development, focusing on core functionality for the MVP release. The platform is designed to validate the AI-assisted flashcard generation concept and spaced repetition learning methodology.

### Development Priorities

1. Core AI flashcard generation functionality
2. User authentication and deck management
3. Spaced repetition study system implementation
4. Performance optimization and user experience refinements

## License

License information not specified. Please contact the project maintainers for licensing details.

---

**Contributing**: This project follows clean code practices with ESLint and Prettier configuration. Please run `npm run lint:fix` and `npm run format` before submitting contributions.

**Support**: For questions or issues, please refer to the project documentation or create an issue in the repository.
