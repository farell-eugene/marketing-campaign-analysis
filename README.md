# Marketing Campaign Performance Analysis

Exploratory data analysis and regression modeling of **200,000 digital marketing campaigns**. The goal was to understand what drives **ROI** and **conversion rate** across campaign types, channels and audiences. Data Analysis course final project (Group 2).

## Questions explored

- How do campaign types (Email, Influencer, Display, Search, Social Media) and channels compare on ROI and conversion rate?
- Which target audiences and customer segments respond best?
- How do conversion rates move over time?
- Can ROI be predicted from campaign attributes?

## Workflow

1. **Data preprocessing**: type conversion (e.g. `Acquisition_Cost` from currency text to numeric)
2. **Data cleaning**: missing-value and duplicate checks
3. **Encoding**: label encoding of categorical attributes
4. **Correlation analysis**: heatmap of features
5. **Visualization**: campaign counts by type, target-audience distribution, conversion-rate trend over 2021
6. **Modeling**: **Linear Regression** and **Polynomial Regression** to predict ROI

## Key finding

Both regression models reached R² ≈ 0 (MAE ≈ 1.51), so ROI **cannot be explained linearly** by the available campaign attributes. Campaign counts and audience shares were almost evenly distributed, which suggests ROI depends on factors the dataset does not capture.

## Dataset

[Marketing Campaign Performance Dataset](https://www.kaggle.com/datasets/manishabhatt22/marketing-campaign-performance-dataset) on Kaggle. It is not included here because of its size (≈26 MB). Download `marketing_campaign_dataset.csv` into the `notebooks/` folder before running.

| Column | Description |
|---|---|
| `Campaign_ID` | Unique campaign identifier |
| `Company` | Company running the campaign |
| `Campaign_Type` | Email, Influencer, Display, Search, Social Media |
| `Target_Audience` | e.g. Men 18–24, Women 35–44 |
| `Duration` | Campaign length (e.g. 30 days) |
| `Channel_Used` | e.g. Google Ads, YouTube |
| `Conversion_Rate` | Share of the audience that completed the target action |
| `Acquisition_Cost` | Cost to acquire the audience |
| `ROI` | Return on investment |
| `Location`, `Language` | Geography and language of the campaign |
| `Clicks`, `Impressions` | Engagement volume |
| `Engagement_Score` | 1–10 interaction score |
| `Customer_Segment` | Specific targeted segment |
| `Date` | Campaign date |

## Run

```bash
pip install -r requirements.txt
jupyter notebook notebooks/marketing_campaign_analysis.ipynb
```

Notebook commentary is in Indonesian.

## Tech stack

Python · pandas · NumPy · scikit-learn · SciPy · Matplotlib · Seaborn
