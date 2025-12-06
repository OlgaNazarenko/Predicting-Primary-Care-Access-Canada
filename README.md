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
**Dataset 1**: Patient satisfaction with family doctors"
- **Source**: [Statistics Canada CCHS (Canadian Community Health Survey)](https://open.canada.ca/data/en/dataset/95938131-77e3-4ae9-8fde-9bb024dad418)
- **Table**: 13-10-0495
- **Coverage**: All Canadian provinces and territories, 2000-present
- **Variables**: Patient satisfaction by age, sex, geographic region

**Dataset 2**: Physician supply, distribution and migration
- **Source**: [CIHI (Physician Supply Data), select "Supply, Distribution and Migratio" XLSX](https://www.cihi.ca/en/physicians )
- **Coverage**: All Canadian provinces and territories, 1968-2024
- **Variables**: Physicians by jurisdiction, specialty, demographic characteristics, geographic distribution, physician migration, practice patterns and employment, gender composition of workforce.

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
- Statsmodels
- Jupyter Notebook

Tools
- Git & GitHub
- VS Code or JupyterLab

**Data Limitations**
- Satisfaction is subjective
- Survey-based data subject to response bias
- Does not directly measure physician supply or shortage

---

## 📁 Folder Structure

```
Predicting-Primary-Care-Access-Canada/
│
├── data/
│   ├── CIHI.ipynb
│   └── satisfactory_surveys.ipynb
│
├── notebooks/
│   ├── 01_data_exploration.ipynb
│   ├── 02_feature_engineering.ipynb
│   ├── 03_time_series_modeling.ipynb
│   └── 04_ml_modeling.ipynb
│
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