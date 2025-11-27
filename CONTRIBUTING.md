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
