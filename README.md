# Electricity Consumption Prediction

## Overview
Predict the **next-hour average household electricity consumption** using the UCI Individual Household Electric Power Consumption dataset. This is a medium-level regression project with time-series feature engineering and a leakage-aware chronological split.

## Dataset
Official UCI page: https://archive.ics.uci.edu/dataset/235/individual+household+electric+power+consumption

The supplied dataset contains minute-level `Date`, `Time`, `Global_active_power`, `Global_reactive_power`, `Voltage`, `Global_intensity`, and three sub-metering fields.

## Models
- Linear Regression
- Ridge Regression
- Lasso Regression

## Features
Calendar features, cyclical time features, 1/2/3/24/48/168-hour lags, and 3-hour/24-hour/7-day rolling averages.

## Evaluation
MAE, RMSE and R². The first 80% of the timeline is used for training and the final 20% for testing.

## Technologies
Python, Pandas, NumPy, Scikit-learn, Matplotlib, Joblib, Jupyter Notebook.

## IBM Bob
IBM Bob was used as an AI-assisted coding/development tool during preparation. The final notebook contains the reproducible project implementation.

## Setup
Place the dataset at `data/household_power_consumption.txt`. Then:

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook
```

Open `main.ipynb` and run it from top to bottom.

## Structure
```text
electricity-consumption-prediction/
├── data/
│   └── household_power_consumption.txt
├── models/
│   └── electricity_consumption_model.pkl
├── main.ipynb
├── requirements.txt
├── README.md
└── Shourya_Basu_ProjectReport.docx
```

## Future Scope
Weather integration, tree-based model comparison, FastAPI service, React/Streamlit dashboard, ESP32 live monitoring, and model monitoring/retraining.

