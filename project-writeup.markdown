## Capstone Project Milestone

### Problem to Solve

In the movie *Moneyball*, Oakland Athletics general manager Billy Beane attempts to build a baseball team with a budget of less than $40 million, less than 1/3 than the budget of the New York Yankees. In just one season (2002), he built a team nearly from the ground up that won 103 out of 162 games, winning their division by 4 games. Their season ended when they were defeated by the Minnesota Twins in the first round of the playoffs, but Beane changed the game forever by introducing robust statistical analysis to the game of baseball.

If someone wanted to do this today, how could a new team owner or GM achieve this? What is the minimum amount of money an MLB team needs to be successful? If a new team is going to be formed, how much money does the owner need to spend on players for the team to win at least half their games?

### Client

While in reality some team owners may have goals other than winning championships (such as having flashy players or minimizing costs above all), our target client will be an brand new team owner or general manager who wants to be successful on the field. His or her main goal will be to maximize the number of wins and chance of winning the World Series, while spending the least possible amount of money on player salaries.

### The Data and Some Background about Baseball

For this project, I will use the Lahman Baseball Database. I acquired the data through [Kaggle](https://www.kaggle.com/seanlahman/the-history-of-baseball/data). The dataset includes a wide variety of data from every Major League Baseball (MLB) league, team, and player. Although much of the data is available from the 1871 to the 2015 seasons, the `salary` dataset only includes data on players from 1985 to 2015, so we will limit our analysis to these years.

Most of the datasets are organized by season and player. For example, row 21109 of the `salary` dataset includes salary data about Alex Rodriguez in 2010. Players often play for multiple seasons in their career. The mean number of seasons played for all players 1985-2015 is about 5 seasons. Modern-day seasons include 162 games, running from March to September.

The `player` dataset is organized by player alone, as these data do not change from year to year. The `team` dataset, obviously, is organized by season and team, not player.

In baseball, and thus in this dataset, there are two different kinds of players: pitchers and batters. For pitchers, we have the `pitching` dataset, which includes stats like strikeouts, wins, and earned run average (average number of runs per nine innings the pitcher is responsible for). For batters, we have the `batting` dataset, which includes stats like hits, at-bats, home runs, doubles, triples, and runs-batted-in (a hit resulting in one or more players on the team scoring a run). Among batters, there are also other positions, such as infielders and outfielders, each of which may have different salaries.

One factor that may contribute to differences in stats is that some teams are in the American League while others are in the National League. The American League, because they have a designated hitter and the pitchers do not hit, tend to have bigger hitters, who tend to be paid higher salaries. Statistically, this means that while the leagues have similar median and mean salaries, the standard deviation of AL salaries tends to be larger.

### Salary Over Time

Salaries have increased significantly since 1985. From 1985 to 2015, total team salaries increased by over a factor of 11, though about half of the increase is due to inflation. Adjusting for inflation, total team salaries have still increased by a factor of 5. The rise in salaries has been fairly steady over time, though there is a sharp increase in median salary beginning in 2013.

The distributions of both total team salaries and individual player salaries are consistently right-tailed over time, even when logged.

### Impact of Salary on Wins

In our proposed problem, we assume a relationship between total team salary and the number of wins a team will achieve. In order to test this relationship, I set up a set of linear regressions between log of total team salary for a given year and total number of wins for that year. Results vary from year to year. A number of years (1996, 1998, 1999, 2002-2007, 2009, 2010, and 2013) show a statistically significant (alpha=0.05) positive relationship between log of total team salary and number of wins.

For the years that do not show a statistically significant relationship between salary and wins, 

### Composition of Salaries

When putting together a team, the total sum of player salaries is not the only factor. The spread of salaries is also important. One way of measuring the spread of salaries of a team is the standard deviation of salaries for that team. As mentioned above, the standard deviation of salaries consistently differs between the American and National League. When we include standard deviation of team salary along with log of total team salary in the linear regressions from above, the results are inconsistent. But when a statistically significant relationship is found (e.g. in 1996 and 2012), standard deviation appears to have a negative relationship with number of wins.

Another way to measure the composition of salaries within a team is to see what kind of salaries each position on the team has.

### Machine Learning Integration

To finish the project, I will include a machine learning component. The selected features will be individual player features that a new team owner could know ex ante (an owner cannot before the season begins how well a player will perform that year). Some factors include player age, number of years in the MLB, height and weight, starting position, and stats from previous years.

Five Thirty Eight writer Nate Silver suggests that age is one of the most important factors for predicting player performance in the MLB (cite needed).

#### Stats from previous years


