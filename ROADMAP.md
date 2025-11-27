# Roadmap

This roadmap defines the future direction of the D7460N Starter.

---

## 1. Core Architecture Enhancements

- Expand theme tokens for extended color channels
- Add optional high-contrast theme
- Introduce view-transition patterns in `spa.css`
- Strengthen a11y defaults for focus rings and motion preferences

---

## 2. Layout & Scaffolding

- Add grid-based layout examples
- Provide common structural primitives:
  - header/nav/main/footer variants
  - card patterns
  - list/table hybrids (`<ul><li>` data views)

---

## 3. Components (CSS-only)

- Expand navigation patterns (tabs, pills, breadcrumbs)
- Form scaffolding with `<fieldset>` and `<legend>`
- Semantic dialogs using native `<dialog>` with CSS state logic
- Toggleable panels using `:has()` + checkbox strategy

---

## 4. Optional Modules

- Dark/light/high-contrast theme toggle (CSS-only)
- Drop-in PWA enhancements (`manifest.json` + icons)
- Expand responsive layers using container queries

---

## 5. Documentation

- Add architecture diagrams
- Provide examples of:
  - conditional UI via `:has()`
  - pseudo-element fallbacks
  - pattern-based folders for multi-page SPA behavior

This roadmap is intentionally small and high-level.  
The architecture evolves through refinement, not bulk features.
