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
>
> **This applies to BENCH contingency plans too, not just starters.** A bench
> player earmarked as insurance for an injury-questionable starter is only
> real insurance if his own game hasn't happened yet. If the backup's game
> already passed while he sat on the bench, he can't be retroactively
> inserted for points he already missed — check the contingency's kickoff
> time, not just the starter's, when deciding whether a "we have a backup"
> plan actually holds up. (Real example: a TE whose team played Wednesday
> can't cover a TE1 who becomes a late Sunday scratch — by then his own game
> is already over. The real fallback in that case is a waiver-wire streamer,
> claimed proactively once the starter looks shaky, not the bench name.)

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

## Post-game recap discipline (learned the hard way — Week 1, 2026)

> ⚠️ **Never call a stat line "good" from raw yardage/TD counting stats alone.**
> A first pass of Week 1 recaps described several modest-in-our-scoring
> performances as a "great week" purely from box-score yardage — without
> running a single stat line through either league's actual scoring formula,
> and without checking the real result against the league. The manager caught
> it: "we scored the least amount of points in the entire league." That's the
> failure mode to never repeat.

- **Always compute, never eyeball.** Before judging any performance, run it
  through that league's real scoring formula in
  `leagues/<league>/league-settings.md`. A 4-catch, 40-yard, no-TD WR game
  reads as "fine" on a highlight reel and can be genuinely weak in a
  reception-scoring league (or vice versa in a no-PPR league) — the raw stats
  don't tell you the fantasy verdict, the math does.
- **Never make a standings-relative claim without real data.** "Great week,"
  "worst in the league," "top scorer" — none of these are sayable from web
  search alone. Either compute an actual point total and compare it to real,
  known opponent/league numbers, or say plainly "I can estimate X points, but
  I don't have the real league total to compare it against."
- **There is no platform API access to either league.** The agent cannot see
  actual final scores, opponent lineups, or standings directly — ever. When a
  recap needs that ground truth (a final score, whether a matchup was won,
  where the team ranks), **ask the manager** for it (a screenshot or a quick
  paste of the final score/standings) rather than estimating from search.
- **Treat search results for a game that's live or very recently finished as
  unreliable, not authoritative.** Live/recent-game search results can be
  stale, inconsistent, or flatly contradictory across queries (one query
  returning an early-game snapshot, another a late-game or final-sounding
  one that doesn't match). When results disagree with each other, say so
  explicitly and ask the manager for the real number rather than picking
  whichever result sounds most confident.
- Once real point totals are known (from the manager, or a stable/settled box
  score), state them explicitly per player **and** as a team total — not just
  narrative color like "huge game" or "quiet day."

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
- **After games finish, share the actual final score/result and, when it
  matters, the league standings.** The agent has no API access to either
  platform — it cannot see real final scores or standings on its own, only
  what it can compute from public web data (which is often incomplete or
  wrong for very recent games). A quick screenshot or paste turns an estimate
  into a fact.
