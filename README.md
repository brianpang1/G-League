# G-League

## Background:

The NBA G-League is the official minor league of the National Basketball Association.
In total, there are 28 teams with a roster capacity of 10-13 players each.
Each G-League team's season runs on a 50 game schedule which runs concurrently with the NBA season, with the G-League starting 2 weeks after the NBA season start and ending two weeks before the NBA season end.
Since its inception in 2001, the NBA G-League has continuously grown in size and support from the NBA, resulting in the G-League becoming a viable second option for professional basketball players who did not make it into the NBA after college.


Players not at the NBA-level choose to play in the G-League for the chance at impressing NBA scouts and ultimately signing a contract with an NBA team.

NBA G-League players who are called up to an NBA team are signed onto contracts ranging in length from a 10-day to multi-year deal.

Any NBA contract significantly increases a G-League player's salary. For the 2018-2019 season, G League players were paid $7000/month, or $35000 for the full season, while 10-day NBA contracts were worth a minimum of $46080 (increased based on years of experience).


## Purpose:

This project's purpose is to use machine learning to predict which G-League players are NBA contract worthy. I defined a variable "NBA_Player" as a player who was signed to an NBA team with any kind of contract in the same season that they played in the G-League.
To create the dataset necessary for this analysis, I utilised webscraping to gather G-League player statistics, G-League callups, G-League assignments, and two way player historical data from various basketball websites for all seasons from the 2009-2010 season to the 2018-2019 season.


## Data I scraped:

G League Player statistics. source: www.basketball-reference.com

Called Up: Players who played in the G-League then signed with an NBA team mid-season on anywhere from a 10 day to multiyear contract. source: www.gleague.nba.com

Assigned: NBA Assignees (G-League assignments): NBA Players who were sent to the G-League while still under contract with NBA, most commonly because they were not getting enough playing time to develop on the NBA team they were on, or in some cases were easing back into basketball after injury. source: www.gleague.nba.com

Two-Way Player: Players under contract with an NBA team who spend the bulk of the season in the NBA G League, and no more than 45 days with their NBA team, allowing the NBA team to retain their rights while the players stays in the G-League. source: www.hoopsrumors.com

NBA Minutes: Players with NBA Minutes: There were fringe cases where a player will have signed with an NBA team, gets waived (contract is renounced), then join the G-League. To account for these players, I also scraped 10 years of NBA per game stats to get the names of all players who played minutes in the NBA. source: www.basketball-reference.com

In the end, I create a new variable called 'NBA_Player' which is equal to 1 if the player fulfilled the requirements any of the above during a given season.

## Player Statistics Variable Definitions (from Basketballreference.com):
Tm -- Team

Age -- Player's age on February 1 of the season

G -- Games

GS -- Games Started


MP -- Minutes Played Per Game

FG -- Field Goals Per Game

FGA -- Field Goal Attempts Per Game

FG% -- Field Goal Percentage

3P -- 3-Point Field Goals Per Game

3PA -- 3-Point Field Goal Attempts Per Game

3P% -- 3-Point Field Goal Percentage

2P -- 2-Point Field Goals Per Game

2PA -- 2-Point Field Goal Attempts Per Game

2P% -- 2-Point Field Goal Percentage

eFG% -- Effective Field Goal Percentage -- This statistic adjusts for the fact that a 3-point field goal is worth one more point than a 2-point field goal.

FT -- Free Throws Per Game

FTA -- Free Throw Attempts Per Game

FT% -- Free Throw Percentage

ORB -- Offensive Rebounds Per Game

DRB -- Defensive Rebounds Per Game

TRB -- Total Rebounds Per Game

AST -- Assists Per Game

STL -- Steals Per Game

BLK -- Blocks Per Game

TOV -- Turnovers Per Game

PF -- Personal Fouls Per Game

PTS -- Points Per Game

