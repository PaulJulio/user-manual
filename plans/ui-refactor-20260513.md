# 📋 Implementation Plan: Verbatim CSS-Only UI Refactor

Refactor the User Manual UI to a modern, card-based modular layout using CSS-only techniques to ensure 100% content fidelity. No prose will be rewritten or summarized.

## ## Approach
- **Adaptive Color Tokens:** Transition to CSS variables in `@theme` for a professional "Relentless Excellence" palette.
- **CSS-Driven Cards:** Instead of modifying Markdown files, use CSS selectors and layout adjustments to style sections (headers and their content) as cards.
- **Verbatim Integrity:** Not a single word of the original Markdown will be changed. The "Information Architecture" will be achieved purely through visual styling.
- **Modern Sidebar:** Refine the navigation and footer to align with the new high-signal aesthetic.

## ## Steps

1. **Define Adaptive Color Tokens** (15 min)
   - Update `assets/css/main.css` with `@theme` variables for `surface-bg`, `surface-card`, `text-heading`, etc.
   - Ensure a clean, high-contrast dashboard aesthetic.

2. **Tailwind v4 / Typography Refinement** (15 min)
   - Configure the typography plugin to support the card-based structure.
   - Adjust spacing and margins to create a "grid" feel even without explicit grid containers in the HTML.

3. **Layout Refactor (Verbatim Stage)** (20 min)
   - Update `_layouts/default.html` to set the dashboard background (`bg-surface-bg`).
   - Update `_layouts/page.html` to provide a clear container for the verbatim content.

4. **CSS-Only Card Styling** (30 min)
   - Use CSS in `main.css` to style `h3` headers as card headers and the following content as card bodies.
   - Use techniques like `border-t`, `shadow`, and `rounded-xl` applied to the `h3` and its subsequent siblings (or a Jekyll wrapper if absolutely necessary for the card effect).

5. **Validation & Content Audit** (15 min)
   - Run `npm run build`.
   - Use `diff` to verify that the Markdown files remain identical to their current state.
   - Verify that the UI looks modern and is easier to consume.

## ## Timeline
| Phase | Duration |
|-------|----------|
| Token Definition | 15 min |
| Layout Refactor | 35 min |
| CSS Styling | 30 min |
| Validation | 15 min |
| **Total** | **~1.5 hours** |

## ## Rollback Plan
- `git checkout -- .` to revert all changes.
