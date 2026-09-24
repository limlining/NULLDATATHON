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
