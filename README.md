# 🚗 Car Price Prediction using Machine Learning

A complete end-to-end regression pipeline that predicts used car resale prices using Python, Pandas, Scikit-learn, and Matplotlib.

## 📌 Problem Statement

Predict the resale/selling price of a used car based on features like brand, present price, mileage, fuel type, and more.

---

## 📂 Project Structure

```
car_price_prediction/
│
├── car_data.csv                     # Raw dataset (301 cars, 9 features)
├── car_price_prediction.ipynb       # Full ML pipeline script
├── car_price_analysis.png           # Auto-generated visualisation dashboard
└── README.md                        # Project documentation
```

---

## 📊 Dataset Features

| Column          | Description                              |
|-----------------|------------------------------------------|
| `Car_Name`      | Model name of the car                    |
| `Year`          | Manufacturing year                       |
| `Selling_Price` | **Target** — resale price in Lakhs ₹    |
| `Present_Price` | Current ex-showroom price in Lakhs ₹    |
| `Driven_kms`    | Total kilometres driven                  |
| `Fuel_Type`     | Petrol / Diesel / CNG                    |
| `Selling_type`  | Dealer / Individual                      |
| `Transmission`  | Manual / Automatic                       |
| `Owner`         | Number of previous owners                |

---

## ⚙️ Feature Engineering

New features created to improve model performance:

- **`Car_Age`** — `Car_Age — Current Year - Year`
- **`Depreciation_Pct`** — % value lost vs. present price
- **`Kms_Per_Year`** — usage intensity (driven_kms / car_age)
- **`Brand_Goodwill`** — average selling price per brand (encodes brand reputation)

---

## 🤖 Models Trained

| Model               | MAE  | RMSE | R² Score |
|---------------------|------|------|----------|
| Linear Regression   | 1.04 | 1.65 | 0.881    |
| Random Forest       | 0.47 | 0.84 | 0.969    |
| Gradient Boosting   | 0.40 | 0.69 | **0.979**|

> ✅ **Gradient Boosting** achieves the best performance with R² = 0.979

---

## 🔑 Key Findings

1. **Present Price** is the single strongest predictor (55% importance)
2. **Brand Goodwill** is the second most important feature (34%)
3. Tree-based ensemble models massively outperform linear regression
4. Fuel type and number of owners have minimal direct effect on price

---

## 🚀 How to Run

```bash
# 1. Clone the repo
git clone https://github.com/YOUR_USERNAME/car-price-prediction.git
cd car-price-prediction

# 2. Install dependencies
pip install pandas numpy scikit-learn matplotlib seaborn

# 3. Run the pipeline
Open car_price_prediction.ipynb in Jupyter Notebook and run all cells.
```

---

## 📈 Output

The script produces:
- Model performance metrics printed to console
- `car_price_analysis.png` — a full 9-panel visualisation dashboard covering:
  - Price distribution
  - Price vs car age
  - Fuel type comparison
  - Correlation heatmap
  - Feature importance chart
  - Actual vs Predicted plots for all 3 models

  <img width="2521" height="2171" alt="car_price_analysis" src="https://github.com/user-attachments/assets/d4abf706-7113-44f4-b674-5ceb2abc8c5f" />


---

## 🛠️ Tech Stack

- **Python 3.x**
- **Pandas** — data loading & manipulation
- **NumPy** — numerical operations
- **Scikit-learn** — ML models, preprocessing, evaluation
- **Matplotlib / Seaborn** — visualisations

---

## 📝 License

MIT License — free to use and modify.
