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
   - **Update `data/watch-list.md`** — add/upgrade/downgrade/retire names as their
     status changes. This is the running list the brief's Watch List renders from.
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

> **No duplication rule:** the headline names the single biggest item; the
> "What changed today" section carries the day's NEW movers **once**. Do NOT
> restate the same players in a separate "top of the brief" bullet list — that was
> the old repetitive format. New news lives in exactly one place.

```markdown
# 🏈 Morning Brief — <Weekday, Mon DD, YYYY>
*Scoring: FULL PPR · Draft: Sept 3 (<n> days) · Team: Claude Me Daddy*

**Headline:** <one sentence — the single most important thing today.>

## 🆕 What changed today
- **Player (POS·TM):** what happened → the action (draft/value/monitor/fade/stash).
  <Only genuinely NEW items vs. the last brief. If quiet, say "quiet day" and keep
  it to 1–2 lines.>

## 📊 Draft board by position  (pre-draft — render from data/watch-list.md)
Organize BY POSITION and show **who to draft high vs. low** at each — this is what
the manager wants this close to the draft. Cover **every** position (QB, RB, WR, TE,
D/ST, K).

**Readability rule (important):** do NOT tag a status emoji onto every name — that's
visual noise. Keep names plain inside each tier (the tier label already says
high-vs-low). Put the injury/role flags in a **"Flags:" bullet with one indented
sub-bullet per player** — each line = one status emoji + player + one-line why/action
(e.g., "⚠️ Josh Jacobs — groin, out ≥1 wk → target only if he slides"). This keeps
tiers glanceable while each flag stays legible on its own line. Include a small flag
legend once. Shape per position:
- **QB:** wait — name the R6–10 targets + late streamers; "don't draft before R6."
- **RB:** Early/R1 → mid → RB2/flex → late sleepers → avoid/fade.
- **WR:** Early/R1–2 → WR2/WR3 → flex/upside → avoid/fade.
- **TE:** the two to pay up for → value target → stream late → don't-pay-up.
- **D/ST & K:** one line each — last two rounds, stream (note the scoring quirks).
Bold the day's movers so "what changed" connects to the board. Full detail lives in
`data/watch-list.md`; the email shows the highlights.

## 🎯 Action items for you
- <Concrete: draft slot, draft time, "bump X a tier," run a mock; in-season:
   start/sit, waiver adds.>

## 🧠 Learn-with-me
- <One short teaching note — the concept behind today's news.>
```

- In-season, swap the Watch List for a **start/sit + waiver** snapshot from
  `in-season-playbook.md` (same "many names, scannable" spirit).

## Tone & rules
- Concise, confident, and **explain the "why"** — the manager is relearning
  football. Lead with actions.
- Only report **new** information vs. the last brief; **never** repeat a player in
  two sections of the same brief.
- The Watch List is the exception to "only new" — it's a rolling snapshot of many
  monitored names, refreshed (not necessarily new) each day.
- If a day is genuinely quiet, say so briefly rather than padding.
- Never fabricate news or injuries. If sources conflict, say so.
