# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Kose Bilali

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
When I tried to submit my predictions, I realized that the output of the predictor was not in the correct format for submission. Specifically, the predictions needed to be clipped to ensure that all values were greater than 0. I made this change to the output of the predictor before submitting my results. Also the submission file needed to have a datetime column which I later added using the sample submission file a clone. 
### What was the top ranked model that performed?
The top-ranked model that performed was the WeightedEnsemble_L3.
## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
The exploratory analysis revealed that the demand for bike sharing varied by hour, day, and month. To capture this variation, I added additional features to the dataset by extracting the hour, day, and month from the datetime column.
### How much better did your model preform after adding additional features and why do you think that is?
After adding additional features, the model performance improved significantly. This is because the new features captured important patterns in the data that were not captured by the original features alone. The score improved from 1.80840 to 1.69644
## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
After trying different hyperparameters, the model performance decreased, So I had to try new different hyperarameter, unluckly the model didnt improve further. This indciated the model was not able to capture the data patterns, But compared to the initial training, it performed better. Ie from 1.80840 to 1.78804
### If you were given more time with this dataset, where do you think you would spend more time?
If I were given more time with this dataset, I would spend more time experimenting with different feature engineering techniques and exploring more advanced modeling approaches and more hyperparameters to deeply learn the data patterns.
### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|WeightedEnsemble_L3|LightGBM_BAG_L2|LightGBMXT_BAG_L2|1.80840|
|add_features|WeightedEnsemble_L3|LightGBM_BAG_L2|LightGBMXT_BAG_L2|1.69644|
|hpo|WeightedEnsemble_L3|WeightedEnsemble_L2|LightGBM_BAG_L2|1.78804|


### Create a line plot showing the top model score for the three (or more) training runs during the project.

![model_training_score.png](/model_training_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

![model_testing_score.png](/model_testing_score.png)

## Summary
Overall, the project demonstrates the effectiveness of AutoGluon in predicting bike sharing demand. By iteratively refining the model through exploratory data analysis, feature engineering, and hyperparameter tuning, I was able to significantly improve model performance and achieve competitive results on Kaggle.
