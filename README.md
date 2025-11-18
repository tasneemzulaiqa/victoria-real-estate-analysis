# Victoria Real Estate Pricing Analysis – Group Project 7, 2025

## Project Overview
This project analyzes the Victorian real estate market to identify affordable, liveable, and high-growth suburbs. By integrating demographic, income, crime, amenities, and property data, predictive models were built to generate actionable insights for urban planning and investment decisions.

> **Note:** This project was completed as part of a university group assignment for Applied Data Science (2025) at the University of Melbourne.
---

## My Contributions

- Preprocessed and cleaned rental property dataset (domain) for modeling.
- Obtained and processed population dataset; forecasted population data for use as features in rent prediction.
- Used OpenStreetMap and OpenRouteService to compute distances from properties to key amenities (supermarkets, train stations, CBD).
- Merged all datasets into a single integrated dataset ready for analysis and modeling.
- Developed property rent prediction models, including feature selection, parameter tuning, and implementation using Random Forest, XGBoost, and Linear Regression baselines.
- Combined property rent model outputs with historical SA2 growth model results to generate final predictions.
- Restructured and organized notebooks and repository to ensure clarity, reproducibility, and maintainable workflow.
- Reviewed and integrated teammates’ notebooks to ensure reproducibility and consistent workflows.

---

## Key Skills & Tools
- **Languages & Libraries:** Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Statsmodels, GeoPandas, Folium, RapidFuzz  
- **Techniques:** Data cleaning, feature engineering, regression modeling, geospatial analysis, data visualization  
- **Data Sources:** Victorian property datasets, ABS demographic data, crime statistics, points of interest (POI) datasets  

---

## Project Pipeline
1. **Data Cleaning & Preprocessing:** Standardized and structured raw datasets.  
2. **Data Integration:** Combined property, demographic, crime, and amenities data for modeling.  
3. **Modeling:** Developed predictive models for property rents and suburb growth forecasts.  
4. **Analysis & Visualization:** Created insights on affordability, liveability, and high-growth suburbs.  

---

## Highlights & Insights
- Identified key internal and external property features influencing rental prices.  
- Predicted top 10 suburbs with highest expected growth rates.  
- Produced interactive maps showing affordability and liveability rankings across Victoria.  

---

## Setup & Dependencies
Install dependencies using:

```bash
pip install -r requirements.txt
