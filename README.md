# 💎 DiamondMachineModel: High-Precision Price Estimation

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![ML](https://img.shields.io/badge/Machine_Learning-Ensemble-orange.svg)
![Accuracy](https://img.shields.io/badge/R2_Score-98.32%25-green.svg)

## 👤 Author
**Developed by [Emre Zorlu]**

---

## 📖 Project Overview
**DiamondMachineModel** is a state-of-the-art price prediction engine designed to estimate diamond market values with extreme precision. By leveraging a **Hybrid Stacking Ensemble** architecture, this project goes beyond individual model limitations to achieve a remarkable **98.32% R² score**.

## 🚀 The Architecture (Stacking Ensemble)
This model doesn't rely on a single algorithm. Instead, it uses a "Council of Experts" approach:

1.  **Base Learners (The Experts):**
    * **XGBoost:** Master of capturing non-linear trends.
    * **CatBoost:** Optimized for categorical features like color and clarity.
    * **LightGBM:** High-speed leaf-wise growth for fine-grained details.
    * **Random Forest:** Provides stability and prevents overfitting.
2.  **Meta-Model (The Judge):**
    * **RidgeCV:** A regularized regression head that balances the experts' predictions to deliver the final valuation.

## 📊 Performance Metrics
The model was tested on a dataset of ~54,000 diamonds, yielding the following results:

| Metric | Result |
| :--- | :--- |
| **R² Score** | **98.32%** |
| **Mean Absolute Error (MAE)** | **$260.1** |
| **Framework** | **Scikit-Learn, XGBoost, CatBoost, LightGBM** |

---

## 🔍 Visual Analysis
The project includes a **Residual Analysis** phase where we visualize the error distribution. Most predictions fall within a very narrow band near the zero-error line, proving the model's reliability across various price ranges.

## 🛠️ Usage / Appraisal Function
You can use the built-in appraisal function to get an instant market estimate:

```python
# Example Usage:
# predict_diamond_price(carat=1.5, cut=4, color=4, clarity=4, depth=61.5, table=58, x=7.3, y=7.2, z=4.5)
# Output: 💰 ESTIMATED MARKET VALUE: $12,095.02
