# Formatting & Editor Standards

This repo uses **Prettier** and **EditorConfig** as the single source of truth for formatting.

- Consistent 2-space indentation
- LF line endings
- No semicolons in JS
- Single quotes in JS
- Prettier runs on save in VS Code (when using the workspace settings)

---

## Files

These files define the formatting rules:

- `.prettierrc` – Prettier rules (D7460N edition)
- `.prettierignore` – Paths Prettier must not touch
- `.editorconfig` – Indentation, line endings, and basic rules
- `.vscode/settings.json` – VS Code workspace formatting behavior
- `.vscode/extensions.json` – Extension recommendations
- `.devcontainer/devcontainer.json` – Optional dev container with the same setup

---

## Rules (Summary)

### Global

- Indent: **2 spaces**
- Line endings: **LF**
- Final newline: **required**
- Trailing whitespace: **trimmed** (except in Markdown)

### JavaScript

- `semi: false`
- `singleQuote: true`
- `trailingComma: "none"`
- `arrowParens: "always"`

JS is **data-only** in this architecture. Formatting does not change that rule.

### HTML

- `htmlWhitespaceSensitivity: "ignore"`  
  Prettier will format HTML but is less aggressive about whitespace.
- Indent: 2 spaces
- Use `<!-- prettier-ignore -->` for hand-tuned markup.

### Markdown

- Word wrap: on (in VS Code)
- Prettier formats Markdown, but trailing spaces are preserved where meaningful.

---

## Protecting Hand-Tuned Markup

For sections where formatting must **not** change:

```html
<!-- prettier-ignore -->
<section>
  <!-- Carefully aligned / experimental markup -->
</section>
