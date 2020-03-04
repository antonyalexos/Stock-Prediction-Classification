<h2>Stock-Prediction-Classification</h2>

This repository is the implementation of the final project for the course [ECE454 Machine Learning for Data Science and Analytics](https://www.e-ce.uth.gr/studies/undergraduate/courses/ece454/?lang=en).
The overall target is to predict the Goldman Sachs stock. The main algorith that we use fo this task is the LSTM. We ensure the quality of the algorithms by implementing a gain metric functions, which tells us how much we gain, if we trade every day based on the prediction of the algorithm.
More specifically we created also a custom evaluation metric named Gain, which shows how much we profit or lose. It evaluates our performance based on if we had the same prediction with the way the market moved that day.



<h3>The Data Preprocessing</h3>
<ul>
     <li>We collected the data from Yahoo API and from them we kept the Open, High, Low, Close and Volume.</li>
     <li>We normalised the data and shifted them with the window method to be appropriate for the time series problem.</li>
     <li>We then added more prices and indices such as NASDAQ, Hang Seng Index, NYSE, Nikkei 225, Bank of America, Barclays, Credit Suisse, JPMorgan, Morgan Stanley and VIX. From them we kept only Close.</li>
     <li>We also added some technical indicators such as Moving Average 7 and 21, EMA, MACD, Bollinger Bands, Momentum and Log Momentum.</li>
     <li>For the classification problem we transformed the data to 0 or 1, whether the price goes up or down in accordance to the previous day.</li>
     <li>We also added 3 fourier transformations mostly to denoise the data and see some trends on the time series.</li>
</ul>



<h3>Overview of the files</h3>
<ul>
    <li><b>stock_prediction_approach.ipynb:</b> In this file we show the things that we have tried in order to make produce some very good results. In this file we are encountering the task as a Time Series Prediction pronlem. </li>
    <li><b>stock_price_classification.ipynb:</b> In this file we encounter the task as a binary classification problem in order to predict whether the price goes up or down the next day. </li>
</ul>


