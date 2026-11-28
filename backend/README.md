# backend/

TypeScript service modules used by the Next.js API routes.

```
backend/
├── ai-gateway/   OpenAI + Gemini access, prompt templates, JSON schema validation, fallback, logging
├── rag/          PDF/YouTube text extraction, chunking, embeddings, retrieval
├── usage/        daily usage limiter (Free / Pro)
├── billing/      sandbox payment (bKash / SSLCommerz) and subscription handling
├── admin/        user, activity, report and plan services
└── validators/   Zod schemas shared with the frontend
```
API contract: `documentation/CSE4104-7E-T05_SystemDesign.pdf` (Section 7).
