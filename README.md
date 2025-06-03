# Enhancing VC Decisions: Identifying High-Growth Startups with Machine Learning

## 📌 Project Overview

This project leverages machine learning techniques to help venture capital (VC) investors identify startups with high growth potential. Using a dataset sourced from Harmonic.ai, we analyze over 40,000 startups from Series A to Series C+ to build predictive models that classify companies as either Early Stage or Growth Stage.

Our goal is to improve the investment decision-making process by surfacing the most influential features of high-performing startups, enabling VCs to allocate capital more efficiently and with greater confidence.

---

## 🧠 Business Understanding

VCs often rely on intuition and experience when evaluating startups—an approach that can be prone to bias and inefficiency. This project introduces a data-driven method to:
- Reduce false-positive investment decisions
- Highlight critical success indicators (e.g., funding totals, number of rounds)
- Enable scalable and repeatable analysis

---

## 📊 Data Description

- **Source**: Harmonic.ai
- **Entries**: 41,339 startups
- **Stages**: Series A to Series C+
- **Features**: Funding totals, headcount, industry tags, country, customer type, and more
- **Target Variable**: `Stage` (Early Stage vs. Growth Stage)

---

## 🧹 Data Preparation

- **Missing Values**: Median imputation for numeric fields; "Unknown" for categorical fields
- **Dropped Columns**: High-null columns and irrelevant identifiers
- **Standardization**: Applied to numeric fields
- **Encoding**: One-hot encoding for categorical variables
- **Outliers**: Treated to reduce distortion in funding-related variables

---

## 📈 Exploratory Data Analysis

Key insights include:
- Communications, Life Sciences, and Consumer Products sectors attract the most funding
- Startups in South Korea, Japan, and China show strong investment momentum
- Funding total increases with the number of funding rounds
- Funding peaked around 2015–2017, followed by a decline

---

## 🤖 Modeling and Evaluation

**Algorithms Used:**
- XGBoost (Best performing)
- Random Forest
- Gradient Boosting
- Logistic Regression
- Decision Tree

**Highlights:**
- Original model overfit due to data leakage from `Last Funding Type`
- After correction, XGBoost achieved the highest performance

**Model Metrics (Post Data Leakage Fix):**
- **AUC**: 0.8814
- **Precision (Threshold = 0.6)**: 0.84
- **Recall**: 0.70
- **False Positives**: 717
- **True Positives**: 2,899

---

## 🧩 Feature Importance

Top predictors of startup growth:
- `Funding Total`
- `Headcount`
- `Number of Funding Rounds`
- Geographic region (notably East Asia)

---

## 💥 Business Impact

- Reducing false positives can save millions in poor investment decisions
- Model helps build stronger, more diversified portfolios
- Automates screening, freeing analysts for strategic evaluations

---

## 🚀 Future Work

- Incorporate earlier-stage companies (e.g., seed, pre-seed)
- Integrate investor success data
- Explore additional datasets (e.g., social engagement, market trends)
- Deploy model into an interactive VC decision-support dashboard

---

## 🧑‍💻 Team Members & Roles

| Name            | Role                                     |
|-----------------|------------------------------------------|
| Leon Jon        | Data understanding & preprocessing       |
| Srinidhi Jeyakumar | Exploratory data analysis & visuals    |
| Trent Yu        | Modeling & evaluation                    |
| Zitong Wang     | Reporting & presentation development     |

---

## 📁 Files

- `final_code.ipynb`: All modeling and evaluation code (Python, Jupyter)
- `Final Report.pdf`: Full technical report
- `Final Project.pdf`: Presentation summary slides

---

## 🔗 External Links

- [Google Colab Notebook](https://colab.research.google.com/drive/1hjx153Wvq6Z9JScdNgXyVDRXVNJ3qG6R?usp=sharing)
- [Google Drive (Data & Resources)](https://drive.google.com/drive/folders/1n2OwlfyRclpqgCGmijG980GcgmDPAxiW?usp=sharing)

---

## 📌 Disclaimer

This project was originally completed as a final assignment for the **Data Science for Business** course at **NYU Stern (Fall 2024)** and has been adapted for public presentation in this repository.
