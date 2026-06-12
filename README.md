# SkillRoom

VOICAHIRE
Project Summary

VoicaHire is an AI-powered recruitment and candidate assessment platform designed to automate hiring workflows through voice interviews, multilingual communication, assessments, ATS integration, and candidate management.

The platform combines conversational AI, speech processing, candidate tracking, assessment management, and cloud deployment infrastructure to create a complete recruitment ecosystem.

Project Objectives
Automate candidate screening
Conduct AI-driven voice interviews
Support multilingual communication
Integrate with Applicant Tracking Systems (ATS)
Manage assessments and evaluations
Improve recruitment efficiency
Reduce manual recruiter workload
Enable scalable hiring processes
System Architecture
Candidate
    │
    ▼
Frontend (React)
    │
    ▼
Backend APIs (Node.js + Express)
    │
 ┌──┴─────────────┐
 ▼                ▼
MongoDB         Redis
 │
 ▼
AI Services
 │
 ├── Whisper
 ├── Groq LLM
 ├── Twilio
 └── Exotel
 │
 ▼
Interview Results
 │
 ▼
Recruiter Dashboard
Technology Stack



echnology	Category	Role in Project
React.js	Frontend	User interface development
Vite	Frontend Build Tool	Fast development and build
JavaScript (JSX)	Programming Language	Frontend application logic
Tailwind CSS	Styling Framework	Responsive UI styling
CSS3	Styling	Component and page styling
HTML5	Markup Language	Web page structure
Context API	State Management	Global state handling
Axios	API Client	Backend communication
ESLint	Code Quality	Code linting and standards
Node.js	Backend Runtime	Server-side execution
Express.js	Backend Framework	REST API development
MongoDB	Database	Persistent data storage
Redis	Cache Database	Fast temporary storage
Groq LLM	Artificial Intelligence	AI interview generation
Whisper	Speech Processing	Speech-to-text conversion
Twilio	Communication Service	Phone interview handling
Exotel	Communication Service	Voice calling workflows
Docker	Containerization	Application packaging
Docker Compose	Orchestration	Multi-service management
AWS ECS	Cloud Deployment	Container deployment
AWS Mumbai Region	Cloud Infrastructure	Application hosting
Nginx	Reverse Proxy	Request routing
JSON	Data Format	Data exchange
REST API	Communication Architecture	Frontend-backend interaction
Local Storage	Browser Storage	Theme persistence
Git	Version Control	Source code management
GitHub	Repository Hosting	Code collaboration
npm	Package Manager	Dependency management
Yarn	Package Manager	Alternative dependency management
PostCSS	CSS Processing	CSS transformation
Dockerfile	Container Configuration	Image creation
Environment Variables (.env)	Configuration	Secure application settings




Frontend Technologies
React.js

Purpose:

User Interface Development
Component-based architecture
State management

Used For:

Candidate Portal
Dashboard
Interview UI
Assessment Screens
Vite

Purpose:

Fast frontend build system
Development server

Benefits:

Fast reloads
Optimized builds
Tailwind CSS

Purpose:

UI Styling

Benefits:

Utility-first styling
Responsive design
Faster UI development
Context API

Purpose:

Global state management

Used For:

Theme management
Shared application state
Axios

Purpose:

API communication

Used For:

Frontend ↔ Backend requests
Backend Technologies
Node.js

Purpose:

Backend runtime environment

Responsibilities:

Business logic
API execution
Service integration
Express.js

Purpose:

Backend API framework

Responsibilities:

Route handling
Request processing
Middleware execution
Database Technologies
MongoDB

Purpose:

Primary Database

Stores:

Candidates
Assessments
Interview Data
Recruiter Information
Redis

Purpose:

Caching Layer

Benefits:

Faster responses
Reduced database load
Temporary data storage
AI Technologies
Groq LLM

Purpose:

AI Interview Engine

Responsibilities:

Question generation
Candidate interaction
Response analysis
Conversation flow
Whisper

Purpose:

Speech-To-Text

Responsibilities:

Voice transcription
Audio processing
Language support
Communication Technologies
Twilio

Purpose:

Voice calling infrastructure

Used For:

Phone interviews
Voice communication
Exotel

Purpose:

Telephony integration

Used For:

Candidate calling workflows
Interview calls
DevOps Technologies
Docker

Purpose:

Containerization

Benefits:

Environment consistency
Easy deployment
Docker Compose

Purpose:

Multi-container management

Used For:

Frontend
Backend
Database
Redis
AWS ECS

Purpose:

Container deployment

Benefits:

Scalable infrastructure
Cloud hosting
Nginx

Purpose:

Reverse Proxy

Responsibilities:

Request routing
Traffic handling
Production serving
Complete Project Structure
voicahire-beta/

├── Backend/
│
├── docs/
│
├── Frontend/
│   │
│   ├── public/
│   │   ├── images/
│   │   ├── favicon.ico
│   │   └── index.html
│   │
│   ├── src/
│   │   │
│   │   ├── assets/
│   │   ├── components/
│   │   ├── context/
│   │   ├── hooks/
│   │   ├── pages/
│   │   ├── services/
│   │   ├── utils/
│   │   │
│   │   ├── App.jsx
│   │   ├── App.css
│   │   ├── index.css
│   │   └── main.jsx
│   │
│   ├── Dockerfile
│   ├── package.json
│   ├── vite.config.js
│   ├── tailwind.config.js
│   └── eslint.config.js
│
├── nginx/
├── scripts/
│
├── docker-compose.yml
├── docker-compose.mumbai.yml
│
├── aws-ecs-task-definition.json
├── aws-multilingual-whisper-task.json
├── aws-mumbai-config.env
│
├── FEATURES.md
├── NextFeatures.md
├── PROJECT_STRUCTURE.md
├── README.md
└── setup.bat
Frontend Components
Assessment Module
AssessmentAssignment.jsx

Responsibilities:

Assign assessments
Candidate mapping
Assessment scheduling
AssessmentDashboard.jsx

Responsibilities:

Assessment monitoring
Performance tracking
Assessment overview
AssessmentTaker.jsx

Responsibilities:

Candidate assessment interface
Question handling
Submission process
ATS Integration
ATSIntegrationDashboard.jsx

Responsibilities:

ATS connectivity
Candidate synchronization
Recruitment workflow integration
Candidate Management
CandidateCard.jsx

Responsibilities:

Candidate display
Candidate summary
CandidatePortalAccess.jsx

Responsibilities:

Portal permissions
Candidate access management
CommunicationPreferences.jsx

Responsibilities:

Notification settings
Communication channels
Voice Interview Components
VoiceSimulator.jsx

Responsibilities:

Voice interview simulation
Conversation handling
LanguageSelector.jsx

Responsibilities:

Multilingual support
Language switching
OmnichannelTimeline.jsx

Responsibilities:

Communication history
Interaction timeline
Utility Components
Navbar.jsx

Application Navigation

Footer.jsx

Footer Interface

ThemeToggle.jsx

Theme Switching

Loader.jsx

Loading UI

ErrorBoundary.jsx

Application Error Handling

BackButton.jsx

Navigation Control

Theme Management Flow

File:

src/context/ThemeContext.jsx

Responsibilities:

Create Theme Context
Store theme state
Persist theme using localStorage
Enable dark mode
Enable light mode

Flow:

Application Start
        │
        ▼
Read Theme
from LocalStorage
        │
        ▼
Apply Theme
        │
        ▼
User Toggles Theme
        │
        ▼
Update State
        │
        ▼
Save to LocalStorage
Browser Interview Flow
Candidate Opens Website
          │
          ▼
Language Selection
          │
          ▼
Voice Simulator Starts
          │
          ▼
Microphone Input
          │
          ▼
Whisper Transcription
          │
          ▼
Groq Processing
          │
          ▼
AI Generates Question
          │
          ▼
Candidate Response
          │
          ▼
Repeat Until Completion
Phone Interview Flow
Candidate Receives Call
          │
          ▼
Twilio / Exotel
          │
          ▼
Voice Stream
          │
          ▼
Whisper
          │
          ▼
Text Conversion
          │
          ▼
Groq AI Processing
          │
          ▼
AI Response
          │
          ▼
Voice Output
          │
          ▼
Interview Continues
Assessment Workflow
Recruiter
     │
     ▼
Create Assessment
     │
     ▼
Assign Assessment
     │
     ▼
Candidate Takes Assessment
     │
     ▼
Submit Responses
     │
     ▼
Dashboard Evaluation
     │
     ▼
Result Analysis
Candidate Workflow
Candidate Registration
          │
          ▼
Portal Access
          │
          ▼
Profile Creation
          │
          ▼
Communication Setup
          │
          ▼
Interview / Assessment
          │
          ▼
Result Tracking
AI Workflow
Voice Input
      │
      ▼
Whisper
(Speech → Text)
      │
      ▼
Groq LLM
(AI Reasoning)
      │
      ▼
Generated Response
      │
      ▼
Candidate Interaction
Deployment Architecture
Frontend
    │
    ▼
Nginx
    │
    ▼
Backend APIs
    │
 ┌──┴─────┐
 ▼        ▼
MongoDB Redis
    │
    ▼
AWS ECS Containers
Key Learnings From This Project
React Component Architecture
Context API State Management
AI-Powered Interview Systems
Voice Processing Workflows
Whisper Integration
Groq LLM Integration
ATS Integration Concepts
Docker Deployment
AWS ECS Deployment
Redis Caching
Production Infrastructure
Candidate Lifecycle Management
Assessment Management Systems
Project Outcome

VoicaHire demonstrates the implementation of a scalable AI-driven recruitment platform capable of managing candidate interviews, multilingual voice communication, assessments, ATS integrations, and cloud-native deployment workflows using modern full-stack technologies.
