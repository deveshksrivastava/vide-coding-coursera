# Lint Setup Todo

## Checklist

- [x] 1. Init npm (`npm init -y`)
- [x] 2. Install dev deps: `prettier`, `htmlhint`, `husky`, `lint-staged`
- [x] 3. Create `.htmlhintrc` config
- [x] 4. Create `.prettierrc` config
- [x] 5. Configure `lint-staged` and scripts in `package.json`
- [x] 6. Init husky and create `pre-push` hook

## Review

Added full lint setup for this HTML/CSS project:

- **HTMLHint** validates HTML structure (duplicate IDs, tag pairing, doctype, etc.)
- **Prettier** auto-formats HTML/CSS on every push
- **Husky** wires up git hooks (`.husky/pre-push` and `.husky/pre-commit`)
- **`npm run lint`** — run HTMLHint manually
- **`npm run format`** — run Prettier manually
- **`npm run lint:fix`** — runs both (also called by the pre-push hook)
- `node_modules/` added to `.gitignore`
