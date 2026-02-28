# 🎮 Foresight — Performance Tracker

> **Do losses cluster after certain win thresholds — and if so, is that a reflection of my own fatigue and psychology, the matchmaking system working against me, or both at once?**

A behavioural research instrument designed for the EA FC 26. Tracks the psychological and contextual data that raw win/loss records deliberately obscure, building a personal dataset detailed enough to separate three confounded variables: player fatigue, player psychology, and potential system behaviour.

**Status:** Active | **Phase:** Data collection | **Live tracker:** [View Google Sheets Dashboard](https://docs.google.com/spreadsheets/d/1usN6zVsdgHveMcKy7Ekx5Rhs2AXRDzJd2YRi7jTo-Ms/edit?gid=674564818#gid=674564818)
---

## Why This Exists

In 2017, EA filed and was granted a patent for **Engagement Optimised Matchmaking (EOMM)** — a retention system that analyses behavioural data, including win/loss streaks, playstyle, and rage-quit tendencies, and "may" manipulate match outcomes to keep players engaged for longer.

The patent "indirectly infers" that pairing high-performing players with weaker teammates, or serving easy matches to break losing streaks, is based on when a player is most psychologically at risk of quitting.

**The problem:** Football games have enough natural variance that engineered outcomes have perfect cover. A misplaced pass could be concentration dropping, input lag, or both simultaneously. The system does not need to be obvious.

This creates three variables that raw win/loss data cannot separate:

| Variable | Description |
|----------|-------------|
| Player fatigue | Performance deteriorating across a long session |
| Player psychology | Tilt, expectation bias, pressure responses |
| System behaviour | Matchmaking influencing opponent quality at specific thresholds |

Standard tracking tools show you wins and losses. They do not show you *why* the losses happened or when in a session they cluster. This tracker is built to answer that.

---

## What Gets Tracked and Why

Every field exists for a specific analytical reason. Logging discipline is maintained by capturing key data points at fixed moments — before the match loads, at half-time only, and immediately post-match — to prevent post-rationalisation contaminating the data.

| Field | When Logged | Why |
|-------|-------------|-----|
| WKD / Sitting / Game # | Before session | Session structure affects fatigue curves — 10 games in one sitting vs split across days produces different patterns |
| Pre-match expectation + confidence | Before game loads | Must be logged before seeing the result — pessimism and optimism both influence performance |
| Pressure ratio | Auto-calculated | Wins needed ÷ games remaining. Highlights when you are in the high-pressure window |
| HT input flag | Half-time only | Single Yes/No. Did inputs feel off? Logged before the result exists to prevent bias |
| Result + rage quit flag | Immediately post-match | Distinguishes a normal loss from a full discipline collapse |
| Discipline + concentration | Post-match | Two separate metrics — discipline is reactive (emotional regulation), concentration is anticipatory (mental presence) |

---

## The Three Zones

Every game in a 15-game Weekend League session falls into one of three psychological states. The tracker identifies zone automatically based on wins needed vs games remaining.

| Zone | Games | Description |
|------|-------|-------------|
| **PURSUIT** | 1 → target-1 | Full stakes. Both discipline and concentration are active. Baseline performance lives here |
| **THRESHOLD** | One win from target | Highest pressure in the entire set. This single game deserves more analytical attention than any other |
| **BEYOND TARGET** | Past benchmark | Lower personal stakes. Risk of mentally checking out. Tests whether your ceiling is real or psychological |

---

## Live Data (Week 1 — Early Phase: SCREENSHOT)

*The dataset is in early collection and is being populated as of publication. Patterns below are directional, not statistically significant yet.*

**Session summary:**

| Metric | Value |
|--------|-------|
| Games logged | 7 |
| Win rate | 71.4% |
| Avg score margin (wins) | +2.8 |
| Avg score margin (losses) | -1.5 |
| Your rage quits | 0 |
| Opponent rage quits | 3 |
| HT input flags | 0 |

**Tilt indicators:**

| Metric | Value | Signal |
|--------|-------|--------|
| Avg discipline — wins | 3.8 | Baseline emotional regulation |
| Avg discipline — losses | 3.0 | Drops on losses — tilt present but moderate |
| Avg concentration — wins | 3.8 | Consistent with discipline |
| Avg concentration — losses | 4.5 | Higher on losses — suggests increased focus after falling behind |

**Win rate by sitting:**

| Sitting | Win % | Note |
|---------|-------|------|
| Sitting 1 | 66.7% | First block of the day |
| Sitting 2 | 75.0% | Second block — performing better |
| Sitting 3 | 0.0% | No games logged yet |

**Win rate by zone:**

| Zone | Win % | Played |
|------|-------|--------|
| PURSUIT | 33.3% | 15 |
| THRESHOLD | 0.0% | 0 |
| BEYOND TARGET | 0.0% | 0 |
| ASPIRATION | 0.0% | 0 |

*Note: All games currently fall within the Pursuit zone as the dataset is being established.*

---

## Hypotheses Being Tested

After 3–4 weekends of clean logging, the data will be analysed to look at answering:

- **Do losses cluster after a specific win count?** If the loss rate rises sharply above (X), wins regardless of session length; that is a pattern worth examining — ceiling, fatigue, or system behaviour.
- **Does concentration drop after hitting the win target?** If concentration scores fall after reaching (X), the ceiling may be partly psychological.
- **Do high pressure ratios correlate with lower discipline scores?** If discipline drops when pressure ratio hits 0.7+, that is a tilt threshold that can be trained around.
- **Does pre-match expectation predict outcome?** If pessimism before a game has no correlation with loss, psychological state going in is less influential than assumed.
- **Does win rate differ between sittings?** Is session management a larger variable than matchmaking or skill?

---

## Current Limitations

| Gap | Impact |
|-----|--------|
| Dataset too small for statistical significance | 7 games across 1 weekend — directional only, no conclusions yet |
| Cannot separate system behaviour from player behaviour | The core confound — this is why the dataset needs to be large enough to control for known psychological variables first |
| Time of day logging incomplete | No data yet — will reveal whether session timing affects performance independently of fatigue |
| Tracker design still being refined | Some fields and formulas under review — early logs may need retroactive correction |

---

## Tracker Structure

The Google Sheets tracker has three tabs:

| Tab | Purpose |
|-----|---------|
| **Setup** | Player name, win target, aspiration target — all formulas pull from here |
| **Match Log** | Row-by-row game logging with pre-match, in-game, and post-match fields |
| **Dashboard** | Auto-updating summary statistics, zone analysis, sitting breakdown, and tilt indicators |

**[Access the live tracker here](https://docs.google.com/spreadsheets/d/1usN6zVsdgHveMcKy7Ekx5Rhs2AXRDzJd2YRi7jTo-Ms/edit?gid=674564818#gid=674564818)**

Feel free to test and track your own progression

---

## The Honest Caveat

The tracker only works if the data is accurate. A discipline score of 5 when you were visibly tilted is worse than no score at all. The goal is not to look good in your own data. It is to understand yourself clearly enough to make better decisions — including the decision to stop playing.

The environment is designed to resist your self-audit. This tracker is the countermeasure.

---

*Earlier versions can works as a FIFA stats tracker. But the aim is to serve as a behavioural research instrument in a competitive environment, specifically engineered to make self-analysis difficult, thereby assisting decision-making and reducing influence based on emotional states.*
