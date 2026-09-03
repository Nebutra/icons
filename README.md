# @nebutra/icons

Public mirror for [@nebutra/icons](https://www.npmjs.com/package/%40nebutra%2Ficons) from [Nebutra/Nebutra-Sailor](https://github.com/Nebutra/Nebutra-Sailor/tree/main/packages/design/icons).

This repository is generated from the Nebutra Sailor monorepo. Package releases are cut from the monorepo and mirrored here for discovery, standalone cloning, and contribution intake.

- Canonical source: `packages/design/icons` in `Nebutra/Nebutra-Sailor`
- Package registry: npm and GitHub Packages
- Contributions: open issues or PRs here; maintainers port accepted changes back into the monorepo source package

---
541 Geist icons packaged as typed TypeScript React components.

## Design Intent

Icons are scraped from the Vercel Geist design system and generated via an SVGR pipeline (`scripts/generate.ts`). Each icon is an individual TSX component that accepts standard SVG props, enabling tree-shaking at the bundler level — importing one icon does not bundle the other 540.

The generation script handles duplicate CSS-in-JSX style keys present in some Geist SVG sources, producing valid component output without manual post-processing.

See `apps/storybook` (Foundation/Icons story) for the full visual gallery.

## Usage

```tsx
import { IconGitHub, IconVercel } from "@nebutra/icons";

<IconGitHub width={20} height={20} />
<IconVercel className="text-foreground" />
```

## Regenerating Icons

```bash
pnpm --filter @nebutra/icons generate
pnpm --filter @nebutra/icons build
```

## License

MIT
