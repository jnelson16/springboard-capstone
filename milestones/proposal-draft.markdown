## Capstone Project Proposal

### Problem to Solve

Question: How can a cost-minimizing professional baseball team best compile
a team while still being successful? In other words, what is the minimum
amount of money a team can spend in player salaries while still
having good enough players to win the World Series?

### Client

Baseball team owners and managers are constantly making decisions on what
players to start or acquire. With data-driven answers to the above
question, team owners can improve their decision making in a way that
translates to more wins and more championships. While in reality some team
owners may have goals other than winning championships (such as having flashy
players or minimizing costs above all), our target client will be an owner
who wants to be successful on the field.

### Data

For this project, I will use the Lahman Baseball Database. I acquired the data
through [Kaggle](https://www.kaggle.com/seanlahman/the-history-of-baseball/data).
The dataset includes a wide variety of data from every Major League Baseball
(MLB) league from 1871 to 2015.

The datasets that will be most useful for solving the problem will be the
`batting`, `pitching`, `fielding`, `team`, `postseason`, and `salary` datasets.
Data from `team` (specifically season-end record) and `postseason` will
be the goals, while data from the other datasets will be the inputs. Since
the `batting`, `pitching`, and `fielding` datasets are largely raw data
at the season level, there will be a lot of room for feature creation. For
example, with `batting`, different kinds of averages can be created, some
of which may be more indicitive of team success than others.

Since the database includes 144 years of data, annual trends will be the most
obvious to observe, so I will begin there when exploring the data. I will
also look at the distributions of several key variables, and for any strange
anomolies or inconsistencies in the data that may exist.

### Project Deliverables

1. The code used to clean the data, solve the problem, and produce relevant
charts and graphs.

2. A paper explaining the process and describing the data story.
