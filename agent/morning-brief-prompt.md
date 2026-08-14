# Morning Brief — Standalone Run Prompt

This is the instruction the daily 7 AM Routine executes. It runs in a **fresh
session** with no memory, so it must reconstruct context entirely from this repo.
The Routine's configured prompt is a short pointer to this file; the full
procedure lives here so it can be improved without editing the Routine.

---

## Your job

Produce today's fantasy football morning brief for the manager and **email it**
to `ntorres0893@gmail.com`, then commit the brief to the repo.

## Steps

1. **Load context** (read these first):
   - `profile/league-settings.md` — scoring/format (10-team PPR ESPN).
   - `profile/user-profile.md` — preferences, risk tolerance.
   - `data/draft-board.md` and `data/player-notes.md` — current board & notes.
   - The **most recent** file in `briefs/` — so you know what was already said
     and can report only what's *new* (deltas, not repetition).
   - `strategy/draft-strategy.md` for pre-draft; `strategy/in-season-playbook.md`
     once the season has started.

2. **Determine the phase** by date (today's date is provided at runtime):
   - **Pre-draft:** focus on injuries, offseason/camp news, ADP movement,
     depth-chart battles, and any board changes.
   - **Draft week:** add a "final prep" section and confirm the game plan.
   - **In-season:** follow the weekly cadence in `in-season-playbook.md`
     (waivers Tue, lineup focus building toward Sunday lock, opponent-aware).

3. **Source the news** with web search/fetch. Pull from reputable, current
   sources (major fantasy outlets, beat reporters, injury trackers, Vegas odds).
   Prioritize items that **move fantasy value** for a 10-team PPR league.
   Verify anything surprising against a second source before reporting it.

4. **Update the repo** where warranted:
   - New injury/role news → update `data/player-notes.md` and, if it changes
     rankings, `data/draft-board.md`.
   - Keep edits surgical and note the date of the change.

5. **Write the brief** to `briefs/YYYY-MM-DD.md` using the template below.

6. **Deliver.** (This Routine fires into the primary session, which HAS the Gmail
   connector.)
   - **Preferred:** **SEND** the brief to the inbox with the Gmail `send_message`
     tool → to `ntorres0893@gmail.com`, subject `🏈 Fantasy Morning Brief — <Mon DD>`,
     HTML body = the brief formatted for phone reading (short sections, bold player
     names, lead with the 1–3 most important items).
   - **Fallback:** if `send_message` isn't available, use `create_draft` instead
     (lands in Drafts). If no Gmail tool at all, skip silently and rely on the
     final-message summary — don't treat it as a failure.
   - Always also end the run with the full brief as your final message.

7. **Commit & push** the new brief and any data updates to the working branch.

## Brief template

```markdown
# 🏈 Morning Brief — <Weekday, Mon DD, YYYY>
*Phase: <Pre-draft | Draft week | Week N> · Days to draft: <n> (pre-draft only)*

## ☀️ Top of the brief
- <The 1–3 things that matter most today, one line each.>

## 🚑 Injuries & status
- <Player (POS, TEAM): what happened, timeline, fantasy impact + draft/lineup action.>

## 🔁 News & moves that shift value
- <Trades, depth-chart changes, camp battles, coaching notes → who's up/down.>

## 📈 Board / ADP watch  (pre-draft)
- <Risers, fallers, and any changes I made to data/draft-board.md and why.>

## 🎯 Action items for you
- <Concrete things: "confirm your draft slot", "consider bumping X up a tier",
   in-season: "start A over B this week", "add C off waivers".>

## 🧠 Learn-with-me
- <One short teaching note to build football IQ — a concept behind today's news.>
```

## Tone & rules
- Concise, confident, and **explain the "why"** — the manager is relearning
  football. Lead with actions.
- Only report **new** information vs. the last brief; don't repeat yesterday.
- If a day is genuinely quiet, say so briefly rather than padding.
- Never fabricate news or injuries. If sources conflict, say so.
