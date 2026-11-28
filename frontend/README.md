# frontend/

Next.js (React + TypeScript) application. Pages follow `design/prototype`.

Planned structure (created in Week 06):
```
frontend/
├── app/                (public)/ login, register, forgot-password, landing
│                       (app)/ dashboard, documents, flashcards, chat-pdf, chat-youtube, notes, quizzes, tutor, answers, projects, progress, plans, profile
│                       (admin)/ overview, users, plans, reports
│                       api/ route handlers that call backend/ services
├── components/         ui/ (shadcn), layout/, cards/, charts/
├── hooks/  lib/  styles/
```
Design tokens: see `design/design-system.md`.
