## Capstone Project Proposal

### Problem to Solve

Question: What factors in players best contribute to success in the postseason
for a professional baseball team? Is good pitching more important than good
batting? What role does fielding play? Is it better to have power hitters
(more home runs) or batters who can make consistent contact (more hits)?

Potential addition: How can teams maximize their ability to be successful
in the posteason while minimizing costs (as measured by player salaries)?
Does an increase in salary expenditures translate to better team performance?

### Client

Baseball team owners and managers are constantly making decisions on what
players to start or acquire. For most owners, the pinnacle of success is
defined by winning the World Series. With data-driven answers to the above
question, team owners can improve their decision making in a way that
translates to more wins and more championships.

### Data

For this project, I will use the Lahman Baseball Database. I acquired the data
through [Kaggle](https://www.kaggle.com/seanlahman/the-history-of-baseball/data).
The dataset includes a wide variety of data from every Major League Baseball
(MLB) league from 1871 to 2015.

#### Datasets most useful for solution

The datasets that will be most useful for solving the problem will be the
`batting`, `pitching`, `fielding`, `team`, and `postseason` datasets.
Data from `team` (specifically season-end record) and `postseason` will
be the goals, while data from the other datasets will be the inputs.

Since the `batting`, `pitching`, and `fielding` datasets are largely raw data
at the season level, there will be a lot of room for feature creation. For
batting, different kinds of averages can be created, some of which may be more
indicitive of team success than others. Pitching and fielding are similar,
thought to a lesser extent.

If the salary-minimization constraint is included, the `salary` dataset will
also be used. Salaries are reported by player and year, though team-wide
aggregates and trends can be produced.

#### Distributions, trends, and patterns in the data

Since the database includes 144 years of data, annual trends are the most
obvious to observe. One of the most important trends is the increase in the
number of professional baseball players over time. Since the game itself has
not changed significantly since 1871 (9 starting players per game), an increase
in the number of players will have important implications for the data. Even
when the increase in the amount of teams is taken into account, the number
of players per team as increased about three-fold since 1871.

In the `batting` dataset, we see an increase in home runs per player per year
over time, but a decrease in hits per player per year.

In the `pitching` dataset, we see an increase in strikeouts per game per year
over time, while walks per game per year is fairly consistent. Shutouts and
complete games by pitchers declines over time.

In the `fielding` dataset, there is a steady but sharp decline in the number
of errors per player over time. Since errors are fairly rare for professional
players, the distribution is very right-tailed. 

Since the datasets include data for both starters and non-starters (and these
roles may change throughout a season), most of the raw variables are extremely
right-tailed. Much of this can be corrected by adjusting to per-game (or
per-at-bat) stats. The distribution of batting averages (hits divided by at-bats)
looks quite normal.

Salaries grouped by team experience an upward trend, with some severe 
heteroskedasticity, even when adjusted for inflation. A few teams
(Yankees, Dodgers, and Red Sox) experience explosive salary growth in recent
years. May be something to look into.

#### Missing values/anomalies and important dates

Since each dataset includes data for every relevant player by year, there are
missing values for many variables for some players (those who do not start
or even play very often). For example, there are a total of 101,332 entries
in the `batting` dataset, but for the variable `ab` (at-bats) there are
about 50,000 missing values.

Some of the data in `batting` is inconsistent (many `NaN` or 0 values) until
around 1950. Similar case for some of the `pitching` data, which also has
some missing values until 2000.

As the game of baseball has become more popular and technology has improved,
data collection has greatly improved over time. For this reason, some data
in the database is only available for later years. For example, salary data
begins in 1985.

Two player strikes took place throughout MLB history, as shown in data.
These strikes took place in 1981 and 1994. Additionally, the start of
World War I caused the 1918 season to end prematurely. Because there were
less games, for each of these years, season stats will be inconsistent
(though this may be fixed by adjusting to per-game averages).

In both 1884 and 1890, there were one-year spikes in the number of players.
Conversely in 1900, there is a one-year decline in the number of players.
A steadily increasing trend in the number of players begins around 1917.

According to the `appearances` dataset, beginning in 1974, the American League
added the designated hitter, a non-fielding batter. Starting here, there may be
a divergence in batting stats between the Leagues.

### Project Deliverables

1. The code used to clean the data, solve the problem, and produce relevant
charts and graphs.

2. A paper explaining the process and describing the data story.
