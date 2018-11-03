# fantasyfootball <br>
Fantasy Football - Predicting Player Performance<br>
<b>Problem and Target Audience<b><br>
The inspiration for this project was work done a Stanford University Computer Science student here. Daily Fantasy Football websites allow users to select a new lineup of NFL players each week to compete against other fans. Each user has a fixed budget for their team, with players with high expected value drawing a high price tag. Users’ teams then accrue points based on player performance. The goal of this project is to develop a regression algorithm to predict weekly performance for the players, then determine opportunities where predicted performance is significantly higher than cost to acquire the player. The previously cited project focused only on previous performance, while my aim is to expand this work to include more qualitative factors such as opponent, weather, week of season, etc. A successful model could be used by a Fantasy Football fan to outperform their peers.<br>

Data: <br>
The main source of data is a public repo (https://github.com/BurntSushi/nfldb), containing a SQL database dump of raw NFL game data, dating back to 2009. Of this database, I utilized four tables: plays, teams, games, and players.
I also merged in other data that may have an effect on player performance, specifically weather data(http://www.nflweather.com/) scraped with BeautifulSoup.
<br><br>
Methodology:<br>
I began by merging and flattening the full data set to produce a wide table where each row contains the ‘fantasy score’ (i.e. performance value) for a given player-game pair, with player and game attributes, such as opponent, age.. Next, I used recent historical fantasy scores to engineer features such as rolling average score and scoring variance. Also, I’ll look to non-numeric columns to find certain player affinities, such as correlation between opponent and performance, as well as creating features from other data sources as outlined in the Data section. 
I’ll apply a regression algorithm to predict the weekly performance for every offensive player. Given the data set covers the entire season from multiple years, I’ll experiment with using previous years as training data, then using current year for test data as well as using first xx% of the season as training data, then testing the algorithm on the remainder of the season. 
<br><br>
Project Goal:
The goal of this project is to provide a standalone repository with which others may replicate and use my prediction algorithm to help guide their own fantasy football season. Specifically, I will include a brief deck outlining my methodology, results, and suggestions for future improvement. Secondly, I will include the Jupyter notebooks (with instructions) used to wrangle and explore the data, as well as the code for the prediction algorithm.
<br><br>
Project Goal Update:
Having attempted to apply and tune several different regression models to the data, with consistently high error, it’s necessary to update the project’s goal. Initially, I set out to accurately predict the fantasy for a given player, based on past behavior and other game metadata. Going forward, my goal will be to separate players, teams, and / or games into useful groups, using classification algorithms. Examples of these clusters could be ‘low-scoring game overall’ or ‘advantageous to RBs’. Furthermore, I’ll attempt to support or debunk common Fantasy Football techniques, such as never selecting a player in a Thursday game.<br><br>



<br><br>
*nflgame library not available for Python 3.
*Used pdoc (pip install pdoc), as API docs for nflgame are no longer supported. 
<br>
column library: https://github.com/BurntSushi/nfldb/wiki/Statistical-categories
