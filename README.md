# Ellen’s portfolio

Minimal Next.js project with App Router, TypeScript, Tailwind CSS, and ESLint.
The homepage is an unstyled component scaffold based on the supplied Figma design.
No animation or UI libraries are installed.

## Local development

Use Node.js 24 LTS and npm.

```sh
npm install
npm run dev
```

Open http://localhost:3000. On Windows PowerShell, use `npm.cmd` if script execution is restricted.

## Structure

```text
src/
  app/
    globals.css          # Tailwind and global styles
    layout.tsx           # Shared layout and metadata
    page.tsx             # Homepage
  components/
    site-header.tsx
    site-footer.tsx
    logo.tsx
    intro-section.tsx
    experience-section.tsx
    folder-card.tsx
    hanging-lamp.tsx
    social-links.tsx
  content/
    home.ts              # Figma copy and configurable destinations
public/                  # Static assets
```

Use `@/` imports for files inside `src`. Keep page-specific sections in the page until reuse warrants another component.

## Checks

```sh
npm run lint
npm run typecheck
npm run build
```

Run `npm run start` after building to preview the production build locally.

## Vercel

Push to a Git repository and import into Vercel using the Next.js preset.
Use the repository root as the project root. No custom deployment configuration or environment variables are needed for this starter.

## Figma implementation

See [homepage architecture](docs/homepage-architecture.md) for the Figma analysis and component responsibilities.
Add case-study and social destinations in `src/content/home.ts` when available.
Add design colors and typography in `globals.css`, shared components in `src/components`,
and images in `public`. System fonts are used until the design’s fonts are known.
