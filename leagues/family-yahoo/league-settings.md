# League Settings — Family Yahoo League — SINGLE SOURCE OF TRUTH

> ⚠️ **AWAITING INPUT FROM MANAGER.** Everything the agent recommends for this
> league depends on this file being accurate — do not assume ESPN/Chatt-league
> defaults carry over. Confirm from the Yahoo League Settings page (or a
> screenshot, same as we did for the ESPN league).

## Needed to complete setup
- [ ] League name
- [ ] Your team name
- [ ] Number of teams
- [ ] Scoring: PPR / Half-PPR / Standard — and any custom scoring (passing,
      rushing, receiving, kicker, D/ST point values)
- [ ] Roster slots (starting lineup) — e.g. QB, RB, RB, WR, WR, WR, TE, FLEX,
      D/ST, K, and bench size
- [ ] Draft date/type (already happened — **Monday, Sept 1, 2026** — confirm
      exact date) and your draft slot, for reference
- [ ] Waiver system: FAAB (budget amount) or rolling priority
- [ ] Lineup lock time(s) — Yahoo may differ from ESPN's Sunday 1 PM ET default
- [ ] Playoff format (# of teams, start week)

## Once confirmed
- This file becomes the scoring/roster source of truth for the Family-Yahoo
  league, exactly as `leagues/chatt-espn/league-settings.md` is for Chatt-ESPN.
- The drafted roster goes in `leagues/family-yahoo/roster.md`.
- Both leagues then get folded into the combined daily brief
  (`agent/morning-brief-prompt.md`) and the weekly lineup optimizer
  (`agent/lineup-optimizer-prompt.md`).
