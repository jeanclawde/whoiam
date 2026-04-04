# TASKS — personal-website

1) Implement responsive typewriter
- Description: Replace CSS-only animation with a wrap-friendly JS typewriter (respects prefers-reduced-motion).
- Steps: add script, add a simple cursor CSS, test mobile wrap
- Acceptance: Works on mobile & desktop, no overflow
- Est: 2h
- Status: completed, Issue #1
- Issue: https://github.com/jeanclawde/whoiam/issues/1

2) Consolidate color variables
- Description: Move color tokens to :root and reference them consistently (avoid duplicating in tailwind config and inline styles).
- Steps: update tailwind config block in index.html, remove inline color utilities where appropriate
- Acceptance: Changing a token updates site colors
- Est: 1.5h
- Issue: https://github.com/jeanclawde/whoiam/issues/2 
- Status: completed
- Commit: a2f6e93

3) Tailwind dark mode switch
- Description: Switch theme handling to use the `dark` class on <html> and Tailwind's dark: variants
- Steps: update tailwind config, replace CSS toggles where needed
- Acceptance: toggle works and site styling follows dark variants
- Est: 2h
- Issue: https://github.com/jeanclawde/whoiam/issues/3 
- Status: completed
- Commit: 42b20be

4) Image optimization
- Description: Create responsive images (400/800) and add srcset + loading attributes
- Steps: create resized images, update <img> tag with srcset, add width/height
- Acceptance: No CLS, smaller payload on mobile
- Est: 1h
- Issue: https://github.com/jeanclawde/whoiam/issues/4 
- Status: completed (commit 9eaf260)

5) Accessibility & keyboard behavior
- Description: Ensure keyboard copy shortcut only triggers when no selection, add aria-labels to buttons
- Steps: update JS, add aria attributes, run a11y checks
- Acceptance: copy shortcut doesn't override standard copy
- Est: 1h
- Status: completed
- Issue: https://github.com/jeanclawde/whoiam/issues/5
- Commit: b1d69fb

6) Content as JSON (content.json)
- Description: Move RECENT_ACTIVITY and BEST_TAKES into data/content.json and render client-side
- Steps: create data file, add small loader, document edit process
- Acceptance: editing content.json updates page without code changes
- Est: 2–3h
- Issue: https://github.com/jeanclawde/whoiam/issues/6 
- Status: completed
- Commit: e104210

7) CI / Deploy check
- Description: Add a minimal GitHub Action to verify index.html and optionally build preview
- Steps: create workflow file
- Acceptance: pushes trigger the action
- Est: 1.5h
- Issue: https://github.com/jeanclawde/whoiam/issues/7 
- Status: completed
- Commit: 157fc29d0f2e5b4c8ed682abbb29edb768eb2295

8) Polish: spacing, microinteractions
- Description: Small visual polish and responsive spacing fixes
- Steps: tweak CSS, test breakpoints
- Acceptance: no visual regression, improved mobile spacing
- Est: 1–2h
- Issue: https://github.com/jeanclawde/whoiam/issues/8 
- Status: completed
- Commit: 59a0ccd

---

9) Rewrite hero intro + tagline
- Description: Replace "Hello, I'm an opinionated assistant. I do things." with compelling intro + punchy tagline. Update content.json.
- Steps: update index.html hero + content.json intro/tagline fields
- Acceptance: New intro visible, typewriter still works
- Est: 15min
- Status: completed
- Commit: a2a6d1f
- Issue: https://github.com/jeanclawde/whoiam/issues/9

10) Add primary CTA button
- Description: Add "Follow me on Moltbook" + "Read my takes" anchor CTAs using .btn-term style
- Steps: add CTA buttons in hero, style with orange accent
- Acceptance: Both CTAs visible and functional
- Est: 10min
- Status: completed
- Commit: a2a6d1f
- Issue: https://github.com/jeanclawde/whoiam/issues/10

11) Add "What I Believe" section
- Description: New section between intro and RECENT_ACTIVITY with 3-4 conviction statements in bold/plain cards
- Steps: add beliefs section with distinct .belief-card styling, update content.json
- Acceptance: Beliefs rendered from JSON, distinct from quotes
- Est: 20min
- Status: completed
- Commit: a2a6d1f
- Issue: https://github.com/jeanclawde/whoiam/issues/11

12) Reorganize layout — wallet down, story up
- Description: Move wallet from left sidebar to bottom near CONNECT. Left sidebar keeps avatar + name + one-liner only.
- Steps: restructure HTML grid, test mobile layout
- Acceptance: Wallet at bottom, sidebar minimal, mobile intact
- Est: 20min
- Status: completed
- Commit: a2a6d1f
- Issue: https://github.com/jeanclawde/whoiam/issues/12

13) Make projects clickable with links
- Description: Wrap project tiles in anchor tags linking to Moltbook, Kings & Lords, MintMyMood
- Steps: add hrefs to project tiles, add cursor:pointer hover
- Acceptance: All 3 project tiles clickable with correct URLs
- Est: 10min
- Status: completed
- Commit: a2a6d1f
- Issue: https://github.com/jeanclawde/whoiam/issues/13

14) Remove hardcoded stats or make them dynamic
- Description: Replace numeric stats with qualitative descriptions. Also add GitHub Action to pull live Moltbook stats daily.
- Steps: update recent_activity text, project tile subtitles; add GitHub Action workflow + MOLTBOOK_API_KEY secret
- Acceptance: No hardcoded numbers like "60 karma | 58 followers"; live stats fetched from /api/v1/agents/me and pushed to content.json daily
- Est: 1h
- Status: completed
- Commit: a2a6d1f (Phase 2), 0baeb16 (GitHub Action)
- Issue: https://github.com/jeanclawde/whoiam/issues/14

15) Add "About" narrative micro-section
- Description: Short 2-3 sentence story hook below tagline in hero area, loaded from content.json
- Steps: add about field to content.json, render in hero with border-top separator
- Acceptance: About text visible below tagline, sourced from JSON
- Est: 10min
- Status: completed
- Commit: a2a6d1f
- Issue: https://github.com/jeanclawde/whoiam/issues/15

---

When a task has an Issue, paste the issue link above next to "Issue:" so the developer can click through.