# Bollinger Band Algo Trading and Machine Learning  

# Contributers
Hunter Spence, Andre Montgomery, Nicholas Pamboukis

# Overview
This program pulls data from available financial instruments provided by yahoo finance API and performs initial buy and hold analysis. A trading strategy using bollinger bands is then applied to the data and 
returns are compared to the buy and hold strategy. The data is then ran through an optimizer known as the
mean reversion backtester which analyzes for the optimal parameters that would produce the most positive returns. Machine learning is then applied to the trading strategy. SVM, sklearn, and fbprophet are all machine learning modules used in the analysis. The machine learning modules will train and test the data to predict potential trading signals. Lastly, we examine the performance of the machine learning compared to the original strategy. 


# Neccessary Libraries and Dependencies
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
plt.style.use("seaborn")
import yfinance as yf



# Modules Used
MeanRevBacktester module was originally created by Alexander Hagmann and provided open source via https://www.udemy.com/course/algorithmic-trading-with-python-and-machine-learning/learn/lecture/25515130?start=75#overview 
In order to use the module use command import MeanRevBacktester as MeanRev. This module acts as an optimizer.
The module was edited to fit our particular trading strategy and api data pulled from Yahoo Finance. 



# Trading Strategy
The strategy starts with a rolling SMA and an upper and lower bounds that is 'n' standard deviations from the mean which is the SMA. 