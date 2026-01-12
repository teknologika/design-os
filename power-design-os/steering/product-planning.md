# Product Planning (Design OS)

Use this when the user is defining the product foundation.

## Commands and outputs
- `/product-vision` → `product/product-overview.md`
- `/product-roadmap` → `product/product-roadmap.md`
- `/data-model` → `product/data-model/data-model.md`
- `/design-tokens` → `product/design-system/colors.json`, `product/design-system/typography.json`

## Guidance
- Focus on plain-language descriptions, not implementation.
- Keep the data model minimal: entities + relationships only.
- Choose Tailwind built-in colors and Google Fonts for tokens.
- Roadmap section titles become slugs and must map to folder names under `product/sections/` and `src/sections/`. Use simple ASCII words; avoid punctuation, slashes, and special characters.
