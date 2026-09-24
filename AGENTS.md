# CLAUDE.md — vitrine

Vitrine do portfólio: página única (hero → produtos → stats → checkout → dock).

## Stack
- React19 + Vite8 + Tailwind v4 + shadcn (**JS/JSX, `tsx: false`** — não migrar pra TS)
- Deps: framer-motion, lenis, gsap, lucide-react, @storefront-ui/react (tokens via `@theme` em `index.css`)
- Design system: `design-system/vitrine/MASTER.md` — roxo `#7C3AED`, verde `#16A34A`, Orbitron + JetBrains Mono. **Ler antes de mexer em UI.**

## Comandos
```bash
pnpm install
pnpm dev              # :3000
pnpm lint             # oxlint
pnpm build --outDir dist-local   # build de teste (NÃO usar dist/ — root-owned sem sudo)
pnpm build --base ./  # build com paths relativos (GitHub Pages)
```

## Regras
- `vitrine/dist/` e `node_modules/.vite` são **root-owned** — não apagar, usar `dist-local` e `cacheDir .vite-local` (já configurado no `vite.config.js`).
- Components UI ficam em `src/components/ui/` (button, silk-aurora, kinetic-text-reveal, magnetic-dock, sticky-scroll-cards + webgl-error-boundary).
- Registry shadcn: `components.json` → `@componentry` (https://componentry.dev/r/{name}.json). Instalar via `pnpm dlx shadcn@latest add @componentry/<nome>`. **21st.dev é pago — nunca instalar de lá.**
- Skill offline de design: `python3 .opencode/skills/ui-ux-pro-max/scripts/search.py "<q>" --domain <style|typography|chart|ux|icons>`.
- Build publicado no GitHub Pages vem de `../public-pages/` (repo `New-Experiments`, branch `gh-pages`) — sincronizar manualmente.

## Repo
GitHub: `Victor-Enginner/vitrine` · branch `main`.
