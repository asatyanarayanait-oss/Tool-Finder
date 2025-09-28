# Tool Finder - Smart Tool Recommendation Platform

![Tool Finder Logo](https://img.shields.io/badge/Tool%20Finder-AI%20Powered-8b5cf6?style=for-the-badge&logo=lightbulb)

## Project Overview

Tool Finder is an AI-powered smart tool recommendation platform designed to eliminate tool discovery fatigue for students, researchers, and knowledge workers. The application leverages Google's Gemini 2.5 Flash API with search grounding to provide personalized, evidence-backed tool recommendations based on specific user requirements.

## 🎯 Problems Solved

- **Tool Discovery Fatigue**: Eliminates hours spent researching options manually
- **Decision Paralysis**: Provides clear, ranked recommendations with confidence scores
- **Wasted Resources**: Prevents time and money spent on unsuitable tools
- **Trial and Error**: Offers use-case specific recommendations

## 👥 Target Users

- 📚 **Students**: Finding academic and productivity tools within budget constraints
- 🔬 **Researchers**: Discovering specialized research software and analysis tools
- 💼 **Knowledge Workers**: Selecting professional tools for specific business tasks
- 🚀 **Startups**: Making informed tool decisions for growing teams

## 🚀 Key Features

### Core Functionality
- ✨ **AI-Powered Recommendations**: Intelligent matching using Google Gemini API
- 🔍 **Smart Search Grounding**: Real-time search integration for accuracy
- 📊 **Confidence Scoring**: Transparent quality metrics (0-100%)
- 💰 **Budget-Aware Filtering**: Recommendations within specified price ranges
- 🔐 **Privacy-First Options**: GDPR compliant and local/on-premise solutions
- 📱 **Progressive Web App**: Offline functionality and native app experience

## 🛠️ Technical Stack

### Backend Technologies
- **Runtime**: Node.js 14+ with Express.js 4.18.2
- **Database**: SQLite3 5.1.6 with foreign key constraints
- **Authentication**: express-session + bcryptjs (12 salt rounds)
- **Security**: helmet, CORS, express-rate-limit, input validation
- **AI Integration**: Google Gemini 2.5 Flash API with real-time search
- **API**: RESTful endpoints with comprehensive error handling

### Frontend Technologies
- **Core**: HTML5, CSS3, JavaScript ES6+ with modern APIs
- **Styling**: Tailwind CSS 3.x with custom animations
- **Icons**: Font Awesome 6.4.0 for consistent iconography
- **PWA**: Service Worker, Web App Manifest, offline caching
- **Animations**: CSS keyframes, transforms, and transitions

### Infrastructure & DevOps
- **Containerization**: Docker with multi-stage builds
- **Orchestration**: Docker Compose with health checks
- **Environment**: dotenv for configuration management
- **Process Management**: PM2 ready for production deployment
- **Database**: Automatic schema migration and initialization

## 📦 Installation & Setup

### Prerequisites
- **Node.js**: Version 14.0.0 or higher ([Download](https://nodejs.org/))
- **npm**: Comes with Node.js installation
- **Google Gemini API Key**: Required for AI functionality ([Get API Key](https://makersuite.google.com/app/apikey))

### 🚀 Quick Start Guide

#### Option 1: Automated Setup (Recommended)

**Windows:**
```batch
# Navigate to project directory and run:
start.bat
```

**Unix/Linux/macOS:**
```bash
# Make script executable and run:
chmod +x start.sh
./start.sh
```

The startup scripts automatically:
- ✅ Verify Node.js installation and version
- ✅ Install all required dependencies
- ✅ Create database directory structure
- ✅ Initialize SQLite database with proper schema
- ✅ Generate default environment configuration
- ✅ Start the development server

#### Option 2: Manual Installation

```bash
# 1. Install dependencies
npm install

# 2. Initialize database
npm run init-db

# 3. Create environment file
cp .env.example .env
# Edit .env file with your settings

# 4. Start the application
npm start        # Production mode
npm run dev      # Development mode with nodemon
```

### 🔧 Environment Configuration

Create a `.env` file in the project root:

```env
# Application Settings
NODE_ENV=development
PORT=3000
FRONTEND_URL=http://localhost:3000

# Security Configuration
SESSION_SECRET=change-this-secure-key-in-production
BCRYPT_ROUNDS=12

# Database Configuration
DB_PATH=./database/tool-finder.db

# Optional: Global Gemini API Key
# GEMINI_API_KEY=your-api-key-here
```

### 🐳 Docker Deployment

```bash
# Build and run with Docker Compose
docker-compose up --build

# Run in background
docker-compose up -d

# View logs
docker-compose logs -f

# Stop services
docker-compose down
```

### 🌐 Accessing the Application

1. Open your browser and navigate to `http://localhost:3000` or the port it is hosted on
2. Create a new account or login
3. Configure your Gemini API key in the dashboard
4. Start getting AI-powered tool recommendations!

## 🏗️ Architecture Overview

```mermaid
graph TB
    subgraph "Client Layer"
        A[Progressive Web App]
        B[Service Worker]
        C[Local Storage]
    end
    
    subgraph "Server Layer"
        D[Express.js Server]
        E[Authentication Middleware]
        F[Rate Limiting]
        G[Security Headers]
    end
    
    subgraph "Data Layer"
        H[SQLite Database]
        I[Session Store]
        J[Search History]
    end
    
    subgraph "External Services"
        K[Google Gemini API]
        L[Real-time Search]
    end
    
    A --> D
    B --> C
    D --> E
    E --> F
    F --> G
    G --> H
    D --> K
    K --> L
    H --> I
    H --> J
```
 ## Disclaimer
 
 This is a prototype that is build for eureka juniors by abhiram(with the registered email "a.m.s.s.abhiram492@gmail.com) who is part of the "Abhi's Team" with team id:EJ25T518480.
