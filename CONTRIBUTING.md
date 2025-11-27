
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

