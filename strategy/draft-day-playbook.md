# 🎯 Draft-Day Playbook — Live Operating Procedure

This is the exact procedure we run **during your live draft**. Open a Claude
session, point it at this repo, and say: *"It's draft day — let's run the
playbook."* The agent loads your board, your slot, and tracks every pick.

---

## Before the draft (do this the morning of)

1. **Confirm league settings** in `profile/league-settings.md` — especially your
   **draft slot** and roster requirements.
2. Run a final morning brief for last-minute injury/inactive news.
3. **Read `strategy/mock-draft-log.md`** — apply the "Standing lessons" from every
   prior mock (WR depth discipline, bye-week checks, back-to-back turn strategy,
   staying flexible on QB timing, etc.) to the real draft.
4. The agent generates a **slot-specific game plan**: your likely targets at each
   of your picks, plus 2–3 fallback names per pick in case they're gone.
5. Open `data/draft-log.md` (created fresh on draft day) to record picks.

---

## The information you feed the agent, in real time

You are the agent's eyes on the ESPN draft room. Each time a pick happens, tell
the agent in the simplest form:

- **"Pick 7: Player X."** (any pick, any team)
- Or just the picks since your last turn: *"Since my last pick: A, B, C, D went."*
- When it's your turn: **"I'm on the clock."**

The agent maintains the full draft board, so it always knows who's left. You do
**not** need to tell it whole rosters — just who came off the board.

## What the agent gives you on every one of your picks

When you're on the clock, the agent returns a fast, scannable recommendation:

```
🟢 PICK: <Player> (<POS>, <TEAM>) — Tier <n>
   Why: <1–2 lines: value vs ADP, roster fit, scarcity>
   Runner-up: <Player> — <why you'd take them instead>
   Punt/pivot: <if a run is happening, the alternative approach>
   Roster after: QB_ RB__ WR__ TE_ FLEX_ | needs: <what's still open>
```

It decides using, in priority order:

1. **Tier scarcity** — is this the last player in a tier? (Take before the cliff.)
2. **Value vs. ADP** — are we getting a discount, or reaching?
3. **Roster construction** — positional needs and the FLEX math (see below).
4. **Upside for a 10-team league** — shallow league ⇒ chase ceilings; stars win.
5. **Bye-week / stacking** considerations (light — don't overweight early).

---

## Roster-construction rules of thumb (10-team PPR)

Starters assumed: **QB / RB / RB / WR / WR / TE / FLEX / D-ST / K** + 7 bench.

- **Rounds 1–5: best player available, RB/WR heavy.** In PPR, elite WRs and
  pass-catching RBs are gold. Do **not** draft QB, TE (unless elite tier), D/ST,
  or K here.
- **Target 5–6 of your first 7 picks on RB/WR.** You start up to 5 of them
  (2 RB, 2 WR, FLEX) and need depth for byes/injuries.
- **QB:** In a 10-team, 1-QB league, wait. There are ~20 startable QBs for 10
  starting spots — stream or grab a mid-tier guy rounds 8–11. Only pay up if a
  truly elite dual-threat QB falls to a value price.
- **TE:** Either pay for the elite tier early (there's a steep cliff — the board
  will show it) **or** wait and stream. Avoid the mushy middle.
- **D/ST + K:** **Last two rounds. Never earlier.** Stream them weekly in-season.
- **Handcuffs:** In a 10-team league, prioritize high-upside standalone players
  over handcuffing your own RB. Grab a handcuff only late and only for a truly
  workhorse back.

## When a "run" happens

If 3+ of one position go in a short span, a tier is about to empty. The agent
will flag: *"RB run — Tier 3 has 2 left, and you don't pick for 6 spots. Take
one now or accept the drop to Tier 4."* You decide; it lays out the tradeoff.

## Reach vs. value discipline

We take **best value by tier**, not by name. If your gut wants a player going a
full round early, the agent will say so and offer the disciplined alternative —
but it's your pick. You can always override; just say "take X anyway."

---

## After the draft

- The agent saves the final roster to `data/draft-log.md` and writes a
  **team review**: strengths, weaknesses, which bye weeks are stacked, and the
  **first week's waiver targets** to shore up holes.
- We flip into **in-season mode** (`strategy/in-season-playbook.md`).
