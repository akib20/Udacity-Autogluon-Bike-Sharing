# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Akib IFTAKHER

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
In the beginning, I had issue with looping due to the kernel settings. Later with the proper suggestion, I overcome this issue. I also had to correct some of the syntax errors. I also found that ipywidgets library is needed to  be installed. Otherthan that, the operation run smoothly. 

### What was the top ranked model that performed?
During the training, the WeightedEnsemble_L3 has been identified as top ranked model. Finally the score for the initial training has been listed as 1.80957. 

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
Here, some of the observation has been documented.
1. temp and atemp column is more like a normal distribution. 
2. datatime has been modified into three different columns which are year, month, day.
3. season and categories has been transformed into the categories. 
4. work and holiday column is represening the binary data. 
5. humidity and windspeed are left and right skewed respectively.

### How much better did your model preform after adding additional features and why do you think that is?
After the feature engineering, the model has scored around 1.33315. The model which performed better is identified as WeightedEnsemble_L3. One distinctive things to notice in this part of the computation is, if we make an additional feature based on the hour from the datetime column, it gives lower score which is around 0.4830 or something like this.  

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
So with changes of the preset values, I have noticed that the score made by the model varies with a little fluctuation. At the end, I found that high quality preset values outperform rest of the parameters. Moreover, by tuning the hyperparamater values such as num_epochs, num_boost_round the model performs well. It seems additional improvement is possible with more details tuning of the related hyper parameters from tabular data provided by autogluon. 

### If you were given more time with this dataset, where do you think you would spend more time?
With additional time, I would try to opmtimize the performance of the models. Moreover, I will create more features from the existing ones. I will also try other models. 


### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|presets|num_boost_round|num_bag_folds|score|
|--|--|--|--|--|
|initial|best_quality|--|--|1.80957|
|add_features|best_quality|--|--|1.33315|
|hpo|high_quality|20|5|1.33126|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](img/model_train_score_1.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](img/model_test_score_1.png)

## Summary
With this project some of the part of the ML made it clear for a learner like me such as feature engineering and so on. With this practical approach and EDA, this project can play a role by more being accurate to predict the higher demand of the bikes on the basis of working hour and also prepare a industry to tackle high demand during the seasonal pick. 