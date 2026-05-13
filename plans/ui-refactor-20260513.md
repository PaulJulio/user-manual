# 📋 Implementation Plan: Modular UI Refactor

Refactor the User Manual UI to a modern, card-based modular layout with interactive accordions and adaptive color tokens for better readability and a professional "dashboard" feel.

## ## Approach
- **Adaptive Color Tokens:** Transition from hardcoded Tailwind classes to CSS variables defined in `@theme`. This allows for theme flexibility and centralized design control.
- **Card-based Layout:** Move away from a single flow of text to a structured "Information Architecture" using cards to group logical sections (e.g., Values, Scope, Learning).
- **Interactive Accordions:** Use native `<details>` and `<summary>` elements styled with Tailwind for "Interactive Accordions" to handle high-density information (like detailed lists) without overwhelming the user.
- **Modular Components:** Create Jekyll includes for `card.html` and `accordion.html` to ensure consistency across pages.

## ## Steps

1. **Define Adaptive Color Tokens** (15 min)
   - Modify `assets/css/main.css` to include a `@theme` block with CSS variables.
   - Define tokens for: `surface-primary`, `surface-secondary`, `border-muted`, `accent-primary`, `text-heading`, `text-body`.
   ```css
   @theme {
     --color-brand-indigo: #4f46e5;
     --color-surface-card: #ffffff;
     --color-surface-bg: #f8fafc;
     --border-radius-card: 1rem;
     /* ... */
   }
   ```

2. **Configure Tailwind v4 Compatibility** (10 min)
   - Ensure `tailwind.config.js` (if still needed) or `main.css` correctly maps these tokens.
   - Update `tailwind.config.js` to include the new tokens in the `extend` block if they aren't auto-detected by v4.

3. **Create Modular Components** (20 min)
   - Create `_includes/ui/card.html`:
     ```html
     <div class="bg-white border border-slate-200 rounded-2xl shadow-sm overflow-hidden hover:shadow-md transition-shadow">
       {% if include.title %}
       <div class="px-6 py-4 border-b border-slate-100 bg-slate-50/50">
         <h3 class="text-lg font-bold text-slate-900 m-0">{{ include.title }}</h3>
       </div>
       {% endif %}
       <div class="p-6">
         {{ include.content }}
       </div>
     </div>
     ```
   - Create `_includes/ui/accordion.html`:
     ```html
     <details class="group border-b border-slate-100 last:border-0">
       <summary class="flex justify-between items-center cursor-pointer py-4 list-none">
         <span class="font-semibold text-slate-800">{{ include.label }}</span>
         <span class="transition group-open:rotate-180">
           <svg class="w-5 h-5" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path d="M19 9l-7 7-7-7" /></svg>
         </span>
       </summary>
       <div class="pb-4 text-slate-600 prose prose-sm max-w-none">
         {{ include.content }}
       </div>
     </details>
     ```

4. **Refactor Page Layout** (20 min)
   - Modify `_layouts/page.html` to support a grid or stacked card layout.
   - Introduce a `content_blocks` system if possible, or update the main container to `bg-slate-50`.

5. **Content Migration & Enhancement** (30 min)
   - Update `index.md` to wrap "Who are you?" and "Scope" into cards.
   - Use accordions for the "What Stakeholders should come to you for" and "What Direct Reports should come to you for" sections to reduce vertical scrolling.

6. **Testing & Validation** (15 min)
   - Verify responsiveness on mobile/desktop.
   - Test interactive accordion transitions.
   - Check color token consistency across pages.

## ## Timeline
| Phase | Duration |
|-------|----------|
| Token Definition | 15 min |
| Config & Setup | 10 min |
| Component Dev | 20 min |
| Layout Refactor | 20 min |
| Content Update | 30 min |
| Validation | 15 min |
| **Total** | **~2 hours** |

## ## Rollback Plan
- Revert `assets/css/main.css` and `_layouts/page.html` to previous git state.
- Delete new `_includes/ui/` directory.

## ## Security Checklist
- [x] No sensitive data in UI
- [x] Validate HTML structure for accessibility (ARIA labels for accordions)
- [x] Ensure CSS/JS doesn't introduce XSS vectors (Jekyll handles markdown sanitization)
