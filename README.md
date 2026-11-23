# EduNexa AI: Your Intelligent Learning & Project Workspace

| | |
|---|---|
| **Course** | CSE4104 |
| **Team** | CSE4104-7E-T05 |
| **Section** | 7E |
| **Department** | Department of CSE, Northern University of Business and Technology, Khulna |
| **Course Instructor** | Md. Riaz Mahmud, Assistant Professor |

EduNexa AI is an AI-based web platform where university students turn their own study material into flashcards, notes, quizzes and cited answers, and get structured help with their course projects.

## Team Information

| No. | Name | Student ID | Role |
|-----|------|-----------|------|
| 1 | Nayan Kumar Mayra | 11230321373 | Team Leader |
| 2 | Ishani Roy Chowdhury | 11230321334 | Member |
| 3 | Mohua Kabir Mumu | 11230321246 | Member |

Team Leader Email: nayanmayra7878@gmail.com

## Objectives

- Generate flashcards and quizzes automatically from text, a PDF or a topic name.
- Let students chat with a PDF or a YouTube video and receive answers based on the actual content, with source references.
- Create short, structured notes and step-by-step answers from text or images.
- Provide an AI Tutor for concept explanations and a Project Assistant for project ideas, outlines and report drafting help.
- Show learning progress, study streak and recent activity on a simple dashboard.
- Offer a calm, easy-to-use interface with a soft light theme, optional dark mode and a mobile-friendly layout.
- Provide Free and Pro plans with usage limits, so the service stays affordable.

## Features

- Authentication (email and Google)
- Dashboard (progress ring, study streak, recent activity)
- Flashcard Generator
- Chat with PDF (RAG with page references)
- Chat with YouTube
- Magic Notes
- Quiz Generator
- AI Tutor
- Instant Answers
- Project Assistant
- Progress Tracking
- Plans and Usage Limits (sandbox payment)
- Admin panel (users, monitoring, reports, plan limits)

## Technology Stack

| Layer | Technologies |
|-------|--------------|
| Frontend | Next.js (React), TypeScript, Tailwind CSS, shadcn/ui, Framer Motion, TanStack Query, Zustand, Recharts, next-themes |
| Backend | Node.js with Next.js API routes, Prisma ORM |
| Database | PostgreSQL on Supabase with pgvector |
| Auth and Storage | Supabase Auth (email and Google), Supabase Storage |
| AI Integration | OpenAI API, Google Gemini API, LangChain, pdf-parse, youtube-transcript |
| Payment (sandbox) | SSLCommerz or bKash sandbox |
| Deployment | Vercel, Sentry, GitHub |

## System Design Summary

- **Architecture:** Frontend (Next.js) -> Backend API (Next.js API routes and service modules) -> Database (PostgreSQL + pgvector), with an AI Gateway to OpenAI / Gemini and external APIs (YouTube transcripts, payment sandbox).
- **Database:** 18 entities including USER, DOCUMENT, DOCUMENT_CHUNK (embeddings), FLASHCARD_SET, QUIZ, NOTE, CHAT_SESSION, PROJECT, PLAN, SUBSCRIPTION and PAYMENT.
- **API:** 66 planned REST endpoints (Auth, User, Dashboard, Documents, Flashcards, Quizzes, Notes, Chat, Projects, Plans and Payments, Admin).
- **AI workflow:** documents are split into chunks and embedded; a question retrieves the most relevant chunks (RAG) and the model answers only from them, with sources shown.

## Documents

| Document | File |
|----------|------|
| Project Proposal | [docs/CSE4104-7E-T05_Proposal.pdf](docs/CSE4104-7E-T05_Proposal.pdf) |
| Team Information Sheet | [docs/CSE4104-7E-T05_TeamInfo.pdf](docs/CSE4104-7E-T05_TeamInfo.pdf) |
| Software Requirements Specification (SRS) | [docs/srs/CSE4104-7E-T05_SRS.pdf](docs/srs/CSE4104-7E-T05_SRS.pdf) |
| System Design Document | [documentation/CSE4104-7E-T05_SystemDesign.pdf](documentation/CSE4104-7E-T05_SystemDesign.pdf) |
| AI Integration Workflow | [documentation/CSE4104-7E-T05_AIWorkflow.pdf](documentation/CSE4104-7E-T05_AIWorkflow.pdf) |
| Architecture notes | [docs/ARCHITECTURE.md](docs/ARCHITECTURE.md) |
| Project plan | [docs/PROJECT_PLAN.md](docs/PROJECT_PLAN.md) |

## Diagrams (docs/diagrams)

| Diagram | File |
|---------|------|
| Updated Use Case Diagram | [CSE4104-7E-T05_UseCaseDiagram.pdf](docs/diagrams/CSE4104-7E-T05_UseCaseDiagram.pdf) |
| ER Diagram | [CSE4104-7E-T05_ERDiagram.pdf](docs/diagrams/CSE4104-7E-T05_ERDiagram.pdf) |
| System Architecture Diagram | [CSE4104-7E-T05_SystemArchitectureDiagram.pdf](docs/diagrams/CSE4104-7E-T05_SystemArchitectureDiagram.pdf) |
| Architecture Diagram (Week 03) | [CSE4104-7E-T05_ArchitectureDiagram.pdf](docs/diagrams/CSE4104-7E-T05_ArchitectureDiagram.pdf) |
| Activity Diagrams (all four) | [CSE4104-7E-T05_ActivityDiagram.pdf](docs/diagrams/CSE4104-7E-T05_ActivityDiagram.pdf) |
| Activity: User Registration Process | [CSE4104-7E-T05_User Registration Process.pdf](docs/diagrams/CSE4104-7E-T05_User%20Registration%20Process.pdf) |
| Activity: Login Process | [CSE4104-7E-T05_Login Process.pdf](docs/diagrams/CSE4104-7E-T05_Login%20Process.pdf) |
| Activity: Chat with PDF (RAG) Workflow | [CSE4104-7E-T05_Chat with PDF (RAG) Workflow.pdf](docs/diagrams/CSE4104-7E-T05_Chat%20with%20PDF%20%28RAG%29%20Workflow.pdf) |
| Activity: AI Flashcard Generation Workflow | [CSE4104-7E-T05_AI Flashcard Generation Workflow.pdf](docs/diagrams/CSE4104-7E-T05_AI%20Flashcard%20Generation%20Workflow.pdf) |

## Repository Structure

```
CSE4104-7E-T05/
├── README.md
├── .env.example                 example environment variables (API keys are not stored here)
├── .gitignore
├── frontend/                    Next.js pages, components and UI state (added during development)
├── backend/                     service modules: AI Gateway, RAG, usage limiter, billing, admin
├── database/                    database design files: migrations, pgvector SQL, seed data
├── documentation/               System Design and AI Workflow documents
├── docs/
│   ├── CSE4104-7E-T05_Proposal.pdf
│   ├── CSE4104-7E-T05_TeamInfo.pdf
│   ├── ARCHITECTURE.md
│   ├── PROJECT_PLAN.md
│   ├── srs/                     Software Requirements Specification
│   └── diagrams/                use case, ER, architecture and activity diagrams
└── prisma/                      Prisma schema (database design)
```

The `frontend`, `backend` and `database` folders are the initial project folders; application source code will be added in the development phase.

## Project Status

- [x] Project Proposal
- [x] Software Requirements Specification (SRS) and initial diagrams
- [x] System Design and Software Architecture
- [ ] Development
- [ ] Testing and Deployment
