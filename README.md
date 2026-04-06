# Data-ML-Engineer-ex3

## ML Challenge – LastFM Session Forecasting

### Overview
This project applies an ARIMA(1,1,1) model to forecast the number of weekly listening sessions for the most active user in the LastFM dataset.

### Problem Definition
A user **session** consists of one or more songs played by a given user, where each song is started within **20 minutes** of the previous song's start time.

The selected metric to forecast is the **number of sessions per week**.

### Assignment Steps
1. Build sessions from the LastFM dataset using PySpark
2. Identify the **top 10 songs** played in the **top 50 longest sessions** by track count
3. Select the **top 1 user** by number of sessions
4. Forecast the next **3 months** of weekly sessions using ARIMA(1,1,1)

### Stack
- **PySpark** — data loading, session building, aggregations
- **statsmodels** — ARIMA(1,1,1) forecasting
- **pandas / matplotlib** — time series plotting

### Project Structure
```
Data-ML-Engineer-ex3/
├── notebooks/
│   └── ARIMA_LastFM_forecast.ipynb
├── data/
│   └── userid-timestamp-artid-artname-traid-traname.tsv  ← not tracked in git
├── requirements.txt
└── README.md
```
### Dataset
Place the file `userid-timestamp-artid-artname-traid-traname.tsv` inside the `data/` folder before running the notebook.

### Setup
```bash
pip install -r requirements.txt
jupyter notebook notebooks/ARIMA_LastFM_forecast.ipynb
```
