# 🏈 Fantasy Football Agent

A personal fantasy football assistant for the **2026 NFL season**, covering
**two leagues** — preps for draft day, helps make live picks, and keeps
lineups optimized all season, even coming in cold after ~a decade away.

## Who this is for

Manager: **ntorres0893@gmail.com**

| League | Platform | Team | Status |
|--------|----------|------|--------|
| Chatt's Original Cool Kids | ESPN, 10-team, FULL PPR, snake | Claude Me Daddy | Slot 8 · Drafts **Sept 3, 2026** |
| Family league | Yahoo | *(TBD)* | Drafted **Sept 1, 2026** — settings/roster being entered |

One combined daily/weekly email covers both leagues.

## How it works

This repository **is the agent's memory.** A scheduled Routine runs daily in a
fresh, ephemeral session, reads the committed files here, sources the latest
NFL/fantasy news, and emails a combined brief. Because each run starts clean,
everything the agent needs to know lives in these files — keep them current.

**Shared across both leagues:** real NFL news (injuries, roles, depth charts)
is identical regardless of league, so it lives once in `data/player-notes.md`.
**League-specific:** scoring, roster, draft board/log, and lineup decisions
each live under that league's own `leagues/<league>/` folder — never mixed.

### The phases (tracked per league)

| Phase | What the agent does |
|-------|--------------------|
| **Pre-draft** (Chatt-ESPN only, now → Sept 3) | Morning briefs: injuries, offseason moves, ADP shifts, camp storylines. Builds and refines the draft board. |
| **Draft day** (Chatt-ESPN, Sept 3) | Live pick assistant. You feed it your draft slot + who's been taken each round; it recommends the pick using the board, tiers, roster construction, and value. |
| **In-season** (Family-Yahoo now; Chatt-ESPN from Sept 3) | Morning/weekly syncs + lineup optimization. Knows your matchup and roster per league, flags injuries/inactives, sets the lineup with the best odds to win. |

## Repository map

```
profile/
  user-profile.md              You, your preferences, both leagues at a glance
leagues/
  chatt-espn/                  ESPN league — "Chatt's Original Cool Kids"
    league-settings.md         Scoring, roster slots, draft format (SOURCE OF TRUTH)
    draft-board.md             Ranked, tiered big board (pre-draft)
    watch-list.md              Draft guide by position, high→low (pre-draft)
    draft-strategy.md          PPR 10-team strategy: tiers, roster build, plan
    draft-day-playbook.md      Live draft operating procedure
    slot-cheat-sheet.md        Per-slot game plans (slot 8 confirmed)
    mock-draft-log.md          Standing lessons from every mock draft
    draft-log.md               Live pick record + final roster (created draft day)
    draft-day-cheat-sheet-slot8.pdf   Printable one-page draft reference
  family-yahoo/                Yahoo family league
    league-settings.md         Scoring, roster slots (⚠️ awaiting manager input)
    roster.md                  Drafted roster + moves log (⚠️ awaiting manager input)
strategy/
  in-season-playbook.md        SHARED weekly cadence, lineup rules, waivers, trades
data/
  player-notes.md              SHARED running NFL news: sleepers, busts, injuries
briefs/
  YYYY-MM-DD.md                Dated combined briefs (newest = latest intel)
agent/
  morning-brief-prompt.md      Standalone prompt the daily Routine runs (both leagues)
  draft-assistant-prompt.md    How to run the live draft assistant (Chatt-ESPN)
  lineup-optimizer-prompt.md   How to set the weekly lineup (either/both leagues)
```

## Getting the most out of it

- **Keep each league's `league-settings.md` accurate.** Scoring and roster
  rules drive every recommendation — never assume the two leagues match.
- **Reply to the briefs.** Reactions ("I love this sleeper", "I'm punting TE")
  fold into `data/player-notes.md` (shared) or the relevant league's own notes.
- **On Chatt-ESPN draft day (9/3)**, open a session and follow
  `leagues/chatt-espn/draft-day-playbook.md`.
- **Weekly, for either league**, say *"Set my Week N lineup"* (both) or name
  the league to get just one.
