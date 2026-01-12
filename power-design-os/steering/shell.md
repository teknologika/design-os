# Application Shell

Use this when designing the persistent navigation and layout.

## Command and outputs
- `/design-shell` → `product/shell/spec.md`, `src/shell/components/AppShell.tsx`, `src/shell/components/MainNav.tsx`, `src/shell/components/UserMenu.tsx`, `src/shell/ShellPreview.tsx`

## Guidance
- Match shell pattern to product type: sidebar for dashboards, top nav for simpler apps.
- Use product design tokens for the shell preview.
- Shell handles navigation; section screens must not include nav chrome.
