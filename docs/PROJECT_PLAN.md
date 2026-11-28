# Project Plan: EduNexa AI (updated in Week 05)

Team: CSE4104-7E-T05 | Section 7E | Full details: `documentation/CSE4104-7E-T05_DevelopmentPlan.pdf`

## Roles
| Member | Lead areas | Support areas |
|---|---|---|
| Nayan Kumar Mayra (Leader) | Backend, database, AI Gateway and RAG, deployment, GitHub | Frontend integration, prompts |
| Ishani Roy Chowdhury | Frontend, UI/UX design system | API client, UI tests, documentation (UI) |
| Mohua Kabir Mumu | AI prompts and schemas, testing, documentation | API tests, seed data, demo |

## Roadmap
| Week | Focus | Milestone |
|---|---|---|
| 05 | UI/UX design and planning | Design approved (this submission) |
| 06 | Backend foundation: scaffold, CI, Supabase, Prisma, auth, usage limiter; UI shell and public pages | Register, log in, empty dashboard |
| 07 | Frontend core (dashboard, documents, profile, theme); PDF upload, parsing, chunking, embeddings | PDF reaches status Ready |
| 08 | AI integration: AI Gateway, RAG, Chat with PDF, Chat with YouTube, Flashcards | Cited answers; flashcards generated |
| 09 | Feature completion: Quiz, Notes, Tutor, Instant Answers, Project Assistant, progress, plans, payment sandbox, admin | All SRS modules usable |
| 10 | Testing and debugging, responsive and accessibility pass, admin reports | No high-severity bugs |
| 11 | Deployment (Vercel, Sentry), user manual, final report, demo | Live demo |

## Priorities (MoSCoW)
Must: M1 to M9, M14, M15. Should: tutor / answers / projects, progress and plans, admin. Could (cut first): sandbox payment.

## Risks
- AI API cost: daily usage limits from Week 06, low-cost models, Gemini fallback.
- Hallucination: answer only from retrieved chunks, show sources, "not found" message.
- Scope: build in module order; cut "Could" items first if time is short.
- Late deployment problems: deploy a Vercel preview in Week 06 and redeploy every week.
