🏒 **NHL Hockey Players Predictive Model**
## 📌 **Project Overview**
- The project involves use of Simple and Multiple linear regression to forecast NHL Hockey player salaries, based on historical data. The model aims to understand the influence of important variables like Games played, points scored, shots percentage and variables associated with style of play.
  
## 📊 **Dataset Used**
- *Source*: nhl_players.csv
- *Number of Players*: 336
- *Key features*: **Player Name** - Unique identifier for each player
- **Games Played** - Number of games played in a their career.
- **G** - Total goals scored.
- **A** - The number of assists credited to the player in the season for which the data is captured. A goal can have either 0, 1, or 2 assists. Assists are credited to the teammate(s) whose stick touched the puck prior to the stick of the person who scored the goal.
- **P** - Points. In hockey, a player is credited with one point for every goal that he scores, as well as one point for every assist that he is credited for.
- **Team_Y** - The player's team
- **Position_y** - The player’s position. The players in this dataset are either C(Center), W (Wing), or D (Defenseman)
- **HANDED** - This indicates whether the player is left-handed or right-handed
- **Sh** - Total shots on goal taken by the player
- **Sh_perc** - Shot percentage. Of all the shots that this player has taken, how many have gone in the net (how many were goals?)
- **SALARY** - Total annual salary earned by the player, in dollars
- **PIM** - Penalties in Minutes. More serious penalties in hockey require a player to spend more time in the “penalty box,” which gives the opposing team an advantage (since they have an extra skater)
- **Giveaways** -  No. of times the player lost the puck to an opponent
- **Takeaways** - No. of times the player took the puck away from an opponent
- **Hits** - A body check that physically separates an opponent from the puck or significantly disrupts their play. Each number in the dataset represents a time when this player "hit" an opponent
- **Hits.Taken** - Each number in the dataset represents a time when this player was “hit” by an opponent.
- **blocked_shots** - These players are not goaltenders, but they can be credited for stopping a shot with their body, stick, or skates.
- **PlusMinus** - A player earns a +1 when their team scores a goal while they are on the ice and a -1 when the opposing team scores.
  
## 🚀 **Objective**
*Simple Linear Regression* - Predict hockey player salaries based on the points scored by them (single predictor)
*Multiple Linear Regression* - Predict hockey player salaries based on multiple performance indictors (multiple predictors)

## 🔬 **Approach & Methodology**
1. Data preprocessing
   - Assessing the structure of the dataset, variables and their distribution
   - Identifying if there are any anomalies due to errors in the data (eg player with less goals and games played, has extremely high salary)
   - Renamed variables to ensure consistency and readability, also converted outcome variable (Salary) to numeric format from string with special characters
2. Exploratory Data Analysis (EDA)
   - Identified the correlation strength of Points and Salary
   - Verified the relationship between Points and Salary is linear using Scatterplot.
   - Identified outliers and distribution of variables
   - Developed Correlation matrix for Multiple Regression model to avoid *multicollinearity* in the model.
3. Model Building
   - Used random sampling for data partitioning (60% train data and 40% test data), same proportions used for MLR as well.
   - Performed backward elimination for feature selection in MLR
4. Performance Evaluation
   - Evaluated R2 (variability explained by the model in salary of the players), RMSE and MAE.
   - Evaluated any chances of overfitting of the data comparing performance indicators of the model from training data with test data
     
## 📈 **Key Findings**
1. Simple Linear Regression model did explain the variability in the data using a single predictor (points) however it did indicate slight overfit of the data, indicating the need to add more predictors. 
2. From a business context of the hockey as well, a players impact does not come only by scoring goals that contribute to points, that just explains one dimension of the game hence we need to incorporate more predictors.
3. The RMSE and MAE for the MLR model were very close between training data and test data which explains stability of the model, however the MAE was still high as seen with SLR model which suggested the need to further improve the model to subsequently increase its prediction accuracy. R-squared value of 0.54 indicates that the model explains 54% variability in the Salary of the hockey players which is strong. 
  



