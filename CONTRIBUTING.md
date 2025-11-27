# Contributing

Thank you for contributing to this project.  
This codebase follows the D7460N Architecture: **HTML = structure**, **CSS = UI + state logic**, **JavaScript = data-only**.

Please follow the guidelines below to keep the project consistent and maintainable.

---

## 1. Project Principles

- **Zero dependencies** (no npm, no frameworks, no build pipeline)
- **Semantic HTML only**  
  - No IDs  
  - No classes  
  - No `data-*` attributes  
  - No inline styles  
- **CSS controls all UI, states, visibility, and behaviors**  
  - Use `:has()` and `:empty()` for conditional logic  
  - Use native selectors and attributes  
  - Avoid unnecessary wrappers
- **JavaScript (if used) must be data-only**  
  - No DOM manipulation  
  - No UI state changes  
  - No event listeners for presentation  
  - JS may only handle fetching, storing, or transforming JSON

---

## 2. Formatting

This project relies on **editor-level** formatting only.

- Prettier is required via the VS Code extension
- Formatting is controlled by:
  - `.prettierrc`
  - `.editorconfig`
  - `.vscode/settings.json`

Before committing, ensure:

- Files are saved and formatted
- There are no stray blank lines
- There is **LF line endings only**

No CLI tools or npm scripts exist.

---

## 3. File Structure

Place files in the correct directories:

index.html
assets/css/...
assets/js/...
assets/images/...


Each CSS file has a single responsibility:

- `themes.css` — tokens, color-scheme, environment themes  
- `scaffolding.css` — layout primitives, structure  
- `typography.css` — font settings, type rules  
- `a11y.css` — accessibility behaviors  
- `transitions.css` — global transition behaviors  
- `layout.css` — page-local rules  
- `responsive.css` — responsive breakpoints  
- `spa.css` — SPA/view-transition states  
- `pwa.css` — PWA display-mode adjustments  

Avoid combining files unless necessary.

---

## 4. HTML Contributions

When editing HTML:

- Keep markup **semantic and structural**
- Do not add arbitrary elements to “fix” layout issues  
  (Solve in CSS instead)
- Do not add:
  - classes
  - IDs
  - data attributes
  - inline styles
- Do not introduce ARIA unless it improves accessibility meaningfully

Use meaningful landmarks:

- `<header>`
- `<main>`
- `<section>`
- `<nav>`
- `<footer>`

---

## 5. CSS Contributions

- Prefer **element selectors**
- Use **custom properties** for all theme values
- Use `light-dark()` when possible
- Leverage modern CSS:
  - `:has()`
  - `@layer` (if needed)
  - `@media (prefers-reduced-motion)`
  - CSS transitions and animations
- Avoid CSS hacks, legacy resets, or browser-targeting rules

If adding new CSS files, keep them single-purpose.

---

## 6. JavaScript Contributions (if needed)

- JS must remain **data-only**
- Do not:
  - Manipulate DOM nodes
  - Apply styles
  - Add/remove attributes
  - Control UI state
- JS may:
  - Fetch JSON data
  - Store state in memory
  - Transform or filter data

If JS begins touching UI, the contribution will be rejected.

---

## 7. Pull Requests

Before opening a PR:

1. Ensure all files are formatted (save in VS Code).  
2. Confirm no HTML/CSS rules violate architecture principles.  
3. Add comments only when necessary for clarity.  
4. Keep changes small and focused on a single concern.  
5. Include a brief description of **why** the change is needed.

---

## 8. Questions

If anything in this architecture is unclear, ask before implementing.  
The goal is to maintain a **clean, predictable, and declarative** codebase.

