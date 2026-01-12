# Section Design Workflow

Use this when shaping, populating, and designing a section.

## Commands and outputs
- `/shape-section` → `product/sections/[section-id]/spec.md`
- `/sample-data` → `product/sections/[section-id]/data.json`, `product/sections/[section-id]/types.ts`
- `/design-screen` → `src/sections/[section-id]/components/*.tsx`, `src/sections/[section-id]/components/index.ts`, `src/sections/[section-id]/[ViewName].tsx`
- `/screenshot-design` → `product/sections/[section-id]/[screen-name].png` (optional)

## Design requirements
- Mobile responsive with Tailwind prefixes (`sm:`, `md:`, `lg:`).
- Light and dark mode with `dark:` variants.
- Use product design tokens when defined; otherwise `stone` + `lime`.
- Exportable components must be props-based and portable.
- No navigation in section screens; shell provides it.

## Slug and naming rules
- Section IDs are derived from roadmap titles and must match folder names under `product/sections/` and `src/sections/`.
- Use simple ASCII words for section titles to avoid slug mismatches (avoid punctuation, slashes, and non-Latin characters).
- Screen design filenames become URL segments; keep them URL-safe (PascalCase or kebab-case, no spaces).
