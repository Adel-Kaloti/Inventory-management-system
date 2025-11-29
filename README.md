<p align="center">
 <img align="center" width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/e65788ed-ac36-4271-92e3-fe2143eeeb95" />
</p>

<h1 align="center">Inventory Mnagement ML Model </h1>

# Executive Summary

### Random Forest Model

<p align="center">
  <img src="Ml Model.png" width="1000" />
</p>

The New model predicts key operational parameters:
- **Daily Demand Prediction**
- **Lead Time Prediction**
- **Standard Deviation of Demand During Lead Time (σdL)**

These predictions replace the traditional static inputs used in classical inventory formulas.

---
## 📊 KPIs

- **num_orders** – Total number of purchase orders created during the period.  
- **zero_inv_events** – How many times inventory reached zero.  
- **zero_inv_days** – Total days the product stayed out of stock.  
- **total_cost** – Combined cost (ordering + holding + stockout).  
- **total_order_cost** – Cost generated from placing orders.  
- **total_holding_cost** – Cost of keeping items in storage.  
- **total_stockout_cost** – Cost caused by stockouts and lost sales.
-----

# 📦 Inventory Management ML Model – Pilot Phase  
### Hybrid Model (Random Forest + EOQ + Continuous Review)

After analyzing simulation insights, we decided to build a new hybrid inventory management model that combines Machine Learning with classical inventory optimization methods.  
This new model replaces fixed statistical averages with ML-driven predictions to create a smarter and more adaptive replenishment system.


<img width="1486" height="604" alt="image" src="https://github.com/user-attachments/assets/2e751d98-1f77-4554-9748-8ec5649bdc60" />


This transforms the ROP from a static threshold into a dynamic ML-driven decision point.

---

# Why a Hybrid Model?

This integrated model combines the strengths of both traditional methods and machine learning:

- **Demand variability (D)** is dynamically predicted using Random Forest instead of fixed averages.  
- **Lead time variability** is estimated by the ML model, improving responsiveness to supplier behavior.  
- **σdL** is computed using ML rather than normal-distribution assumptions.  
- **More accurate replenishment decisions** due to real-time adaptive predictions.

This results in a replenishment model that reacts daily to operational conditions rather than relying solely on statistical assumptions.

---
## 🔄 Model Update – Version 2

### Version 1
Used only basic features: `id`, `date`, `demand` (no categorical fields).

### Version 2
Added new features that explain demand behavior:
- **day, month, year**
- **weekday**
- **is_weekend** – identifies Friday/Saturday behavior
- **Added Z-score** to improve the model’s ability to detect:
  - Demand spikes (positive outliers)
  - Demand drops (negative outliers)
  - Abnormal purchasing patterns

<img width="753" height="858" alt="image" src="https://github.com/user-attachments/assets/0cfe7b57-41b7-4622-a7b6-71a8aed7ebf3" />

## 📈 Model Comparison – Version 1 vs Version 2

The comparison shows a clear improvement after adding the Random Forest model.

- **Version 1:**  
<img width="970" height="249" alt="image" src="https://github.com/user-attachments/assets/da6a9252-badd-42e5-9447-a5432f8a8262" />

- **Version 2:**  
<img width="970" height="249" alt="image" src="https://github.com/user-attachments/assets/6fcc5c33-bd83-4420-bc8d-fbcdffebdd67" />

Overall, Version 2 demonstrates the advantage of machine learning in capturing complex demand patterns and improving prediction accuracy.











<img width="791" height="383" alt="image" src="https://github.com/user-attachments/assets/550500e5-64a4-44c3-9c58-dd319f224e11" />

<img width="827" height="396" alt="image" src="https://github.com/user-attachments/assets/c9439eba-d886-408f-bf5d-5f7fdf9a7bce" />


<img width="921" height=396" alt="image" src="https://github.com/user-attachments/assets/1bf497b7-f0c7-43d2-8709-52f7b3dca11d" />







