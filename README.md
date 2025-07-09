
# 🚗 Dynamic Parking Pricing Using Real-Time Data

## 📌 Project Overview

This project implements **real-time dynamic pricing for urban parking spots** based on live occupancy, traffic conditions, vehicle types, and queue lengths. The system ingests data, processes it to derive relevant features, and applies machine learning models to assign optimal parking prices dynamically.

This is part of a capstone project where multiple models were compared and evaluated for pricing accuracy and stability.

---

## 🧰 Tech Stack

- **Python**
  - `pandas`, `numpy`, `datetime`, `math`
- **Jupyter Notebook** (Colab)
- **Pathway (for streaming)**
- **Bokeh (for visualization)**
- **Mermaid** (for architecture visualization)

---

## 🏗️ Architecture Diagram

```mermaid
graph TD
    A[Raw CSV Parking Data] --> B[Preprocessing + Cleaning]
    B --> C[Feature Engineering<br/>(Vehicle Weight, Occupancy Ratio)]
    C --> D[ML Models<br/>Model 1, 2, 3]
    D --> E[Price Prediction]
    E --> F[Streamed Output<br/>(JSONL)]
    F --> G[Dashboard / Output Sink]
```

---

## 🔄 Workflow & Architecture Explanation

1. **Data Ingestion**  
   Raw CSV files containing timestamped parking sensor data are ingested.

2. **Preprocessing**  
   - Timestamps normalized and combined (`LastUpdatedDate`, `LastUpdatedTime`)
   - Invalid/missing values handled with default or median strategies.
   - Non-numeric fields like `VehicleType`, `TrafficConditionNearby` mapped to numerical values.

3. **Feature Engineering**
   - New features created: `OccupancyRatio`, `VehicleWeight`, `TrafficScore`
   - Sorting and filtering ensures each parking system is evaluated over time.

4. **Modeling**
   - Multiple ML models (e.g., Linear Regression, Decision Tree, etc.) are applied.
   - Model performance is compared for pricing stability.

5. **Streaming & Output**
   - Final outputs are generated in `.jsonl` format (mimicking real-time stream).
   - These can be consumed by dashboards or downstream applications.

---

## 📁 Repository Structure

```
📦 Capstone-Project
 ┣ 📜 Capstone_Proj.ipynb
 ┣ 📜 Data.csv
 ┣ 📜 streamed_prices.jsonl
 ┣ 📜 README.md
 ┗ 📄 (Optional) report.pdf
```

---

## 📄 Optional Documentation
- **Notebook**: `Capstone_Proj.ipynb` includes all code, from preprocessing to modeling.
- **Live Stream Output**: `streamed_prices.jsonl` mimics real-time model pricing predictions.
