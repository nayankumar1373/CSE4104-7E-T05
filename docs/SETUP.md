# Project Setup Guide

> The application scaffold is added in Week 06. Steps 1 to 3 work now; steps 4 to 6 work after the scaffold is committed.

## Requirements
- Node.js LTS (v22 or later) and npm
- Git
- Accounts: Supabase, OpenAI (API key), Google AI Studio (Gemini key), Vercel (deployment)

## Steps
1. Clone the repository
   ```bash
   git clone https://github.com/nayankumar1373/CSE4104-7E-T05.git
   cd CSE4104-7E-T05
   ```
2. Create your environment file and fill in your own keys (never commit it)
   ```bash
   cp .env.example .env.local
   ```
3. Open the design prototype to see the target screens: `design/prototype/index.html`
4. Install dependencies
   ```bash
   cd frontend && npm install
   ```
5. Prepare the database (Supabase PostgreSQL with pgvector)
   ```bash
   npx prisma generate --schema=../prisma/schema.prisma
   npx prisma migrate dev --schema=../prisma/schema.prisma
   ```
6. Run the app
   ```bash
   npm run dev      # http://localhost:3000
   ```

## Environment variables
See `.env.example`. Keys are used only on the server (API routes and `backend/` modules).

## Useful scripts (planned)
`npm run lint`, `npm run typecheck`, `npm test`, `npm run build`.
