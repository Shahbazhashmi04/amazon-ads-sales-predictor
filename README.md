Smart Sales Predictor for Amazon Advertising Campaigns

A machine learning project that predicts sales revenue (USD) from Amazon pay per click advertising metrics.

Built as a group project (team of 3) for the Data Science course at Iqra University, Karachi, Spring 2025.

## What it does

You enter the numbers from an Amazon ad campaign, for example impressions, clicks, spend, and cost per click, and the model predicts how much revenue that campaign is likely to produce.

## Dataset

- 7,800 campaign records
- 29 features covering ad spend, clicks, impressions, and campaign settings
- Target variable: sales revenue in USD

## What I did

**Data cleaning**
- Filled missing categorical values using the mode
- Removed outliers using the interquartile range (IQR) method

**Feature engineering**
- Click conversion rate
- Spend per impression

**Models compared**
| Model | Result |
|---|---|
| Random Forest Regressor | tested |
| Extra Trees Regressor | tested |
| Gradient Boosting Regressor | tested |
| **Stacking Regressor (final)** | **R squared 0.947, MAE 26.82 USD** |

The stacking regressor combined the three individual models and gave the best result.

**Deployment**
- Flask API with endpoints for prediction, model metrics, and data summary
- Simple web interface where a user types in their own campaign numbers

## Tech used

Python, scikit-learn, pandas, NumPy, Flask

## How to run

```bash
pip install -r requirements.txt
python app.py
```

Then open the local address shown in the terminal.

## Note

This was a university group project. The dataset is included for reproducibility.
