# 🧪 Mock-Draft Playbook — 10-Team FULL PPR

> A mock is **not** a small real draft. The real draft's goal is *win*. A mock's
> goal is *learn* — find out where players actually go, stress-test a build, and
> discover which slot you want. You should be **willing to lose a mock** to learn
> something. Team: **Claude Me Daddy** · Draft: **Sept 3, 2026**.

---

## How to start one with me

Open a session on this repo and say:

> **"Mock starting, I'm at slot X."**

I'll load `data/draft-board.md`, `data/player-notes.md`, and
`profile/league-settings.md`, compute your pick numbers, and give you a slot game
plan before pick 1.01. Then feed me picks exactly like the real thing:

- **"Pick 7: Player X"** — any pick, any team
- **"Since my last pick: A, B, C, D went"** — the fast way
- **"I'm on the clock"** — I return the recommendation card

**Mock-specific commands** (these don't exist in the real draft):
- **"Test zero-RB"** / **"Test hero-RB"** / **"Test BPA"** — I'll bias
  recommendations toward that build so we can see how it survives contact.
- **"What would the other build have done?"** — after any pick, I'll show the
  road not taken.
- **"Debrief"** — at the end, I write the post-mock review into
  `data/mock-draft-log.md`.

---

## Before you start (2 minutes)

1. **Set the platform to your real settings** if it lets you: **10 teams, PPR,
   snake, ESPN roster (QB/RB/RB/WR/WR/TE/FLEX/D-ST/K + 7 bench).** A 12-team
   half-PPR mock teaches you the wrong ADP.
2. **Turn OFF autopick** and give yourself the longest clock available.
3. **Know your pick numbers.** 10-team snake, slot *S*:
   picks are `S`, `21−S`, `20+S`, `41−S`, `40+S`, … (odd rounds count up from *S*,
   even rounds count *21−S*).
4. Have `data/draft-board.md` open in one window. That's the queue.

---

## The fast-clock rule (mocks run 60–90 seconds)

You will not have time to read a paragraph. On the clock, work this order and
stop as soon as one fires:

1. **Is a tier about to empty?** → take the last guy in the tier.
2. **Is someone 10+ spots above where we are on the board?** → take the value.
3. **Otherwise, take the best RB/WR available** and keep the 5-of-7 rule.

If you're truly stuck with 10 seconds left: **best available WR or
pass-catching RB.** In a 10-team PPR you are almost never punished for that.

---

## Run these three mocks (in this order)

Each one answers a different question. Don't run the same draft three times.

### Mock 1 — Balanced BPA, from a *middle* slot (4–7)
**Question: where does the board actually break?**
Just take best-value-by-tier every pick and note where the runs happen. This is
your calibration run — you're learning real ADP, not testing a thesis.
**Watch for:** when the elite WR tier empties, when TE1 goes, how early QBs fly
off in a 10-team room (usually later than people fear).

### Mock 2 — Zero-RB, from an *early* slot (1–3)
**Question: can we survive without an early RB in PPR?**
Load elite WRs (and possibly Bowers/McBride) rounds 1–4, then attack RB from
round 5: Irving, Hall, Judkins, Swift, Brooks, Allgeier, Tuten.
**The test:** by Round 8, do you have two startable RBs you'd actually play?
If yes, zero-RB is live for you. If you're staring at three handcuffs, it isn't.

### Mock 3 — Hero-RB / Robust-RB, from a *late* slot (8–10)
**Question: is the turn worth pairing two RBs?**
Slots 8–10 pick back-to-back. Take a pass-catching RB early and see whether the
WR pool really does hold up into Rounds 5–6 the way our strategy claims.
**The test:** compare your Round-6 WR2 to what Mock 2's WR2 looked like. If
they're close, the deep-WR thesis is confirmed and RB-early is the better use of
premium picks.

---

## What to actually record (this is the whole point)

After each mock, capture these six things in `data/mock-draft-log.md`:

| What | Why it matters |
|------|----------------|
| **Where each tier cliff hit** | Tells us which round to "reach" a half-round early |
| **Players who consistently fell** | Free value we can plan around at the real draft |
| **Players who consistently went early** | Names to stop planning on — someone always takes them |
| **Your dead zone** | The 2–3 round stretch where you had no good options |
| **Final roster grade by position** | Which build actually produced a startable lineup |
| **The one pick you regret** | The single most valuable line in the log |

**One mock is noise. Three mocks is a pattern.** Only change the board when the
*same* thing happens twice.

---

## Mock-draft traps (the stuff that makes mocks lie to you)

- **Mock rooms are QB-happy and RB-happy.** Casual mockers reach for names.
  Don't recalibrate our whole board off one aggressive room.
- **Autodrafters distort the late rounds.** If half the room goes on autopick by
  Round 9, everything after that is fiction. Note it and discard those rounds.
- **Never mock in a different format.** Half-PPR ADP will teach you to
  under-draft Godwin/Downs/Wan'Dale types who are worth more in full PPR.
- **Don't draft your favorites to feel good.** A mock where you took everyone you
  like taught you nothing.
- **Preseason injuries move fast.** A mock from 8/16 has stale names by 9/3 —
  the value *lessons* survive, the specific *names* need re-verifying.

---

## Known open questions a mock can answer for us

These are live gaps in our prep — a mock is the cheapest way to close them:

1. **Which slot do we actually want?** (Right now our slot is TBD. If ESPN lets
   you request one, mocks tell you what to ask for.)
2. **Bowers/McBride at their price — worth it, or take Kraft 4 rounds later?**
   Mock it both ways. This is the single biggest structural call on our board.
3. **Does Achane really last to 9–10?** Our cheat sheet assumes he might.
4. **How late can we truly wait on QB?** Our strategy says R6–10; a real room
   will tell us if that's optimistic.

---

## After the mock

Say **"Debrief"** and I'll write the full review into `data/mock-draft-log.md`:
roster by position, build grade, tier-cliff map, value fallers, and — most
importantly — **any board changes the mock justifies.** Board edits get committed
so the next mock starts smarter.

> Real draft day is a different document: `strategy/draft-day-playbook.md`.
