# S&P 500 Stock Price EDA (2014–2017)

Exploratory data analysis of daily S&P 500 stock prices from January 2014 through December 2017, using the [S&P 500 Stock Prices 2014-2017](https://www.mavenanalytics.io/data-playground) dataset from Maven Analytics.

The notebook walks through four guiding questions about trading volume, volatility, and historical returns across the ~500 constituent stocks, plus a look at how volume and volatility relate to each other.

## Questions explored

1. **Which date saw the largest overall trading volume, and which two stocks were traded most that day?**
2. **On which day of the week does volume tend to be highest?**
3. **On which date did Amazon (AMZN) see the most volatility** (measured as high − low)?
4. **If you could go back in time and invest in one stock from 1/2/2014 to 12/29/2017, which would you choose, and what % gain would you realize?**
5. **Is there a relationship between a company's total trading volume and its total volatility?**

## Key findings

- Highest single-day trading volume: **2015-08-24**, led by BAC and AAPL.
- Volume tends to be highest on **Wednesdays**.
- AMZN's most volatile trading day was **2017-06-09**.
- The best-performing stock over the full window was **NVIDIA (NVDA)**, up roughly **1,115%** from its 2014-01-02 open to its 2017-12-29 close — consistent with rising GPU demand from data centers over that period.
- Most companies show low volume and low volatility, with a handful of high-volume outliers (like BAC) standing apart from the rest of the S&P 500.

## Visualizations

**Volume vs. volatility by company**

![Volume vs volatility scatter](images/volume_vs_volatility_scatter.png)

**Volume traded by top 5 companies**

![Top 5 companies by volume](images/volume_top5_pie.png)

**Top 5 companies by volatility**

![Top 5 companies by volatility](images/volatility_top5_bar.png)

**Volume and volatility by year**

<img src="images/volume_per_year.png" width="49%"> <img src="images/volatility_per_year.png" width="49%">

**Monthly trading volume by year**

<img src="images/volume_per_month_2014.png" width="49%"> <img src="images/volume_per_month_2015.png" width="49%">
<img src="images/volume_per_month_2016.png" width="49%"> <img src="images/volume_per_month_2017.png" width="49%">

## Data

The dataset (`S&P 500 Stock Prices 2014-2017.csv`) contains daily OHLCV (open, high, low, close, volume) records for S&P 500 constituents between 2014-01-02 and 2017-12-29, one row per stock per trading day.

Get the file from [Maven Analytics' Data Playground](https://mavenanalytics.io/data-playground) (search "S&P 500 Stock Prices") and place it in the project root before running the notebook — it isn't included in this repo.

## Setup

```bash
git clone https://github.com/<your-username>/sp500-stock-eda-2014-2017.git
cd sp500-stock-eda-2014-2017
pip install -r requirements.txt
jupyter notebook project1.ipynb
```

## Tools

- Python, pandas
- matplotlib, seaborn
- Jupyter Notebook

## Project structure

```
.
├── project1.ipynb   # main EDA notebook
├── images/           # exported chart images used in this README
├── README.md
└── requirements.txt
```
