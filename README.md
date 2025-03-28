# 🦵 Meniscal Injury Analysis

A comprehensive statistical analysis of meniscus injuries based on a dataset of 597 patients who underwent arthroscopic meniscus surgery.

## 📌 Overview

Meniscal injuries are among the most frequent causes of knee pain, impacting mobility and quality of life. This project explores the distribution and relationships between different types of meniscal injuries using descriptive statistics and statistical hypothesis testing.

📅 **Study Period:** January 2013 – May 2018  
🏥 **Source:** First Affiliated Hospital of the University  
📊 **Dataset:** 597 patient records  
🔗 **Citation:** [Jiang, Peishi (2019). Meniscal injury (Arthroscopy)](https://doi.org/10.6084/m9.figshare.11309312.v1)

---

## 🎯 Goals

- Analyze injury distribution by **gender**, **age group**, and **injury location**.
- Examine prevalence of **medial**, **lateral**, and **combined (bilateral)** injuries.
- Identify **statistical relationships** between injury types.
- Create **visualizations** to support findings.

---

## 🧼 Data Cleaning Summary

- ✅ No missing values (`COUNTBLANK = 0`)
- ✅ Age values verified (4 categorical groups)
- ✅ All binary columns contain only 0 or 1 values (manually and via `UNIQUE` check)

---

## 📊 Key Findings

### Gender Distribution
- **58.29% Female**, **41.71% Male**
- Female patients are more represented (ratio ~1.4:1)

### Age Distribution
- **48.74%** of patients fall in the **45–60** age group  
- Indicates middle-aged population is most affected

### Injury Types
- **Medial Injuries**: 56.3%  
- **Lateral Injuries**: 67.2%  
- **Bilateral Injuries**: 24.0%  

### Relationships Between Injuries

| Pair | p-value | Odds Ratio | Association |
|------|---------|------------|-------------|
| Medial vs Lateral | < 2.2e-16 | 0.0057 | Very Strong Negative |
| Lateral vs Bilateral | < 2.2e-16 | 106.48 | Very Strong Positive |
| Medial vs Bilateral | < 2.2e-16 | 189.26 | Extremely Strong Positive |

👉 Fisher’s Exact Test (via R) was used due to low observed frequencies violating Chi-Square assumptions.

---

## 📈 Tools & Technologies

- **Excel** – Cleaning, PivotTables, Charts, Chi-Square Test
- **R** – Fisher’s Exact Test (`fisher.test()` function)
- **Markdown** – Reporting
- **Data Source** – figshare.org

---

## 📷 Visualizations

### 🧍‍♂️🧍‍♀️ Gender Distribution

![Gender Distribution](images/gender_dist.png)

The chart above shows that **58.29%** of patients are **female** and **41.71%** are **male**, suggesting a slight female dominance in the dataset.

---

### 🎂 Age Group Distribution

![Age Group Distribution](images/age_group_dist.png)

Most patients (48.74%) fall within the **45–60 age group**, indicating middle-aged individuals are the most affected by meniscus injuries.

---

### 🩺 Injury Type Distribution

![Injury Type Distribution](images/injury_type_dist.png)

- **Medial Injuries:** 56.3%  
- **Lateral Injuries:** 67.2%  
- **Bilateral Combined Injuries:** 24.0%

The chart illustrates that **lateral injuries** are the most common among the patient sample.

---


## 📄 License

This project is for educational and analytical purposes only.

---

## 🙋‍♂️ Author

**Emir Doğan** 

---

