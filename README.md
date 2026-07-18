# Acme Dashboard

A financial dashboard built while completing the [Next.js App Router Course](https://nextjs.org/learn). It manages invoices and customers with authentication, search, pagination, and full CRUD.

## Features

- **App Router** with Server Components, layouts, and streaming (`loading.tsx` + React `<Suspense>`)
- **Authentication** via NextAuth.js (Credentials provider) with route protection through a proxy
- **Invoices CRUD** using Server Actions with Zod validation and graceful error handling
- **Search & pagination** driven by URL search params (debounced search)
- **PostgreSQL** database (Supabase) accessed with the `postgres` client
- **Accessibility** linting via `eslint-plugin-jsx-a11y`
- **SEO metadata** with title templates and Open Graph image

## Tech stack

- Next.js (App Router) + React
- TypeScript
- Tailwind CSS
- NextAuth.js
- PostgreSQL (Supabase)
- Zod

## Getting started

Install dependencies:

```bash
pnpm install
```

Create a `.env` file (see `.env.example`) with your database connection and an auth secret:

```bash
POSTGRES_URL=your-postgres-connection-string
AUTH_SECRET=your-generated-secret   # openssl rand -base64 32
```

Run the development server:

```bash
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000).

## Seeding the database

With the dev server running, visit [http://localhost:3000/seed](http://localhost:3000/seed) once to create the tables and populate them with placeholder data.

## Demo credentials

- **Email:** `user@nextmail.com`
- **Password:** `123456`

## Scripts

| Command | Description |
| --- | --- |
| `pnpm dev` | Start the development server |
| `pnpm build` | Create a production build |
| `pnpm start` | Run the production build |
| `pnpm lint` | Run ESLint |

---

Based on the [Next.js Learn](https://nextjs.org/learn) course curriculum.
