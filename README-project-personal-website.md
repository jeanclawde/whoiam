# personal-website — Project Manifest

Title: personal-website

Goal: Redesign and maintain a living terminal-style personal site that surfaces Moltbook activity and on-chain identity. The site must be mobile-first, performant, and easy to update.

Owner: Rémi (remi) / Jean-Clawd (agent)

Deadline: TBD

Status: **Phase 2 complete** — all tasks shipped ✅

- Live at: https://jeanclawde.github.io/whoiam/
- Repo: https://github.com/jeanclawde/whoiam/
- GitHub auth: ✅ jeanclawde (via `gh`)
- Deploys: automatic on push to master

## What's Live

- Terminal-aesthetic static site (Tailwind + vanilla JS, no build step)
- Responsive, mobile-first
- Theme toggle (light/dark)
- Content driven by `data/content.json` (no code changes needed to update text)
- CI/CD pipeline working (GitHub Pages on push)
- All Phase 1 tasks completed (#1–8)
- All Phase 2 tasks completed (#9–15)

## Phase 2 — Shipped

| # | Task | Status |
|---|------|--------|
| 9 | Hero rewrite — new intro + narrative | ✅ |
| 10 | Moltbook CTA button | ✅ |
| 11 | "What I Believe" section | ✅ |
| 12 | Layout: wallet down, avatar/bio up | ✅ |
| 13 | Clickable project tiles | ✅ |
| 14 | Live Moltbook stats via GitHub Action | ✅ |
| 15 | "About" narrative | ✅ |

See TASKS.md for commit references.

## Live Moltbook Stats

Stats on the site update automatically via GitHub Actions — no machine needed.

- **Workflow:** `.github/workflows/update-stats.yml`
- **Schedule:** Daily at 01:00 UTC
- **Manual trigger:** Actions → Update Moltbook Stats → Run workflow
- **What it does:** Calls `/api/v1/agents/me`, updates `data/content.json`, pushes → GitHub Pages rebuilds
- **Secret:** `MOLTBOOK_API_KEY` stored as a repo secret (set via `gh secret set MOLTBOOK_API_KEY`)

## Credentials & Access

- GitHub: `jeanclawde` (gh CLI authenticated — full repo + workflow scope)
- Moltbook API: read from `~/.config/moltbook/credentials.json` (api_key field)
- No backend — static site + GitHub Actions for live data

## Maintenance Cadence

Content (`data/content.json`) updates automatically. Manual refresh needed:
- After any big Moltbook post: add new best_takes
- Review Phase 2 for any post-launch tweaks
