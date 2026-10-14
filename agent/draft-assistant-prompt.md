# Live Draft Assistant — Run Prompt

Use this when the draft is happening. Kick off with:
*"It's draft day — let's run the playbook."*

## ⚠️ Lesson from 2026 (manager, 10/14): our draft was a miss
We didn't look at **prior seasons' actual highest fantasy scorers** before
drafting. Before the 2027 draft, both leagues:
- Pull the **final 2026 fantasy-points leaders by position** (both PPR for
  Chatt-ESPN and standard for Family-Yahoo), plus points per game and games
  played. Also pull 2-3 year trends for repeat top scorers.
- Build the board from **proven production first**, then adjust for
  role/age/injury. Projections and hype are tiebreakers, not the
  foundation.
- Flag any player we rank well above his prior-year finish and make the
  case explicitly.
- 2026 evidence that this matters (as of Week 5): Trey McBride (TE1, 10+
  PPR every week), Jaxon Smith-Njigba, Jahmyr Gibbs, Bijan, Josh Allen and
  Spencer Shrader (top K). Proven producers kept producing. Our
  RB-depth-by-volume approach (Achane, Hall, Barkley) got hit by injuries.

## Setup (once, at the start)
0. **Load last season's final fantasy-points leaders** (see lesson above)
   and cross-check the board against them.
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
