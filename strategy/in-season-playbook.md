# 📅 In-Season Playbook — Weekly Operating Procedure

Once the season starts, the agent shifts from draft prep to **winning weeks.**
The goal every week: **set the lineup with the best odds to win your matchup.**

---

## Weekly cadence

| Day | What the agent does |
|-----|--------------------|
| **Tue AM** | Waiver-wire report: who to add/drop, FAAB/priority guidance based on injuries, snap counts, and breakout usage from the week prior. |
| **Wed–Fri AM** | Morning briefs continue: injury designations (Q/D/O), practice reports, weather, Vegas lines moving. |
| **Sat AM** | Early lineup pass for any Sat/international games; flag decisions to make. |
| **Sun AM (lock day)** | **Final lineup call.** Optimal starters vs. your specific opponent, with the reasoning and the close calls. Loud alerts for any late inactives before the 1 PM lock. |
| **Mon** | Monday-night context; set expectations vs. opponent's remaining players. |

## The weekly lineup decision

The agent sets your lineup using, in order:

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
