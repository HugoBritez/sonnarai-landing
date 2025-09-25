# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is an Astro-based landing page project using the basics template. The project uses Bun as the package manager and runtime.

## Common Commands

All commands should be run from the project root:

- `bun install` - Install dependencies
- `bun dev` - Start development server (runs on localhost:4321)
- `bun build` - Build for production (outputs to ./dist/)
- `bun preview` - Preview production build locally
- `bun astro ...` - Run Astro CLI commands
- `bun astro check` - Type check the project

## Project Structure

```
/
├── src/
│   ├── assets/          # Static assets (SVG files, images)
│   ├── components/      # Astro components (.astro files)
│   ├── layouts/         # Layout components (base HTML structure)
│   └── pages/           # File-based routing (index.astro = homepage)
├── public/              # Static files served directly
└── dist/                # Build output directory
```

## Architecture Notes

- **Framework**: Astro 5.x with TypeScript support
- **Styling**: Component-scoped CSS using `<style>` blocks in .astro files
- **Assets**: SVG imports are handled as objects with `.src` property
- **TypeScript**: Uses Astro's strict TypeScript configuration
- **File-based routing**: Pages in `src/pages/` automatically become routes
- **Component structure**: .astro files can contain frontmatter (JS/TS), HTML template, and scoped styles

## Project Documentation

**IMPORTANT**: The original documentation in `docs/sonar-ai-landing.md` is OUTDATED.

The current product concept is documented in `docs/sonarai-concept.md`:

- **Product Overview**: SonarAI is a company specializing in AI agents, chatbots, and automations
- **Core Concept**: "Army of virtual employees" that never sleep, never miss work, and know every detail of the business
- **Services**: Sales agents, customer service, system integrations, internal process automation
- **Target Market**: B2B companies (SMEs to mid-size), primarily Paraguay expanding to LATAM
- **Value Proposition**: "The perfect employee that never existed"
- **Pricing**: Starting from $200/month for specialized agents

## Development Notes

- The project currently uses only Astro components (no external UI frameworks)
- Images and assets should be imported from the `src/assets/` directory
- All styling is currently done with vanilla CSS in component style blocks
- The build uses Bun instead of npm/yarn for faster operations
- **Important**: Always refer to `docs/sonar-ai-landing.md` for content, messaging, and branding guidelines
- Landing page should be responsive/mobile-first with WhatsApp Business API integration