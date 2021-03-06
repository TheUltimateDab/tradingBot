# tradingBot

## Video Demonstration
[![Alternate Text](docs/video_thumbnail.jpg)](https://www.youtube.com/watch?v=Xvz8WsJ7hD0 "Link Title")

## Project Overview
A trading bot that analyzes a period of stock price data of certain stock, then takes a date as input and outputs whether one should buy or sell the stock based on the stock price on that day

## What it does
trading bot: the trading bot performs the following functions:
1. [x] determines whether a stock price on a certain day is a good entry or exit point for the stock based on analysis on the stock's past history
2. [ ] periodically filters out tweets and news related to stocks according to user preference
3. [ ] keeps check on market price movement at every second across multiple financial instruments

In particular, the user first enters the start and end date of a stock's data and then the quote of the stock. Then, the program downloads and analyzes the specified stock data.
![tradingBot setup](docs/tradingBot_setup.gif)

The program then prompts for a date, for which the program recommends whether the user should buy or sell the stock on that date. Then, the program generates a plot of stock price just prior to the specified date.
![tradingBot dont buy](docs/tradingBot_dont_buy.gif)

![tradingBot sell](docs/tradingBot_sell.gif)

## How We built it
We wrote the whole program using python. We first get stock price data through the API of Yahoo Finance. Then, we use dataFrame, numpy array, python list operations to operate on and analyze data so that we can extract useful data from the stock price data. In particular, we calculated the average increasing interval and the average decreasing interval of the stock specified by the user. then, we use these useful information to evaluate the stock prices the user specifies and determine whether the user should buy or sell at the price specified.