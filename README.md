# Predicting Sales with ML models
## LinearRegression vs. DecisionTree vs. RandomForest

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
#### Summary Plot (bar)
![image](https://github.com/Glutt0n/Project-1/assets/118066797/2f0f064f-d501-41fd-8443-c95460d52272)
Our previously created feature importance plot shares the top 4 most important features with our new summary bar-plot. This doesn't quiet tell us any details on how the features positively or negatively influence our model's prediction.

#### Summary Plot (dot)
![image](https://github.com/Glutt0n/Project-1/assets/118066797/9d7f4c36-3263-4323-9490-f576d96e0df7)
Item_MRP is shown to have the highest impact on model output with higher MRP equating to increased sales (and lower MRP having the opposite effect). The same case goes for instances of Supermarket Type 3. We see the opposite in the case of instances of Grocery Stores and increased Item_Visibility. The larger the values of those features, the lower the impact on sales.
#### Force Plots:
Max Item_MRP:
![image](https://github.com/Glutt0n/Project-1/assets/118066797/40aa0b62-c7d8-4297-943f-c147dfd4597e)
In the row holding the highest Item MRP, the force plot shows Item_MRP unsurprisingly to be the feature with the highest impact on our outcome.

Min Item_MRP:
![image](https://github.com/Glutt0n/Project-1/assets/118066797/8f018c72-26c4-4635-ab8d-c346b83bc765)
Again, like the previously shown force plot the Item_MRP has the largest affect on our model's prediction. 

#### Lime Explanations: 
Max Item_MRP:
![image](https://github.com/Glutt0n/Project-1/assets/118066797/517e1563-8770-4b1e-b2f8-9be688775cc7)
The row with the highest Item MRP is actually shown by the lime explainer to have the Item MRP to be the second most impactful on our randomforest's prediction among all features used in the row. Grocery Stores have the highest impact with Supermarket Type3 outlets following Item MRP. 
Min Item_MRP:
![image](https://github.com/Glutt0n/Project-1/assets/118066797/c32535f5-b35b-4a2d-944f-7c104ef606dc)
Like the previously explained row with the highest Item MRP, the row with the minimum Item MRP is actually shown by the lime explainer to have Item_MRP to be the second most impactful among all features used in the row, with the Grocery Store Outlet Type being the most impactful and the Supermarket Type3 Outlet Type being the third most impactful.

Although the Decision Tree is the better model of the three, taking into account metrics, I wouldn't use this to predict sales for another sales prediction-related business problem. The MSE for both the training and test splits is ridiculous. And that's on top of having a mediocre R² score. Not a very predictive model at all.
## Recommendations:

Overall, I would recommend the use of the decision tree model. This regressor had a higher R² score for both splits than our linear regressor did (both before and after tuning). The decision tree also had better metrics across the board. It isn't a perfectly fit model by any means, but it is definitely better than the linear model.


For any additional questions, please contact **leardrussell@gmail.com**
