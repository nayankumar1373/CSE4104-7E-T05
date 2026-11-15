# EduNexa AI: Your Intelligent Learning & Project Workspace

**Course:** CSE4104 | **Team:** CSE4104-7E-T05 | **Section:** 7E
**Department of CSE, Northern University of Business and Technology, Khulna**
**Course Instructor:** Md. Riaz Mahmud, Assistant Professor

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

## Repository Structure

```
CSE4104-7E-T05/
├── README.md
├── .env.example
├── .gitignore
├── prisma/                     (database schema, Prisma ORM)
├── docs/
│   ├── CSE4104-7E-T05_Proposal.pdf
│   ├── CSE4104-7E-T05_TeamInfo.pdf
│   ├── ARCHITECTURE.md
│   ├── PROJECT_PLAN.md
│   ├── srs/
│   │   └── CSE4104-7E-T05_SRS.pdf
│   └── diagrams/
│       ├── CSE4104-7E-T05_UseCaseDiagram.pdf
│       ├── CSE4104-7E-T05_ERDiagram.pdf
│       └── CSE4104-7E-T05_ArchitectureDiagram.pdf
└── src/                        (application source code, added during development)
```

## Project Status

- [x] Project Proposal
- [x] Software Requirements Specification (SRS) and initial diagrams
- [ ] System Design
- [ ] Development
- [ ] Testing and Deployment
