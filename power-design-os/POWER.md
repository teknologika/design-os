---
name: "design-os"
displayName: "Design OS Product Planning"
description: "Plan products, design sections, and export handoff packages with Design OS."
keywords: ["design os", "product vision", "product roadmap", "data model", "design tokens", "design system", "application shell", "shape section", "sample data", "design screen", "screenshot design", "export product", "product plan", "handoff", "tailwind v4"]
mcpServers: ["structured-thinking", "context7", "shadcn"]
---

# Onboarding

## Step 1: Confirm workspace
You should be in a Design OS repository. Look for:
- `docs/` with Design OS guides
- `product/` for planning outputs
- `src/sections/` and `src/shell/` for designs

If those folders are missing, ask the user for the correct repo path before proceeding.

## Step 2: Optional local setup
If the user wants to preview designs locally:
- Install dependencies: `npm install`
- Start dev server: `npm run dev`
- Open: `http://localhost:5173`

## Step 2.1: Quick clone (optional)
If starting from the upstream template:
- `git clone https://github.com/buildermethods/design-os.git my-project-design`
- `cd my-project-design`
- `git remote remove origin`

## Step 3: shadcn/ui baseline (for implementation)
When implementing the exported UI in a separate codebase, use shadcn/ui as the primary component library.

Required baseline packages:
- `tailwindcss` (v4)
- `clsx`
- `tailwind-merge`
- `class-variance-authority`
- `lucide-react`

Install shadcn/ui in the target codebase:
- `npx shadcn@latest init`
- Add components as needed: `npx shadcn@latest add <component>`

## Step 4: shadcn MCP (optional)
If you want shadcn MCP tools available inside Kiro, add an `mcp.json` for your preferred shadcn MCP server package and command. If you don't already have a package/command, ask the user which shadcn MCP server they want to use.

# When to Load Steering Files
- Product planning (vision, roadmap, data model, design tokens) → `steering/product-planning.md`
- Application shell design → `steering/shell.md`
- Section design workflow → `steering/section-design.md`
- Export and handoff → `steering/export.md`
- Codebase implementation guidance → `steering/codebase-implementation.md`

# General Rules
- Design OS outputs are planning assets, not final product code.
- Screen designs are props-based React components; never import sample data in exportable components.
- Use Tailwind CSS v4 utilities only; do not add or reference `tailwind.config.js`.
- Use `dark:` variants for color utilities in screen designs.
- Recommend shadcn/ui as the primary UI component library when implementing exports.

# MCP Tools Available
- `structured-thinking`: Structured reasoning workflows for planning and decomposition.
- `context7`: Context lookup and retrieval support when drafting specs or guidance.
- `shadcn`: shadcn/ui tooling (component add/init) when implementing exports.

# Troubleshooting
- `Cannot find module 'lucide-react'` → run `npm install` in the repo.
- `react/jsx-runtime` missing → ensure deps are installed, then restart your TS server/IDE.
- Tailwind v4 required → do not add a `tailwind.config.js`.
- shadcn/ui setup → run `npx shadcn@latest init` in the target codebase, then add components as needed.

# Repositories
- Current repo: https://github.com/teknologika/design-os-mcp
- Upstream repo: https://github.com/buildermethods/design-os
