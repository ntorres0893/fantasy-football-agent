# Weekly Lineup Optimizer — Run Prompt

Use in-season to set the optimal lineup. Kick off with:
*"Set my Week N lineup."*

## Steps
1. Read `strategy/in-season-playbook.md`, `profile/league-settings.md`, and the
   current roster in `data/draft-log.md` (kept updated with adds/drops).
2. Confirm the manager's **opponent** this week (ask or read from notes).
3. Pull current data via web search: injury designations (Q/D/O) and expected
   inactives, Vegas implied team totals & spreads, weather for outdoor games,
   and any late-breaking role news (snap/target trends).
4. For each starting slot, choose the optimal player using the priority order in
   the in-season playbook (health → matchup → Vegas → volume → floor/ceiling by
   your favorite/underdog status → weather).
5. Return a clear lineup card:

```
Week N Lineup vs <Opponent> (their implied total: <x>)
QB:  <player>   RB: <player>, <player>   WR: <player>, <player>
TE:  <player>   FLEX: <player>   D/ST: <stream pick>   K: <stream pick>

Close calls:
- <Slot>: <A> over <B> — <why>
Bench alert: <anyone injured/risky to monitor before lock>
Waiver/stream: <best available D/ST or fill-in for this week>
```

6. **Loudly** flag any player who is a game-time decision and give a lock-time
   plan ("if X is inactive, start Y"). Re-check before the Sunday 1 PM lock.
7. Update `data/draft-log.md` with any moves and commit.
