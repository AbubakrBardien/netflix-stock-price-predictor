# Netflix Stock Price Predictor

This is a Machine Learning model trained to predict the **Weekly Stock Price** of Netflix with data across roughly a **5 year** period (April 2019 to April 2024). I explored data from multiple sources, and chose a dataset from the Nasdaq website. The original data can be downloaded [here](https://www.nasdaq.com/market-activity/stocks/nflx/historical?page=1&rows_per_page=10&timeline=y5). The Netflix stock price data is updated regularly, so the prices won't be the same as in my Jupyter Notebooks, but the accuracy of the ML model should be the same.

The stock prices were collected as <u>Daily Intervals</u> and needed to be converted to to <u>Weeekly Intervals</u>.

After the converting the data from daily to weekly, these are the features that the model will make <u>Closing Price</u> (**Close/Last**) predictions based off of: 
- **Year**
- **Week_Nr** (Week Number) 
- **Open** (Opening Price) 
- **High** (Highest price in week) 
- **Low** (Lowest price in week) 
- **Volume** (Number of shares traded in the week)

I've trained the model on the **K-Nearest Neighbors** algorithm, and used **Walk-forward Validation**. After fine-tuning the model (experimenting with different Training Window sizes and K values), I was able to train the model to show very accurate predictions, meaning a Mean Absolute Percentage Error (MAPE) of just **0.04%**.
