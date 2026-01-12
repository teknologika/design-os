# Export and Handoff

Use this when the user is ready to generate the implementation package.

## Command and outputs
- `/export-product` → `product-plan/` and `product-plan.zip`

## What gets generated
- Prompts for coding agents: `product-plan/prompts/`
- Implementation instructions: `product-plan/instructions/`
- Design system tokens: `product-plan/design-system/`
- Data model types and sample data: `product-plan/data-model/`
- Shell and section components: `product-plan/shell/`, `product-plan/sections/`
- Test instructions per section: `product-plan/sections/[section-id]/tests.md`

## Guidance
- Export is a snapshot; you can re-export anytime.
- Components are production-ready; implementation focuses on wiring data, routing, and tests.
