# Initial Project Planning: EduNexa AI

Team: CSE4104-7E-T05 | Section 7E

## Roles (suggested split, adjust as the team agrees)

| Member | Main focus |
|---|---|
| Nayan Kumar Mayra (Leader) | Project setup, backend and database, RAG pipeline, deployment |
| Ishani Roy Chowdhury | Frontend pages and components, dashboard, UI theme |
| Mohua Kabir Mumu | AI prompts (flashcards, quizzes, notes), testing, documentation |

## Milestones

| Phase | Work | Output |
|---|---|---|
| 1. Setup | Next.js project, Supabase project, Prisma schema, auth | Login works, empty dashboard |
| 2. Core AI | PDF upload, chunking, embeddings, Chat with PDF | Cited answers from a PDF |
| 3. Study tools | Flashcards, Quiz, Magic Notes, YouTube Chat | Structured JSON generation screens |
| 4. Tutor and projects | AI Tutor, Instant Answers, Project Assistant | Conversational and outline features |
| 5. Progress and plans | Study streak, activity feed, Free/Pro limits, sandbox payment | Dashboard with real data |
| 6. Polish | Dark mode, mobile layout, error tracking, testing, deploy | Live demo on Vercel |

## Risks

- AI API cost: apply daily usage limits early.
- Hallucination: always answer from retrieved chunks and show the source.
- Scope: build in the phase order above; cut Phase 5 extras first if time is short.
