#RollStats

RollStats tracks roll statistics and displays them in various formats.  Rolls
are tracked for each player, for each die size, both for the current session
(since the API sandbox was started) and for all time.

It is recommended that this script be used in conjunction with the CommandShell
module, which will improve output formatting and command discovery.


##Syntax:

```
!rollstats [options]
```

The "rollstats" command accepts the following options:

    -h, --help		Displays a help message and exits.

    -g, --global	Shows stats for all players.
    -p P, --player P	Shows stats for player P, specified by display name,
			player ID, or Roll20 user ID.

    -l, --leaderboard	Shows summary information (roll count, average value,
			and expected value) for each player, sorted in
			decreasing order of value / expected (i.e. lucky to
			unlucky).
    -d N, --die N	Shows more detailed stats (count and %, plus expected
			count and %, for each possible roll, along with the mean
			and expected mean) for the specified die size.

    -s, --session	Shows only stats for the current session (since the API
			sandbox was last restarted).  In most cases, this will
			be for the current play session, but it might be less if
			the sandbox was restarted during play or more if players
			remain connected between play sessions.

    -c, --chat		Shows stats in the chat instead of whispering them to
			the player who executed the command.

    --clear		Clears session stats if combined with -s; otherwise
			clears "all time" stats.  Can only be executed by a GM.

The default mode of operation shows a high-level summary (roll count, mean
value, and expected value for each die size rolled) of all the rolls made by the
player who executed the command.
