# Flight Fare Predictor

To test the deployed model click [here](https://flight-fare-predict-ml2.herokuapp.com/).<br/>
Note : It takes some time to load the heroku page. Patience is the key!!

## Overview
- The dataset consists of records for different airlines,travel routes,stops,sources,destination,date of journeyprice,etc.Price is the target variable.This dataset is present on kaggle.Please check [here](https://www.kaggle.com/nikhilmittal/flight-fare-prediction-mh/) for more details on dataset. 

- The train dataset has about 10682 records. The test dataset is a different file and you will have to test on that. 

## Motivation
- I like to travel a lot. So for this purpose I thought it would be better if try to analyse this data and make a model out of it just for academic purpose.

- As I am a traveller, I found this project interesting as I would analyse how different features affect the flight prices.

-  This model would give you approximate fare value and not the exact!

## Project Structure
- [main.py](https://github.com/Pratik872/ML/blob/main/E2E%20Project/FlightFarePredictor/main.py) : This file has the flask application which is created.

- [utils.py](https://github.com/Pratik872/ML/blob/main/E2E%20Project/FlightFarePredictor/utils.py) : This file has all the helper functions which are required to run the application.

- [constants.py](https://github.com/Pratik872/ML/blob/main/E2E%20Project/FlightFarePredictor/constants.py) : This file has all the constant variables required in developing the application.

- [templates](https://github.com/Pratik872/ML/blob/main/E2E%20Project/FlightFarePredictor/templates) : This folder has all the templates which are rendered in the application

- [readme_resources](https://github.com/Pratik872/ML/blob/main/E2E%20Project/FlightFarePredictor/readme_resources) : This folder has all the images used to create readme file.

- [requirements.txt](https://github.com/Pratik872/ML/blob/main/E2E%20Project/FlightFarePredictor/requirements.txt) : This file has all the packages used to code and build the application.

- [Flight Fare Prediction.ipynb](https://github.com/Pratik872/ML/blob/main/E2E%20Project/FlightFarePredictor/Flight%20Fare%20Prediction.ipynb) : This jupyter notebook has the code for making models.

## Problem Objective
- To build a model which predict the prices of flight using a dataset

## Methodology

### EDA (Exploratory Data Analysis)
- I have plotted various graphs to visualize the data. Some of them are as follows : 

![PriceVsAirline](https://github.com/Pratik872/ML/blob/main/E2E%20Project/FlightFarePredictor/readme_resources/AirlineVsPrice.png)
![PriceVsDest](https://github.com/Pratik872/ML/blob/main/E2E%20Project/FlightFarePredictor/readme_resources/DestinationVsPrice.png)
![PriceVsSource](https://github.com/Pratik872/ML/blob/main/E2E%20Project/FlightFarePredictor/readme_resources/SourceVsPrice.png)
![PriceVsStops](https://github.com/Pratik872/ML/blob/main/E2E%20Project/FlightFarePredictor/readme_resources/StopsVsPrice.png)

- Required Graphs are plotted using seaborn,matplotlib libraries.

- Also heatmap is plotted for checking the corelation between target and predictor variables.
![PriceVsStops](https://github.com/Pratik872/ML/blob/main/E2E%20Project/FlightFarePredictor/readme_resources/StopsVsPrice.png)

### Feature Engineering
- I have derived many features from existing features so that I can use them in my model. You can check the notebook attached.

- I have handled categorical variables i.e nominal ar well as ordinal by using one-hot-encoding and label encoding whereever necessary.

### Model Making

- I have prepared Naive Bayes Classifier and RandomForests Classifier models.

- I have chosen RandomForests Classifier as my final model as I got better results.

- I have tuned the hyperparameters i.e 'alpha' for NB Classifier and 'n_estimators' for RF Classifier by using GridSearchCV

- Further I have used StratifiedKFold as my cv to balance training and validation data.

### Metrics

- To check how many messages are correctly identified as spams and hams I have used confusion matrices for both models.

![CF_NB](https://github.com/Pratik872/AI-ML/blob/main/E2E%20projects/SMSSpamClassifier/readme_resources/NB_CF.png)
![CF_RF](https://github.com/Pratik872/AI-ML/blob/main/E2E%20projects/SMSSpamClassifier/readme_resources/RF_CF.png)

Correction : The image on right side is for RandomForestsClassifier instead of Naive Bayes.

- I have given importance to 'precision' score as we need to correct identify the spam message.eg : What if model detects a ham message as spam!!!The person would miss important message!!

### DATA SOURCE
- [Flight Fare Dataset](https://github.com/Pratik872/AI-ML/blob/main/Natural%20Language%20Processing/SpamHam%20Classifier/SMSSpamCollection)

### Notebook
- [SMS Spam-Ham Classifier](https://github.com/Pratik872/AI-ML/blob/main/E2E%20projects/SMSSpamClassifier/SMSClassifier.ipynb)

### Built with 🛠️
- Packages : Pandas,Numpy,Seaborn,Matplotlib,NLTK,Sklearn,re(Regular Expressions),Imblearn,Flask,pickle

- Dataset : Kaggle

### Deployment
- Deployed using Heroku(PAAS)

- For deployment repository click [here](https://github.com/Pratik872/AI-ML/tree/NLPDeploy)

- For Web Application click [here](https://sms-classifier-nlp-ml.herokuapp.com/)
