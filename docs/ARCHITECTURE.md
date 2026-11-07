# Architecture Overview

```
Browser (Next.js + React)
        |
        v
Next.js API routes  --->  Supabase Auth / Storage
        |
        +--->  Prisma  --->  PostgreSQL (Supabase) + pgvector
        |
        +--->  LangChain  --->  OpenAI / Gemini
```

## RAG flow

1. Upload PDF (or fetch YouTube transcript) -> extract text (pdf-parse / youtube-transcript).
2. Split into chunks, keep page number.
3. Create embeddings, store in `DocumentChunk.embedding` (pgvector).
4. On a question: embed the question, find nearest chunks, send them with the question to the LLM.
5. Return the answer plus the source chunks and page numbers.

## Structured generation

Flashcards, quizzes, notes and project outlines are requested as JSON from the model, validated, saved, then rendered by the UI.
