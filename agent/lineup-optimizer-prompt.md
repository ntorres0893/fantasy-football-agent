# Weekly Lineup Optimizer — Run Prompt

Use in-season to set the optimal lineup for **either or both** leagues. Kick off
with:
*"Set my Week N lineup"* (both leagues) or *"Set my Week N lineup for Chatt"* /
*"...for Yahoo"* (one league only).

## Steps
1. Read `strategy/in-season-playbook.md` (shared cadence/priority rules), and for
   each league in scope:
   - `leagues/chatt-espn/league-settings.md` + `leagues/chatt-espn/draft-log.md`
     (current roster, kept updated with adds/drops), or
   - `leagues/family-yahoo/league-settings.md` + `leagues/family-yahoo/roster.md`.
2. Confirm the manager's **opponent** this week in each league (ask, or read from
   notes if already logged).
3. **Check the NFL schedule against the roster FIRST, before anything else.**
   Identify anyone in either league playing Thursday/Friday/international —
   those slots lock independently and early, well before the Sunday slate's
   injury news is even final. Call these out as a separate, time-sensitive
   decision, not folded into the general "Sunday" lineup call. If it's
   currently before Thursday's games, this is often the most urgent part of
   the whole run — say so up front.
4. Pull current data via web search: injury designations (Q/D/O) and expected
   inactives, Vegas implied team totals & spreads, weather for outdoor games,
   and any late-breaking role news (snap/target trends). This research is
   shared — do it once, apply to both leagues' rosters.
4b. **Research every starter's actual NFL game, not just the player.** Build
   one table row per starter and per realistic bench option:
   - the game, day, and kickoff
   - spread and total, with the team's implied total
   - the opposing defense's rank vs. that position (use the rank the
     platform app shows)
   - injuries on BOTH sides, especially QBs, which change game script
   - weather for outdoor games
   - one line on what decides the game
   Then do the same read on the **opponent's** lineup. Ask the manager for a
   matchup screenshot if we don't have it. Log the table in the league's
   roster file. Added 9/23 at the manager's request after an 0-2 start.
5. **For any real decision point (a bench player could plausibly start over
   the incumbent), pull numeric/ordinal projection data, not just Vegas +
   matchup narrative** — see in-season-playbook.md's "Consensus rankings &
   start/sit verdicts" factor. Query FantasyPros ECR, PFF matchup grades, and
   CBS/Yahoo/FantasyPros start-or-sit columns by name for the players in
   question. Skip this step for slots with no real alternative (most weeks,
   most slots) — it's for close calls, not a rubber stamp on every player.
6. For each starting slot **in each league**, choose the optimal player using the
   priority order in the in-season playbook (kickoff timing → health → matchup →
   Vegas → consensus rankings/start-sit → volume → floor/ceiling by your
   favorite/underdog status → weather). **Respect each league's own roster
   slots and scoring** — don't assume they match.
7. Return a clear lineup card **per league**, with early-locking (Thu/Fri/intl)
   players called out at the top before the rest of the card:

```
### Chatt-ESPN — Week N vs <Opponent> (their implied total: <x>)
⏰ Locks early (Thu/Fri/intl — decide NOW): <slot: player, or "none this week">

QB:  <player>   RB: <player>, <player>   WR: <player>, <player>
TE:  <player>   FLEX: <player>   D/ST: <stream pick>   K: <stream pick>

Close calls:
- <Slot>: <A> over <B> — <why>
Bench alert: <anyone injured/risky to monitor before lock>
Waiver/stream: <best available D/ST or fill-in for this week>

### Family-Yahoo — Week N vs <Opponent> (their implied total: <x>)
<same shape, using that league's actual roster slots>
```

8. **Loudly** flag any player who is a game-time decision and give a lock-time
   plan ("if X is inactive, start Y"). Re-check before **each individual
   player's own kickoff** — not one blanket Sunday time — since Thu/Fri/intl
   starters lock separately from the Sun/Mon slate (see the in-season playbook's
   weekly cadence).
9. Update `leagues/chatt-espn/draft-log.md` and/or `leagues/family-yahoo/roster.md`
   with any moves and commit.
