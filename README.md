# Predicting Sales with ML models
## LinearRegression vs. DecisionTree

**Author**:Leard Russell 

### Business problem:

Can we predict future sales when given info on:
Item Fat Content, 'Item Visibility', 'Item Type', 'Item MRP', 'Outlet Establishment Year', 'Outlet Size', 'Outlet Location Type', 'Outlet Type', and 'Item Outlet Sales'. 

### Data:
https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/ 

## Methods
- Data preparation steps with explanation and justification for choices
- Data Cleaning: getting rid of duplicates rows and incorrect/questionable values
- Validation Split: splitting data to prepare it for machine learning
- Data Transformation: Using transformers and pipelines for preprocessing
- Evaluating a linear regression model and a decision tree regression model for sales predictions


#### Linear Regression performance:
• Results for training data:
  - R² = 0.561
  - MAE = 847.536
  - MSE = 1300544.784
  - RMSE = 1140.414
• Results for test data:
  - R² = 0.566
  - MAE = 805.335
  - MSE = 1197623.654
  - RMSE = 1094.36

#### Visualizing Coefficients:

![image](https://github.com/Glutt0n/Project-1/assets/118066797/a6593768-fb91-4257-8e87-b900f520a973)


#### Decision Tree performance:
• Results for training data:
  - R² = 0.604
  - MAE = 762.584
  - MSE = 1172164.969
  - RMSE = 1082.666
• Results for test data:
  - R² = 0.595
  - MAE = 738.338
  - MSE = 1118083.684
  - RMSE = 1057.395
#### RandomForestRegressor performance:
• Results for training data:
  - R² = 0.94
  - RMSE = 431.98
• Results for test data:
  - R² = 0.55
  - RMSE = 1112.38
#### Visualizing Feature Importance:
![image](https://github.com/Glutt0n/Project-1/assets/118066797/09236545-eb1b-47db-9c5c-31fe6c2fa1a4)

Although the Decision Tree is the better model of the two, taking into account metrics, I wouldn't use this to predict sales for another sales prediction-related business problem. The MSE for both the training and test splits is ridiculous. And that's on top of having a mediocre R² score. Not a very predictive model at all.
## Recommendations:

Overall, I would recommend the use of the decision tree model. This regressor had a higher R² score for both splits than our linear regressor did (both before and after tuning). The decision tree also had better metrics across the board. It isn't a perfectly fit model by any means, but it is definitely better than the linear model.


For any additional questions, please contact **leardrussell@gmail.com**
