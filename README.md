# fantasyfootball
Fantasy Football - Predicting Player Performance
Problem and Target Audience
The inspiration for this project was work done a Stanford University Computer Science student here. Daily Fantasy Football websites allow users to select a new lineup of NFL players each week to compete against other fans. Each user has a fixed budget for their team, with players with high expected value drawing a high price tag. Users’ teams then accrue points based on player performance. The goal of this project is to develop a regression algorithm to predict weekly performance for the players, then determine opportunities where predicted performance is significantly higher than cost to acquire the player. The previously cited project focused only on previous performance, while my aim is to expand this work to include more qualitative factors such as opponent, weather, week of season, etc. A successful model could be used by a Fantasy Football fan to outperform their peers.
Data Acquisition (https://github.com/BurntSushi/nflgame)
The above github repo contains a Python lib to map the dataset to relevant objects, such as games, players, teams, etc. The set contains per-play data for every game from 2009-2017.

*nflgame library not available for Python 3.
*Used pdoc (pip install pdoc), as API docs for nflgame are no longer supported. 
TODO:
Add requirements.txt, gitignore.txt
