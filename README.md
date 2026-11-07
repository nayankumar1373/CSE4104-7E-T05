# EduNexa AI: Your Intelligent Learning & Project Workspace

**CSE4104 | AI-Based Software Development Project**
Department of CSE, Northern University of Business and Technology, Khulna

---

## Team Information

| Field | Details |
|---|---|
| Team Name | CSE4104-7E-T05 |
| Section | 7E |
| Project Title | EduNexa AI: Your Intelligent Learning & Project Workspace |
| Team Leader | Nayan Kumar Mayra |
| Leader Email | nayanmayra7878@gmail.com |
| Course Instructor | Md. Riaz Mahmud, Assistant Professor |
| Proposal Submission | 9th November 2026 |
| GitHub Repository | https://github.com/nayankumar1373/CSE4104-7E-T05 |

### Members

| No. | Name | Student ID | Role |
|---|---|---|---|
| 1 | Nayan Kumar Mayra | 11230321373 | Team Leader |
| 2 | Ishani Roy Chowdhury | 11230321334 | Member |
| 3 | Mohua Kabir Mumu | 11230321246 | Member |

---

## Project Description

EduNexa AI is an AI-based web platform where university students turn their own study material into flashcards, notes, quizzes and cited answers, and get structured help with their course projects.

### Problem

Every semester, students collect lecture slides, PDF books, class notes and video lectures. Turning this into revision notes, flashcards and practice questions takes many hours. Course projects add more pressure because students must choose a topic, plan the work and write a report with little guidance. Existing general chatbots do not know the student's own material and may invent facts, study tools are spread over separate apps, and most good AI tools are paid in dollars.

### Solution

One workspace where AI works on the **student's own documents** using Retrieval-Augmented Generation (RAG), so every answer is grounded in the source and shows where it came from.

### Objectives

- Generate flashcards and quizzes automatically from text, a PDF or a topic name.
- Let students chat with a PDF or a YouTube video and receive answers with source references.
- Create short, structured notes and step-by-step answers from text or images.
- Provide an AI Tutor for concept explanations and a Project Assistant for ideas, outlines and report drafting.
- Show learning progress, study streak and recent activity on a simple dashboard.
- Offer a calm, easy-to-use interface with a soft light theme, optional dark mode and a mobile-friendly layout.
- Provide Free and Pro plans with usage limits so the service stays affordable.

---

## Proposed Features

| Feature | What it does | Role of AI |
|---|---|---|
| Authentication | Sign up and login with email or Google; private data per user | None |
| Dashboard | Greeting, quick actions, progress ring, study streak, recent activity | None |
| Flashcard Generator | Creates Q&A cards from notes, text or a topic; cards flip and show progress | Generates the cards |
| Chat with PDF | Upload a PDF and ask questions; answers include page references | RAG, embeddings, answer generation |
| Chat with YouTube | Video transcript turned into summary, key points and answers | RAG, summarisation |
| Magic Notes | Short structured notes from a PDF, web page or image | Summarisation, vision model |
| Quiz Generator | Multiple-choice questions with scoring | Generates questions and options |
| AI Tutor | Explains difficult concepts in simple steps | Conversational explanation |
| Instant Answers | Step-by-step answers streamed as they are written | Streaming answer generation |
| Project Assistant | Suggests project ideas, builds an outline, helps with report writing | Idea and outline generation |
| Progress Tracking | Records activity for study streak and recent work | None |
| Plans and Usage Limits | Free and Pro plans, daily limits, sandbox payment flow | None |

### How AI is integrated (RAG pipeline)

1. The uploaded PDF or video transcript is converted to text and split into small chunks.
2. Each chunk is turned into an embedding and stored in PostgreSQL with `pgvector`.
3. When the student asks a question, the closest chunks (by meaning) are retrieved and sent to the language model (OpenAI or Gemini).
4. The model answers from those chunks and the answer is shown with its source text so the student can verify it.

Flashcards, quizzes, notes and project outlines use designed prompts that return structured JSON, which the app renders in its own screens.

---

## Technology Stack

| Layer | Technologies | Purpose |
|---|---|---|
| Frontend | Next.js (React), TypeScript, Tailwind CSS, shadcn/ui, Framer Motion, TanStack Query, Zustand, Recharts, next-themes | Pages, components, animations, data fetching, charts, light/dark theme |
| Backend | Node.js with Next.js API routes, Prisma ORM | APIs, business logic, rate limits, database access |
| Database | PostgreSQL on Supabase with pgvector | Users, cards, notes, chats, projects, embeddings |
| Auth & Storage | Supabase Auth (email and Google), Supabase Storage | Sign up, login, storage of PDFs and images |
| AI Integration | OpenAI API (ChatGPT), Google Gemini API, LangChain, pdf-parse, youtube-transcript | Text generation, answers, RAG pipeline, PDF text, video transcripts |
| Payment (sandbox) | SSLCommerz or bKash sandbox | Pro plan demonstration |
| Deployment | Vercel, Sentry, GitHub | Hosting, error tracking, source control |

---

## Repository Structure

```
CSE4104-7E-T05/
├── README.md
├── .gitignore
├── .env.example
├── docs/
│   ├── CSE4104-7E-T05_Proposal.pdf
│   ├── CSE4104-7E-T05_TeamInfo.pdf
│   ├── PROJECT_PLAN.md
│   └── ARCHITECTURE.md
├── prisma/
│   └── schema.prisma
├── public/
└── src/
    ├── app/          # Next.js pages and API routes
    ├── components/   # Reusable UI components
    └── lib/          # AI, RAG, Supabase and helper code
```

## Getting Started

> The application code will be added during development. The setup below describes the planned workflow.

```bash
git clone https://github.com/nayankumar1373/CSE4104-7E-T05.git
cd CSE4104-7E-T05
cp .env.example .env.local     # fill in your own keys
# install dependencies once the Next.js app is initialised
npm install
npx prisma generate
npm run dev
```

Never commit `.env.local` or any API key.

## Team Workflow

- `main` is always stable; work happens on feature branches (`feature/<name>`).
- Every change goes through a Pull Request reviewed by at least one other member.
- Commit messages: `feat: ...`, `fix: ...`, `docs: ...`.

## Documents

- [Project Proposal (PDF)](docs/CSE4104-7E-T05_Proposal.pdf)
- [Team Information Sheet (PDF)](docs/CSE4104-7E-T05_TeamInfo.pdf)
- [Project Plan](docs/PROJECT_PLAN.md)
- [Architecture](docs/ARCHITECTURE.md)
