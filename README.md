# JPX_Tokyo_Stock_Exchange_Prediction

In order to succeed in any financial market, one must first identify sound investments. It makes sense to buy when a stock or derivative is undervalued. If it's overpriced, it could be time to sell. While specialists used to make these financial judgments manually, technology has opened up new doors for retail investors. Quantitative trading, in which choices are made programmatically based on predictions from trained models, may be of interest to data scientists in particular.

## Data

The data and challenge was gotten from Kaggle: 

[jpx-tokyo-stock-exchange-prediction](https://www.kaggle.com/competitions/jpx-tokyo-stock-exchange-prediction/overview)

## Data Preprocessing and feature engineering
### Data cleaning 
Data cleaning and filling is a process that is used to clean up and fill in missing data in data sets. This process can be used to improve the accuracy of data sets, as well as to improve the efficiency of analysis processes. Missing values were fill with forward fill method. 


### New features
the original data includes essential indicators such as closing, open, high and low prices, as well as volume. With new features we introduce more sophisticated technical indicators:

Prices: 
- Prices lag: these are the prices with lag 1, i.e., from the previous day/period.

- RSI: relative strength index
- Log Return 
- SMA: simple moving average
- MACD: Moving Average Convergence/Divergence
- Volatility

please see notebooks for details:
+ Feature engineering_P: [Feature_engineering_P](notebooks/Feature_engineering_P.ipynb) <br>
+ Feature engineering_P Nan Research: [Feature_engineering_P_Nan_Research](notebooks/Feature_engineering_P_Nan_Research.ipynb) <br>

## Our Stakeholder Requirements

Takeshi is a proud Japanese investor,he only invests in Japanese Companies. 
However,he is also very suspicious person. He is only willing to invest in the biggest japanese Companies. 
Takeshi isn’t looking for long-Time investments, as he thinks life is too short to wait for profits.

## Our Objectives,
To recommend stocks that Takeshi can invest in to make short term profits.


## EDA Exploration
A detailed Eda exploration was done on the all the Dataset available.
Please see notebook for details:
+ EDA Exploration: [EDA_Exploration](notebooks/EDA_Exploration.ipynb) <br>


## Model Exploration

Seven models were explored on selected stock.
please see notebook for details:
+ Model Exploration: [Model_Exploration](notebooks/Model_Exploration.ipynb) <br>


Based on our model performance Fbprophet & Long short Term Memory(LSTM) was further explored in subsequent notebooks based on our stakeholder requirements


## Models

### FbPhrophet


### Long short Term Memory(LSTM)



## Requirements:

- pyenv with Python: 3.9.4

### Setup

Use the requirements file in this repo to create a new environment.

```BASH
make setup

or

pyenv local 3.9.8
python -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
pip install -r requirements_dev.txt

