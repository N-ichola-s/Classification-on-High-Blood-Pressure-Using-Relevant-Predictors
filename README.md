For this project, we first came up with the following proposal: NHANES datasets: 
2017-March 2020 Pre-Pandemic Questionnaire Data - Continuous NHANES, including:
Diet Behavior & Nutrition, Weight History, Physical activity, Alcohol Use, Smoking - cig use, Health insurance,  Income, Sleep disorders, Blood pressure & Cholesterol,  Mental health - Depression Screener

Question 1: Prediction of depression questionnaire score

Response Variables: Depression Questionnaire Score

Predictors:  Income, Sleep disorders, Physical activity, Diet Behavior & Nutrition, Alcohol Use, Weight History.

Method:

Select the best model among the following 3 models:

Method_1: Use cross-validated lasso/ridge regression to predict the value of depression score.

Method_2: Use spline with curvature penalties to predict the value of depression score.

Method_3: Use cross-validated KNN regression to predict the value of depression score.

Question 2: Classification of high blood pressure using relevant predictors

Response Variables: Whether one has been informed by a healthcare professional to have high blood pressure

Predictors: Diet Behavior & Nutrition, Weight History, Physical Activity, Alcohol Use, Smoking - Cig Use, Health Insurance.

Method:

Select the best model among the following 4 models:

Model_1: First use bootstrap and boosted tree to conduct ‘leave one covariate out’ method to drop the features with low importance. Then use cross-validation to get an optimal max depth for Model_1.

Model_2: First use bootstrap and KNN model to conduct ‘leave one covariate out’ method to drop the features with low importance. Use cross-validation to get the best K for KNN model at the same time to get Model_2.

Model_3: Use cross-validation to get an optimal C and gamma for supporting the vector machine model, the model with the least error rate will be Model_3.

Model_4: Use linear discriminant analysis and quadratic discriminant analysis to fit Model_4.


My colleague and I collaborated on the 2nd approach. Once we implemented each approach, we would use ROC curves to determine which model works best with our data.
