# Algorithmic Trading and Machine Learning  

_________________________________
# Contributers
Hunter Spence, Andre Montgomery, Nicholas Pamboukis

_________________________________
# Overview
This project is for an entry level developer or trader to get a start in Algorithmic Trading and Machine Learning Models. With a simple API, the user can make mininal changes to the code to utilize our program. With this project the user will be able to view how the trading strategy performs, with visuals and calaculations. Plus they will be able to see a 180 day trend project, using FbProphet, and the cumualtive returns of a Machine Learning Model. With this, the user will get insights in how Alogrithmic Trading works.
This program pulls data from available financial instruments provided by yahoo finance API and performs initial buy and hold analysis. A trading strategy using bollinger bands is then applied to the data and returns are compared to the buy and hold strategy. The data is then ran through an optimizer known as the mean reversion backtester which analyzes for the optimal parameters that would produce the most positive returns. Machine learning is then applied to the trading strategy.The machine learning modules used in the analysis were, SVM, sklearn, and fbprophet. The machine learning modules trained and tested the data to predict potential trading signals. Lastly, we examine the performance of the machine learning compared to the original strategy. 

_________________________________
# Neccessary Libraries and Dependencies
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
plt.style.use("seaborn")
import yfinance as yf
from sklearn.preprocessing import StandardScaler
from sklearn import svm
from sklearn.metrics import classification_report
from sklearn.metrics import zero_one_loss

_________________________________
# Machine Learning
The program use's SKlearn library for the Machine Learning Models. The program first use's a Standard Sclaer to fit the modle to the trainign data. Then we create a SVM classifier to make predictions. We used a Zero Loss Score and a Classification Report to analyze the model. 

_________________________________
# Mean Rev Backtester
MeanRevBacktester module was originally created by Alexander Hagmann and provided open source via https://www.udemy.com/course/algorithmic-trading-with-python-and-machine-learning/learn/lecture/25515130?start=75#overview 
In order to use the module use command import MeanRevBacktester as MeanRev. This module acts as an optimizer.
The module was edited to fit our particular trading strategy and api data pulled from Yahoo Finance. 

_________________________________
# Trading Strategy (Bollinger Bands)
The strategy starts with a rolling SMA and an upper and lower bounds that is 'n' standard deviations from the mean which is the SMA. This strategy is referred to as the Bollinger Band Trading strategy. Since 90% of the trading activity happens within the range, traders use the prices position within the bands to predict price movement. It is also used to find a "Squeeze" in the market. 

