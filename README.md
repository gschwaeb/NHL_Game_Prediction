# NHL Game Prediction Modeling
by Gary Schwaeber

## Business Problem
With sport betting becoming increasingly popular and mainstream, I believe that data science can be used to make superior decisions over gut intuitions. By building a game prediction model, built with features inspired by the latest in advanced analytics and using machine learning models, games can be predicted with greater accuracy that can potentially allow users to gain an edge on bookmakers. Another potential users of this model are media analysts looking to enrich their analysis with a better understanding of which team is likely to win their game

## Data Collection
Team and goalie game logs were scraped from [Natural Stat Trick](https://www.naturalstattrick.com/). Official NHL game results were scraped from the NHL API via the python library [hockey_scraper](https://hockey-scraper.readthedocs.io/en/stable/hockey_scraper.html).

## Features
Team features include:
- Fenwick For% 
- Goals For %
- Expected Goals For %
- Shooting %
- PP TOI Per Game
- PK TOI Per Game
- xGF Per Minute PP
- xGA Per Minute PK
- Played Back to Back

Goalie Features include:
- Fenwick SV%
- Goals Saved Above Expected Per 60
- High Danger Save %

## Exploratory Data Analysis

Different amount of rolling games were for the features was tested. I ultimately found the using 40 game rolling feature was optimal. 

## Exploratory Data Analysis


In this notebook I will attempt to train logistic regression, ada boost, and gradient boosting models in an attempt to make the best possible game prediction model. I will train my models and tune model hyperparemetres using game results from seasons '2017-2018', '2018-2019', '2019-2020'. Then I will predict on held out games from the current 2021 season and evaluate my model. There are currently a handful of public models whose log loss on the current season's games is being [tracked](https://hockey-statistics.com/2021/05/03/game-projections-january-13th-2021/) on which I can compare the quality of my model to. The score I will look to optimize is log loss, however, I will also review accuracy scores due to their interpretability.
