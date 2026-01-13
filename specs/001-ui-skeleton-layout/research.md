# Research & Technical Decisions

## Technical Context
- **Framework**: Next.js 16.1.1 (App Router)
- **Language**: TypeScript
- **Styling**: Tailwind CSS v4 (PostCSS)
- **State/Data**: N/A for this skeleton

## Decisions

### 1. Tailwind CSS v4 Theme Configuration
- **Decision**: Use CSS variables within `app/globals.css` under the `@theme` directive (or just root variables mapped to theme) to define the specific colors.
- **Rationale**: Tailwind v4 moves configuration to CSS. We need to enforce a specific dark theme (`#0F1115`) regardless of system preference.
- **Implementation**:
  - Remove `@media (prefers-color-scheme: dark)` block.
  - Set `:root` variables to the required dark mode values.
  - Define custom colors if needed for semantic naming (e.g., `--color-brand-green: #22C55E`).

### 2. Layout Structure
- **Decision**: Use `app/layout.tsx` for the global `<html>` and `<body>` structure, and create a separate `components/layout/MainLayout.tsx` (or similar) if we need to wrap content specifically, but standard Next.js `app/layout.tsx` is sufficient for a global Header/Footer.
- **Rationale**: `app/layout.tsx` persists across route changes, making it ideal for the Header and Footer.
- **Implementation**:
  - `app/layout.tsx` imports `Header` and `Footer` components.
  - Wraps `{children}`.

### 3. Font Loading
- **Decision**: Continue using `next/font` (Geist) as present in `globals.css` and `layout.tsx`.
- **Rationale**: Optimized font loading built-in to Next.js.

### 4. Component Strategy
- **Decision**: Create atomic components for `Header`, `Footer`, `Logo`.
- **Rationale**: Separation of concerns and reusability.
- **Path**: `app/components/Header.tsx`, `app/components/Footer.tsx`.

### 5. Responsive Design
- **Decision**: Use standard Tailwind breakpoints (`md`, `lg`).
- **Rationale**: Proven, standard approach.

## Unknowns Resolved
- **Tailwind Config**: Verified v4 is installed; no `tailwind.config.ts` needed. Configuration happens in CSS.
