# Chess Analysis with R

## Overview:
This R script performs analysis on chess game data obtained from the Chess.com API. It includes various tasks such as data retrieval, data processing, visualization, modeling, and clustering.

## Features:

1. **Data Retrieval**: The script retrieves game data from the Chess.com API for a list of specified usernames.
   **Scraping the Data**:
      1. **API Request**: The code makes HTTP GET requests to the Chess.com API endpoint (`https://api.chess.com/pub/player/{username}/games/archives`) to retrieve the game archives for each specified username. It               iterates through each player's username to gather their game archives.

      2. **Iterating through Years and Months**: For each player, the API provides game archives organized by year and month. Therefore, the code iterates through each year and month to retrieve the game data for that           specific period. This involves constructing the appropriate URLs for each year and month and making API requests to fetch the game data.

      3. **JSON Parsing**: The JSON response from the API is parsed using the `jsonlite::fromJSON()` function to convert it into a structured R object.

      4. **Data Retrieval**: The code loops through each archive URL obtained from the JSON response and retrieves the game data from each URL.

      5. **Data Processing**: The retrieved game data is filtered based on specific criteria such as time control (blitz), rules (chess), and rated games.

      6. **Time Calculation**: Time spent per move is calculated for each game using custom functions.

      This process ensures that the code systematically collects game data from Chess.com for each player, navigating through their game archives organized by year and month.

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
