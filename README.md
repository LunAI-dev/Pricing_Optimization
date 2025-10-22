# Pricing Optimization

A predictive model for **dynamic room pricing**, engineered to optimize revenue while balancing occupancy.  
This experiment is part of my [Data Science Lab](https://github.com/LunAI-dev/data-science-lab); a playground of applied ML and DL experiments where chaos meets logic.

---

## ⚗️ Project Overview

In the hospitality universe, pricing is deceptively complex: seasonal fluctuations, occupancy dynamics, and guest preferences interact in mysterious ways.  

- How can historical booking patterns and occupancy rates inform pricing strategy?  
- Which variables exert the strongest influence on price?  
- Can we increase revenue while preserving occupancy and fairness?

---

## 🧩 Dataset

The dataset is **synthetic designed** to mimic real hotel operations:

| Feature | Description |
|---------|-------------|
| room_type | Standard, Deluxe, Suite |
| season | Low, Mid, High |
| occupancy_rate | % occupancy at booking |
| length_of_stay | Nights booked |
| historical_price | Previous booking prices |
| bedrooms, bathrooms, beds | Room composition |
| balcony, garden | Binary amenities |
| sqft_room | Room size |
| price | Target variable with realistic noise |

> No proprietary data is used; the dataset is a sandbox for experimentation.

---

## 🛠 Experimental Workflow

### 1️⃣ Data Generation & Feature Engineering
- Generated a **synthetic dataset** with controlled randomness to simulate real-world unpredictability.  
- Encoded categorical variables numerically.  
- Created interaction features (e.g., occupancy × season) to reveal non-linear dependencies.  
- Ensured target variable `price` is realistic, with noise to emulate market fluctuations.  

### 2️⃣ Train/Test Split
- Partitioned data to simulate controlled experiments: 85% train, 15% test.  
- Setting seeds for reproducibility, even a mad scientist respects order.

### 3️⃣ Model Selection & Evaluation
- Explored **linear models** (Linear Regression, Ridge, Lasso) with and without polynomial expansion.  
- Tested **ensemble and non-linear models**: Random Forest, Gradient Boosting, Extra Trees, XGBoost, SVR.  
- Evaluation metrics: R² (train/test), RMSE, cross-validated R².  
- Classified models as **Underfitting**, **Overfitting**, or **Balanced**... and only the balanced survive.

### 4️⃣ Feature Importance Analysis
- Extracted **coefficients** or **feature importances** depending on model type.  
- Highlighted top variables driving pricing: room size, type, season, occupancy, number of rooms/bathrooms.  
- Visualized influence with barplots to translate science into intuition.

### 5️⃣ Model Visualization & Comparison
- Barplots of R² across all models with overfitting/underfitting flags.  
- Identified the champion model combining **accuracy and generalization**.  

