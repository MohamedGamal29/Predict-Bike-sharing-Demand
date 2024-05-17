# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Mohamed Gamal Mohamed Sobhy

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
I my predictions no were needed because all of my predictions were > 0

### What was the top ranked model that performed?
The top ranked model was  WeightedEnsemble_L3 with score_val of -53.126572 and pred_time_val, fit_time, pred_time_val_marginal, fit_time_ of  15.802999	, 347.191529 , 0.000953 , 0.034414	 respectively

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
I my exploratory data analysis created a histogram of all features to show the distribution of each one relative to the data.
I added new features by seprating the "datetime" column in year, month, day and hour

### How much better did your model preform after adding additional features and why do you think that is?
The model score_val ,pred_time_val, fit_time, pred_time_val_marginal, fit_time_ became -30.411089, 23.059340 , 387.839850 , 0.000770 , 0.043106 respectively.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
The model score_val , pred_time_val, fit_time, pred_time_val_marginal, fit_time_ became -39.023894 ,  0.276403 , 40.153157 , 0.131418 , 19.432361 respectively

### If you were given more time with this dataset, where do you think you would spend more time?
i will spend the time in 
1) Feature Engineering: While adding datetime features was beneficial, there might be additional features that could capture more nuanced patterns in bike sharing demand. Exploring weather data or incorporating holiday information could enhance the model's ability to capture variations in demand.
2) Hyperparameter Optimization: Perform a systematic search for optimal hyperparameters for each chosen model. This could involve utilizing more sophisticated optimization techniques such as Bayesian optimization or genetic algorithms to efficiently explore the hyperparameter space. Fine-tuning hyperparameters can significantly improve model performance and robustness.
### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|default_values|default_values|default_values|1.80| 			
|add_features|default_values|default_values|default_values|0.61| 			
|hpo|GBM: num_boost_round=100|default_values|RF:num_trees= 100|0.51| 			

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](img/model_test_score.png)

## Summary
## Summary

The project leverages AutoGluon to automate the process of model selection, hyperparameter tuning, and feature engineering. It consists of the following key phases:

- **Initial Training:** The initial training phase involved experimenting with AutoGluon's default settings. The top-ranked model was identified as WeightedEnsemble_L3, achieving a validation score of -53.126572 .

- **Exploratory Data Analysis and Feature Creation:** Exploratory data analysis revealed insights into the distribution of features, aiding in feature engineering. New features were created by parsing the "datetime" column into year, month, day, and hour components, resulting in a validation score improvement to -30.411089.

- **Hyperparameter Tuning:** Hyperparameter tuning further enhanced model performance, improving the validation score to -39.023894. This phase also optimized the fit time and prediction time.
