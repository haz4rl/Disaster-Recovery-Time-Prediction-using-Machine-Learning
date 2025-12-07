# Disaster-Recovery-Time-Prediction-using-Machine-Learning


This project uses machine learning to predict **recovery time (in days)** after global disaster events between 2018 and 2024.  
Using features like disaster severity, casualties, economic losses, response times and aid provided, the model estimates how long it takes for a region to recover.

---

##  Project Goal

Given information about a disaster event, predict:

> **How many days will recovery take?**

This can help governments, NGOs and relief organizations plan resources better and understand which factors most affect recovery time.

---

##  Dataset

The dataset contains **50,000 records** with the following key columns:

- `country`
- `disaster_type`
- `severity_index`
- `casualties`
- `economic_loss_usd`
- `response_time_hours`
- `aid_amount_usd`
- `response_efficiency_score`
- `recovery_days` 
- `latitude`, `longitude`
- Engineered features:
  - `year`
  - `month`
  - `dayofyear`

---

##  Methods

### 1. Data Preprocessing

- Converted `date` into:
  - `year`
  - `month`
  - `dayofyear`
- Dropped the original string `date` column
- Label-encoded:
  - `country`
  - `disaster_type`
- Split data into **train (80%)** and **test (20%)**

### 2. Models

- **Linear Regression** (baseline)
- **Random Forest Regressor** (main model)

### 3. Evaluation Metrics

- **MSE** (Mean Squared Error)
- **RMSE** (Root Mean Squared Error)
- **MAE** (Mean Absolute Error)
- **R²** (Coefficient of Determination)

_Add your real numbers here:_

- Random Forest:
  - RMSE: `5.106426288511369`
  - MAE: `4.0739339999999995`
  - R²: `0.9357721586507368`

---

##  Exploratory Data Analysis (EDA)

The notebook includes:

- Top 10 countries by number of disasters
- Distribution of disaster types
- Correlation heatmap between numerical features
- Scatter plots:
  - Severity vs Recovery Days
  - Response Time vs Recovery Days
- Boxplot:
  - Recovery Days by Disaster Type
- Feature importance plot from the Random Forest model

---

##  Key Insights

- Higher **severity index** and **economic losses** tend to increase recovery time.
- Longer **response times** are associated with longer recovery periods.
- Some disaster types have much wider variation in recovery time than others.

---

##  How to Run

```bash
git clone <your-repo-url>
cd disaster-recovery-ml

pip install -r requirements.txt

jupyter notebook
