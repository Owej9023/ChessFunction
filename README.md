# Chess Analysis with R

## Overview:
This R script performs analysis on chess game data obtained from the Chess.com API. It includes various tasks such as data retrieval, data processing, visualization, modeling, and clustering.

## Features:

1. **Data Retrieval**: The script retrieves game data from the Chess.com API for a list of specified usernames.

2. **Data Processing**: 
   - The retrieved data is filtered based on specific criteria such as game time control (blitz), rules (chess), and rated games.
   - Time spent per move is calculated for each game.
   - Additional data processing tasks include formatting and filtering.

3. **Visualization**:
   - Various visualizations are created using the ggplot2 and plotly libraries, including box plots, bar graphs, scatter plots, and more.
   - Visualizations cover aspects such as time spent per move, cumulative percentage of games, Elo ratings distribution, and pair plots of variables vs. Elo by cluster.

4. **Modeling**:
   - Linear regression models are built to analyze the relationship between time spent per move and other variables such as move number, game number, and time format.
   - Decision tree model is trained and tested to predict the outcome (username) based on game features.
   - Random Forest classifier is trained and tested to predict usernames based on game features.

5. **Clustering**:
   - K-means clustering is performed to group players based on game features and Elo ratings.
   - Elbow method is used to determine the optimal number of clusters.
   - Pair plot is generated to visualize relationships between variables and Elo ratings by cluster.

## Dependencies:
- plotly
- httr
- shiny
- stringr
- tidyr
- ggplot2
- chron
- scales
- lubridate
- bigchess
- jsonlite
- dplyr
- purrr
- nnet
- rpart
- GGally
- randomForest

## Usage:
1. Ensure that all required libraries are installed.
2. Run the provided R script in an R environment.
3. The script will retrieve data, perform various analyses, and generate visualizations.

## Note:
- Make sure to adjust the list of usernames and any other parameters as needed.
- Some parts of the code may require specific data files or APIs to be accessible.
- Results and visualizations may vary based on the input data and parameters used.

---
