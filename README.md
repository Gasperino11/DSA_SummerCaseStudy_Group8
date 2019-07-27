# Beating FiveThirtyEight's Elo Model for forecasting NFL Games
This repo provides a series of notebooks which goes through how we built a model to try and beat FiveThirtyEight at their own game. We go through data preperation and cleaning, provide multivariate and univariate analysis notebooks, and finally a notebook on how to run and score the model.

## The Game
For the past 3 years, FiveThirtyEight has forecasted the outcome of games for the upcoming NFL season. They allowed readers to participate and compete against them by doing their own predictions. A description of the game can be found at [1](https://fivethirtyeight.com/features/how-to-play-our-nfl-predictions-game/) with a description of FiveThirtyEight's Elo model being found at [2](https://fivethirtyeight.com/features/introducing-nfl-elo-ratings/).

The basics of the game are that each participant assigns a probabilities to each team winning in each game. Depending on the outcome and the prediction made, the participant either loses points (up to -75) or they gain points (up to +25) related to how aggressive or conservative their prediction was. For instance, if a prediction was made that the probability that the Steelers would beat the Browns was 90% then a correct prediction would net most of the 25 points whereas an incorrect one would lose most of the 75 points.

In the series of notebooks we provide, we build a decision tree model that makes predictions for us and then assess how that model would have done against the FiveThirtyEight Elo model as well as Vegas betting odds since the 2002 season. We used Vegas betting data from [3](https://www.kaggle.com/tobycrabtree/nfl-scores-and-betting-data) and encorporated it with the FiveThirtyEight Elo data in order to create a model which outperforms (on average) either model seperately.

### Contributors:
- Nathan Duvenick (nadbn4@mail.missouri.edu)
- Gary Gasperino (gdgp63@mail.missouri.edu)
- Jason Hensley (jh5xf@mail.missouri.edu)
- Jared Wetzel (jdwkr3@mail.missouri.edu)

### This Repo

In this repo you'll find three folders:
- Notebooks: this folder contains the jupyter notebooks with our code along with any output from those notebooks
- Data: this folder contains all the data we used, downloaded from the source
- Images: this folder contains images of the output of our analysis

### The Notebooks

There are five total notebooks that we used. Only two of them are required to run the model which generates the predictions:

- Data_Preparation_and_Cleaning
- Adapting_the_Elo_Model

**Data_Preparation_and_Cleaning** runs through the process of loading the data, joining any disparate data frames, and then removing/imputing any null values.

**Adapting_the_Elo_Model** takes the output from Data_Preparation_and_Cleaning, adds additional variables required for generating Elo ratings, and evaluates those models based on Brier Scores. Each model is there compared over time to see which one performed the best in a given season.

The other three notebooks are used for data exploration and visualization. They are not required to prepare predictions for the FiveThirtyEight NFL Forecasting game.

**Univariate_Analysis** and **Multivariate_Analysis** provide our initial findings from our data exploration as well as our visualizations. The **Data_Story_Visualizations** notebook has the code used to generate the visualizations in our Group8_Outsmarting_Elo powerpoint.

### Run Order

1. Data_Preparation_and_Cleaning
2. Adapting_the_Elo_Model
3. Data_Story_Visualizations

All other notebooks can be run independently.

### Considerations

These notebooks were written in R in a JupyterHub environment and have been exported in the .ipynb format. If you'd like to run this on your own, you will need either the ability to open and run Jupyter notebooks or a way to run R. Beyond that, all of the data and code is included in this repo. You can simply export it as a zip file and run through everything.

### Results

We have compiled our data story into a powerpoint, which is also available in the repo under Group8_Outsmarting_Elo. It is the culmination of our work thus far, explaining our conclusion regarding using FiveThirtyEight's Elo ratings along with Vegas betting data. We will continue to refine it as we build more complicated ML models to help us better forecast NFL games.

### References
1: https://fivethirtyeight.com/features/how-to-play-our-nfl-predictions-game/

2: https://fivethirtyeight.com/features/introducing-nfl-elo-ratings/

3: https://fivethirtyeight.com/methodology/how-our-nfl-predictions-work/

4: https://www.kaggle.com/tobycrabtree/nfl-scores-and-betting-data

5: https://en.wikipedia.org/wiki/Elo_rating_system

6: https://en.wikipedia.org/wiki/Brier_score

7: https://medium.com/the-intelligent-sports-wagerer/what-point-spreads-can-teach-you-about-implied-win-probabilities-a8bb3623d2c5
