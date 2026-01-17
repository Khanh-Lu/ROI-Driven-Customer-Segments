# Optimizing 6-Month Marketing ROI through RFM Clustering

**Table of Contents**

- [Project Background](#project-background)
- [Executive Summary](#executive-summary)
- [Insights Deep-Dive](#insights-deep-dive)
- [Recommendations](#recommendations)
- [Assumptions and Caveats](#assumptions-and-caveats)

<div align="center">
  <img src="https://github.com/Khanh-Lu/ROI-Driven-Customer-Segments/blob/805cd1f90b54fcb299d49845283b98d46a15d3f0/Images/clusters_3d_offcial.png" alt="image alt" />
</div>

## 🛠️ Tech Stack & Core Concepts

### **Languages & Libraries**
<a href="https://www.python.org/">
    <img alt="Python" src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white">
</a>
<a href="https://pandas.pydata.org/">
    <img alt="Pandas" src="https://img.shields.io/badge/Pandas-150458?logo=pandas&logoColor=white">
</a>
<a href="https://numpy.org/">
    <img alt="NumPy" src="https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white">
</a>
<a href="https://scikit-learn.org/">
    <img alt="Scikit-learn" src="https://img.shields.io/badge/scikit--learn-F7931E?logo=scikit-learn&logoColor=white">
</a>
<a href="https://matplotlib.org/">
    <img alt="Matplotlib" src="https://img.shields.io/badge/Matplotlib-3C3F4D?logo=matplotlib&logoColor=white">
</a>

### **Methodology & Logic**
<a href="https://en.wikipedia.org/wiki/K-means_clustering">
    <img alt="K-Means" src="https://img.shields.io/badge/K--Means-FFCC00?logo=scikitlearn&logoColor=black">
</a>
<a href="https://en.wikipedia.org/wiki/RFM_(market_research)">
    <img alt="RFM Analysis" src="https://img.shields.io/badge/RFM%20Analysis-007ACC?logo=analytics&logoColor=white">
</a>
<a href="https://en.wikipedia.org/wiki/Customer_lifetime_value">
    <img alt="CLV Forecasting" src="https://img.shields.io/badge/CLV%20Forecasting-E10098?logo=chartdotjs&logoColor=white">
</a>

---

## **Purpose**

This project identifies distinct customer segments using **K-Means Clustering** to move away from "mass marketing" toward **segment-specific ROI optimization**. By calculating the actual 6-month value of each cluster, we provide a prescriptive financial roadmap for reinvestment.

## **Executive Summary**

- **Strategic Segmentation:** Identified distinct customer clusters using K-Means based on RFM features (Recency, Frequency, Monetary).

- **Feature Engineering:** Developed advanced metrics including Average Order Value (AOV), Tenure, and Average Time Between Purchases (TBP) to enhance clustering accuracy.

- **ROI Optimization:** Shifted focus from total revenue to a 6-month prediction window (March 2023 snapshot) to provide a realistic roadmap for reinvestment.

## **Insights Deep-Dive**

![image alt](https://github.com/Khanh-Lu/ROI-Driven-Customer-Segments/blob/805cd1f90b54fcb299d49845283b98d46a15d3f0/Images/Clusters_Official.png)

### RFM Analysis & Customer Segmentation

- **Cluster 1:** "Active High-Value Spenders" - Most recent activity with the highest average spend ($10,752), though lower frequency than Cluster 3.
- **Cluster 2:** "Active Low-Value Spenders" - "Everyday Shoppers" who are currently active but spend less per transaction ($6,253).
- **Cluster 3:** "Loyal Power Users" - Recent shoppers with exceptionally high frequency (21 purchases). They interact with the brand constantly.
- **Cluster 0:** "Mid-Tier Spenders but Inactive"- High-value historical customers who haven't purchased in ~920 days; likely churned.

---

## **Recommendations**

### Segment-Specific Reinvestment Strategy

![image alt](https://github.com/Khanh-Lu/ROI-Driven-Customer-Segments/blob/805cd1f90b54fcb299d49845283b98d46a15d3f0/Images/Post-Hoc%20Validation.png)

| Customer Segment | Core | Strategic Goal | Max Allowable Spend |
| :--------------- | :--- | :------------- | :---------------------------- |
| **Cluster 1** | **Active High-Value Spenders** | Primary goal is Frequency growth, use personalized offers to drive them toward Cluster 3 behavior. | **$984.00** |
| **Cluster 2** | **Everyday Shoppers** | Focus on Efficiency through automated upselling/cross-selling to increase basket size. | **$579.00** |
| **Cluster 3** | **Loyal Power Users** | Focus 100% on Retention and referral programs to leverage their high brand affinity. | **$727.54** |
| **Cluster 0** | **Inactive Mid-Tier** | Deploy a Fixed Test Budget (e.g., $50 total) for a one-time "Win-back" re-engagement campaign rather than an LTV-based spend. | **Fixed $50 (Total)** |


## **Future Work: Moving from Descriptive to Predictive CLV**

Currently, the model looks at **actual** past behavior. My next step is to build a **Predictive CLV Model**:
- **Probabilistic Modeling**: Implementing BG/NBD and Gamma-Gamma models to predict *expected* future transactions.
- **ML Forecasting:** Use **Decision Trees** and **XGBoost** to predict a customer's future CLV


## **Assumptions and Caveats**

**Important Caveats & Limitations**

- **Snapshot Date**: Analysis based on a **March 1, 2023** observation date.
- **Gross Margin**: Budget ceilings assume **100% gross margin**. For final execution, stakeholders should apply specific contribution margins (e.g., 40%).
- **LTV:CAC Target**: Recommendations follow a **3:1 ROI target**—every $1 spent targets $3 in return.

---

## **General Info**

- See the notebook for data cleaning, visualization, and analysis in the [Python Notebook](https://github.com/Khanh-Lu/ROI-Driven-Customer-Segments/tree/main/Exploration).
