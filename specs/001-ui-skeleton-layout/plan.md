# Implementation Plan: UI Skeleton & Layout

**Branch**: `001-ui-skeleton-layout` | **Date**: 2026-01-13 | **Spec**: [specs/001-ui-skeleton-layout/spec.md](specs/001-ui-skeleton-layout/spec.md)
**Input**: Feature specification from `specs/001-ui-skeleton-layout/spec.md`

## Summary

Implement the global UI skeleton using Next.js 16 (App Router) and Tailwind CSS v4. This includes configuring the global dark theme (#0F1115 background, #FFFFFF text), implementing a responsive Layout component with a sticky Header (containing "Anonymous Advice" text logo) and a sticky-bottom Footer, and ensuring responsive design mobile-first.

## Technical Context

**Language/Version**: TypeScript 5.x  
**Primary Dependencies**: Next.js 16.1.1, React 19, Tailwind CSS v4  
**Storage**: N/A  
**Testing**: Manual Verification (Independent Tests defined in Spec)  
**Target Platform**: Web (Responsive)  
**Project Type**: Web Application (Next.js App Router)  
**Performance Goals**: First Contentful Paint < 1s  
**Constraints**: Zero-config Tailwind v4 (CSS-first configuration)  
**Scale/Scope**: Global layout affecting all pages  

## Constitution Check

*GATE: Must pass before Phase 0 research. Re-check after Phase 1 design.*

- **Absolute Anonymity**: N/A (UI only)
- **Simplicity and Speed**: Check. Using lightweight Tailwind classes.
- **User Safety**: N/A (UI only)
- **Mobile-First**: Check. Design is responsive.
- **Unrestricted Content**: Check. Layout supports public access.

**Status**: PASSED

## Project Structure

### Documentation (this feature)

```text
specs/001-ui-skeleton-layout/
├── plan.md              # This file
├── research.md          # Tailwind v4 config decisions
├── data-model.md        # (Empty)
├── quickstart.md        # Verification steps
└── tasks.md             # Implementation tasks
```

### Source Code (repository root)

```text
app/
├── globals.css          # Global styles & Tailwind theme
├── layout.tsx           # Main Root Layout
├── page.tsx             # Home page (content placeholder)
└── components/          # New directory for UI components
    ├── Header.tsx       # Sticky Header with Logo
    └── Footer.tsx       # Sticky Footer
```

**Structure Decision**: Standard Next.js App Router structure.

## Complexity Tracking

*No violations.*