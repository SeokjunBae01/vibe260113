# Tasks: UI Skeleton & Layout

**Feature**: UI Skeleton & Layout  
**Status**: Done  
**Spec**: [specs/001-ui-skeleton-layout/spec.md](specs/001-ui-skeleton-layout/spec.md)

## Phase 1: Setup
*Goal: Prepare the project structure for UI implementation.*

- [X] T001 Create components directory `app/components`
- [X] T002 Clean up `app/page.tsx` to serve as a simple placeholder

## Phase 2: Foundational
*Goal: Establish core style configurations required by all stories.*

- [X] T003 Remove default Next.js dark mode media queries in `app/globals.css`
- [X] T004 Define project colors (#0F1115, #FFFFFF, #22C55E) as CSS variables in `app/globals.css`

## Phase 3: User Story 1 - Global Dark Theme
*Goal: Users encounter a consistent dark theme across the application.*
*Priority: P1*

**Independent Test**: Open the application root. Verify the background is dark (#0F1115) and text is white (#FFFFFF).

- [X] T005 [US1] Apply global background and text color to body in `app/globals.css`
- [X] T006 [US1] Verify `app/layout.tsx` includes base font and global css import

## Phase 4: User Story 2 - Consistent Layout Structure
*Goal: Users see a consistent Header and Footer on every page.*
*Priority: P1*

**Independent Test**: Create two dummy pages wrapped in the Layout. Navigate between them and verify Header/Footer persist.

- [X] T007 [P] [US2] Create Header component with Logo in `app/components/Header.tsx`
- [X] T008 [P] [US2] Create Footer component with copyright in `app/components/Footer.tsx`
- [X] T009 [US2] Implement sticky footer layout (flex-col min-h-screen) in `app/layout.tsx`
- [X] T010 [US2] Integrate Header and Footer into `app/layout.tsx`

## Phase 5: User Story 3 - Responsive Design
*Goal: Users on different devices see a layout optimized for their screen size.*
*Priority: P2*

**Independent Test**: Resize browser window from mobile width to desktop width and verify layout adaptability.

- [X] T011 [P] [US3] Implement responsive padding and font sizes in `app/components/Header.tsx`
- [X] T012 [P] [US3] Implement responsive container constraints (max-width, centering) in `app/layout.tsx` main wrapper

## Phase 6: Polish & Cross-Cutting Concerns
*Goal: Final quality checks and cleanup.*

- [X] T013 Validate accessibility (contrast ratios) for text and background
- [X] T014 Verify zero console errors and successful `npm run build`

## Dependencies

1. **User Story 1** (Global Theme) must complete first to ensure visual consistency.
2. **User Story 2** (Layout Structure) depends on Theme for colors but primarily establishes the DOM structure.
3. **User Story 3** (Responsive Design) refines the components created in US2.

## Implementation Strategy

- **MVP Scope**: Complete Phase 1 through Phase 4 (Setup, Theme, Basic Layout).
- **Parallel Execution**: 
  - `Header.tsx` and `Footer.tsx` (T007, T008) can be built simultaneously.
  - Responsive adjustments (T011, T012) can be applied to separate files in parallel once the base files exist.
