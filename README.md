# 📊 Google Ecommerce Analytics: Causal Impact of Paid Advertising

## 📌 Introduction  
> **"Correlation ≠ Causation"**

While widely cited, this principle is often overlooked in business analytics.  
This project rigorously examines whether paid advertising **causes** higher conversions compared to organic traffic.

---

## 📂 Dataset Overview  
**Google Merchandise Store (GMS)** Analytics  

🔗 [Google Analytics BigQuery Public Dataset](https://support.google.com/analytics/answer/7586738#where-the-data-comes-from&zippy=%2Cin-this-article)

The `ga4_obfuscated_sample_ecommerce` dataset (available via BigQuery Public Datasets) contains:
- **Sample period**: 2020-11-01 to 2021-01-31 (3 months)  
- **Data type**: BigQuery GA4 event export  
- **Size**: 500,000+ raw rows requiring cleaning and transformation  

---

## ❓ Research Question  

> **Does paid advertising drive significantly higher conversion rates compared to organic visits?**

This study explores:
- ✅ Whether paid traffic (e.g., CPC/CPM) converts better than organic
- ✅ Which channels perform better for specific user segments
- ✅ Whether observed correlations can be interpreted causally

---

## ⚙️ Methodology

### 1. **Data Preparation**
- Clean and filter ~500K raw GA4 event records  
- Handle missing data and normalise unconventional values

### 2. **Exploratory Data Analysis (EDA)**
- Examine feature distributions and conversion rates  
- Understand treatment vs. control group characteristics  
- Identify potential confounders

### 3. **Causal Inference**
- Build causal DAG / Bayesian Network to visualise relationships  
- Estimate causal effect using:
  - Logistic Regression (baseline)
  - Propensity Score Matching (PSM)
  - Inverse Probability Weighting (IPW)
- Estimate Average Treatment Effect (ATE)

### 4. **Validation & Conclusion**
- Perform sensitivity analysis to check robustness  
- Summarise key insights and recommendations

### 5. **BI Dashboard**
- Interactive summary
