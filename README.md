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

<img width="955" height="423" alt="image" src="https://github.com/user-attachments/assets/48dee0f7-cdcb-43fb-826a-ed5cd1c6a5e3" />


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

---


## 📌 Model Behavior – 3 Key Phases

### **1) Classical EOQ + Continuous Review (Baseline)**
The model reacted late to sudden demand spikes or drops because it relied on fixed averages.  
This caused temporary shortages and unstable inventory levels.

<img width="791" height="383" alt="image" src="https://github.com/user-attachments/assets/550500e5-64a4-44c3-9c58-dd319f224e11" />

---

### **2) ML Integration (Random Forest – Version 1)**
Machine learning improved reaction speed and prediction accuracy.  
The model learned daily demand patterns and adapted to changes in real time.

<img width="827" height="396" alt="image" src="https://github.com/user-attachments/assets/c9439eba-d886-408f-bf5d-5f7fdf9a7bce" />

---

### **3) ML Integration (Random Forest – Version 2)**
The ML-based model detected abnormal trends earlier, reduced stockouts, and kept inventory levels more consistent compared to the classical method.

<img width="921" height="573" alt="image" src="https://github.com/user-attachments/assets/a41bc463-b99a-45d0-afca-b1fb507b8c29" />

---


## 📊 Key Success Results (Summary)

<img width="970" height="496" alt="image" src="https://github.com/user-attachments/assets/c23c2838-7a42-4890-a3e7-9cae4d90f47f" />

1. **zero_inv_days (Days with Zero Inventory)**  
   The new model reduced days with zero stock by ~75%, meaning better product availability and fewer lost sales.

2. **num_orders (Number of Orders)**  
   The new model created fewer but more efficient orders, cutting total orders by ~33% and improving operational stability.

3. **Holding Cost**  
   Inventory holding cost decreased by ~21%, thanks to maintaining optimal stock levels and reducing excess inventory.

4. **Stockout Cost**  
   Stockout cost dropped by ~75%, showing major improvement in meeting customer demand and preventing lost sales.

5. **R² Accuracy**  
   Prediction accuracy increased from **0.79 → 0.92**, proving the new model explains demand behavior much more effectively.


<p align="center">
<img width="274" height="231" alt="image" src="https://github.com/user-attachments/assets/61f4337c-31c8-4bc5-bf81-f4b928be07c2" />
</p>


   ## ✅ What We Improved in This Project

- **Better demand forecasting:** The model predicts demand more accurately than traditional methods.  
- **Weekend effect captured:** Adding weekend logic improved demand stability.  
- **Simple but powerful system:** Excel-based, easy to operate, and highly reliable.  
- **Major upgrade from Version 1:** Significant improvement in KPIs and overall performance.  
- **Scalable to other departments:** The model can be expanded to any product category in the future.

### 🧰 Tools Kit

<p align="center">
  <img width="1051" height="202" alt="image" src="https://github.com/user-attachments/assets/4af1169a-17d8-4508-828e-818e47f9b56d" />
</p>






