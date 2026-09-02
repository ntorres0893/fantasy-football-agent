# League Settings — Family Yahoo League — SINGLE SOURCE OF TRUTH

> ⚠️ Everything the agent recommends for this league depends on this file.
> Confirmed from the Yahoo League Settings page (manager-provided, 9/2/2026).

## Confirmed

| Setting | Value |
|---------|-------|
| Platform | Yahoo |
| League ID | 1383677 |
| League name | **Family Fantasy Football** |
| **Your team** | **Claude Me Daddy** *(same name as the Chatt-ESPN team — don't confuse the two leagues when talking rosters!)* |
| Teams | **8** (shallower than Chatt-ESPN's 10 → deeper/better waiver wire) |
| Scoring type | Head-to-Head (points-based) |
| Draft type | Live Standard Draft |
| **Draft date** | **Monday, August 31, 2026, 10:00 PM EDT** ✅ (already happened) |
| Pick time | 1 minute |
| Playoffs | 6 of 8 teams make it — Weeks 15, 16, 17 (ends Mon Jan 4) |
| Waivers | Reverse order of standings · weekly waivers process Tuesday (game time) · 2-day waiver claim window |
| Trades | Unlimited · league-vote review · 2-day reject window · trade deadline **Nov 28, 2026** |
| Draft pick trades | Not allowed |
| IR slot | Yes (1) |

## ⚠️ Scoring type — likely STANDARD (0 PPR), please confirm

The settings you provided list **Receiving Yards** and **Receiving TDs** as scored
categories, but there is **no "Reception" line item** anywhere in the offense
table — that's the tell for a PPR league, and it's absent here. Reading this as
**standard scoring: 0 points per reception.** This is the **opposite** emphasis
of the Chatt-ESPN league (FULL PPR) — if I've misread this, it changes RB/WR
rankings substantially, so **flag it if you see a "Reception" line I missed.**

## Full scoring (as provided)

**Passing**
- 25 yds/pt (0.04/yd), **+2 bonus at 300 yds, +5 bonus at 400 yds**
- Passing TD: **6** (Yahoo default is 4 — this league pays a full point extra per
  passing TD, a notable QB boost, especially for high-volume/high-TD passers)
- Interception thrown: **−1**

**Rushing**
- 10 yds/pt (0.1/yd), **+2 bonus at 100 yds, +5 bonus at 150 yds**
- Rushing TD: **6**

**Receiving**
- 10 yds/pt (0.1/yd), **+2 bonus at 100 yds, +5 bonus at 150 yds**
- Receiving TD: **6**
- **No point-per-reception** (see caveat above)

**Misc offense**
- Return TD: 6 · 2-pt conversion: 2 · Fumble lost: **−2** · Offensive fumble
  return TD: 6

**Kicker**
- FG 0–19: 3 · FG 20–29: 3 · FG 30–39: 4 · FG 40–49: 5 · FG 50+: 6 · PAT: 1

**Defense/Special Teams**
- Sack: **2** (Yahoo default is 1 — doubled, favors high-sack defenses) · INT: 2 ·
  Fumble rec: 2 · Def/ST TD: 6 · Safety: 2 · Block kick: 2 · Extra point
  returned: 2
- Points allowed: 0 = 10, 1–6 = 7, 7–13 = 4, 14–20 = 1, 21–27 = 0 (implied),
  28–34 = −1, 35+ = −4

## What this scoring means for roster decisions

- **No PPR → volume-via-catches doesn't matter, yardage and TDs do.** A
  high-target, short-route possession receiver is worth much less here than in
  the Chatt-ESPN league; a big-play deep threat or a bell-cow rusher is worth
  **more.**
- **Big statistical games are rewarded extra** (the 100/150 rush-rec and
  300/400 pass-yd bonuses) — favors true workhorse RBs and every-week WR1s over
  committee/timeshare guys, since hitting the bonus tier requires volume.
- **Passing TDs at 6 pts** meaningfully boosts high-TD-rate and rushing QBs
  (dual-threat QBs double-dip: passing TD bonus + rushing yardage bonus).
- **Doubled sack scoring** makes DEF streaming lean toward high-pressure
  defenses even more than usual.

## Roster positions (starting lineup)
**QB, WR, WR, RB, RB, TE, W/T (WR/TE flex — no RB in flex), K, DEF**
+ 4 bench (BN) + 1 IR = 14 total roster spots.

⚠️ **No RB-eligible flex** — only 2 RB starting slots exist, period. This makes
RB depth on the bench more valuable than usual, since a 3rd RB can never start
even if it outscores your WR2.

## Draft-day logistics
- Already drafted (8/31). Full roster in `leagues/family-yahoo/roster.md`.
- This league goes straight to weekly lineup-setting — see
  `strategy/in-season-playbook.md` and `agent/lineup-optimizer-prompt.md`.
