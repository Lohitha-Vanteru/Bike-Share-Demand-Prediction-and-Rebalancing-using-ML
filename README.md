# Intelligent Bike Station Rebalancing using Machine Learning and Reinforcement Learning

## Overview
This project focuses on addressing the challenges posed by the rapid urbanization and the increasing demand for bike-sharing systems. We aim to predict bike share demand using various machine learning regression models and propose an intelligent bike station environment using reinforcement learning to optimize the rebalancing process.

## Significance to the Real World
The growth of on-road automobiles and traffic congestion necessitate high-quality transportation services. By leveraging bike-sharing systems, we aim to reduce traffic congestion, lower Greenhouse Gas Emissions, and promote a healthier and environmentally friendly mode of commuting.

## Dataset
- **Data Source:** [Bay Wheel’s trip data](https://www.lyft.com/bikes/bay-wheels/system-data), [Weather data](https://meteostat.net/en/)
- **Attributes:**
  - Date, Rented Bike count, Hour, Temperature, Humidity, Windspeed, Visibility, Dew point temperature, Solar radiation, Rainfall, Snowfall, Seasons, Holiday, Functional Day.

## Exploratory Data Analysis
- Analyze ride patterns based on time of day, day of the week, and seasons.
- Investigate the distribution of rides on different types of days.

## Data Transformation
- Address multicollinearity in independent variables for linear regression models.
- Apply label encoding for categorical variables.
- Transform the target variable using logarithmic and square root transformations.
- Scale features for normalization.

## Proposed Approach
The project involves predicting bike share demand using the following machine learning models:
- Linear Regression Models: Lasso, Ridge, Polynomial, Elastic
- Tree-Based Models: Decision Tree, Random Forest, Gradient Boosting

Additionally, we implement reinforcement learning for intelligent bike station rebalancing. The reinforcement learning model includes the following components:
![image](https://github.com/Lohitha-Vanteru/Bike-Share-Demand-Prediction-and-Rebalancing-using-ML/assets/113141006/e723d547-9d8a-4038-9ab9-c35ec9c3ed8c)

### Reinforcement Learning
- **Environment:** Analogous to a bike station, simulates bike stock linearly or randomly based on input.
- **Agent:** Similar to a bike station operator, receives feedback about bike inventory, rewards/penalties, and termination conditions.
- **Trainer:** Responsible for end-to-end processing based on input. The agent moves from one state to the next through actions, receiving rewards or punishments.

#### Rewards and Penalties
- **Reward Structure:**
  - -30 if the hourly bike stock falls outside the range [0, 100].
  - +20 if bike stock is in the range [0, 100] at 23 hours; otherwise, -20.
  - -0.5 times the number of bikes eliminated every hour.
- **Punishment:**
  - -30 for falling outside the acceptable stock range.

## Model Development
- Utilize linear regression models (Lasso, Ridge, Polynomial, Elastic) and tree-based models (Decision Tree, Random Forest, Gradient Boosting).
- Tune models using grid search and hyperparameter tuning.
- Evaluate models using metrics like Mean Squared Error, Root Mean Squared Error, Mean Absolute Error, Accuracy, R2, and adjusted R2.

## Technical Difficulty
- Defining appropriate reward or penalty functions in real-life scenarios.
- Optimizing model training time complexity and iterations.
- Efficient feature selection from real-time data.
- Understanding and implementing bike rebalancing strategies.

## Novelty
- Unique approach using Reinforcement Learning in bike-sharing system rebalancing.
- Potential for productivity improvements and novel human-machine interactions in operational scenarios.

## Impact
- Aiming for a faster, more accurate, and efficient system compared to human operators.
- Potential contributions to smart, green cities and customer satisfaction.
- Future enhancements for prioritizing bike access, reservation options, and cost optimization.
  
## Acknowledgments
We would like to acknowledge [Bay Wheels](https://www.lyft.com/bikes/bay-wheels/system-data) for providing the trip data and [Meteostat](https://meteostat.net/en/) for the weather data.

## License
This project is licensed under the [MIT License](LICENSE).
