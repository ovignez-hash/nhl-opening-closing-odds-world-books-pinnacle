# NHL Matchup & Stats — free sample, the same 20 games

The nine tables of **NHL Matchup & Stats** for the 20 games of this repository's odds sample. Same files and same columns as the full product: only the number of games differs.

| File | One row per | Rows |
|---|---|---:|
| `NHL_Matchup_Stats_Games_2006-2026_SAMPLE.csv` | game | 20 |
| `NHL_Matchup_Stats_Team_Box_Scores_2006-2026_SAMPLE.csv` | team and game | 40 |
| `NHL_Matchup_Stats_Skater_Box_Scores_2006-2026_SAMPLE.csv` | skater and game | 720 |
| `NHL_Matchup_Stats_Goalie_Box_Scores_2006-2026_SAMPLE.csv` | dressed goalie and game | 80 |
| `NHL_Matchup_Stats_Scratches_2006-2026_SAMPLE.csv` | scratched player and game | 290 |
| `NHL_Matchup_Stats_Goals_2006-2026_SAMPLE.csv` | goal | 110 |
| `NHL_Matchup_Stats_Penalties_2006-2026_SAMPLE.csv` | penalty | 171 |
| `NHL_Matchup_Stats_Shootouts_2006-2026_SAMPLE.csv` | shootout attempt | 17 |
| `NHL_Matchup_Stats_Players_2006-2026_SAMPLE.csv` | player | 888 |

Every table except Players joins the odds sample on `Game_ID`, the same key as in *NHL Opening & Closing Odds — Pinnacle and 7 international books, 2006–2026*:

```python
import pandas as pd

odds = pd.read_csv("../sample/NHL_World_Opening_Closing_Odds_2006-2026_SAMPLE.csv", low_memory=False)
games = pd.read_csv("NHL_Matchup_Stats_Games_2006-2026_SAMPLE.csv")

stats_cols = ["Game_ID"] + [c for c in games.columns if c not in odds.columns]
df = odds.merge(games[stats_cols], on="Game_ID")   # 20 games, odds and game sheet side by side
```

The full product: 26,211 games from 2006-07 to 19 November 2026, 943,457 skater rows, 104,848 goalie rows, 150,177 goals and 223,402 penalties.

→ **[Get NHL Matchup & Stats](https://sportsdataolivier.gumroad.com/l/vavcu?utm_source=github&utm_medium=readme&utm_campaign=nhl_world&utm_content=matchup_sample)** · also on [Whop](https://whop.com/oliviersportsdata/nhl-matchup-stats-2006-2026/?utm_source=github&utm_medium=readme&utm_campaign=nhl_world&utm_content=matchup_sample_whop)

Sample: free to explore and evaluate. Full product: single commercial user; redistribution and resale of the files, or of the raw data in another format, are not permitted. A question: contact@oliviersportsdata.com

---

*The README of the full product follows.*

## NHL Matchup & Stats — game sheets, team, skater and goalie box scores, 2006–2026

Every NHL game from the 2006-07 season to 19 November 2026: the game sheet (period scores, shots, venue, attendance, real puck drop, officials, coaches, starting goalies, three stars), both teams' box scores, every skater's and every goalie's line, the scratches, and every goal, penalty and shootout attempt. Nine tables, one key.

Built to sit next to the two NHL Opening & Closing Odds files: `Game_ID` is the same key and the game columns are identical, so every game of the odds files finds its row here with no name matching. Statistics only: there are no odds in this file.

| | |
|---|---|
| Games | 26,211 |
| Seasons | 2006-07 to 2026-27 (2026-27 through 19 November 2026) |
| Team box scores | 52,422 rows |
| Skater box scores | 943,457 rows, 3,352 skaters |
| Goalie box scores | 104,848 rows, 493 goalies |
| Scratches | 234,528 rows |
| Goals | 150,177 rows |
| Penalties | 223,402 rows |
| Shootout attempts | 17,577 rows |
| Players | 4,054 rows |
| Files | 9 CSV files, UTF-8, comma-separated |
| Source | the NHL's official statistics and game reports |

### Games

| Season | Regular season | Playoffs | Total |
|---|---:|---:|---:|
| 2006/2007 | 1,230 | 81 | 1,311 |
| 2007/2008 | 1,230 | 85 | 1,315 |
| 2008/2009 | 1,230 | 87 | 1,317 |
| 2009/2010 | 1,230 | 89 | 1,319 |
| 2010/2011 | 1,230 | 89 | 1,319 |
| 2011/2012 | 1,230 | 86 | 1,316 |
| 2012/2013 | 720 | 86 | 806 |
| 2013/2014 | 1,230 | 93 | 1,323 |
| 2014/2015 | 1,230 | 89 | 1,319 |
| 2015/2016 | 1,230 | 91 | 1,321 |
| 2016/2017 | 1,230 | 87 | 1,317 |
| 2017/2018 | 1,271 | 84 | 1,355 |
| 2018/2019 | 1,271 | 87 | 1,358 |
| 2019/2020 | 1,082 | 130 | 1,212 |
| 2020/2021 | 868 | 84 | 952 |
| 2021/2022 | 1,312 | 89 | 1,401 |
| 2022/2023 | 1,312 | 88 | 1,400 |
| 2023/2024 | 1,312 | 88 | 1,400 |
| 2024/2025 | 1,312 | 86 | 1,398 |
| 2025/2026 | 1,312 | 82 | 1,394 |
| 2026/2027 | 358 | – | 358 |
| **Total** | **24,430** | **1,781** | **26,211** |

2012/2013 is the 48-game lockout season. 2019/2020 stopped on 11 March 2020 after 1,082 regular-season games; its playoffs include the 44 games of the qualifying round and the seeding round-robin played in August 2020 in Edmonton and Toronto, which the NHL counts as playoff games. 2020/2021 was a 56-game season. Vegas joined in 2017-18 and Seattle in 2021-22 (1,312 games a season from 2021-22 to 2025-26). 2026/2027 is an 84-game season (1,344 games scheduled).

3,546 games were decided in overtime and 2,489 in a shootout. In the playoffs, 328 games needed one overtime, 67 two, 11 three, 3 four and 1 five. 2 games of the August 2020 round-robin, played under regular-season overtime rules, ended in a shootout (Washington at Tampa Bay on 3 August, Dallas at St. Louis on 9 August): they are the only playoff games with `Match_Ending` `Shootout`.

### Nine tables, one key

| File | One row per | Rows | Columns |
|---|---|---:|---:|
| `NHL_Matchup_Stats_Games_2006-2026.csv` | game | 26,211 | 67 |
| `NHL_Matchup_Stats_Team_Box_Scores_2006-2026.csv` | team and game | 52,422 | 40 |
| `NHL_Matchup_Stats_Skater_Box_Scores_2006-2026.csv` | skater and game | 943,457 | 33 |
| `NHL_Matchup_Stats_Goalie_Box_Scores_2006-2026.csv` | dressed goalie and game | 104,848 | 26 |
| `NHL_Matchup_Stats_Scratches_2006-2026.csv` | scratched player and game | 234,528 | 9 |
| `NHL_Matchup_Stats_Goals_2006-2026.csv` | goal | 150,177 | 25 |
| `NHL_Matchup_Stats_Penalties_2006-2026.csv` | penalty | 223,402 | 20 |
| `NHL_Matchup_Stats_Shootouts_2006-2026.csv` | shootout attempt | 17,577 | 15 |
| `NHL_Matchup_Stats_Players_2006-2026.csv` | player | 4,054 | 18 |

Every table except Players carries `Game_ID`, the key shared with the odds files, and `NHL_Game_ID`, the NHL's own game number. Player tables carry `Player_ID`, the NHL's player number, the same across seasons and teams; the Players table gives each player's birth date and place, height, weight, shooting side and draft.

### Joining an odds file

`Game_ID` is `YYYYMMDD_AWAY_HOME`, date in US Eastern time, team codes of the time: the same key as in *NHL Opening & Closing Odds — Pinnacle and 7 international books, 2006–2026* and *NHL Opening & Closing Odds — 11 books and 2 prediction markets, 2020–2026*. The first 18 columns of the Games table are the game columns of those two files, value for value. This file runs a little further in time: the odds files stop at the end of their own update.

```python
import pandas as pd

games = pd.read_csv("NHL_Matchup_Stats_Games_2006-2026.csv", low_memory=False)
odds = pd.read_csv("NHL_World_Opening_Closing_Odds_2006-2026.csv", low_memory=False)

stats_cols = ["Game_ID"] + [c for c in games.columns if c not in odds.columns]
df = odds.merge(games[stats_cols], on="Game_ID", how="left")
```

### Columns

**Games — 67 columns**

| Column | Content |
|---|---|
| `League` | NHL |
| `Game_ID` | `YYYYMMDD_AWAY_HOME`, date in US Eastern time, team codes of the time |
| `NHL_Game_ID` | the NHL's game number (`2006020001`): season, `02` regular season or `03` playoffs, game |
| `Season` | `2006/2007` |
| `Stage` | `Regular Season` or `Playoffs` |
| `Kickoff_UTC`, `Epoch` | scheduled start, ISO 8601 (`2006-10-04T23:00:00Z`) and Unix seconds |
| `Home_Team`, `Away_Team` | full team names, as the team was named that season |
| `Home_Score`, `Away_Score` | official final score: overtime included, and a shootout counts as one goal for the winner |
| `Winner` | `Home` or `Away` |
| `Total_Score`, `Margin` | sum and absolute difference of the two scores |
| `Match_Ending` | `Regulation`, `Overtime` or `Shootout` |
| `Home_Score_60`, `Away_Score_60`, `Result_60` | score after 60 minutes, and `Home`, `Away` or `Draw` |
| `Date_ET` | game date, US Eastern time |
| `Home_Code`, `Away_Code` | team codes of the time |
| `Overtime_Periods` | overtime periods played: 0, or 1 in the regular season, up to 5 in the playoffs |
| `Home_P1` … `Home_P3`, `Home_OT` | home goals in each period, and in overtime (all overtime periods together); `Home_OT` is empty when no overtime was played |
| `Away_P1` … `Away_P3`, `Away_OT` | the same for the away team |
| `Home_SO_Goals`, `Home_SO_Attempts`, `Away_SO_Goals`, `Away_SO_Attempts` | shootout goals and attempts, when the game went to a shootout |
| `Home_Shots`, `Away_Shots` | shots on goal (shootout attempts are not shots) |
| `First_Goal`, `First_Goal_Period`, `First_Goal_Time` | `Home` or `Away`, period and time in the period (`09:09`) of the first goal; empty when no goal was scored before the shootout |
| `Playoff_Round`, `Playoff_Series`, `Series_Game` | playoffs only: round (0 for the 2020 qualifying round and round-robin, 4 for the final), series number in the round, game number in the series |
| `Venue`, `Venue_City`, `Venue_Timezone` | where the game was played |
| `Attendance` | spectators, from the NHL's official game report |
| `Puck_Drop_UTC` | real start of the game, from the official game report (see below) |
| `Duration_Min` | minutes from the real start to the end of the game |
| `Home_Coach`, `Away_Coach` | head coaches |
| `Home_Starting_Goalie_ID`, `Home_Starting_Goalie`, `Away_Starting_Goalie_ID`, `Away_Starting_Goalie` | the goalies who started the game |
| `Referee_1`, `Referee_2`, `Linesman_1`, `Linesman_2` | the officials |
| `Star_1_ID`, `Star_1`, `Star_1_Team` … `Star_3_Team` | the three stars of the game |

Team names follow the season: Atlanta Thrashers (`ATL`) until 2010-11, then Winnipeg Jets (`WPG`); Phoenix Coyotes (`PHX`) until 2013-14, then Arizona Coyotes (`ARI`) until 2023-24; Utah Hockey Club in 2024-25, then Utah Mammoth (`UTA` for both).

**Team box scores — 40 columns, two rows per game**

| Column | Content |
|---|---|
| `Game_ID`, `NHL_Game_ID`, `Season`, `Stage`, `Date_ET` | as in the games table |
| `Side` | `Home` or `Away` |
| `Team_Code`, `Team`, `Opponent_Code`, `Opponent` | the team and its opponent |
| `Result` | `W`, `L` (lost in regulation), `OTL` (lost in overtime) or `SOL` (lost in a shootout) |
| `Goals`, `Opponent_Goals` | final score |
| `Goals_P1` … `Goals_P3`, `Goals_OT` | goals by period |
| `Shootout_Goals`, `Shootout_Attempts` | when the game went to a shootout |
| `Shots`, `Shots_P1` … `Shots_P3`, `Shots_OT` | shots on goal, total and by period |
| `Missed_Shots` | shot attempts that missed the net |
| `Attempts_Blocked` | the team's shot attempts that were blocked |
| `Shot_Attempts` | `Shots` + `Missed_Shots` + `Attempts_Blocked` |
| `EV_Goals`, `PP_Goals`, `SH_Goals` | goals at even strength, on the power play and short-handed (shootout goal not counted) |
| `EN_Goals` | goals scored into an empty net |
| `PP_Opportunities` | power-play opportunities |
| `PIM` | penalty minutes |
| `Hits`, `Blocked_Shots`, `Giveaways`, `Takeaways` | team totals, goalies included |
| `Faceoff_Wins`, `Faceoffs`, `Faceoff_Pct` | faceoffs won, faceoffs taken, and the ratio (`0.5694`) |

**Skater box scores — 33 columns**

| Column | Content |
|---|---|
| `Game_ID`, `NHL_Game_ID`, `Season`, `Stage`, `Date_ET`, `Side`, `Team_Code`, `Opponent_Code` | the game, the skater's team and its opponent |
| `Player_ID`, `Player`, `Jersey`, `Position` | the skater; position `C`, `L`, `R` or `D` |
| `Goals`, `Assists`, `Points`, `Plus_Minus`, `PIM` | scoring line |
| `Shots`, `Missed_Shots`, `Attempts_Blocked` | shots on goal, attempts that missed the net, attempts that were blocked |
| `Hits`, `Blocked_Shots`, `Giveaways`, `Takeaways` | |
| `PP_Goals` | power-play goals |
| `Faceoff_Wins`, `Faceoff_Losses`, `Faceoff_Pct` | faceoffs; the ratio is empty when the skater took none |
| `TOI_Seconds` | time on ice, in seconds |
| `EV_TOI_Seconds`, `PP_TOI_Seconds`, `SH_TOI_Seconds` | time on ice at even strength, on the power play and short-handed |
| `Shifts` | number of shifts |

One row per skater who dressed. `Missed_Shots`, `Attempts_Blocked`, `Faceoff_Wins`, `Faceoff_Losses` and the three time-on-ice splits come from the NHL's official event summary of the game; the other columns come from the NHL's box score.

**Goalie box scores — 26 columns**

| Column | Content |
|---|---|
| `Game_ID` … `Opponent_Code` | as in the skater table |
| `Player_ID`, `Player`, `Jersey` | the goalie |
| `Starter` | 1 for the goalie who started |
| `Played` | 1 when the goalie was on the ice; 0 for the backup who dressed and did not play |
| `Decision` | `W`, `L` or `OTL` (loss in overtime or in a shootout), for the goalie of record |
| `TOI_Seconds` | time on ice, in seconds |
| `Shots_Against`, `Saves`, `Goals_Against`, `Save_Pct` | empty when the goalie did not play |
| `EV_Shots_Against`, `EV_Goals_Against`, `PP_Shots_Against`, `PP_Goals_Against`, `SH_Shots_Against`, `SH_Goals_Against` | shots and goals against by strength: `PP_` while the opponent was on the power play, `SH_` while the opponent was short-handed |
| `PIM` | penalty minutes |

Two goalies dress for each team, now and then three: 56,259 rows with `Played` 1 and 48,589 with `Played` 0. 3,837 times a goalie came in during the game without having started it. Goalies have no goal or assist column: the 10 goals and 1,150 assists credited to a goalie are in the goals table.

**Scratches — 9 columns**

`Game_ID`, `NHL_Game_ID`, `Season`, `Stage`, `Date_ET`, `Side`, `Team_Code`, `Player_ID`, `Player`: the players each team listed as scratched for the game (injured, suspended or healthy), 4.47 per team and game on average.

**Goals — 25 columns**

| Column | Content |
|---|---|
| `Game_ID`, `NHL_Game_ID`, `Season`, `Stage`, `Date_ET` | the game |
| `Goal_No` | order of the goal in the game |
| `Period`, `Period_Type` | period number (4 and above: overtime) and `REG` or `OT` |
| `Time`, `Game_Seconds` | time in the period (`09:09`) and seconds from the start of the game |
| `Side`, `Team_Code` | the scoring team |
| `Scorer_ID`, `Scorer`, `Assist_1_ID`, `Assist_1`, `Assist_2_ID`, `Assist_2` | scorer and assists |
| `Strength` | `EV`, `PP` or `SH` |
| `Empty_Net` | 1 when the goal was scored into an empty net |
| `Goal_Modifier` | `empty-net`, `penalty-shot`, `own-goal`, `own-goal-empty-net`, `awarded`, `awarded-empty-net`, or empty |
| `Shot_Type` | wrist, snap, slap, backhand, tip-in… |
| `Home_Score_After`, `Away_Score_After` | score after the goal |
| `Situation_Code` | the NHL's four-digit code at the time of the goal: away goalie, away skaters, home skaters, home goalie (`1551` is five against five) |

Shootout goals are not in this table: the shootout has its own.

**Penalties — 20 columns**

| Column | Content |
|---|---|
| `Game_ID` … `Date_ET`, `Period`, `Period_Type`, `Time`, `Game_Seconds`, `Side`, `Team_Code` | the game, the time and the penalised team |
| `Player_ID`, `Player` | the penalised player; empty for a bench penalty |
| `Drawn_By_ID`, `Drawn_By` | the opponent who drew the penalty, when the NHL gives it |
| `Served_By_ID`, `Served_By` | the player who served it, when it was not the penalised player |
| `Type` | `MIN` minor, `MAJ` major, `MIS` misconduct, `GAM` game misconduct, `MAT` match, `BEN` bench, `PS` penalty shot, `GRO` gross misconduct |
| `Minutes` | 2, 4, 5, 10; 0 for a penalty shot |
| `Infraction` | tripping, hooking, high-sticking… |

**Shootout attempts — 15 columns**

`Game_ID`, `NHL_Game_ID`, `Season`, `Stage`, `Date_ET`, `Sequence`, `Side`, `Team_Code`, `Shooter_ID`, `Shooter`, `Result` (`goal` or `save`), `Shot_Type`, `Game_Winner` (1 for the deciding goal), `Home_SO_Goals_After`, `Away_SO_Goals_After`. 5,633 goals in 17,577 attempts.

**Players — 18 columns**

`Player_ID`, `First_Name`, `Last_Name`, `Position`, `Shoots_Catches`, `Birth_Date`, `Birth_City`, `Birth_State_Province`, `Birth_Country`, `Height_cm`, `Weight_kg`, `Height_in`, `Weight_lb`, `Draft_Year`, `Draft_Team`, `Draft_Round`, `Draft_Pick`, `Draft_Overall`: every player who appears in a box score or among the scratches, 3,125 of them drafted, born in 37 countries. Height and weight are those of the NHL's current player page.

### Checks run on every game

- The score is the sum of the periods, plus one goal for the shootout winner; the score after 60 minutes is the sum of the three periods.
- Each team's goals are the sum of its players' goals, and the goals table gives the same scorers and running score.
- Each team's shots on goal are the sum of its periods and of its skaters' shots (one more when the goalie took one); hits and blocked shots are the sum of the skaters' lines.
- One starting goalie and one goalie of record per team; a goalie's saves plus goals against make the shots against.
- No duplicate game, team line, player line or scratch, and no scratched player has a line in the box score of the same game.
- The 18 game columns are identical to those of the two NHL odds files.
- A second pass, written separately, compares the tables with the NHL's play-by-play of each game, a page the tables are not built from: the list of goals (period, time, team, scorer, assists) is identical on 99.97% of the games, the goals by period and the number of penalties on every team line, the shots on goal on 98.31% of the team lines. From 2009-10, when the play-by-play becomes complete: hits on 99.80% of the team lines, and each skater's shots, hits and blocked shots on more than 99.9% of the lines.

### Said plainly

- **`Kickoff_UTC` is the scheduled start; `Puck_Drop_UTC` is the real one**, read from the NHL's official game report, as is `Duration_Min`. The report prints the time on a 12-hour clock without morning or afternoon: the reading closest to the scheduled start is kept. The puck drops a median of 8 minutes after the scheduled time. `Puck_Drop_UTC` is empty for 34 games and `Duration_Min` for 28: report missing, or a time that cannot be right (an end before the start, a start hours away from the schedule).
- **`Attendance` is empty for 729 games**: the 130 playoff games of August and September 2020 played without spectators, 573 games of 2020/2021 and 10 of 2021/2022 for which the report gives no figure, and 16 games from 2007 to 2011 whose report is missing or unreadable.
- **The columns that come from the official event summary** (`Missed_Shots`, `Attempts_Blocked`, `Faceoff_Wins`, `Faceoff_Losses`, the three time-on-ice splits, and the team's `Missed_Shots` and `Shot_Attempts`) are empty for 50 games: 40 games of 2006/2007 whose summary has another layout, 1 game of 2008/2009 for which the NHL serves the summary of another game, and 9 games from 2007/2008 to 2010/2011 whose summary is blank or incomplete (its faceoffs do not match the game's). In 2006/2007 the summary does not give `Attempts_Blocked` by skater: the column is empty for the skaters of that season, and the team's value is the opponent's `Blocked_Shots`.
- **Time-on-ice splits are empty on 2,287 skater lines in all**: those games, plus the lines where the event summary's total time on ice differs from the box score by more than 2 seconds.
- **`Attempts_Blocked` and the opponent's `Blocked_Shots`** are the same number until 2022/2023, bar 4 team lines. From 2023/2024 the NHL also counts in `Attempts_Blocked` the attempts blocked by a teammate, so it can be higher.
- **Team `Giveaways` and `Takeaways` include the goalies'**, who have no such column: they can exceed the sum of the skaters' lines.
- **The three stars are incomplete for 89 games**: none for 46 of them (22 in 2020/2021), one or two for the other 43. A star is left empty when the NHL names none, or names someone who did not play in the game.
- **Shootouts**: 11 shootouts of 2009/2010 have no usable detail at the NHL: their shootout columns are empty and they have no rows in the shootout table (2,478 shootouts detailed out of 2,489). `Game_Winner` is worked out from the sequence of attempts (the winner's goal that puts it ahead for good), because the NHL does not flag it in the early seasons.
- **83 goalie lines since 2022/2023 carried one save too many at the NHL**: `Saves` is `Shots_Against` minus `Goals_Against`, and `Save_Pct` follows. 6 decisions the NHL attached to the goalie who did not play are given to the one who did. One regular-season loss in overtime is recorded as an `L` (Minnesota Wild, 30 March 2024), as the NHL publishes it.
- **`Decision` in the playoffs**: an overtime loss is an `L`, as the NHL records it; `OTL` only exists in the regular season and in the August 2020 round-robin.
- **Goalies' shots against do not include empty-net goals**: `Shots_Against` of a team's goalies plus the opponent's empty-net goals make the opponent's `Shots`, with 95 exceptions out of 52,422 team lines in the NHL's own figures; their `Goals_Against` plus the same empty-net goals make the opponent's goals, except on 11 team lines.
- **`Situation_Code` starts in 2009/2010**: it is empty for the 22,113 goals of the first three seasons and for 14 later goals.
- **5,622 penalties have no player**: bench penalties, for the most part. 199,917 penalties name the opponent who drew them.
- **Goals by goalies**: 10 goals of the file are credited to a goalie (empty-net goals, or own goals the goalie touched last). They are in the goals table only: in those 10 games, the skater lines of the team add up to one goal fewer than its score.
- **Columbus at Dallas, 9 April 2014**: the game of 10 March was stopped in the first period and replayed in full on 9 April with Columbus keeping its 1-0 lead. The score is 3-1, the goals table has the three Columbus goals, and the box score credits Columbus's skaters with two.
- **A few figures do not add up at the NHL itself**: in 164 team lines out of 52,422, the hits, the blocked shots, the missed shots, the shots on goal, the faceoffs won or the power-play goals of the skaters differ from the team total, always by one or two; in 8 games the two teams' `Faceoffs` differ by one. They are left as published.
- **Assists**: on 270 skater lines out of 215,062 with an assist, the box score and the goals table do not credit the player with the same number of assists, 268 of them in 2009/2010. Both are left as the NHL publishes them.
- **A skater's `Faceoff_Pct` comes from the box score, his `Faceoff_Wins` and `Faceoff_Losses` from the event summary**: on 21 of the 353,599 skater lines with a faceoff, the two do not give the same ratio.
- **Officials**: two referees and two linesmen, except 5 games with one referee listed and 11 with one linesman.
- **Outdoor games** are in the file with their real attendance: 105,491 at Michigan Stadium on 1 January 2014 is the largest.
- **The 2026/2027 season stops on 19 November 2026**, 358 games. Later games come with the monthly update.

### Quick start

```python
import pandas as pd

games = pd.read_csv("NHL_Matchup_Stats_Games_2006-2026.csv", low_memory=False)
teams = pd.read_csv("NHL_Matchup_Stats_Team_Box_Scores_2006-2026.csv")
skaters = pd.read_csv("NHL_Matchup_Stats_Skater_Box_Scores_2006-2026.csv")
goalies = pd.read_csv("NHL_Matchup_Stats_Goalie_Box_Scores_2006-2026.csv")
goals = pd.read_csv("NHL_Matchup_Stats_Goals_2006-2026.csv")

# share of shot attempts of each team in each game
both = teams.merge(teams[["Game_ID", "Side", "Shot_Attempts"]], on="Game_ID", suffixes=("", "_Opp"))
both = both[both.Side != both.Side_Opp]
both["Attempt_Share"] = both.Shot_Attempts / (both.Shot_Attempts + both.Shot_Attempts_Opp)

# save percentage of each starting goalie over his last 10 starts before a date
starts = goalies[(goalies.Starter == 1) & (goalies.Date_ET < "2026-11-01")].sort_values("Date_ET")
last10 = starts.groupby("Player_ID").tail(10).groupby("Player_ID")[["Saves", "Shots_Against"]].sum()
last10["Save_Pct"] = last10.Saves / last10.Shots_Against

# games in which the home team scored first, and how often it then won
first = games[games.First_Goal == "Home"]
print(len(first), (first.Winner == "Home").mean())
```

### Licence

Single commercial user. Use the data as you wish, including the models, predictions and products you sell. Redistribution and resale of the files, or of the raw data in another format, are not permitted.

A question: contact@oliviersportsdata.com
