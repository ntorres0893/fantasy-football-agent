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
5. For each starting slot **in each league**, choose the optimal player using the
   priority order in the in-season playbook (kickoff timing → health → matchup →
   Vegas → volume → floor/ceiling by your favorite/underdog status → weather).
   **Respect each league's own roster slots and scoring** — don't assume they
   match.
6. Return a clear lineup card **per league**, with early-locking (Thu/Fri/intl)
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

7. **Loudly** flag any player who is a game-time decision and give a lock-time
   plan ("if X is inactive, start Y"). Re-check before **each individual
   player's own kickoff** — not one blanket Sunday time — since Thu/Fri/intl
   starters lock separately from the Sun/Mon slate (see the in-season playbook's
   weekly cadence).
8. Update `leagues/chatt-espn/draft-log.md` and/or `leagues/family-yahoo/roster.md`
   with any moves and commit.
