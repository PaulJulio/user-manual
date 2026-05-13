# 📋 Implementation Plan: Modular UI Refactor (v2 - High-Signal Synthesis)

Refactor the User Manual UI to a modern, card-based modular layout that acts as a "Dashboard" for Paul's professional Operating System. This design is directly informed by his roots as a **US Marine** and **9-1-1 Dispatcher**, his focus on **AI Mastery**, and his **"No Surprises"** philosophy.

## ## Approach
- **Adaptive Color Tokens:** Transition to CSS variables in `@theme` using a "Relentless Excellence" palette: deep slate, indigo accents, and high-contrast text to ensure **Semantic Precision** is never clouded by poor legibility.
- **Bento Grid Architecture:** Structure the 8 core sections into a modular grid. High-leverage categories (Identity, Scope, Decision-Making) will take larger "Hero Cards," while others (Rhythm, Personal Context) use supporting cards.
- **Root-Value Mapping:** Create a "Roots & Values" component that visualizes how formative experiences (Marines, 9-1-1, Large Family) directly inform the "Top 3 Values" and "Stakeholder Scope."
- **Interactive "AI-Ready" Accordions:** Use `<details>` for the "Master List" of granular questions. This maintains **High-Signal Synthesis** for human readers while keeping the full Markdown accessible for AI tools (following the "AI-Ready Documentation" rule).
- **Personalized Visual Identity:** Incorporate subtle design cues for his passions (Puget Sound boating, SF Giants) without cluttering the professional signal.

## ## Steps

1. **Define Adaptive Color Tokens** (15 min)
   - Update `assets/css/main.css` with `@theme` variables.
   - Set `--color-brand-indigo` and `--color-surface-bg: #f8fafc` (slate-50).
   - Ensure color contrast meets AA standards for "Excellence."

2. **Tailwind v4 / Typography Optimization** (15 min)
   - Configure `@tailwindcss/typography` to handle nested cards.
   - Add a custom `prose-ai` class for the "AI-Ready" documentation sections.

3. **Develop Modular UI Components** (30 min)
   - `_includes/ui/card.html`: Support for titles, icons, and flexible content.
   - `_includes/ui/accordion.html`: Native HTML structure with custom Tailwind markers.
   - `_includes/ui/roots-map.html`: Specialized component for the Marine/Dispatcher -> Value mapping.

4. **Refactor Page Layouts** (20 min)
   - `_layouts/page.html`: Switch to a max-width container with a subtle card-stacking effect on mobile.
   - `_layouts/default.html`: Refine the sidebar to highlight the "8-Section Dashboard."

5. **Content Migration & Strategic Synthesis** (45 min)
   - **Identity Card:** Merge elevator pitch and 9-1-1/Marine roots.
   - **Scope Card:** Use the "Alignment Map" component to show Stakeholder vs. Direct Report value.
   - **Personal Card:** Use a sub-grid for Boating, Baseball, and Family context.
   - **Quirks/Stress:** Use accordions for "Pet Peeves" and "Stress Signals."

6. **Testing & Validation** (15 min)
   - Run `npm run build` and verify all draft content is correctly rendered.
   - Check responsiveness on mobile (essential for "on-the-go" stakeholders).

## ## Timeline
| Phase | Duration |
|-------|----------|
| Token & Config | 30 min |
| Component Dev | 30 min |
| Layout Refactor | 20 min |
| Strategic Content Update | 45 min |
| Validation | 15 min |
| **Total** | **~2.5 hours** |

## ## Rollback Plan
- Revert via `git checkout main` (current branch is `design/color-and-layout`).
- Remove `_includes/ui/` and revert `assets/css/main.css`.

## ## Security Checklist
- [x] No PII exposed beyond what's in the draft files.
- [x] Maintain "AI-Ready" accessibility standards.
