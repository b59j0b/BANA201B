java cBANA201B Prof. John Turner
Homework 2
Please read “Homework Formatting Instructions”
Be sure to read the description below carefully
The National Basketball Association (NBA) is composed of 30 teams which are divided into two 
conferences of three divisions with five teams each. NBA games are divided into regular season 
and playoffs. The NBA regular season follows an asymmetrical round-robin tournament 
(otherwise known as uneven paired competition) format where the number of games between any 
two teams depends on their conference and divisional affiliations. In an NBA season each team 
plays 82 games, 41 at home and 41 on the road; in total, there are 1230 games in an NBA season. 
Each regular season takes approximately 180 days, spanning from mid-October to mid-April. 
Games are scheduled throughout the day, every single day except the All-star game break which 
is a one-week period in which the NBA All-star game as well as other events (e.g., slam dunk 
contest, three-point shooting contest, rising stars match, etc.) take place. Holidays (e.g., Christmas 
and MLK day) and weekends are more popular times to watch NBA games. Multiple national and 
local TV channels air the NBA games, including ESPN, TNT, ABC, and NBA-TV. 
Scheduling the entire 1230-game season and assigning games to dates, arenas, and TV channels is 
an extremely challenging task. Matt Winick, Senior Vice President of Scheduling and Game 
Operations is the main person responsible for producing the NBA regular season schedule. Matt 
has decided to break the scheduling task into two parts: i) for each four-day period, selecting a set 
of games that should be played, and then ii) assigning the selected games to specific days within 
this 4-day period. Matt’s wishes to produce a schedule that maximizes the revenue generated from 
airing TV commercials.
In this assignment, you will help Matt produce the NBA game schedule for a four-day time period 
which spans Thursday, February 4 through Sunday, February 7. The following table liststhe games 
Matt has selected to be played during this time period, as well as popularity ratings for each game 
on a scale of 0 to 2, with 0 being the least popular and 2 being the most popular. The popularity 
rating is determined by the ranking of the host and guest teams, location, and overall popularity of 
those franchises. 
Matt estimates that the NBA’s revenue for each game is directly related to its popularity rating. In 
general, games played on Thursday generate $1 million in revenue for each popularity point, 
Friday games generate $1.5 million in revenue for each popularity point, and weekend games 
generate $2 million in revenue for each popularity point. However, since Sunday, February 7th
coincides with the National Football League (NFL) Super Bowl, the games played on that Sunday 
will generate only $0.5 million in revenue for each popularity point. As an example, the first game 
BANA201B Prof. John Turner
(Celtics at Lakers) in the table below would generate $2M in revenue if played on Thursday, $3M 
if played on Friday, $4M if played on Saturday, and $1M if played on Sunday.
Game Abbreviation Popularity Rating
1 Boston Celtics @ LA Lakers BOS – LAL 2
2 Atlanta Hawks @ LA Clippers ATL – LAC 0.75
3 Portland Trail Blazers @ Milwaukee Bucks POR – MIL 1.25
4 Denver Nuggets @ Washington Wizards DEN – WAS 0.6
5 Utah Jazz @ Brooklyn Nets UTA – BKN 1.5
6 Indiana Pacers @ Dallas Mavericks IND – DAL 1.1
7 Charlotte Hornets @ New Orleans Pelicans CHA – NOP 1.2
8 New York Knicks @ Houston Rockets NYK – HOU 0.6
9 Toronto Raptors @ Phoenix Suns TOR – PHX 1
10 Chicago Bulls @ Cleveland Cavaliers CHI – CLE 0.45
11 Miami Heat @ Orlando Magic MIA – ORL 1.1
12 Detroit Pistons @ San Antonio Spurs DET – SAS 0.5
13 Sacramento Kings @ Golden State Warriors SAC – GSW 1.25
14 Memphis Grizzlies @ Oklahoma City Thunder MEM – OKC 0.75
15 Philadelphia 76ers @ Minnesota Timberwolves PHI – MIN 1.3
16 Toronto Raptors @ 代 写BANA201B、Python
代做程序编程语言LA Lakers TOR – LAL 1.9
17 Phoenix Suns @ Golden State Warriors PHX – GSW 1.4
18 LA Clippers @ Sacramento Kings LAC – SAC 0.9
19 Utah Jazz @ Washington Wizards UTA – WAS 1.1
20 New York Knicks @ San Antonio Spurs NYK – SAS 0.8
BANA201B Prof. John Turner
The number of game slots for each day during this four-day period is given in the table below:
Date Game slots available
Thursday, February 4 5
Friday, February 5 6
Saturday, February 6 6
Sunday, February 7 3
Matt must consider the following managerial constraints when producing the schedule:
i. Each team should play at most one game each day.
ii. At least one game with a popularity rating of 1.25 or higher should be assigned to each 
day.
iii. Due to using the same arena (i.e., Staples Center) the two Los Angeles teams, Lakers and 
Clippers, cannot host a game on the same day.
iv. Because of Super Bowl, Sunday cannot have a game with popularity rating above 1.4 (it is 
okay to have a game with popularity rating of exactly 1.4 on Sunday).
v. Continuing their road trip from the days prior to this 4-day block, the New York Knicks 
and Utah Jazz will need to play the rest of their road games as back-to-back games on 
Thursday and Friday, with no games on Saturday and Sunday to have time to get back to 
their home cities for their Monday home games.
Given the above information, please answer the following questions:
1. Help Matt formulate the problem of scheduling games during the four-day period while 
maximizing revenue. Explicitly write down your decision variables, the objective function,
and constraints. What kind of optimization problem have you defined?
2. Solve this problem using Python/Pyomo and Gurobi. 
a. Write code to represent the model in Python/Pyomo and solve it with Gurobi. With
your report, include a pdf generated by printing the Jupyter Notebook to pdf after 
running all parts of the notebook (so the pdf includes both your code and the output 
from the code, as described in the “Homework Formatting Instructions” document).
b. Which games are assigned to each of the 4 days? What is the maximum revenue?
3. Matt is notified by the NBA commissioner about a new restriction on the number of back to-back games (i.e., a team plays games on two consecutive days, e.g., Thursday and 
Friday). According to this new restriction and in order to have equity in the number of 
back-to-back games among all the teams throughout the season, Matt cannot assign back to-back games for the following two teams during the four-day time period: Phoenix Suns 
BANA201B Prof. John Turner
and Los Angeles Lakers. Explain in detail how the current formulation should be modified 
to address the back-to-back games constraint. Do you expect the total revenue to be higher 
or lower than in your original formulation, once this constraint is added to the model? 
Apply these changes and re-solve the problem. How much does the total revenue change?
4. The NBA usually selects very popular games to be broadcast on national television. 
Multiple TV channels including TNT, ESPN, ABC, and NBA-TV have doubleheader or 
tripleheader series, featuring two or three highly-rated games within the week. In particular, 
the TNT doubleheader series, with half-time report by NBA Hall of Famers Shaquille 
O’Neal and Charles Barkley, normally hosts the most popular games. The NBA wishes to 
assign two highly-popular games to a TNT doubleheader on one of the days within the 
four-day block from February 4th-7th. The NBA wants to make sure that if game 1 (Celtics 
at Lakers) is selected, then one of the following two games, game 3 (Blazers at Bucks) or 
5 (Jazz at Nets), should be included in the TNT doubleheader. Modify your formulation 
from part 1 of this assignment to incorporate the doubleheader scheduling requirement. 
Please describe any variables and constraints that you add or modify in your formulation.
You do not need to re-solve the problem.

         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
