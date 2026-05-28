# VIDE·AI Landing Page — Design Spec

## Context

A single-file HTML educational website for an AI learning platform called VIDE·AI. The goal is a beautiful, designer-agency-quality landing page that uses CSS art in place of real images — no external assets, no frameworks, no JavaScript dependencies. Dark futuristic aesthetic.

## Visual Style

- **Background:** `#0a0a0f` (deep near-black)
- **Accent palette:** Purple `#7c3aed` / `#a78bfa`, Cyan `#0ea5e9` / `#38bdf8`, Green `#10b981` / `#34d399`
- **Gradients:** Linear purple→cyan for primary CTAs; radial glow orbs for ambient depth
- **Typography:** System font stack (`-apple-system, Inter, sans-serif`); heavy weights (800–900), tight letter-spacing for headlines
- **Border language:** `1px solid #ffffff0d` (very subtle) for cards; `#7c3aed44` for highlighted borders
- **Image stand-ins:** CSS gradient rectangles with radial highlight spots — no `<img>` tags

## Page Structure (single `index.html`)

### 1. Nav
- Left: `VIDE·AI` wordmark — "VIDE" in purple→cyan gradient, "·AI" in white
- Center: `Courses`, `About`, `Community` links in muted `#888`
- Right: `Get started free` button with purple→cyan gradient background
- Bottom border: `1px solid #ffffff0a`
- Sticky at top

### 2. Hero
- Ambient effect: large radial gradient orb centered behind text (purple), secondary orb bottom-left (cyan)
- Pill badge: `AI-POWERED EDUCATION` with pulsing dot, subtle purple border
- H1: `Master AI.` + `Build what's next.` — second line uses gradient text
- Subtext: one sentence about structured courses, `color: #8888aa`
- Two CTA buttons: primary gradient + ghost "▶ Watch intro"
- Stats row below a divider: `42k+ Students`, `98% Satisfaction`, `12 Courses`

### 3. Features (3-column grid)
Each card: subtle background `#ffffff06`, faint border, rounded corners

| Icon | Title | Body |
|------|-------|------|
| ⚡ (purple bg) | Learn at your pace | Self-paced modules, no deadlines |
| 🧠 (cyan bg) | Expert instructors | Built by researchers and practitioners |
| 🎯 (green bg) | Hands-on projects | Exercises and projects in every course |

### 4. Featured Courses (3-column grid)
Section header: `FEATURED COURSES` tag + `Start your AI journey` title

| Thumb gradient | Emoji | Tag | Title | Level |
|---|---|---|---|---|
| Purple deep→light | 🤖 | BEGINNER · 6 HRS | Introduction to AI | Free |
| Cyan dark→light | 📊 | BEGINNER · 8 HRS | Machine Learning Basics | Free |
| Green dark→light | 🧬 | INTERMEDIATE · 10 HRS | Neural Networks | Free |

Each card: dark `#0f0f1a` background, gradient thumbnail with radial highlight, course metadata below.

### 5. Footer
- Left: `VIDE·AI` logo (same gradient treatment)
- Center: `Courses`, `About`, `Privacy` links
- Right: `© 2025 Vide AI`
- Top border: `1px solid #ffffff08`

## Technical Constraints

- **Single file:** Everything in one `index.html` — inline `<style>` and no external resources
- **No JavaScript** (except optional smooth scroll)
- **No real images** — CSS gradients and emoji serve as all visual media
- **Responsive:** Desktop-first, basic mobile stacking via media query at 640px
- **Font:** System stack only — no Google Fonts import

## Verification

1. Open `index.html` directly in a browser (no server needed)
2. Confirm all 5 sections render without external requests (check DevTools Network tab — should be empty)
3. Resize to mobile width — cards should stack to single column
4. Confirm gradient text renders in Chrome, Firefox, and Safari
