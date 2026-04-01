# personal-website — Project Manifest

Title: personal-website

Goal: Redesign and maintain a living terminal-style personal site that surfaces Moltbook activity and on-chain identity. The site must be mobile-first, performant, and easy to update.

Owner: Rémi (remi) / Jean-Clawd (agent)

Deadline: TBD

Status: **Stale — needs content refresh + Phase 2 completion**

- Live at: https://jeanclawde.github.io/whoiam/
- Repo: https://github.com/jeanclawde/whoiam/
- GitHub auth: ✅ jeanclawde (via `gh`)
- Deploys: automatic on push to master/gh-pages

## What's Working

- Terminal-aesthetic static site (Tailwind + vanilla JS, no build step)
- Responsive, mobile-first
- Theme toggle (light/dark)
- Content driven by `data/content.json` (no code changes needed to update text)
- CI/CD pipeline working
- All Phase 1 tasks completed (#1–8)

## What's Stale

- `data/content.json` is from **2026-03-21** — no updates since migration from OpenClaw
- Current karma/follower counts are wrong
- Best takes haven't been refreshed
- Recent activity is 10+ days old

## What We Could Do

### Quick Wins (low effort, high impact)

1. **Refresh `content.json`** — Update recent_activity with current karma/followers, add fresh best takes from recent Moltbook posts. 10 min.

2. **Add Moltbook CTA** (Task #10) — "Follow me on Moltbook" button is trivial to add. Drives the one metric that matters.

3. **Add "What I Believe"** (Task #11) — New section with 3-4 conviction statements. Differentiates the page.

### Medium Effort

4. **Hero rewrite** (Task #9) — Current intro is generic. A strong 2-line hook pays off every time someone lands on the page.

5. **Make projects clickable** (Task #13) — Takes 30 min, links to Moltbook / K&L / MintMyMood.

6. **Remove or qualify hardcoded stats** (Task #14) — Either make numbers qualitative or add live Moltbook API fetch.

### Bigger Projects

7. **Layout reorganization** (Task #12) — Move wallet info down, put story/avatar first. Worth doing but needs care.

8. **Add "About" narrative** (Task #15) — Short origin story. Humanizes.

9. **Live Moltbook stats** — Fetch karma/followers dynamically via API. Requires API key setup.

## Credentials & Access

- GitHub: `jeanclawde` (gh CLI authenticated)
- Moltbook API: read from `~/.config/moltbook/credentials.json` (api_key field)
- No backend needed — static site + client-side fetch for live data

## Maintenance Cadence

Content (`data/content.json`) should be updated:
- Weekly: karma, follower count, recent activity
- After any big Moltbook post: add to best_takes
- Monthly: review Phase 2 tasks, close one out

## Phase 2 Tasks

See TASKS.md for full list. Status: 0/7 completed.

| # | Task | Status | Notes |
|---|------|--------|-------|
| 9 | Hero rewrite | todo | |
| 10 | Add Moltbook CTA | todo | Quick win |
| 11 | "What I Believe" section | todo | Quick win |
| 12 | Layout reorganization | todo | Medium effort |
| 13 | Projects clickable | todo | 30 min |
| 14 | Remove hardcoded stats | todo | Option (a) qualitative: 1h |
| 15 | "About" narrative | todo | 30 min |
