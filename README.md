# Energy-Consumption-in-Smart-Homes-analysis
 Smart Home Energy Consumption Analysis
This project entails the analysis of hourly energy consumption in smart homes. The dataset comprised information on energy usage, temperature, humidity, occupancy, HVAC, kitchen, and electronics usage across various Indian cities. The objective was to clean the data, perform some exploratory data analysis (EDA), and finally develop a predictive model for energy consumption based on environmental and usage factors.

 Overview of Project

1. Dataset:

The attributes in this data are as follows:
 `Energy_Consumption_kWh`: Total energy consumed in kWh.
 `Temperature_C`: Temperature in Celsius.
 `Humidity_%`: Relative percentage of humidity.
 `HVAC_Usage_kWh`: Energy usage of the HVAC system.
 `Kitchen_Usage_kWh`: Energy usage in the kitchen.
 `Electronics_Usage_kWh`: Energy usage of electronic devices.
- `Occupants`: Number of people residing in the house.
   - `Weather_Conditions`: categorical values describing the weather conditions.
   - `City`: Indian city where the house resides.
2. Data Cleaning:
   - Missing values were filled using the median value in numerical columns
   - Outlier that appears in energy consumption was identified and treated with IQR-based capping.
- Removes duplicates and ensures that the `Date` column is converted to a datetime format and ensures time-series consistency.
   - Performs normalization on key numerical features to standardize the scales.
3. Exploratory Data Analysis (EDA):

   - Univariate Analysis: Summarizes distributions of energy consumption and temperature using histograms and box plots.
- Bivariate & Multivariate Analysis: Identified the relationship between energy consumption and occupancy features, including weather using scatter plots and correlation analysis.
   - Time-Series Analysis: Used line plots and moving averages to visualize trends in energy consumption over time.
4. Feature Engineering:
 
   Developed a new feature, `Energy_per_Occupant`, to study energy usage as a function of the number of occupants.
A correlation test was done to identify the relationship that existed between the newly designed feature and the existing one.
5. Advanced Visualizations:
 
   Violin plots were used for energy consumption analysis at various temperature conditions.
   An interactive scatter plot was used to visualize the energy consumption vs temperature of all cities at different occupancy levels.
6. Machine Learning Model:

A linear regression model was developed that predicts energy consumption based on features such as `Temperature_C`, `HVAC_Usage_kWh`, and `Occupancy`. 
MAE and R-squared scores were measured for the model to understand its efficiency.
Feature importance analysis has been done to observe the impact of each feature on this energy consumption.
7. Prediction System:

- A very simple predictive model for energy consumption that predicts based on user-input temperature, HVAC usage, and occupancy.
 Results

- The simple linear regression is just about average in performance. There is an MAE of 0.77 and an R-squared of -0.008 again indicating that a better optimal model and maybe something beyond linear models are needed.
- Feature importance analysis revealed that HVAC usage and occupancy were the most important factors in predicting energy consumption.
 Future Work
Explore more advanced machine learning models like decision trees or random forests to extend the accuracy.
Additional relevant features can be used, such as weather conditions and humidity, to further improve the model's predictive capability.
The deployment of the predictive system for the real-time prediction of energy consumption could also be done.



