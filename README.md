# Brain Brew

**An AI-Powered Socratic Learning Platform**

Brain Brew transforms passive PDF reading into an engaging, interactive learning experience by combining the ancient Socratic method with cutting-edge AI technology. Instead of simply consuming information, students develop critical thinking skills through guided questioning and active learning.

## Overview

Brain Brew addresses a growing challenge in modern education: the over-reliance on AI tools for instant answers rather than deep understanding. Our platform flips this dynamic by using AI as a Socratic tutor that asks thoughtful questions, encouraging students to think critically and discover insights independently.

### Key Benefits

- **Active Learning**: Transform lecture slides into interactive learning sessions
- **Adaptive Difficulty**: Questions automatically adjust based on your performance
- **Critical Thinking**: Develop problem-solving skills through guided discovery
- **Personalized Experience**: AI adapts to your learning pace and understanding level

## Features

### User Authentication & Account Management
- Secure sign up and login powered by Supabase
- Cloud-based PDF storage accessible from anywhere
- Personal dashboard to manage all your learning materials
- Persistent learning progress across sessions

### Intelligent PDF Processing
- Drag-and-drop or browse file upload interface
- Automatic content extraction and analysis using Google Gemini AI
- Smart topic identification from lecture materials
- Support for PDFs up to 10MB
- File management with upload date and topic tracking

### Socratic Learning Experience
- AI-generated questions based on your PDF content
- Four progressive difficulty levels (Basic → Foundational → Intermediate → Advanced)
- Adaptive difficulty system that responds to your performance
- Progressive hint system (up to 3 hints per question)
- Real-time feedback on answer quality
- Performance tracking for continuous improvement

### Voice Input Support
- Speech-to-text for hands-free answer submission
- Natural language processing for conversational interaction
- Cross-browser speech recognition support

### Modern User Interface
- Sleek gradient design with smooth animations
- Interactive LiquidEther background effects
- Responsive layout optimized for desktop learning
- Intuitive navigation between features
- Clean, distraction-free learning environment

## Technology Stack

### Frontend
- **React 18** - Component-based UI architecture
- **TypeScript** - Type-safe development
- **Vite** - Fast build tooling and hot module replacement
- **Tailwind CSS** - Utility-first styling framework
- **React Router** - Seamless client-side navigation
- **React Hot Toast** - User-friendly notifications

### Backend & Services
- **Supabase** - Complete backend infrastructure
  - PostgreSQL database for metadata storage
  - Authentication system for secure user management
  - File storage (1GB free tier)
  - Row-level security for data protection
- **Google Gemini AI** - Advanced AI capabilities
  - PDF content extraction and analysis
  - Socratic question generation
  - Natural language understanding
  - Topic identification

### Additional Libraries
- **Three.js** - 3D graphics and animations
- **Web Speech API** - Voice input functionality

## Getting Started

### Prerequisites
- Node.js 18 or higher
- npm or yarn package manager
- Supabase account ([sign up free](https://supabase.com))
- Google Gemini API key ([get one here](https://makersuite.google.com/app/apikey))

### Installation

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd brain-brew
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Configure Supabase**
   - Follow the setup guide in [SUPABASE_SETUP.md](./SUPABASE_SETUP.md)
   - Create a new Supabase project
   - Set up the database schema and storage bucket
   - Configure Row Level Security policies

4. **Set up environment variables**
   
   Create a `.env` file in the root directory:
   ```env
   VITE_SUPABASE_URL=your_supabase_project_url
   VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
   VITE_GEMINI_API_KEY=your_gemini_api_key
   ```

5. **Start the development server**
   ```bash
   npm run dev
   ```
   
   Access the application at `http://localhost:5173`

## How to Use

1. **Create an Account**: Sign up with your email to get started
2. **Upload Materials**: Upload your lecture PDFs (drag-and-drop or browse)
3. **AI Processing**: Brain Brew automatically analyzes and extracts key topics
4. **Start Learning**: Begin your Socratic learning session with AI-generated questions
5. **Adaptive Learning**: The system adjusts difficulty based on your responses
6. **Track Progress**: Monitor your performance and revisit materials anytime

## Learning Methodology

Brain Brew implements a proven pedagogical approach:

1. **Introduction**: AI provides context about the topic
2. **Questioning**: Thought-provoking questions guide discovery
3. **Feedback**: Constructive responses help refine understanding
4. **Hints**: Progressive hints support learning without giving answers
5. **Explanation**: Comprehensive explanations confirm learning
6. **Adaptation**: Difficulty adjusts to maintain optimal challenge

## Project Structure

```
brain-brew/
├── src/
│   ├── components/          # React components
│   │   ├── Landing.tsx      # Landing page
│   │   ├── Login.tsx        # Authentication
│   │   ├── SignUp.tsx       # User registration
│   │   ├── PDFUpload.tsx    # File upload interface
│   │   ├── LearningInterface.tsx  # Main learning UI
│   │   ├── Dashboard.tsx    # User dashboard
│   │   └── Layout.tsx       # App layout wrapper
│   ├── services/            # Backend integrations
│   │   ├── auth.ts          # Authentication service
│   │   ├── pdfStorage.ts    # File storage service
│   │   └── gemini.ts        # AI service integration
│   ├── contexts/            # React contexts
│   │   └── AuthContext.tsx  # Auth state management
│   ├── lib/                 # Configuration
│   │   └── supabase.ts      # Supabase client
│   └── App.tsx              # Main application
├── SUPABASE_SETUP.md        # Database setup guide
├── brainbrew_overview.pdf   # Project Overview ppt
├── Architecture_daigram.png # Project workings daigram
└── README.md                # This file

```

