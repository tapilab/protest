# ecig-classify
Classify e-cigarette tweets


##Twitter Sentiment Analysis toward e-cigarettes

This project aims to analize the sentiment of Twiiter users about electronic cigarrets. Electronic cigarette is an important topic in the health area nowadays, and one important question that arises is to know how people are dealing with this new idea of "smoking free", in other words, how they are concerned about e-cigs? In order to answer questions like that we need to know what people are saying about e-cigs,  if it is positive or negative and how this sentiment changes over the time.

##Files in the repository

**Reading and Sampling tweets.ipynb**

In this file the original dataset is read and sampled. If you have all the data there is no need to run this notebook, otherwise you will have to. 

The necassary data is taken from the orginal data. For this project we used just organic tweets, so we ran the notebook for getting and saving only these tweets. This notebook samples 2000 tweets to have as the training set, they are saved as output in the file organicDef.csv (after labeling all 2000 tweets this file's name becomes 2000_Sample_3Classes.csv). Another sample of 200 tweets is sampled to check accuracy in other notebook (Analysis on 2 clases.ipynb).

**First analysis on the data with 3 classes / First analysis on model with 2 classes**

This notebook was created as a pre-analysis of the data set, so if you want go to the "real" analysis on the data set, there is no need to run this file. **Run Analysis on 2 or 3 classes** notebook. Mindf, idf, stopwords, ngrams and others parameters were tested in several values to check if any changes would make any difference in our first classifier. It is more to know the data and how some parameters can influence the classifier.  First analysis on model with 2 classes notebook is the same as First analysis on the data with 3 classes differing just on the number of classes.


**Analysis on 2 classes / Analysis on 3 classes**

These notebooks are the main analysis of our project (the others are also important) and if you want to know how we got the results and try to re-run them, you can run both of these files and get our results.

In these files we read the tweets, train models (we have two models - Logistic Regression and SGD Classifier) with the best model accuracy we predict,  generate the frequency of tweets per month by sentimen and plot the overall sentiment during the year. Also, we show n-grams and top words analysis.

**Gender inference**

In this file the gender is infered through the name of the user. To run this notebook it is necessary to change 2 variables: - DATA (1st Cell) = directory of the file Classified_testingTweets.csv (classified tweets)
- DIREC (Cell #19) = directory of the file tweets.pkl (tweets with infered gender)

**Age by name folder**

This folder has the data necessary to predict the age of the users. To run the notebook Age Inference it is necessary to change 2 variables:
 - DIR (2nd Cell) =  directory of the folder age_by_name
 - DIREC (Cell #13) = directory of the file tweets.pkl

**Reproducing the results**

In order to reproduce the results, you just need our data set and change the variable DATA which is in each first cell of each notebook that defined the directory where the data set is.
