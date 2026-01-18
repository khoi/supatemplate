## Commands

```bash
bun install                    # install dependencies
bun run dev                    # run all apps (turbo)
bun run build                  # build all apps
bun run lint                   # oxlint
bun run lint:fix               # oxlint --fix
bun run fmt                    # oxfmt
bun run check-types            # typecheck all packages

# Desktop (Tauri)
bun run desktop:dev            # dev mode
bun run desktop:build          # production build

# Rust (from apps/desktop/src-tauri)
cargo fmt --all -- --check     # format check
cargo clippy --all -- -D warnings
```

## Architecture

Turborepo monorepo with bun workspaces:

- `apps/desktop` - Tauri desktop app (React + Vite frontend, Rust backend)
- `apps/web` - Next.js 16 marketing site
- `packages/ui` - Shared React component library (Shadcn/Base UI, Tailwind v4)
- `packages/typescript-config` - Shared tsconfig

UI components use exports: `@repo/ui/components/ui/button`, `@repo/ui/lib/utils`

## References

- Tauri docs https://tauri.app/llms.txt
- Shadcn https://ui.shadcn.com/llms.txt
