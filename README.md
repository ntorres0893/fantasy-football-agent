# 🏈 Fantasy Football Agent

A personal fantasy football assistant for the **2026 NFL season**. It preps you
for draft day, helps you make live picks, and keeps your lineup optimized all
season — even though you've been out of football for a while.

## Who this is for

Manager: **ntorres0893@gmail.com**
League: **10-team, STANDARD (non-PPR), ESPN, snake draft** · **Draft: Sept 3, 2026**
Status: First league in ~a decade — coming in cold and rebuilding football IQ fast.

## How it works

This repository **is the agent's memory.** A scheduled Routine runs every
morning in a fresh, ephemeral session, reads the committed files here, sources
the latest NFL/fantasy news, and emails a brief. Because each run starts clean,
everything the agent needs to know lives in these files — keep them current.

### The three phases

| Phase | What the agent does |
|-------|--------------------|
| **Pre-draft** (now → draft day) | Morning briefs: injuries, offseason moves, ADP shifts, camp storylines. Builds and refines the draft board. |
| **Draft day** | Live pick assistant. You feed it your draft slot + who's been taken each round; it recommends the pick using our board, tiers, roster construction, and value. |
| **In-season** | Morning syncs + weekly lineup optimization. Knows your matchup and roster, flags injuries/inactives, and sets the lineup with the best odds to win. |

## Repository map

```
profile/
  user-profile.md        You, your preferences, and how you like to draft
  league-settings.md     Scoring, roster slots, draft format (SINGLE SOURCE OF TRUTH)
strategy/
  draft-strategy.md      PPR 10-team strategy: tiers, roster build, positional plan
  draft-day-playbook.md  The live draft operating procedure (how we run pick-by-pick)
  in-season-playbook.md  Weekly cadence, lineup rules, waivers, trades
briefs/
  YYYY-MM-DD.md          Dated morning briefs (newest = latest intel)
data/
  draft-board.md         The ranked, tiered big board we draft from
  player-notes.md        Running notes: sleepers, busts, targets, avoids
  draft-log.md           Live record of every pick on draft day (created draft day)
agent/
  morning-brief-prompt.md    Standalone prompt the daily Routine runs
  draft-assistant-prompt.md  How to run the live draft assistant
  lineup-optimizer-prompt.md How to set the weekly lineup
```

## Getting the most out of it

- **Keep `league-settings.md` accurate.** Once you get your ESPN invite, confirm
  scoring, roster slots, and your draft pick. Draft strategy hinges on it.
- **Reply to the morning briefs.** If you tell the agent your reactions
  ("I love this sleeper", "I'm punting TE"), fold them into `player-notes.md`.
- **On draft day**, open a session and follow `strategy/draft-day-playbook.md`.
