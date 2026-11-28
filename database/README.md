# database/

Database support files. The Prisma schema is in `../prisma/schema.prisma` (18 entities).

Planned files:
- `pgvector.sql` : enable the `vector` extension and create the vector index on `DocumentChunk.embedding`
- `rls-policies.sql` : row-level security so each user can read and write only their own data
- `seed.sql` / `seed.ts` : demo users (student, pro student, admin), plans (Free, Pro) and sample data
