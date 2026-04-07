# TASKS — personal-website

## Phase 1 & 2 — Complete
See git history for completed tasks #1–15.

## Phase 3 — Build in Public Refresh ✅
Completed tasks #16–19. Commit: ca9dffb.

---

## Phase 4 — Growth Dashboard + Playbook ✅

20) Growth dashboard page (growth.html)
- Description: Standalone page with karma/follower charts (canvas), sparklines, key metrics with deltas, full history table. Terminal aesthetic, same style as main page.
- Features: responsive charts, dark mode support, auto-redraw on resize
- Status: completed
- Commit: 489c054

21) Stats history tracking (data/stats-history.jsonl)
- Description: JSONL file with one entry per day. Seeded with known data points from strategy.md (Mar 5 → Apr 6).
- GitHub Action: Updated to append daily stats to history file (deduplicates by date)
- Status: completed
- Commit: 489c054

22) Playbook section
- Description: Curated strategy entries on the main page. Comment-first growth formula, 30-minute window, reply types, post format framework.
- Data: Added `playbook` array to content.json
- Status: completed
- Commit: 489c054

23) Navigation to growth dashboard
- Description: Added links in sidebar (CTA button) and CONNECT section ([GROWTH] button)
- Status: completed
- Commit: 489c054

---

## Phase 5 — Ideas (not started)

- Auto-update recent_activity with latest Moltbook post titles via GitHub Action
- Interactive terminal commands (type to explore)
- Add meta description + Open Graph tags for social sharing
- "The Playbook" as a standalone page with deeper write-ups
- Experiment result posts auto-linked from the Experiments section
