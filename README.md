# template-tanstack-start-convex

🚀⚡ Full-stack template with TanStack Start and Convex. Includes SSR, real-time sync, and optimistic updates.

## Features

- **[TanStack Start](https://tanstack.com/start)** + **[Convex](https://convex.dev)** - Full-stack with real-time database
- **SSR** - Server-side rendering with route loaders
- **Optimistic Updates** - Instant UI feedback
- **TypeScript** - End-to-end type safety
- **Tailwind CSS v4** + **@ras-sh/ui** - Modern styling and components

Includes a working todo list demo showing Convex integration, custom hooks, and SSR patterns.

## Quick Start

```bash
pnpm install
npx convex dev --once  # Set up Convex, generate .env.local
pnpm dev               # Start dev servers
```

## Building Your App

1. Update `convex/schema.ts` with your data model
2. Add queries/mutations in `convex/` directory
3. Create custom hooks in `src/hooks/` with optimistic updates
4. Build routes in `src/routes/` with SSR loaders
5. Update `package.json` and branding assets

## Scripts

| Command            | Description                           |
| ------------------ | ------------------------------------- |
| `pnpm dev`         | Start both web and Convex dev servers |
| `pnpm dev:web`     | Start only web dev server (port 5173) |
| `pnpm dev:convex`  | Start only Convex dev server          |
| `pnpm build`       | Build for production                  |
| `pnpm preview`     | Preview production build              |
| `pnpm check-types` | Run TypeScript type checking          |
| `pnpm check`       | Run linter checks                     |
| `pnpm fix`         | Auto-fix linting issues               |

## Project Structure

```
src/
├── routes/         # File-based routing with SSR loaders
├── hooks/          # Custom hooks with optimistic updates
├── components/     # Reusable components
└── router.tsx      # Router + Convex configuration

convex/
├── schema.ts       # Database schema
├── todos.ts        # Queries and mutations
└── _generated/     # Auto-generated types
```

## Deployment

**Convex:** `npx convex deploy` then set `VITE_CONVEX_URL` in your frontend deployment

## License

MIT License - see the [LICENSE](LICENSE) file for details.
