# Credit-risk-modeling-PD-and-scorecard

# Situation:
LendingClub needed to accurately predict the risk of loan defaults to adjust their credit policies appropriately and maintain required capital adequacy. Accurate predictions of loan defaults would allow them to minimize potential losses and optimize revenue from loan interests.

# Task:
The task was to prepare the data thoroughly for predictive modeling and then construct reliable statistical models for predicting the Probability of Default (PD). This involved handling various data types, managing missing values, and selecting significant predictors for the PD model using logistic regression.

# Action:

# Data Preparation:

Continuous Variables:
Transformed date strings (e.g., employment length, term, earliest credit line, issue date) into numerical values representing days or months, making them ready for numerical analysis and model input.
Example Conversion: Employment length expressed in years was converted to an integer count of years.

Handling Missing Values:
Filled missing values strategically based on business understanding—e.g., missing values for 'total revolving high credit limit' were replaced with the 'funded amount' since it could act as a proxy.
For continuous variables like 'annual income', replaced missing values with the mean to maintain distribution characteristics.
Set missing values for several credit-related counts and indicators to 0, under the assumption that absence of record implied the non-occurrence of that credit event.

Creating and Grouping Dummy Variables:
Constructed dummy variables for categorical features such as home ownership, loan grade, and purpose of the loan to convert them into a format suitable for logistic regression.

Applied methods like Weight of Evidence (WoE) and Information Value (IV) to assess the predictive power of each category, allowing for grouping of similar risk categories to simplify the model and enhance interpretability.

# Model Building:

Feature Selection:
Excluded variables that would not be available at the time of loan application to avoid data leakage.
Used statistical methods (p-values) to identify and retain only those features that significantly contributed to predicting the outcome, thereby improving model reliability and performance.

Logistic Regression Modeling:
Chose logistic regression due to its ability to provide probabilities (which are interpretable and useful in risk assessment) and its suitability for binary classification problems like loan default prediction.
Built the logistic regression model incorporating variables selected from the feature selection phase, ensuring each predictor’s contribution was statistically significant.
Model Validation and Evaluation:
Performed out-of-sample testing using a reserved portion of the data to evaluate the model’s predictive accuracy.
Used a variety of metrics (Confusion Matrix, ROC Curve) to assess the model's ability to differentiate between default and non-default cases and to gauge the calibration of predicted probabilities.

# Result:

Successfully prepared a comprehensive dataset ready for modeling with all necessary transformations and preprocessing.
Developed a robust PD model using logistic regression, which showed good predictive performance in distinguishing between potential defaulters and non-defaulters. The model's AUC indicated it was significantly better than random guessing, which is crucial for effective risk management in lending.
The data preparation and modeling actions led to the development of a credit scorecard, which translated model outputs into an easy-to-understand credit scoring system, enhancing decision-making processes at LendingClub.





