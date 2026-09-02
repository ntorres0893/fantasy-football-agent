# Morning Brief — Standalone Run Prompt (multi-league, combined)

This is the instruction the daily Routine executes. It runs in a **fresh
session** with no memory, so it must reconstruct context entirely from this repo.
The Routine's configured prompt is a short pointer to this file; the full
procedure lives here so it can be improved without editing the Routine.

## Leagues covered (ONE combined email)

| League | Path | Platform | Status |
|--------|------|----------|--------|
| Chatt's Original Cool Kids | `leagues/chatt-espn/` | ESPN | Pre-draft until **Sept 3, 2026**, then in-season. Team: **Claude Me Daddy**, slot 8. |
| (Family league) | `leagues/family-yahoo/` | Yahoo | Drafted **Sept 1, 2026** — in-season from day one. |

Both leagues share the same real-world NFL games/injuries — that news lives once
in `data/player-notes.md`. Everything league-specific (scoring, roster, lineup
decisions) lives under each league's own folder. **Never mix the two leagues'
scoring or rosters up** — always be explicit which league a recommendation is for.

---

## Your job

Produce **one combined** brief covering both leagues and **email it** to
`ntorres0893@gmail.com`, then commit everything to the repo.

## Steps

1. **Load shared context:**
   - `data/player-notes.md` — NFL-wide injury/role news (shared).
   - The **most recent** file in `briefs/` — so you know what was already said
     and can report only what's *new* (deltas, not repetition).

2. **Load each league's context:**
   - `leagues/chatt-espn/league-settings.md`, and — depending on phase —
     `leagues/chatt-espn/draft-board.md` + `leagues/chatt-espn/watch-list.md`
     (pre-draft) or `leagues/chatt-espn/draft-log.md` (in-season roster, once
     the draft has happened).
   - `leagues/family-yahoo/league-settings.md` and
     `leagues/family-yahoo/roster.md` (in-season roster).
   - `profile/user-profile.md` — preferences, risk tolerance (shared across both).
   - `strategy/in-season-playbook.md` — shared weekly cadence/lineup rules, once
     a league is in-season.

3. **Determine each league's phase independently** by date (today's date is
   provided at runtime):
   - **Chatt-ESPN:** Pre-draft (→ injuries, ADP, board changes) until 9/3, then
     Draft-week final-prep, then In-season (lineup + waivers).
   - **Family-Yahoo:** already in-season — always follow the in-season cadence
     (see `strategy/in-season-playbook.md`): Tue waiver report, lineup-focused
     the rest of the week, loud final-lineup call before Sunday 1 PM lock.

4. **Source the news** with web search/fetch. Pull from reputable, current
   sources (major fantasy outlets, beat reporters, injury trackers, Vegas odds).
   Prioritize items that move fantasy value for **either** league's format —
   note if a scoring difference changes a player's value between the two
   (e.g. a pass-catching RB matters more in Chatt-ESPN's FULL PPR than it might
   in family-Yahoo's scoring — check `leagues/family-yahoo/league-settings.md`).
   Verify anything surprising against a second source before reporting it.

5. **Update the repo** where warranted:
   - New injury/role news → update `data/player-notes.md` (shared).
   - Chatt-ESPN board/rankings changes → `leagues/chatt-espn/draft-board.md` /
     `leagues/chatt-espn/watch-list.md` (pre-draft) or `leagues/chatt-espn/draft-log.md`
     (in-season roster + moves).
   - Family-Yahoo roster/lineup moves → `leagues/family-yahoo/roster.md`.
   - Keep edits surgical and note the date of the change.

6. **Write the brief** to `briefs/YYYY-MM-DD.md` using the combined template below.

7. **Deliver.** (This Routine fires into the primary session, which HAS the Gmail
   connector.)
   - **Preferred:** **SEND** the brief to the inbox with the Gmail `send_message`
     tool → to `ntorres0893@gmail.com`, subject `🏈 Fantasy Morning Brief — <Mon DD>`,
     HTML body = the brief formatted for phone reading (short sections, bold player
     names, lead with the 1–3 most important items across BOTH leagues).
   - **Fallback:** if `send_message` isn't available, use `create_draft` instead
     (lands in Drafts). If no Gmail tool at all, skip silently and rely on the
     final-message summary — don't treat it as a failure.
   - Always also end the run with the full brief as your final message.

8. **Commit & push** the new brief and any data updates to the working branch.

## Combined brief template

> **No duplication rule:** the headline names the single biggest item across
> either league; each league's section carries its own "what changed" **once**.
> Don't restate the same player twice, even across leagues, unless the news
> genuinely affects both rosters differently.

```markdown
# 🏈 Fantasy Brief — <Weekday, Mon DD, YYYY>
*Two leagues: **Chatt-ESPN** (FULL PPR, <phase>) &middot; **Family-Yahoo** (<scoring>, in-season)*

**Headline:** <the single most important thing today, across either league.>

## 🏆 Chatt-ESPN — Claude Me Daddy (slot 8)
### 🆕 What changed
- <new items only, or "quiet day">
<pre-draft: 📊 Draft board by position (see prior single-league template, unchanged)>
<in-season: 🗓️ This week's lineup snapshot — opponent, close calls, waiver targets>
### 🎯 Action items
- <concrete>

## 🏈 Family-Yahoo — <team name once known>
### 🆕 What changed
- <new items only, or "quiet day">
### 🗓️ This week's lineup snapshot
- Opponent: <team> (implied total <x>)
- Starters: <QB/RB/RB/WR/WR/WR/TE/FLEX/DST/K per that league's roster slots>
- Close calls: <slot: A over B — why>
- Waiver/streaming target: <if applicable>
### 🎯 Action items
- <concrete>

## 🧠 Learn-with-me
- <one short teaching note — can serve either league, pick whichever is more relevant today>
```

- **Pre-draft Chatt-ESPN section** keeps the existing single-league format:
  readability rule (no per-name emoji spam in tiers; flags as indented
  sub-bullets with one status emoji + why/action each), team-tag rule (every
  player name gets its team abbreviation), and organizes
  `leagues/chatt-espn/watch-list.md` by position (QB/RB/WR/TE/D-ST/K, high→low).
- **In-season section** (either league) follows `strategy/in-season-playbook.md`:
  health → matchup → Vegas → volume → floor/ceiling by favorite/underdog →
  weather, opponent-aware, loud alerts for game-time decisions before lock.

## Tone & rules
- Concise, confident, and **explain the "why"** — the manager is relearning
  football. Lead with actions.
- Only report **new** information vs. the last brief; **never** repeat a player
  in two sections of the same brief (repeating the *same* player across the
  *two different leagues'* sections is fine and often necessary — just don't
  repeat within one league's section).
- The Watch List (pre-draft) and lineup snapshot (in-season) are exceptions to
  "only new" — they're rolling snapshots, refreshed (not necessarily new) each day.
- If a day is genuinely quiet for a league, say so briefly rather than padding.
- Never fabricate news, injuries, or rosters. If sources conflict, say so.
- **Always name which league** a recommendation applies to — never let advice
  bleed from one league's scoring/roster into the other's section.
