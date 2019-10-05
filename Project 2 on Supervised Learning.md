
## Objective:
The classification goal is to predict the likelihood of a liability customer buying personal loans.

## Steps and Tasks:
Read the column description and ensure you understand each attribute well
Study the data distribution in each attribute, share your findings
Get the target column distribution. Your comments
Split the data into training and test set in the ratio of 70:30 respectively
Use different classification models (Logistic, K-NN and Naïve Bayes) to predict the likelihood of a liability customer buying personal loans
Print the confusion matrix for all the above models
Give your reasoning on which is the best model in this case and why it performs better?

## Visual Analysis of the Data using MS Excel
Total 5000 rows and 14 columns
Customer Age Starts from 23 thru 67
Experience has negative numbers.
Zipcode has one value that is four digits all others are five digits.
Family size ranges from a single member to 4 members.
CCAvg is in decimal and all the others are integers.
Income / CCAvg / Mortgage - these values are noted in 000's
Education is depicted in numbers 1 for Under Grad, 2 for Grad, 3 for advanced/prof
Personal Loan / Securities Account / CD Account / Online / CreditCard are Yes / No types and are documented as 0 or 1. No other value is found in these columns
No Blank cells in the Data

%matplotlib inline 
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

from sklearn.linear_model import LogisticRegression # Import Logistics Regression machine learning library
from sklearn.utils import resample # for resampling in case of down / up sampling requirements
from sklearn.model_selection import train_test_split # Used to split the data into Training and Testing split
from sklearn.neighbors import KNeighborsClassifier #Importing KNN Classifiers 
from sklearn import metrics # calculate accuracy measures and confusion matrix
from sklearn.naive_bayes import GaussianNB # Naive Bayes package from the Library
from sklearn.metrics import roc_curve, auc # to measure the optimal method
from sklearn.metrics import roc_auc_score # to get the ROC AUC score
from sklearn import preprocessing
import seaborn as sns
