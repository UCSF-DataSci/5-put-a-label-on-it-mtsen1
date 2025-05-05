# Assignment 5: Health Data Classification Results

This file contains your manual interpretations and analysis of the model results from the different parts of the assignment.

## Part 1: Logistic Regression on Imbalanced Data

### Interpretation of Results

In this section, provide your interpretation of the Logistic Regression model's performance on the imbalanced dataset. Consider:

- Which metric performed best and why?
- Which metric performed worst and why?
- How much did the class imbalance affect the results?
- What does the confusion matrix tell you about the model's predictions?

**Interpretation:** The metric that perfromed the best was accuracy and the metric that performed the worst was recall. Accuracy likely performed well because the imbalance between negative and postive disease outcomes. As seen in the confusion matrix, there were 1301 TN predictions and only 1466 observations. Recall performed the worst since the model was unable to correctly predict positive outcomes well. We obtained a class imbalance score of approximately 0.6161 indicating relatively strong class imbalance. All in all, the confusion matrix shows us there are significantly more negative disease outcomes than postive disease outcomes and that the model was unable to predict positve cases well as a result. 



## Part 2: Tree-Based Models with Time Series Features

### Comparison of Random Forest and XGBoost

In this section, compare the performance of the Random Forest and XGBoost models:

- Which model performed better according to AUC score?
- Why might one model outperform the other on this dataset?
- How did the addition of time-series features (rolling mean and standard deviation) affect model performance?

**Interpretation:** According to the AUC scores, the XGBoost model performed better than the random forest model. Due to the nature of XGBoost models, XGboost models are able to handle imbalanced data better than random forest models which would explain why this model performed better. Adding the time-series features should improve model performance as it aides in capturing temporal information in the model .

## Part 3: Logistic Regression with Balanced Data

### Improvement Analysis

In this section, analyze the improvements gained by addressing class imbalance:

- Which metrics showed the most significant improvement?
- Which metrics showed the least improvement?
- Why might some metrics improve more than others?
- What does this tell you about the importance of addressing class imbalance?

**Interpretation:** Recall showed the greatest improvement of 172.09% increase while precision decreased by -48.43%. This is likely because balancing the disease outcomes allowed the model to predict positive outcomes better since there was more information to train on. Precision likely decreased because more positive predictions were made overall and thus more wrong predictions may have also occurred. This tells us that addressing class imbalance is critical when modeling data like this dataset as it allows models to train on data from minority classes and create more fair models. 

## Overall Conclusions

Summarize your key findings from all three parts of the assignment:

- What were the most important factors affecting model performance?
- Which techniques provided the most significant improvements?
- What would you recommend for future modeling of this dataset?

**Answer:** The most important factors affecting model performance appeared to be the class imbalances where reducing the imbalance through SMOTE greatly increased in the sensitivity of the models. For future modeling, addressing the class imbalance will continue to be necessary, but more can be adjusted as well. For instance, missing data was handled by imputing data, but future models can try other methods such as removing the missing data or imputation through a different method than using the mean. For the random forest and XGBoost models, SHAP values for feature importance can be found to find which predictors had the largest impact on the model for more interpretability. 