# Project 2 – Real Estate Industry (Group 7, 2025)

***Team members***

- Ee Wan Rong Amanda (1514578)  
- Ariq Asri (1450762)  
- Tasneem Zulaiqa (1393971)  
- Raja Abdul (1364850)

***Research Goal***

Our primary research goal is to answer the following questions:

1. What are the Most important Internal and External Features?
2. What are the top 10 suburbs with the highest predicted growth rate?
3. Where are the most liveable and affordable suburbs?

# Setup

Python 3 dependencies: 
- **Pandas**
- **NumPy**
- **Seaborn**
- **Matplotlib (pyplot)**
- **Scikit-learn**
- **Statsmodels**
- **GeoPandas** 
- **Fiona** 
- **Shapely** 
- **Folium** 
- **RapidFuzz**
- **JSON**
- **Re (Regex)** 

A requirement.txt including all of the libraries used has been provided. Set up the environment by running:
```bash
pip install -r requirements.txt
```
## Datasets to Download:

### Population & Demographics
**VIC 2023 SA2 Population, Household, and Dwelling Projections (to 2036)**  
**Format:** `.xlsx`  
[Download from ABS](https://www.abs.gov.au/statistics/people/population/regional-population/2023-24/32180_ERP_2024_SA2_GDA2020.zip)

---

### Geospatial Boundaries
**SA2 Shapefile – Statistical Areas Level 2 (2021)**  
**Format:** Shapefile  
[Download from ABS](https://www.abs.gov.au/statistics/standards/australian-statistical-geography-standard-asgs-edition-3/jul2021-jun2026/access-and-downloads/digital-boundary-files)

**LGA Shapefile – Local Government Areas (2021)**  
**Format:** Shapefile  
[Download from ABS](https://www.abs.gov.au/statistics/standards/australian-statistical-geography-standard-asgs-edition-3/jul2021-jun2026/access-and-downloads/digital-boundary-files)

---

### Income Data
**Personal Income by Geography (2016–2021)**  
**Format:** `.xlsx`  
- [Table 3 (2016–2021)](https://www.abs.gov.au/statistics/labour/earnings-and-working-conditions/personal-income-australia/2020-21-financial-year/Table%203%20-%20Employee%20income%2C%20earners%20and%20summary%20statistics%20by%20geography%2C%202016-17%20to%202020-21.xlsx)  
- [Table 1 (2017–2022)](https://www.abs.gov.au/statistics/labour/earnings-and-working-conditions/personal-income-australia/2021-22/Table%201%20-%20Total%20income%2C%20earners%20and%20summary%20statistics%20by%20geography%2C%202017-18%20to%202021-22.xlsx)

---

### SA2 to LGA Mapping
**VicMap Property Dataset – for mapping SA2 to LGA**  
[Download from Data.gov.au](https://data.gov.au/data/dataset/2c79581f-600e-4560-80a8-98adb1922dfc/resource/33d822ba-138e-47ae-a15f-460279c3acc3)

---

### Facilities of Interest (FOI)
**Points of Interest Dataset**  
[Download from DataVic](https://discover.data.vic.gov.au/dataset/vicmap-property)

---

### Crime Statistics
**LGA Criminal Incidents (Year Ending June 2025)**  
**Format:** `.xlsx`, 16.79 MB  
[Download from Crime Statistics Victoria](https://www.crimestatistics.vic.gov.au/crime-statistics/latest-victorian-crime-data/download-data)

---

**LGA Victim Reports (Year Ending June 2025)**  
**Format:** `.xlsx`, 548.85 KB  
[Download from Crime Statistics Victoria](https://www.crimestatistics.vic.gov.au/crime-statistics/latest-victorian-crime-data/download-data)

---

### Historical Rental Prices
**File:** `Moving annual median rent by suburb and town – March Quarter 2025.xlsx`  
**Format:** `.xlsx`  
[Download from DFFH Victoria](https://www.dffh.vic.gov.au/publications/rental-report)

## Pipeline

Run all the Preprocessisng Notebooks in the order listed below, once the notebooks has been run. Proceed running the Modeling and Analysis Notebooks which will give the final answers to our questions

### Preprocessing Notebooks

- `demographics.ipynb` – map suburbs to SA2s  
- `crime.ipynb` – preprocessing and integration of crime dataset  
- `Data_preprocessing_domain1.ipynb` – initial property dataset extraction and cleaning  
- `Data_preprocessing_domain2.ipynb` – feature conversion, imputation, and outlier removal for Domain property dataset
- `Data_preprocessing_pop.ipynb` – processing population dataset  
- `Open_street.ipynb` – open street data download and handling  
- `Openroute.ipynb` – calculating travel distances using Open Route Services API  
- `calc_dist.ipynb` – distance calculations to schools, CBD, etc from a property in the domain dataset   
- `income_cleaning.ipynb` – cleaning, merging and structuring raw income dataset  
- `number_of_foi.ipynb` – calculating number of FOI (points of interest) within a certain distance to a property
- `future_erp_income_interpolate.ipynb` – interpolating future ERP and income data  
- `crime_handling.ipynb` – processing and standardizing crime-related data  
- `data_handling.ipynb` – merging and managing final datasets for model input for Historical Datasets

### Analysis Notebooks

- `data_analysis_pop.ipynb` – correlation between rent and population  
- `geospatial_analysis.ipynb` – spatial FOI point visualizations and suburb-level mapping  

### Modeling Notebooks

- `property_rent_model.ipynb` – models for top 10 features (e.g., Random Forest, XGBoost)  
- `process_time_series.ipynb` – time series forecasting of rental growth (SARIMAX)  
- `final_model.ipynb` – time series forecasting of rental growth (ARIMA/UCM)  
- `affordability.ipynb` – affordability map and ranking  
- `livability.ipynb` – liveability map and ranking

## Answers to Key Research Questions

### 1. **What are the Most Important Internal and External Factors?**
The results for this question can be found in:  
`Property_Rent_Model.ipynb`

### 2. **What are the Top 10 Suburbs with the Highest Predicted Growth Rate?**
The results for this question can be found in:  
`process_time_series.ipynb`

### 3. **Where are the Most Liveable and Affordable Suburbs?**
The results for this question can be found in:  
`afford.ipynb` and `livability.ipynb`
