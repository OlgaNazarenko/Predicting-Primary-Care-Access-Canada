# Predicting-Primary-Care-Access-Canada

## Overview
Analyzes patient satisfaction with family doctor care in Canada using Statistics Canada Data to predict accessibility patterns and identify regional shortages.

---

## 🎯 Project Goals
- Measure actual patient experiences
- Reveal regional disparities in healthcare satisfaction
- Identify demographic groups with poorest access
- Provide quantitative foundatin for predicting family doctor shortage patterns

## 🗂 Datasets
**Dataset**: Patient satisfaction with family doctors"
- **Source**: [Statistics Canada CCHS (Canadian Community Health Survey)](https://open.canada.ca/data/en/dataset/95938131-77e3-4ae9-8fde-9bb024dad418)
- **Table**: 13-10-0495
- **Coverage**: All Canadian provinces and territories, 2000-present
- **Variables**: Patient satisfaction by age, sex, geographic region

Why I chose these datasets:
- Open and reliable data source
- Comprehensive metrics and dimensions
- Directly addresses research problem
- ML ready format (available as CSV, XLXS)
- Practical advantages for analysis (large sample, multiple years of data)

## 🛠 Tech Stack

Languages & Libraries
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- Jupyter Notebook

Tools
- Git & GitHub
- VS Code or JupyterLab

## Data Limitations

- Satisfaction is subjective
- Survey-based data subject to response bias
- Does not directly measure physician supply or shortage

### XGBoost Model Limitations

The XGBoost model accounts for **physician density and rurality** but **cannot capture systemic factors** that also drive shortages, including:

- Physician burnout and mental health
- Healthcare funding constraints
- Inadequate infrastructure and equipment
- Lack of specialist support in remote areas
- Educational opportunities for rural physicians
- Administrative burden on primary care providers

These factors represent important areas for future research and policy consideration.


## Results on the data: CIHI Physician Supply Analysis

![Results](images/output_ph.png)

### Critical Findings

- **Nunavut's 8% access gap exceeds the national average of 0.9% by nearly 9-fold**, indicating a public health crisis requiring urgent intervention.
- **Despite representing only 0.12% of Canada's population**, Nunavut faces the most severe primary care access deficit. The **2020-2024 decline suggests worsening conditions require immediate policy attention**.

### Geographic Disparities

- Provinces with **60% rural population experience 5-8% without primary care access**
- Provinces with **<10% rural population maintain <2% access gaps**
- This reveals that **geographic dispersion is a critical barrier** to healthcare access, independent of total physician supply

### Physician Density Benchmarks

- **To achieve <1-2% access gaps:** Canada should maintain **at least 110-140 family physicians per 100,000 population**
- **Current status:** Only urban centers and well-resourced provinces meet this standard

### Physician Workforce Stability Crisis

- **Nunavut retention rate: 77-85%** (losing 15-23% annually vs. national 0.04%)
- **Quebec retention rate: 99.7%** (losing only 0.3% annually)
- This **3.75 percentage point difference** means Nunavut loses ~31.8% of its physician workforce over 5 years

### Trend Analysis (2020-2024)

- Primary care access gaps remained stable at **0.65%-1.87% from 2020-2023**
- **Sharp deterioration in 2024: jumped to 3.04% from 0.65%** (a 366% increase in one year)
- This sudden worsening indicates an **emerging crisis** requiring immediate intervention

### Recommended Policy Interventions

To address these disparities, the following measures should be implemented:

- **Immediate (0-12 months):** Emergency telemedicine deployment in Nunavut/NWT
- **Short-term (1-2 years):** Double recruitment incentives and housing subsidies for rural physicians
- **Long-term (2-5 years):** Restructure training programs to send more graduates to shortage areas
- **Ongoing:** Infrastructure development in underserved regions
- **Continuous:** Healthcare workforce planning to prevent physician migration

### Model Performance & Limitations

- **XGBoost model accuracy:** R² = 0.95+ (excellent predictions)
- **Accounts for:** Physician density and rurality
- **Cannot capture:** Physician burnout, funding constraints, infrastructure limitations, policy changes

---

## 📁 Folder Structure

```
Predicting-Primary-Care-Access-Canada/
│
├── data/
│   └── supply-distribution-migration-physicians-in-canada-2024-data-tables-en.xlsx
│
├── notebooks/
│   └── 01_data_exploration_physicians.ipynb
│
├── images/
│   └── output_ph.png
│
├── .gitignore
├── README.md
└── requirements.txt

```
---


## ▶️ How to Install and Run

1. Clone the repository
```
git clone https://github.com/....
cd Predicting-Primary-Care-Access-Canada
```

2. Create and activate a virtual environment
```
python3 -m venv venv
source venv/bin/activate  # macOS/Linux
venv\Scripts\activate     # Windows
```

3. Install dependencies
```
pip install -r requirements.txt
```

---