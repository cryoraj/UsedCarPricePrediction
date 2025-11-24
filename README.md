# 🚗 Used Car Price Prediction

Repository: [cryoraj/UsedCarPricePrediction](https://github.com/cryoraj/UsedCarPricePrediction)

---

## 📌 Project Overview
This project analyzes a large dataset of used vehicles to identify the key drivers of resale price and build predictive models for dealership stakeholders.  
The goal is to fine-tune inventory strategy and pricing using **data-driven insights**.

---

## 📊 Summary of Findings
- **Best-performing model:** XGBoost, with the lowest error (RMSE ≈ 4,746, MAE ≈ 2,828).  
- **Key predictors of price:**
  - **Age:** Steep depreciation in the first 5–7 years, then flattens.  
  - **Mileage:** Strong negative effect, especially in the first 50k miles.  
  - **Condition:** Step-wise premiums; “good” → “excellent” → “like new.”  
  - **Brand:** Luxury brands (BMW, Mercedes, Lexus) retain higher value; mass-market brands (Toyota, Honda, Ford) show strong resale reliability.  
- **Business impact:**  
  - Prioritize newer, low-mileage vehicles.  
  - Invest in reconditioning when uplift > cost.  
  - Adjust inventory mix by region and vehicle type (SUVs/trucks command higher resale).

---

## 🛠 Dealer-Facing Recommendations

- **Acquisition Strategy:**  
  - Prioritize newer, low-mileage vehicles.  
  - Focus on brands with strong resale premiums.  

- **Pricing Strategy:**  
  - Use mileage and age tiers to set discounts.  
  - Apply condition premiums consistently to justify reconditioning costs.  

- **Inventory Mix:**  
  - Stock more SUVs and trucks (higher average resale).  
  - Adjust mix by region (e.g., trucks in Texas, hybrids in California).  

---

## 📈 Model Comparison

| Model              | RMSE (Price, $) | MAE (Price, $) |
|--------------------|-----------------|----------------|
| **XGBoost**        | **4,746.60**    | **2,828.19**   |
| GradientBoosting   | 5,809.49        | 3,550.30       |
| Linear Regression  | 6,348.67        | 3,982.93       |
| Ridge (alpha=10)   | 6,370.66        | 3,986.02       |
| Lasso (alpha=0.001)| 6,461.85        | 4,071.03       |

✅ **XGBoost is the most accurate**, reducing pricing error by ~$1,500 compared to linear models.

---

## 📂 Project Organization
UsedCarPricePrediction/ │ ├── notebooks/ │ └── used_car_price_prediction.ipynb # Main Jupyter notebook with analysis & models │ ├── data/ │ └── vehicles.csv # Raw dataset (cleaned during preprocessing) │ ├── reports/ │ └── README.md # Project summary and findings │ └── requirements.txt # Python dependencies

├── [data/](https://github.com/cryoraj/UsedCarPricePrediction/tree/main/data)\
│   └── [vehicles.csv](https://github.com/cryoraj/UsedCarPricePrediction/tree/main/data/vehicles.csv)     # Source Data\
│\
├── [Notebook/](https://github.com/cryoraj/UsedCarPricePrediction/blob/main/notebooks)\
│   └── [WhatDrivesCarPrice.ipynb](https://github.com/cryoraj/UsedCarPricePrediction/blob/main/notebooks/WhatDrivesCarPrice.ipynb)   # Jupyter Notebook (analysis + visualizations)\
│\
├── [README.md](https://github.com/cryoraj/UsedCarPricePrediction/blob/main/README.md)   


- **No unnecessary files** are included.  
- **Directories and files** are named clearly and placed in appropriate locations.  

---

## 📓 Jupyter Notebook
The notebook [WhatDrivesCarPrice.ipynb](https://github.com/cryoraj/UsedCarPricePrediction/blob/main/notebooks/WhatDrivesCarPrice.ipynb) contains:
- Clear headings and explanatory text.  
- Step-by-step workflow: preprocessing, model building, evaluation, and visualization.  
- Visualizations: depreciation curves, condition premiums, brand effects, residual plots.  

---

## ⚙️ How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/cryoraj/UsedCarPricePrediction.git
   cd UsedCarPricePrediction
