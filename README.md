# Predictive Analytics of Student Burnout: A Scalable Study on 1M Records

## 🎓 Project Overview
This project presents a multi-dimensional analysis of student mental health and burnout levels using a massive dataset of **1,000,000 student records**. By leveraging **GPU-accelerated analytics** (NVIDIA RAPIDS) and a dual-tool visualization strategy (**Plotly + Tableau**), our team identified critical socio-economic and behavioral drivers that lead to academic exhaustion.

### 🚀 Key Technical Highlights
- **Scalability:** Processed **1,000,000 rows** with 20 high-dimensional features.
- **Technology Stack:** 
    - **NVIDIA RAPIDS (cuDF):** Used for high-speed GPU-accelerated data cleaning and correlation computation (achieving a **20x speedup** over CPU-based Pandas).
    - **Plotly/Dash:** Developed a responsive 2x2 grid HTML dashboard for macro-statistical analysis.
    - **Tableau:** Utilized for behavioral deep-dives (Interaction between Sleep and Study hours).
- **Presentation Design:** Optimized for **Live Web Embedding** in professional presentation environments.

---

## 📊 Dataset & Processing
The dataset captures demographics, academic performance, and psychological metrics (Anxiety, Depression, Financial Stress, Sleep hygiene).

### Dataset：https://www.kaggle.com/datasets/sharmajicoder/student-mental-health-and-burnout

### Data Pipeline Architecture:
1. **Script 1 (Cleaning.ipynb):** Performed on the full **1M population** using cuDF. We implemented **Z-Score Outlier Removal** to eliminate statistical noise in GPA and sleep metrics, ensuring the integrity of our trends.
2. **Script 2 (Group_Project_Plotly_Visualization.ipynb):** Generates a professional **3-Chart Dashboard** based on a statistically significant 50,000-row cleaned sample:
    - **Chart 1 (Burnout Density):** A Violin Plot visualizing the probability density across genders.
    - **Chart 2 (Stressor Analysis):** A bar chart sorted from **High → Medium → Low** risk to demonstrate factor decay.
    - **Chart 3 (Global Correlation):** A GPU-calculated heatmap providing the roadmap for feature selection in ML.

---

## 🔍 Core EDA Insights
- **Persistent Stressors:** **Financial Stress** was identified as the most persistent factor, remaining high even in "Medium" risk categories, unlike exam pressure which only spikes at extreme burnout levels.
- **The Performance Threshold:** Our analysis identified a non-linear relationship where academic performance remains resilient until a specific stress threshold (8/10), after which it collapses.
- **ML Justification:** Correlation analysis ($r > 0.7$) confirmed that **Sleep Deprivation** and **Financial Stress** are the primary predictors of burnout risk.

---

## 🤖 Preliminary Machine Learning Direction
- **Proposed Task:** Multi-Class Classification (Predicting Low, Medium, and High risk).
- **Model Choice:** **GPU-Accelerated XGBoost**. 
- **Rationale:** Our EDA revealed **non-linear risk thresholds** and significant class imbalances, making gradient-boosted trees more effective than linear regression for this specific population scale.

---

## 👥 Team Contributions (Mid-Presentation)
| Name | Responsibility | Primary Tools |
| :--- | :--- | :--- |
| **Xinghan Chen** | EDA Lead, Plotly Dashboard Design, ML Direction | Plotly, cuDF, Python |
| **Abhijith Reddy** | GPU Data Engineering, RAPIDS Preprocessing | NVIDIA RAPIDS, cuDF |
| **Xinghan Chen** | Statistical Validation, Plotly Layout Logic | Plotly, Pandas |
| **Sanjana Reddy** | Tableau Dashboard Lead, Interaction Mapping | Tableau Desktop |

---
