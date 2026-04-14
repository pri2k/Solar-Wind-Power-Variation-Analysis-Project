# 🌞⚡ Solar & Wind Power Variation Analysis

## 📌 Overview
This project focuses on analyzing **distributed renewable energy data** (solar and wind) using statistical and data-driven methodologies.

Renewable energy sources are **highly variable and uncertain** due to environmental dependencies. This project aims to transform raw, high-dimensional energy data into a **clean, reliable, and statistically validated dataset**.

We use:
- Statistical preprocessing
- Hypothesis testing
- Correlation analysis
- ANOVA
- Dimensionality reduction & clustering

---

## 🎯 Problem Statement
How can we transform a **raw, noisy, and high-dimensional distributed renewable energy dataset** into a **statistically consistent, reliable, and interpretable dataset** using research methodologies such as:
- Hypothesis testing  
- Anomaly detection  
- Correlation analysis  
- Dimensionality reduction  

---

## 🎯 Objectives
- Analyze solar and wind power generation data
- Remove noise and anomalies from the dataset
- Validate temporal and spatial correlations
- Perform **hypothesis testing (t-test & F-test)**
- Apply **One-Way ANOVA** for multi-group comparison
- Validate dataset labels using clustering techniques
- Enable dataset usability for ML and power system analysis

---

## 📊 Dataset Description

### 🔹 Dataset Used
- **DDRE-33 (Distributed Renewable Energy Dataset)**
- Based on IEEE-33 bus system

### 🔹 Key Characteristics
- 2000 single-node time series  
- 300 wind–solar combined scenarios  
- Data recorded every **15 minutes for 1 year**  

### 🔹 Energy Sources
- 🌞 Solar (Photovoltaic - PV)
- 🌬️ Wind Power

### 🔹 Data Representation
- Megawatts (MW)
- Per-unit (p.u.) normalization

---

## ⚙️ Methodology

### 1️⃣ Data Preprocessing

#### ✔️ Outlier Detection
- Method: **Interquartile Range (IQR)**
- Removes extreme anomalies
- Improves model accuracy

#### ✔️ Missing Data Handling
- Linear interpolation
- Time-based averaging
- Ensures continuity in time-series data

---

### 2️⃣ Correlation Analysis

#### 🔹 Temporal Autocorrelation
- Measures similarity across time
- Ensures smooth transitions in data
- Observation:
  - High correlation at low lag
  - Solar correlation drops faster over time

#### 🔹 Spatial Cross-Correlation
- Measures similarity across nodes
- Captures shared weather patterns
- Observation:
  - Strong correlation between nearby nodes

---

### 3️⃣ Hypothesis Testing

#### 🔸 Case 1: Solar (PV Node 18 vs Node 33)
- **t-test** → Mean comparison  
- **F-test** → Variance comparison  

**Result:**
- Node 33 has **higher mean power**
- Node 33 shows **higher variability**

---

#### 🔸 Case 2: Wind (Node 22 vs Node 25)
- **t-test** and **F-test**

**Result:**
- Node 22 produces **higher power**
- Node 22 has **higher fluctuations**
- Node 25 is **more stable but less productive**

---

### 4️⃣ ANOVA (Analysis of Variance)

#### ✔️ Why ANOVA?
- Multiple groups:
  - Solar (Node 18, Node 33)
  - Wind (Node 22, Node 25)
- Avoids multiple t-test errors

#### ✔️ Method
- One-Way ANOVA
- Flattened large-scale dataset (~17M samples per group)

#### ✔️ Hypothesis
- H₀: All groups have equal mean  
- H₁: At least one group differs  

#### ✔️ Result
- Very large F-statistic  
- p-value ≈ 0  

**Conclusion:**
- Significant differences exist across energy sources  
- Solar → Higher output but more variable  
- Wind → Lower output but more stable  

---

### 5️⃣ Label Analysis

#### ✔️ Purpose
- Validate dataset labeling quality

#### ✔️ Goal
- Same label → Similar patterns  
- Different labels → Distinct behavior  

#### ✔️ Impact
- Improves dataset reliability  
- Enables ML-based classification

---

### 6️⃣ Dimensionality Reduction (PCA)

- Converts high-dimensional time-series into features  
- Projects data into **2D space**  
- Preserves maximum variance  

**Impact:**
- Visualization  
- Pattern separability  

---

### 7️⃣ Clustering (K-Means)

#### 🔹 Wind Data
- 4 clusters  
- Seasonal patterns observed  

#### 🔹 Solar Data
- 6 clusters  
- Weather-based patterns observed  

**Validation:**
- Clusters align with labels  
- Confirms meaningful dataset structure  

---

## 📈 Key Insights

- Renewable energy data is **highly variable**
- Solar power:
  - Higher mean output  
  - Higher variability  

- Wind power:
  - Lower mean output  
  - More stable  

- Strong **temporal and spatial correlations** exist  
- Statistical tests confirm **non-random differences**  
- Dataset is:
  - Clean  
  - Complete (no missing values)  
  - Physically valid  

---

## 🧠 Concepts Used
- Hypothesis Testing (t-test, F-test)  
- One-Way ANOVA  
- Correlation Analysis  
- Time-Series Analysis  
- PCA (Dimensionality Reduction)  
- K-Means Clustering  
- Statistical Validation  

---

## 📌 Applications

- ⚡ Power system planning & scheduling  
- 📊 Renewable energy forecasting  
- 🤖 Machine learning model training  
- 🌍 Climate-aware energy systems  
- 📉 Variability and reliability analysis  

---

## 🚀 Conclusion

This project successfully:
- Cleans and validates renewable energy data  
- Demonstrates statistical differences across sources  
- Confirms meaningful labeling using clustering  
- Produces a dataset suitable for **research and ML applications**  

