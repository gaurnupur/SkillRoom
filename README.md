# 🎙️ VoicaHire

## AI-Powered Recruitment & Candidate Assessment Platform

VoicaHire is an AI-powered recruitment and candidate assessment platform designed to automate hiring workflows through voice interviews, multilingual communication, technical assessments, ATS integration, and candidate management.

The platform combines conversational AI, speech processing, candidate tracking, assessment management, and cloud deployment infrastructure to create a complete recruitment ecosystem for modern hiring teams.

---

# 📖 Table of Contents

* Project Overview
* Project Objectives
* Technology Stack
* Key Features
* System Architecture
* Project Structure
* Frontend Components
* Theme Management Flow
* Browser Interview Flow
* Phone Interview Flow
* Assessment Workflow
* Candidate Workflow
* ATS Integration Workflow
* AI Processing Workflow
* Deployment Architecture
* Redis Usage
* AWS Infrastructure
* Production Configuration
* Key Learnings
* Project Outcome

---

# 🚀 Project Overview

VoicaHire streamlines the recruitment process by enabling recruiters to conduct AI-driven interviews, assign technical assessments, manage candidates, and integrate with ATS systems from a single platform.

The platform supports both browser-based interviews and phone interviews while leveraging AI models to generate questions, evaluate responses, and automate candidate screening.

---

# 🎯 Project Objectives

* Automate candidate screening
* Conduct AI-powered voice interviews
* Support multilingual communication
* Integrate with Applicant Tracking Systems (ATS)
* Manage assessments and evaluations
* Improve recruitment efficiency
* Reduce manual recruiter workload
* Enable scalable hiring processes
* Centralize recruitment workflows
* Provide production-ready deployment architecture

---

# 🛠️ Technology Stack

| Technology        | Category                | Role                       |
| ----------------- | ----------------------- | -------------------------- |
| React.js          | Frontend                | User Interface Development |
| Vite              | Build Tool              | Fast Development & Builds  |
| JavaScript (JSX)  | Language                | Application Logic          |
| Tailwind CSS      | Styling                 | Responsive UI Design       |
| CSS3              | Styling                 | Component Styling          |
| HTML5             | Markup                  | Web Page Structure         |
| Context API       | State Management        | Global State Handling      |
| Axios             | API Client              | Backend Communication      |
| ESLint            | Code Quality            | Code Standards             |
| Node.js           | Backend Runtime         | Server Execution           |
| Express.js        | Backend Framework       | REST API Development       |
| MongoDB           | Database                | Data Storage               |
| Redis             | Cache                   | Performance Optimization   |
| Groq LLM          | Artificial Intelligence | Interview Intelligence     |
| Whisper           | Speech AI               | Speech-to-Text             |
| Twilio            | Communication Service   | Phone Interviews           |
| Exotel            | Telephony Service       | Calling Infrastructure     |
| SMTP              | Email Service           | Notifications              |
| Docker            | Containerization        | Application Packaging      |
| Docker Compose    | Orchestration           | Multi-Service Deployment   |
| AWS ECS           | Cloud Platform          | Container Hosting          |
| AWS EC2           | Cloud Platform          | Infrastructure Hosting     |
| AWS Mumbai Region | Cloud Region            | Production Deployment      |
| Nginx             | Reverse Proxy           | Request Routing            |
| JWT               | Authentication          | Secure Access              |
| Local Storage     | Browser Storage         | Theme Persistence          |
| Git               | Version Control         | Source Management          |
| GitHub            | Repository Hosting      | Collaboration              |
| npm               | Package Manager         | Dependency Management      |
| Yarn              | Package Manager         | Package Installation       |

---

# ✨ Key Features

### 🎙 AI Voice Interviews

* Browser-based voice interviews
* Phone-based interviews
* AI-generated questions
* Speech transcription
* Multilingual communication

### 📝 Assessment Platform

* Assessment creation
* Assessment assignment
* Candidate assessment portal
* Automated evaluation
* Performance tracking

### 👨‍💼 Recruiter Dashboard

* Candidate management
* Interview monitoring
* Assessment tracking
* ATS synchronization

### 🤖 AI Capabilities

* Question generation
* Candidate interaction
* Response analysis
* Conversational intelligence

### ☁️ Infrastructure

* Docker deployment
* AWS ECS support
* Redis caching
* Nginx reverse proxy
* Production-ready configuration

---

# 🏗️ System Architecture

```text
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
```

---

# 📁 Project Structure

```text
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
│   │   ├── assets/
│   │   ├── components/
│   │   ├── context/
│   │   ├── hooks/
│   │   ├── pages/
│   │   ├── services/
│   │   ├── utils/
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
```

---

# 🧩 Frontend Components

## Assessment Module

### AssessmentAssignment.jsx

Responsibilities:

* Assign assessments
* Candidate mapping
* Assessment scheduling

### AssessmentDashboard.jsx

Responsibilities:

* Assessment monitoring
* Performance tracking
* Assessment overview

### AssessmentTaker.jsx

Responsibilities:

* Candidate assessment interface
* Question handling
* Submission process

---

## ATS Integration

### ATSIntegrationDashboard.jsx

Responsibilities:

* ATS connectivity
* Candidate synchronization
* Recruitment workflow integration

---

## Candidate Management

### CandidateCard.jsx

Responsibilities:

* Candidate display
* Candidate summary

### CandidatePortalAccess.jsx

Responsibilities:

* Portal permissions
* Candidate access management

### CommunicationPreferences.jsx

Responsibilities:

* Notification settings
* Communication channels

---

## Voice Interview Components

### VoiceSimulator.jsx

Responsibilities:

* Voice interview simulation
* Conversation handling

### LanguageSelector.jsx

Responsibilities:

* Multilingual support
* Language switching

### OmnichannelTimeline.jsx

Responsibilities:

* Communication history
* Interaction timeline

---

## Utility Components

### Navbar.jsx

Application Navigation

### Footer.jsx

Footer Interface

### ThemeToggle.jsx

Theme Switching

### Loader.jsx

Loading UI

### ErrorBoundary.jsx

Application Error Handling

### BackButton.jsx

Navigation Control

---

# 🎨 Theme Management Flow

File:

```text
src/context/ThemeContext.jsx
```

Responsibilities:

* Create Theme Context
* Store Theme State
* Persist Theme using localStorage
* Enable Dark Mode
* Enable Light Mode

Flow:

```text
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
```

---

# 🌐 Browser Interview Flow

```text
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
```

---

# 📞 Phone Interview Flow

```text
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
```

---

# 📝 Assessment Workflow

```text
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
```

---

# 👤 Candidate Workflow

```text
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
```

---

# 🔗 ATS Integration Workflow

```text
ATS Platform
      │
      ▼
ATSIntegrationDashboard
      │
      ▼
Candidate Sync
      │
      ▼
Recruiter Dashboard
      │
      ▼
Hiring Workflow
```

---

# 🤖 AI Processing Workflow

```text
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
```

---

# ⚡ Redis Usage

Redis is used as a caching layer to improve performance.

### Cached Data

* Interview questions
* Candidate evaluations
* AI responses
* Session data
* Frequently accessed records

### Benefits

* Faster response time
* Reduced database load
* Improved scalability

---

# ☁️ Deployment Architecture

```text
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
```

---

# 🔧 Production Configuration

### Database

* MongoDB

### Cache

* Redis

### AI Services

* Groq LLM
* Whisper

### Communication

* Twilio
* Exotel

### Email

* SMTP

### Infrastructure

* Docker
* AWS ECS
* Nginx

---

# 📚 Key Learnings From This Project

* React Component Architecture
* Context API State Management
* AI-Powered Interview Systems
* Voice Processing Workflows
* Whisper Integration
* Groq LLM Integration
* ATS Integration Concepts
* Docker Deployment
* AWS ECS Deployment
* Redis Caching
* Production Infrastructure
* Candidate Lifecycle Management
* Assessment Management Systems
* Cloud-Based Application Deployment

---

# 🎯 Project Outcome

VoicaHire demonstrates the implementation of a scalable AI-driven recruitment platform capable of managing candidate interviews, multilingual voice communication, assessments, ATS integrations, and cloud-native deployment workflows using modern full-stack technologies.

The project showcases expertise in full-stack development, AI integration, speech processing, cloud deployment, candidate management, and production-ready software architecture.
