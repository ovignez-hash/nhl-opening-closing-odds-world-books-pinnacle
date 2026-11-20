# 🏒 NHL Opening & Closing Odds — Pinnacle + 7 World Books (2006–2026)

**20 games, 2006-07 to 2026-27 — the first and last games of the file, four Stanley Cup clinchers, the first Winter Classic, London 2007 and Prague 2024**

Most NHL odds archives give you the US books, or one closing number per game.

The full dataset puts **up to 8 books side by side on each game, in decimal odds**: Pinnacle, Bet365, William Hill,
Bwin, Betway, Betfair Exchange, SBOBET and 1xBet. Moneyline, puck line and totals (overtime included or regular time
only, never mixed), plus the 1X2 in regular time at six books: **the opening and the closing price, each with the time
it was recorded**.

→ **[Get the full archive](https://sportsdataolivier.gumroad.com/l/jytwci?utm_source=github&utm_medium=readme&utm_campaign=nhl_world&utm_content=hero)** — 26,079 games, 2006-07 to 31 October 2026 · also on [Whop](https://whop.com/oliviersportsdata/nhl-opening-closing-odds-pinnacle-7-world-books-2006-2026/?utm_source=github&utm_medium=readme&utm_campaign=nhl_world&utm_content=whop_hero)

This sample is cut from the full file: the same 194 columns, the rows copied byte for byte, at about 0.08% scale.

---

## One game, seven books

Hurricanes at Oilers, 22 October 2026, moneyline. Seven books opened and closed it, all but SBOBET. 5-5 after 60
minutes, Edmonton won the shootout: the moneyline paid the Oilers, and the 1X2 draw, regular time only, paid at
Bet365 4.25, William Hill 4, Bwin 4.1, Betway 4.2, 1xBet 4.31.

| Book | Open, Oilers / Hurricanes | Close, Oilers / Hurricanes |
|---|---|---|
| Pinnacle | 1.9709 / 1.9174 | 2.18 / 1.7634 |
| Bet365 | 1.89 / 1.84 | 2.07 / 1.71 |
| William Hill | 1.8 / 2 | 2.1 / 1.73 |
| Bwin | 1.91 / 1.91 | 2.15 / 1.75 |
| Betway | 1.95 / 1.87 | 2.1 / 1.77 |
| Betfair Exchange | 2.02 / 1.9 | 2.16 / 1.76 |
| 1xBet | 1.9434 / 1.9434 | 2.1 / 1.7519 |

---

## What's in this sample

| | |
|---|---|
| Games | 20 — 15 of the 21 seasons, from the first game of the file (4 Oct 2006) to its last (31 Oct 2026) |
| Stages | 15 regular season · 5 playoffs: 4 Stanley Cup clinchers and 1 game of the 2020 qualifying round |
| Endings | 15 in regulation, 2 in overtime, 3 in a shootout |
| Prices | 931 |
| Books | 8 — Pinnacle, Bet365, William Hill, Bwin, Betway, Betfair Exchange, SBOBET, 1xBet |
| Columns | 194 |
| File | `NHL_World_Opening_Closing_Odds_2006-2026_SAMPLE.csv`, plus the README of the full product |

| Date (ET) | Game | Stage | Final, away–home | Books, closing / opening ML |
|---|---|---|---|---:|
| 4 Oct 2006 | Sabres @ Hurricanes | Regular Season | 3–2 SO | 0 / 0 |
| 29 Sep 2007 | Ducks @ Kings | Regular Season | 1–4 | 0 / 0 |
| 1 Jan 2008 | Penguins @ Sabres | Regular Season | 2–1 SO | 0 / 0 |
| 15 Dec 2008 | Avalanche @ Red Wings | Regular Season | 3–2 | 1 / 1 |
| 9 Jun 2010 | Blackhawks @ Flyers | Playoffs | 4–3 OT | 3 / 3 |
| 6 Oct 2011 | Flyers @ Bruins | Regular Season | 2–1 | 6 / 4 |
| 13 Jun 2014 | Rangers @ Kings | Playoffs | 2–3 OT | 4 / 3 |
| 8 Oct 2014 | Canadiens @ Maple Leafs | Regular Season | 4–3 | 4 / 1 |
| 6 Oct 2017 | Golden Knights @ Stars | Regular Season | 2–1 | 5 / 3 |
| 1 Aug 2020 | Jets @ Flames | Playoffs | 1–4 | 4 / 0 |
| 28 Sep 2020 | Lightning @ Stars | Playoffs | 2–0 | 5 / 4 |
| 20 Jan 2021 | Oilers @ Maple Leafs | Regular Season | 3–1 | 7 / 4 |
| 12 Oct 2021 | Kraken @ Golden Knights | Regular Season | 3–4 | 7 / 1 |
| 24 Jun 2024 | Oilers @ Panthers | Playoffs | 1–2 | 7 / 5 |
| 4 Oct 2024 | Devils @ Sabres | Regular Season | 4–1 | 7 / 2 |
| 8 Oct 2024 | Blackhawks @ Utah HC | Regular Season | 2–5 | 6 / 1 |
| 1 Apr 2026 | Canucks @ Avalanche | Regular Season | 8–6 | 6 / 5 |
| 11 Oct 2026 | Hurricanes @ Flyers | Regular Season | 4–1 | 7 / 7 |
| 22 Oct 2026 | Hurricanes @ Oilers | Regular Season | 5–6 SO | 7 / 7 |
| 31 Oct 2026 | Flames @ Avalanche | Regular Season | 2–5 | 7 / 5 |

*Books* counts, out of 8, the books with a closing / opening moneyline for that game. Why each game is
here, game by game: `sample/README.md`.

---

## In this repository

| File | Content |
|---|---|
| `sample/NHL_World_Opening_Closing_Odds_2006-2026_SAMPLE.csv` | the 20 games, 194 columns |
| `sample/README.md` | why each game is here, then the README of the full product |
| `matchup_stats_sample/` | the same 20 games in NHL Matchup & Stats: game sheets, team, skater and goalie box scores, scratches, goals, penalties, shootouts, players (9 CSV + README) |
| `NHL_World_Verify_Before_You_Buy.ipynb` | the figures of the listing and of its README recomputed from the full file (all the file can show), results shown |

---

## Columns

| Block | Columns | Content |
|---|---:|---|
| Game | 18 | `League`, `Game_ID` (`YYYYMMDD_AWAY_HOME`, US Eastern date), `NHL_Game_ID`, `Season`, `Stage`, `Kickoff_UTC`, `Epoch`, teams, final score, `Winner`, `Total_Score`, `Margin`, `Match_Ending`, score after 60 minutes, `Result_60` |
| Bet365, Betway | 30 each | moneyline, puck line, total and 1X2, opening then closing, with the time of each |
| 1xBet | 30 | moneyline, puck line, regular-time total and 1X2 |
| Pinnacle | 22 | moneyline, puck line and total |
| Bwin | 22 | moneyline, regular-time total and 1X2 |
| William Hill, Betfair Exchange | 14 each | moneyline and 1X2 |
| SBOBET | 14 | moneyline and regular-time total |

`{Book}_ML_Home_Open` · `{Book}_ML_Home_Close` · `{Book}_ML_Close_Time` · `{Book}_PuckLine_Home_Line_Close` · `{Book}_Total_Line_Close` · `{Book}_RegTotal_Line_Close` · `{Book}_1X2_Draw_Close` — the prefixes are `Pinnacle_`, `Bet365_`, `WilliamHill_`, `Bwin_`, `Betway_`, `BetfairExchange_`, `SBOBET_`, `1xBet_`.

### How to read it

**Prices are decimal odds**, up to 4 decimals: `1.91`, `2.375`. **The puck line is ±1.5 only, the home team's line:** `-1.5` means the home team gives 1.5 goals. **The moneyline includes overtime and the shootout; the 1X2 is regular time only**, so a game tied after 60 minutes is a draw. **Two kinds of totals, never mixed:** `Total` counts overtime and the shootout, `RegTotal` regular time only; `Home_Score_60`, `Away_Score_60` and `Result_60` give the score after 60 minutes. **Times are UTC**, ISO 8601 with the T and the Z. **The opening price is the first price recorded for the main line, the closing price the last one before the start**; each one carries its own time, so you can see how close to the start it was taken.

```python
import pandas as pd

df = pd.read_csv("NHL_World_Opening_Closing_Odds_2006-2026_SAMPLE.csv")

# Pinnacle's no-vig probability of the home team at the close
h, a = 1 / df["Pinnacle_ML_Home_Close"], 1 / df["Pinnacle_ML_Away_Close"]
pinnacle_home = h / (h + a)

# the closing 1X2 draw at five books, and the games tied after 60 minutes
draw = df[["Bet365_1X2_Draw_Close", "WilliamHill_1X2_Draw_Close", "Bwin_1X2_Draw_Close", "Betway_1X2_Draw_Close", "1xBet_1X2_Draw_Close"]]
tied_60 = df["Result_60"] == "Draw"

# goals against the line: regular time for 1xBet's total, overtime included for Pinnacle's
reg_goals = df["Home_Score_60"] + df["Away_Score_60"]
over_reg = reg_goals > df["1xBet_RegTotal_Line_Close"]
over_full = df["Total_Score"] > df["Pinnacle_Total_Line_Close"]
```

---

## Said plainly

- **2006-07 and 2007-08 carry the 1X2 only** (regular time): the moneyline, the puck line and the totals start in 2008-09. 232 games have no price at all, 174 of them in November 2007; they stay in the file so that the schedule is complete.
- **Pinnacle starts on 1 August 2020**, with the 2020 playoffs. From then, 469 games have no Pinnacle moneyline: all Arizona Coyotes games to 2023-24, all Utah Hockey Club games of 2024-25, 61 games of the 2020 playoffs and 15 others.
- **The moneyline includes overtime and the shootout; the 1X2 is regular time only.** `Total` counts overtime and the shootout (Pinnacle, Bet365, Betway), `RegTotal` regular time only (Bwin, SBOBET, 1xBet): never mixed in one column.
- **William Hill: moneyline from February 2009, 1X2 from October 2006**; absent from the start of 2025-26 to 31 March 2026.
- **Betfair Exchange: moneyline from February 2009, 1X2 from December 2007 to June 2014.** Its prices appear to be net of the exchange's commission, and it has few openings.
- **SBOBET: moneyline from March 2009 to June 2014 (then 5 games), regular-time total from October 2014 to February 2022.** No puck line.
- **1xBet: 1X2, puck line and regular-time total from October 2014, moneyline from January 2021** (none in 2025-26).
- **Bet365's puck line and total:** 2008-09 and 2009-10 (then a handful of games in 2010-11 and 2011-12), part of 2012-13, then from 31 December 2017. **Betway's:** puck line 2008-09 to 2011-12 (then one game in 2012-13), total 2008-09 and 2009-10 (then 6% of 2010-11), both back from November and December 2024.
- **Moneyline gaps:** Bwin, 30 January to 7 October 2014; Betfair Exchange, 12 June 2014 to 29 February 2016; Betway, 23 March 2015 to 11 October 2016.
- **2026-27 so far (226 games): Pinnacle, Bet365, William Hill, Bwin, Betway, Betfair Exchange and 1xBet**, each with a closing moneyline on at least 91% of the games.
- **No preseason, no All-Star games, no player props, no periods, no live odds, no futures.** One opening and one closing price per book and market, not every move in between. Every recorded move (timestamped odds), other books or another scope: built to order on request.

---

## Verify before you buy

The figures of the listing and of its README — games, prices, the books and their first price, coverage season by
season, opening and closing times, the two kinds of totals, the gaps stated above, the games on the listing's images —
recomputed from the full file and printed PASS or FAIL, all but what the file cannot show (the counts of prices left
out while it was built): [on Kaggle](https://www.kaggle.com/code/oliviersportsdata/nhl-world-books-odds-verify-before-you-buy) · [on GitHub](https://github.com/ovignez-hash/nhl-opening-closing-odds-world-books-pinnacle/blob/main/NHL_World_Verify_Before_You_Buy.ipynb) (results shown).

---

## The full dataset

| | Sample | Full |
|---|---|---|
| Games | 20 | 26,079 |
| Seasons | 15 of the 21, 2006-07 to 2026-27 | 2006-07 to 2026-27, through 31 Oct 2026 |
| Prices | 931 | 1,290,732 |
| Columns | 194 | 194 |
| Files | 1 CSV + README | 1 CSV + README |

Once a year, after the Stanley Cup Final, the file adds the completed season. The games after 31 October 2026 come with
the [NHL World Books monthly updates](https://sportsdataolivier.gumroad.com/l/dhlawd?utm_source=github&utm_medium=readme&utm_campaign=nhl_world&utm_content=monthly): each month's games, same 194 columns, ready to append.

The box score behind each game is sold separately: [NHL Matchup & Stats](https://sportsdataolivier.gumroad.com/l/vavcu?utm_source=github&utm_medium=readme&utm_campaign=nhl_world&utm_content=matchup) (also on [Whop](https://whop.com/oliviersportsdata/nhl-matchup-stats-2006-2026/?utm_source=github&utm_medium=readme&utm_campaign=nhl_world&utm_content=matchup_whop)): game sheets, team, skater and goalie box scores, scratches, goals, penalties and shootouts since 2006-07, on the same Game_ID. Its 20-game sample is in `matchup_stats_sample/`.

→ **[Get the full archive](https://sportsdataolivier.gumroad.com/l/jytwci?utm_source=github&utm_medium=readme&utm_campaign=nhl_world&utm_content=footer)** · also on [Whop](https://whop.com/oliviersportsdata/nhl-opening-closing-odds-pinnacle-7-world-books-2006-2026/?utm_source=github&utm_medium=readme&utm_campaign=nhl_world&utm_content=whop_footer)

---

## Licence

Sample: free to explore and evaluate.
Full product: single commercial user. Use the data as you wish, including the models, predictions and products you sell.
Redistribution and resale of the files, or of the raw data in another format, are not permitted.

A question, an invoice or a custom extract: contact@oliviersportsdata.com

---

*Olivier Sports Data — From Chicken Area 🐔*
