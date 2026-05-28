# Lint Setup Todo

## Agent Diagnostics Fix Todo

## Checklist

- [x] 1. Review the listed diagnostics for the agent prompt
- [x] 2. Tighten review scope and no-code handling in the prompt
- [x] 3. Add explicit incomplete-assessment and checklist-fit guidance
- [x] 4. Simplify memory instructions to remove conflicts and privacy risk
- [ ] 5. Validate the edited prompt for syntax and targeted coverage

## Checklist

- [x] 1. Init npm (`npm init -y`)
- [x] 2. Install dev deps: `prettier`, `htmlhint`, `husky`, `lint-staged`
- [x] 3. Create `.htmlhintrc` config
- [x] 4. Create `.prettierrc` config
- [x] 5. Configure `lint-staged` and scripts in `package.json`
- [x] 6. Init husky and create `pre-push` hook

## Review

### Agent Diagnostics Fix Review

Updated the code review agent prompt to remove the ambiguous "recently modified" scope, require direct code before reviewing, and define how to report incomplete assessments.

Reduced the memory section to a short safety-focused summary so it no longer conflicts with review scope, reviewer persona, or the instruction not to surface private user data in shared project memory.

Clarified that "over-engineered" means complexity without a concrete requirement and added guidance for non-web runtimes where the default security checklist only partially applies.

## Review

Added full lint setup for this HTML/CSS project:

- **HTMLHint** validates HTML structure (duplicate IDs, tag pairing, doctype, etc.)
- **Prettier** auto-formats HTML/CSS on every push
- **Husky** wires up git hooks (`.husky/pre-push` and `.husky/pre-commit`)
- **`npm run lint`** — run HTMLHint manually
- **`npm run format`** — run Prettier manually
- **`npm run lint:fix`** — runs both (also called by the pre-push hook)
- `node_modules/` added to `.gitignore`
