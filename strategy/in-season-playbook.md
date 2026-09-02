# 📅 In-Season Playbook — Weekly Operating Procedure

Once the season starts, the agent shifts from draft prep to **winning weeks.**
The goal every week: **set the lineup with the best odds to win your matchup.**

---

## Weekly cadence

> ⚠️ **There is no single weekly lock.** Each platform locks a player at *that
> player's own game's kickoff*, not one Sunday deadline — a lineup slot with a
> Thursday Night Football (or Friday/international) player locks days before
> the rest of your roster. **Every week, before doing anything else, check the
> NFL schedule against your current roster and flag anyone playing early** so
> that slot gets decided on its own timeline, not lumped into "Sunday."

| Day | What the agent does |
|-----|--------------------|
| **Tue AM** | Waiver-wire report: who to add/drop, FAAB/priority guidance based on injuries, snap counts, and breakout usage from the week prior. |
| **Wed AM** | **Cross-check the week's NFL schedule against your roster.** Identify anyone on a Thursday/Friday/international early game in EITHER league and call it out explicitly — that decision needs to be made by Wednesday night/Thursday morning, before the injury-report cycle for the Sunday slate even finishes. Don't let a TNF starter get decided as an afterthought during the "final lineup call." |
| **Wed–Fri AM** | Morning briefs continue: injury designations (Q/D/O), practice reports, weather, Vegas lines moving — for the Sunday/Monday slate. |
| **Thu (before kickoff)** | **Early lock-in.** Confirm/finalize any lineup slot filled by a Thursday-night player — this is a real, separate deadline, not a preview. |
| **Sat AM** | Early lineup pass for any Saturday/international games (some weeks have them); flag decisions to make. |
| **Sun AM (lock day for the Sunday/Monday slate)** | **Final lineup call** for everyone NOT already locked Thursday. Optimal starters vs. your specific opponent, with the reasoning and the close calls. Loud alerts for any late inactives before each remaining player's individual kickoff. |
| **Mon (before kickoff)** | Confirm any Monday Night Football starters; Monday-night context for the matchup. |

## The weekly lineup decision

The agent sets your lineup using, in order:

0. **Kickoff timing** — is this player's game Thu/Fri/Sat (locks early) or
   Sun/Mon (locks with the main slate)? Decide and communicate early-locking
   slots on their own schedule, well before the "Sunday" pass.
1. **Health & status** — never start an OUT player; sweat every Questionable one.
2. **Matchup** — opponent defense strength vs. your player's position, pace,
   and game script (is the team likely trailing → more passing?).
3. **Vegas** — implied team totals and spreads are the single best public signal
   for expected scoring. High total + favored = good RB spot; high total +
   underdog = good pass-catcher spot.
4. **Volume/role** — target share, snap share, red-zone touches trump name value.
5. **Floor vs. ceiling by situation** — if you're the favorite, play floors; if
   you're the underdog that week, play ceilings. The agent adjusts to your
   matchup, not just raw projections.
6. **Weather** — wind >15–20 mph and heavy precip downgrade passing/kicking.

## Head-to-head awareness

The agent knows **who you're playing each week** and tailors advice: which of
your fringe starts have the highest ceiling to out-score a strong opponent, or
the safest floors to protect a lead. Tell it your opponent (or connect the
league) each week and it factors in their projected total.

## Streaming (10-team edge)

Because the league is shallow, streaming works:
- **QB / TE / D-ST / K:** the agent recommends the best weekly stream based on
  matchup, so you don't waste high picks or roster spots on them.
- **D/ST:** target defenses facing weak offenses, backup QBs, or bad weather.

## Trades & roster management

- The agent proposes **fair, win-now or sell-high** trades and evaluates any
  offer you receive (does it improve your starting lineup, not just your bench?).
- Buy-low / sell-high candidates flagged in briefs when value dislocates
  (e.g., a stud after two quiet weeks, or a backup starting for an injured RB).

## Playoff push

From ~Week 10, the agent tracks your standing, playoff odds, and the
**Week 15–17 schedule strength** of your players — so you can trade for players
with great fantasy playoff matchups.

---

### What the agent needs from you in-season
- Confirm each league is set up in its own `leagues/<league>/league-settings.md`
  (`leagues/chatt-espn/` and `leagues/family-yahoo/`). This playbook's rules
  apply to both — the settings file is what tells the agent *how* to score and
  build the roster for each one.
- Each week, tell it (or connect it to) your **opponent in each league** and
  any **roster moves** you've made so its picture stays accurate. The repo is
  its memory — we keep each league's own folder current, plus the shared
  `data/player-notes.md`.
