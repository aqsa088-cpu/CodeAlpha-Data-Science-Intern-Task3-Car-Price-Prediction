# 🚗 Car Price Prediction Model
**CodeAlpha Data Science Internship | Task 3**

---

## 📌 Project Overview

This project builds a **Machine Learning model** to predict car selling prices based on various features such as fuel type, transmission, kilometers driven, and car age. The model uses a **Random Forest Regressor** and achieves an impressive **R² score of 0.962**, meaning it explains 96.2% of the variance in car selling prices.

---

## 📂 Dataset

- **Source:** `car price prediction.zip` (contains `car_prediction_data.csv`)
- **Features:**

  | Column | Description |
  |---|---|
  | `Car_Name` | Name of the car model |
  | `Year` | Year of manufacture |
  | `Selling_Price` | Price at which car is sold (Lakhs INR) — **Target variable** |
  | `Present_Price` | Current ex-showroom price (Lakhs INR) |
  | `Kms_Driven` | Total kilometers driven |
  | `Fuel_Type` | Petrol / Diesel / CNG |
  | `Seller_Type` | Dealer / Individual |
  | `Transmission` | Manual / Automatic |
  | `Owner` | Number of previous owners |

---

## 🛠️ Tech Stack

- **Python 3**
- **pandas** – Data loading, preprocessing & feature engineering
- **scikit-learn** – ML model training & evaluation
- **matplotlib** – Data visualization
- **seaborn** – Statistical plots
- **Google Colab** – Development environment

---

## 🔄 Data Preprocessing & Feature Engineering

- Mounted Google Drive and extracted dataset from ZIP
- Calculated **Car Age** = 2024 − Year (more informative than raw year)
- Dropped `Year` and `Car_Name` (high cardinality — 98 unique values)
- Converted categorical columns to `category` dtype
- Applied **One-Hot Encoding** with `drop_first=True` to avoid multicollinearity

---

## 🤖 Model Pipeline

| Step | Details |
|---|---|
| Train/Test Split | 80% train, 20% test — `random_state=42` |
| Algorithm | Random Forest Regressor |
| R² Score | **0.962** |
| Mean Absolute Error | **0.617 Lakhs INR** |

---

## 📊 Visualizations

### 1. Feature Distributions (Histograms)
- `Present_Price`, `Kms_Driven`, `Age`, `Selling_Price` — all right-skewed

### 2. Scatter Plots vs Selling Price
- **Present Price** — Strong positive correlation ✅
- **Kms Driven** — Weak negative correlation
- **Car Age** — Moderate negative correlation (older = cheaper)

### 3. Box Plots by Category
- Diesel cars command higher selling prices than petrol/CNG
- Dealer-sold cars fetch higher prices than individually sold ones
- Automatic transmission cars tend to sell for more than manual

---

## 🔍 Key Findings

- **Present Price** is the strongest predictor of Selling Price
- **Car Age** and **Kms Driven** negatively affect the selling price
- **Diesel** and **Automatic** cars have higher resale value
- The Random Forest model achieved **96.2% accuracy** on test data with an average error of only **0.617 Lakhs INR**

---

## 🚀 How to Run

1. Upload `car price prediction.zip` to your **Google Drive** under `MyDrive/codealpha tasks/`
2. Open `code_alpha_task3.ipynb` in **Google Colab**
3. Mount Drive when prompted
4. Run all cells in order (`Runtime > Run all`)

### Dependencies

```bash
pip install pandas scikit-learn matplotlib seaborn
```

---

## 📁 Project Structure

```
├── code_alpha_task3.ipynb        # Main ML notebook
├── car price prediction.zip      # Raw dataset (zipped CSV)
└── README.md                     # Project documentation
```

---

## 👤 Author

**Aqsa Irfan**
CodeAlpha Data Science Internship | Task 3 – Car Price Prediction
