# Live Draft Assistant — Run Prompt

Use this when the draft is happening. Kick off with:
*"It's draft day — let's run the playbook."*

## Setup (once, at the start)
1. Read `leagues/chatt-espn/draft-day-playbook.md` (the operating procedure),
   `leagues/chatt-espn/draft-board.md` (the tiered big board), `data/player-notes.md`, and
   `leagues/chatt-espn/league-settings.md` (confirm slot + roster slots).
2. Confirm the manager's **draft slot** (1–10) and compute their pick numbers
   for a 10-team snake (e.g., slot 4 → picks 4, 17, 24, 37, 44, …).
3. Create/open `leagues/chatt-espn/draft-log.md` and prepare to record every pick.
4. Give the manager their **slot game plan**: likely target + 2 fallbacks at
   each of their next few picks.

## During the draft
- The manager reports picks as they happen ("Pick 7: Player X" or "since my last
  pick: A, B, C went"). **Remove each named player from the available board** and
  log it in `leagues/chatt-espn/draft-log.md`.
- Track the manager's roster and remaining needs continuously.
- When the manager says "I'm on the clock," return the recommendation card from
  the playbook (pick, why, runner-up, pivot, roster-after). Be fast — they're on
  a clock.
- Flag positional **runs** and **tier cliffs** proactively.
- Respect overrides instantly ("take X anyway") and re-plan from the new state.

## After the draft
- Save the final roster and write a **team review** (strengths, weaknesses,
  stacked byes, Week 1 waiver targets) into `leagues/chatt-espn/draft-log.md`.
- Commit everything and switch to in-season mode.

## Key principles (from the playbook)
- Tier scarcity > raw ranking. Value vs. ADP. RB/WR heavy early. Wait on QB/TE
  (unless elite tier falls). D/ST + K last two rounds only. Chase ceilings —
  it's a shallow 10-team league where stars win.
