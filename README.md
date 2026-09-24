# Team Name : Null
Project Name : Tracking Tourist Trends for a Sustainable Malaysia


An end-to-end early-warning system for sustainable tourism in Malaysia, integrating demand forecasting, tourism carrying capacity assessment, and decision-support simulation

## Overview

Malaysia's domestic tourism has recovered strongly post-COVID-19, but growth is highly uneven — over 25% of visitors are concentrated in Selangor and W.P. Kuala Lumpur, while states such as Perlis and W.P. Labuan remain under-utilised. This project develops a three-layer early-warning system to:
1. Forecast domestic visitor arrivals for all 13 states and 3 federal territories (2026–2028)
2. Assess tourism carrying capacity for four high-risk destinations
3. Provide an interactive decision-support dashboard for policymakers

## System Architecture

| Layer | Method | Output |
|---|---|---|
| Predictive | Prophet time-series forecasting | State-level visitor forecasts 2026–2028 |
| Diagnostic | AHP + Entropy Weight Method (CCI) | Tourism Carrying Capacity Index |
| Decision Support | Hierarchical Clustering + Scenario Simulation | Green/Yellow/Red early warning dashboard |

## Data Sources

| Indicator | Source |
|---|---|
| Domestic visitor arrivals | DOSM Tourism Satellite Account |
| Hotel rooms, AOR | Tourism Malaysia, DOSM State Reports |
| Coral cover | Reef Check Malaysia 2025 |
| Non-Revenue Water | SPAN |
| Water consumption | OpenDOSM |
| Population, GDP | OpenDOSM, DOSM |
| Landslide incidents | Pahang State Government |

## Repository Structure
datathon-tourism


├── **data**


│ ├── Null Datathon.xlsx


│ ├── tourism data.xlsx


│ └── cleaned/ # Preprocessed CSVs


├── **notebooks**


│ ├── 01_data_preprocessing.ipynb


│ ├── 02_capacity_index.ipynb


│ ├── 03_scenario_simulation.ipynb


│ └── 04_growth_forecast.ipynb


├── **outputs**


│ ├── powerbi_*.csv # Power BI-ready tables


│ └── dashboard.pbix # Power BI dashboard


├── **report**


│ └── Datathon_Report.pdf


└── README.md


---

## Getting Started

### Prerequisites

```text
pip install -r requirements.txt
pandas>=2.0
numpy>=1.24
prophet>=1.1
scikit-learn>=1.3
scipy>=1.11
matplotlib>=3.7
seaborn>=0.12
openpyxl>=3.1
statsmodels>=0.14
jupyter>=1.0
```

### Run The Pipeline

Step 1: Data preprocessing + CCI + Scenario simulation

      jupyter notebook notebooks/Tourism_1.ipynb

Step 2: Hierarchical clustering

     jupyter notebook notebooks/Tourism_2.ipynb

Step 3: Prophet forecasting

    jupyter notebooks/growthforecast.ipynb
