# Claims-Settlement-Optimization-System
# Claims Settlement Optimization System

## 📌 Project Overview

This system predicts optimal claim settlement amounts for an insurance company, balancing:

- ✅ Legal costs
- ✅ Customer satisfaction
- ✅ Company profitability

It uses Machine Learning models to estimate:

1. Settlement cost
2. Litigation cost
3. Probability of winning if litigated

And recommends whether to **settle** or **litigate** a claim using optimization.

---

## 🛠️ Tech Stack

- Python (Google Colab / Jupyter)
- pandas, numpy
- scikit-learn
- scipy (for optimization)

---

## 📂 Dataset

The dataset includes features such as:

- Policy & vehicle info (age, segment, power, etc.)
- Safety features (airbags, fog lights, ESC, etc.)
- Claim status: used to simulate claim success (`won`)

If not already labeled, we simulate `won` values for demo purposes.

---

## 🧠 ML Models

- **Linear Regression** for:
  - `settlement_cost`
  - `litigation_cost`
- **Logistic Regression** for:
  - `won` (claim success)

---

## 📈 Optimization Logic

For each claim, the system:

1. Predicts `settlement_cost`, `litigation_cost`, and `win_probability`
2. Defines a utility function based on cost savings, satisfaction, and win chance
3. Uses `scipy.optimize.minimize` to compute the **optimal offer amount**

---

## 🔁 Workflow

```
Input Claim ➜ Feature Scaling ➜ ML Predictions ➜ Offer Optimization ➜ Recommend Action
```

---

## 🚀 How to Run

1. Upload dataset (e.g., from Kaggle) into Colab
2. Run each code block:
   - Data preprocessing
   - Simulate `won` column (if needed)
   - Feature scaling
   - Model training
   - Optimization function
   - Evaluation
3. Test on sample claims

---

## ✅ Example Output

```
Predicted Settlement Cost: ₹75000
Predicted Litigation Cost: ₹97500
Win Probability: 0.65
Optimal Offer: ₹70200
Recommended Action: Settle
```

---

## 📌 Future Improvements

- Use real labels for `won` from legal outcomes
- Incorporate more advanced models (e.g., XGBoost)
- Add UI with Streamlit
- Include sensitivity analysis for legal risk

