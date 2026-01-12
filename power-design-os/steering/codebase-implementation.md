# Codebase Implementation Guidance

Use this when the user wants to implement the exported designs in a separate codebase.

## Approaches
- Incremental: follow `product-plan/instructions/incremental/` in order.
- One-shot: use `product-plan/instructions/one-shot-instructions.md`.

## shadcn/ui baseline
Use shadcn/ui as the primary UI component library in the target codebase.

Required baseline packages:
- `tailwindcss` (v4)
- `clsx`
- `tailwind-merge`
- `class-variance-authority`
- `lucide-react`

Install shadcn/ui:
- `npx shadcn@latest init`
- Add components as needed: `npx shadcn@latest add <component>`

## What the implementation agent must handle
- Backend APIs, data modeling, auth, and validation.
- Routing, data fetching, loading/error states.
- Empty states and edge cases.
- Tests based on `tests.md` for each section.

## Reminders
- Use the exported UI components as-is; do not redesign.
- Test with `sample-data.json` first, then wire real data.
