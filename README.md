# Waze-Churn-Prediction

> _This project was used by me to learn more about ML with ensemble of of tree-based models. It is split into 14 sections ->_
1) Imports 
2) Data loading & cleaning
3) Feature Engineering
4) Outliers
5) Variable Encoding
6) Determining target variable and main evaluation metric
7) Feature selection
8) Modelling workflow and Model selection process
9) Split the data
10) Modelling (with Random Forest & XGBoost)
11) Model Selection with validation data
12) Predict on Test Data with champion model
13) Evaluation 
14) Feature importance

### Conclusion

**Questions:**

1. Would you recommend using this model for churn prediction? Why or why not?

> _It depends. The model is not a strong enough predictor, as made clear by its poor recall score. However, if the model is only being used to guide further exploratory efforts, then it can have value._

2. What tradeoff was made by splitting the data into training, validation, and test sets as opposed to just training and test sets?

> _Splitting the data three ways means that there is less data available to train the model than splitting just two ways. However, performing model selection on a separate validation set enables testing of the champion model by itself on the test set, which gives a better estimate of future performance than splitting the data two ways and selecting a champion model by performance on the test data._

3. What is the benefit of using a logistic regression model over an ensemble of tree-based models (like random forest or XGBoost) for classification tasks?

> _Logistic regression models are easier to interpret. Because they assign coefficients to predictor variables, they reveal not only which features factored most heavily into their final predictions, but also whether they have a positive or negative correlation.

4. What is the benefit of using an ensemble of tree-based models like random forest or XGBoost over a logistic regression model for classification tasks?

> _Tree-based model ensembles are often better predictors. If the most important thing is the predictive power of the model, then tree-based modeling will usually win out against logistic regression (but not always!). They also require much less data cleaning and require fewer assumptions about the underlying distributions of their predictor variables, so they're easier to work with._

5. What could you do to improve this model?

> _New features could be engineered to try to generate better predictive signal, but only if we have the required domain knowledge. In the case of this model, the engineered features all made it into the top 10 most-predictive features used by the model.
