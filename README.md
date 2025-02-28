# Predicting-Home-Run-Outcomes-Using-Statcast-Data
For this project, I used MLB Statcast data from the 2021 season to classify home run events from events where a batted ball resulted in a hit (dataset used linked here: https://www.kaggle.com/datasets/s903124/mlb-statcast-data?select=Statcast_2021.csv). This dataset contained 93 features and 709,851 rows worth of data. 

To properly classify home run events versus other hits, I first preprocessed the data and removed some features which had no impact on my analysis. I then ran a scaled logistic regression on the remaining features and determined the features which held the most importance in determining home run events. These features were determined to be hit_distance, launch_angle, delta_run_exp, and hc_y (hit coordinate y). 

I then used VIF scores and correlation matrices to determine if there were any signs of multicolinearity and then created three different machine learning models based on these 4 features: a logisitic regression model, a decision tree model, and a random forest model. After running each of these models, I compared their performance to identify which model performed the best based on four model evaluation metrics: true positive rate (TPR), positive predictive value (PPV), f1_score (F1), and area under the curve (AUC). Ultimately, the model which resulted in the best performance was the random forest model.

Final Project Code.ipynb = Code used for this project

Final Project Description.pptx = PowerPoint presentation describing the processes undertook to set up each of the machine learning models used as well as discussing the key findings from this project.


