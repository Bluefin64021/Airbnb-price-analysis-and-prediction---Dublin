# Airbnb Price Analysis and Prediction – Dublin

Predicting Airbnb nightly prices in Dublin using Python. This project walks through the full data-analysis workflow — from cleaning raw data to building a simple machine-learning model — on real Airbnb listings.

> Course project for **Programming for Analytics (B9BA200)**, MSc, Dublin Business School.

## Overview

Airbnb hosts set their own prices, so prices vary a lot from one listing to another. This project explores **what drives the price of an Airbnb in Dublin** and builds a simple model to predict the nightly price from a listing's features.

**Objectives**
1. Clean and prepare a real-world dataset.
2. Explore the data with summary statistics and visualisations.
3. Build and evaluate a simple price-prediction model.

## Dataset

- **Source:** [Inside Airbnb](https://insideairbnb.com/get-the-data) – Dublin listings
- **Format:** CSV (~6,966 listings, 90 columns)
- **Target:** `price` (nightly price)
- **Key features used:** room type, neighbourhood, accommodates (guests), bedrooms, number of reviews, review score, minimum nights, availability

## Tools

Python · pandas · NumPy · Matplotlib · scikit-learn · Google Colab

## Steps

1. **Load & inspect** the data (`read_csv`, `head`, `shape`, `info`).
2. **Select** the useful columns.
3. **Clean** the `price` column (remove `$` and `,`, convert to numeric).
4. **Handle** missing values and duplicates.
5. **Remove outliers** (keep prices between €0 and €1,000).
6. **Visualise** — price distribution, average price by room type, price by area, price vs guests.
7. **Model** — Linear Regression with an 80/20 train/test split.

## Results

- After cleaning: **3,346 listings**, average price ≈ **€264/night**.
- **Entire homes** averaged ~€303/night vs ~€133 for **private rooms**.
- Most expensive areas: **Dún Laoghaire–Rathdown** and **Dublin City**.
- Strongest price drivers: **number of guests** (correlation 0.67) and **bedrooms** (0.63).
- **Model performance:** R² ≈ **0.44**, RMSE ≈ **€131**.

The model explains a little under half of the variation in price — a reasonable result for a simple linear model using only numeric features.

## How to run

1. Download the Dublin `listings.csv.gz` from [Inside Airbnb](https://insideairbnb.com/get-the-data), unzip it, and rename it to `listings.csv`.
2. Open the notebook in [Google Colab](https://colab.research.google.com) (or Jupyter).
3. Upload `listings.csv`, then run all cells.

```bash
pip install pandas numpy matplotlib scikit-learn
```

## Future work

- Add categorical features (room type, neighbourhood) to the model.
- Try other models (e.g. Random Forest) for better accuracy.
- Use data from multiple time periods to capture seasonal effects.

## Author

**[Your Name]** — MSc student, Dublin Business School

## Acknowledgement

Data provided by Inside Airbnb. This project was completed as part of an MSc assignment.
