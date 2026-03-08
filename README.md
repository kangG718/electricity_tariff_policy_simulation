# ⚡️ Electricity Tariff Policy Simulation
### 산업별 전력 사용 데이터 기반 전기요금 정책 시뮬레이션 

Industrial electricity usage data–based **electricity tariff policy simulation framework** that identifies VVIP power consumers and evaluates the impact of tariff adjustment policies through data-driven analysis.

산업별 전력 사용 데이터를 기반으로 **초대형 전력 소비 산업(VVIP)**을 식별하고, 전기요금 단가 조정 정책이 산업 집단별 비용 부담과 매출 구조에 미치는 영향을 **데이터 기반 시뮬레이션**으로 분석하는 정책 평가 프레임워크이다.

---

## 📊 Project Overview

This project proposes a **data-driven policy analysis framework** for evaluating electricity tariff adjustments.

The framework performs the following steps:

1. Data preprocessing and validation  
2. Electricity consumption structure analysis  
3. Identification of VVIP power consumers  
4. Selection of policy target period  
5. Tariff adjustment simulation  
6. Comparison of electricity cost increase across industry groups  
7. Evaluation of policy fairness and impact  

즉 단순히 특정 정책 결과를 계산하는 것이 아니라  
**전력 소비 구조 분석 → 정책 적용 → 정책 효과 평가**의 전 과정을 하나의 분석 흐름으로 구조화한 **정책 시뮬레이션 프레임워크**이다.

---

## 📂 Dataset

Industrial monthly electricity usage dataset

Structure:

| Variable | Description |
|---|---|
| YearMonth | Observation month (YYYYMM) |
| Households | Number of facilities or establishments |
| Usage | Total electricity consumption |
| ElectricityBill | Total electricity cost |
| AveragePrice | Average electricity price per unit |

Dataset size  
**4473 observations × 5 variables**

---

## ⚙️ Methodology

### 1. Data preprocessing
- Missing value detection  
- Removal of invalid observations (negative usage)

### 2. Consumption structure analysis
- Monthly statistics  
- Industry electricity consumption distribution

### 3. VVIP identification
Industries with electricity bills exceeding **1 trillion KRW** are defined as **VVIP power consumers**.

### 4. Policy simulation

A tariff increase scenario is applied to a selected target month.

Electricity bill recalculation </br>
$ElectricityBill = Usage × AveragePrice$


### 5. Policy evaluation

Electricity bill increase rates are compared between

- VVIP industries  
- Non-VVIP industries  

to evaluate **policy fairness and economic impact**.

---

## 🧪 Example Policy Scenario

Example simulation

Target month: **August 2020**  
Tariff increase: **+5%**

Result

- VVIP electricity bill increase ≈ **4.63%**
- Non-VVIP electricity bill increase ≈ **5.06%**

This result indicates that **uniform tariff increases may impose relatively higher burden on smaller electricity consumers.**

---

## 🧠 Framework Extension

This framework can be extended with

- Electricity demand forecasting models  
- Industry-level electricity elasticity estimation  
- Machine learning-based policy optimization  
- Dynamic electricity pricing strategies  

---

## 🚀 Usage

Run the notebook
전기요금정책_시뮬레이션.ipynb

The notebook automatically loads the dataset and performs the full analysis pipeline.

---

## 👤 Author

**Byungo Kang (강병오)**  
Computer Engineering, Kyung Hee University  

GitHub  
https://github.com/kangG718
