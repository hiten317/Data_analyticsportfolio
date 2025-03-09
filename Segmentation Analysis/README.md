 # This project involves Segmentation of Rides for Lobster Land which is a fictitious amusement park in New Hampshire using K means Clustering
- water_rides.csv is the dataset that contains information on 146 different ride types and the clustering model is being used to identify which type of rides should the park include
- Initial data pre-processing steps included identifying any impossible values in the data and these values were handled appropriately based on the distribution of the variable. 
- Since all variables have different units of measurement, the data was scaled before being used in modeling to avoid unecessary bias. 
- Variable selection was based on consideration of park visitors as well as from a business perspective. 

## 🚀 Approach Taken
1. **Data Cleaning**: Handled impossible values and used appropriate replacement methods.
2. **Exploratory Data Analysis (EDA)**: Summarized and analysed distribution of all variables.
3. **Feature Scaling**: Standardized numerical features using `Standard Scaler`.
4. **Cluster selection**: Used elbow method to identify ideal number of clusters and analysed cluster means using different cluster values to fetch ideal differentiation. 
5. **Clustering Model**: Applied **K-Means Clustering** to segment rides based on the features selected for the model. 
6. **Cluster Analysis**: Evaluated rides and identified differentiating characteristics by visualizing these clusters with original values.

## 📌 Key Insights
- **Segment 1:** Speed Thrills.
- **Segment 2:** Gentle fun.
- **Segment 3:** Quick intense.
- **Segment 4:** Adventure Cruise.
- **Segment 5:** Relaxed ride

## Additional Analysis
- **coaster_ratings.csv** - This dataset has survey responses from Lobster land visitors regarding there preferences for new rides in the park
- **Conjoint Analysis** was performed to make comparisons among different features and the analysis was based on Linear Regression model as the data was dummified and then fit into the regression model.
- **Average_rating** - This was the rating assigned for each variable by the responders and is the outcome variable of the model.
- **Key insights**: Most of the responders preferred catapult in their coaster rides for instant speed but didn't want to experience maximum speed available on the rides and rather opted for a mid-range, same goes for the highest vertical drop height which indicates that the responders preferred some thrill on the coaster rides but didn't fall on the extreme side.
  
