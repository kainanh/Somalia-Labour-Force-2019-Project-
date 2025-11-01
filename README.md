# 🇸🇴 Somalia Labour Force Survey (LFS) 2019 — Data Analysis

### Exploratory Data Analysis and Key Insights  
**Author:** Kainan Hassan  
**Date:** November 2025  

---

## 📘 Overview
This project explores the **Somalia Labour Force Survey (LFS) 2019**, conducted by the **National Bureau of Statistics (NBS)**.  
The survey provides comprehensive information on employment, unemployment, and the structure of Somalia’s labour market.  

Using Python, this project performs an **Exploratory Data Analysis (EDA)** to uncover insights on **labour market participation**, **gender disparities**, and **education-related outcomes**.

---

## 🎯 Research Objectives
- Describe the composition of the **working-age population (15–64 years)**.  
- Examine how **gender** influences labour force participation.  
- Explore the relationship between **education level** and **employment status**.  
- Identify how **educational attainment** affects **labour market outcomes** such as hours worked and employment type.

---

## 📊 Data and Methodology

### 🗂️ Data Source
Dataset: [Somali Labour Force Survey 2019 (SOMLFS2019)](https://microdata.nbs.gov.so/index.php/catalog/57)  
Accessed from the **Somalia National Data Archive (NADA)**.

### 🔑 Key Variables
| Variable | Description |
|-----------|-------------|
| `ilo_sex` | Gender |
| `ilo_edu_aggregate` | Education level (aggregate) |
| `ilo_lfs` | Labour force status |
| `ilo_job1_ste_aggregate` | Employment status (aggregate) |
| `ilo_wgt` | Sample weight |

Weighted values are applied throughout to reflect the survey’s complex sampling design.

---

## 🧮 Methodological Steps
1. **Data Extraction**  
   - Loaded `.sav` files using `pyreadstat`.  
   - Selected relevant variables from household and individual datasets.

2. **Data Cleaning & Transformation**  
   - Renamed columns using variable labels for clarity.  
   - Standardized coded responses (e.g., `1 - Male` → `Male`).  
   - Filtered for **working-age individuals (15–64 years)**.  
   - Converted categorical variables into ordered types for logical sorting.

3. **Analysis Techniques**  
   - Weighted aggregations using `sample_weight`.  
   - Cross-tabulations by gender, education, and employment status.  
   - Data visualization with **matplotlib** and **seaborn**.

---

## 📈 Key Findings

### 1️⃣ Labour Force Composition by Gender
- **Women:** 79% outside the labour force  
- **Men:** 52% outside the labour force  
➡️ Major gender disparity in participation.

### 2️⃣ Labour Force Status by Education Level
- Employment rates **increase with higher education**.  
- Those with *Less than basic* education are mostly outside the labour force.  
- Individuals with *Advanced* education are **twice as likely to be employed**.

### 3️⃣ Education Participation by Gender
- Most women fall within the *“Less than basic”* education category.  
- As education level increases, **female participation declines**, while **male participation rises**.  
➡️ Highlights persistent gender inequality in educational attainment.

### 4️⃣ Employment Status by Education Level & Gender
- Higher education shifts both genders toward **employee roles**.  
- Women show stronger improvement with education in employment type than men.

---

## 🧰 Technologies Used
- **Python 3.11**  
- **Pandas** – Data wrangling and aggregation  
- **Pyreadstat** – Reading SPSS (.sav) files  
- **Matplotlib & Seaborn** – Data visualization  
- **NumPy** – Numeric operations  

---

## 🎨 Visualization Style
A consistent, professional color palette was used across all plots:

```python
vis_colors = ['#4C72B0', '#55A868', '#C44E52', '#8172B3']
