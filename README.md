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
- [Download from ABS](https://www.abs.gov.au/statistics/people/population/regional-population/2023-24/32180_ERP_2024_SA2_GDA2020.zip)
- [VIF2023_SA2_Pop_Hhold_Dwelling_Projections_to_2036_Release_2.xlsx
xlsx
1.7 MB](https://www.planning.vic.gov.au/__data/assets/excel_doc/0028/691660/VIF2023_SA2_Pop_Hhold_Dwelling_Projections_to_2036_Release_2.xlsx)

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

Run all the Preprocessing Notebooks in the order listed below, once the notebooks has been run. Proceed running the Integration, Analysis and Modeling Notebooks which will give the final answers to our questions.

### Data Preprocessing Notebooks

- `01_population_preprocessing.ipynb` – Processing population dataset  
- `02_income_preprocessing.ipynb` – Cleaning, merging and structuring raw income dataset  
- `03_lga_sa2_mapping.ipynb` – Map suburbs to SA2s  
- `04_amenities_preprocessing.ipynb` – Clean and categorize Features of Interest (FOI) points
- `05_crime_preprocessing.ipynb` – Processing and standardizing crime-related data  
- `06_domain_preprocessing.ipynb` – Property dataset extraction and cleaning  
- `07_median_data_prepocessing.ipynb` – Clean and merge rental property spreadsheets
- `08_school_healthcare_cbd.ipynb` – Distance calculations to schools, CBD, etc from a property in the domain dataset   
- `09_supermarket_train_cbd.ipynb` – Compute proximity of properties to key amenities and Melbourne CBD

### Data Integration Notebooks
- `domain_data_integration.ipynb` – Merge and enrich the Domain property dataset
- `historical_data_integration.ipynb` - Merging and managing final datasets for model input for Historical dataset

### Data Analysis Notebooks

- `affordability.ipynb` – Affordability map and ranking  
- `foi_points.ipynb` – Visualize spatial distribution of Features of Interest
- `livability.ipynb` – Liveability map and ranking
- `vic_rent_trends.ipynb` – Analyse historical trends in median weekly rents in Victoria (VIC) from 2020 onward

### Modeling Notebooks

- `forecasting_combined.ipynb` – Project property-level rents to 2030
- `property_rent_model.ipynb` – Train property-level rent prediction models 
- `sa2_growth_model.ipynb` – Forecast quarterly median rents at SA2-level  

## Answers to Key Research Questions

### 1\. **What are the Most Important Internal and External Factors?**
The results for this question can be found in:  
`property_rent_model.ipynb`

### 2\. **What are the Top 10 Suburbs with the Highest Predicted Growth Rate?**
The results for this question can be found in:  
`sa2_growth_model.ipynb`

### 3\. **Where are the Most Liveable and Affordable Suburbs?**
The results for this question can be found in:  
`affordability.ipynb` and `livability.ipynb`

To obtain a conclusive summary and analysis of our research methodology and findings, run the notebook `summary.ipynb`. 
