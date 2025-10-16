# Project 2 – Real Estate Industry (Group 7, 2025)

***Team members***

Ee Wan Rong Amanda (1514578)
Ariq Asri (1450762)
Tasneem Zulaiqa (1393971)
Raja Abdul (1364850)

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
**more....**

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
[Download from DataVic](https://discover.data.vic.gov.au/dataset/vicmap-property)

---

### Facilities of Interest (FOI)
**Points of Interest Dataset**  
[Download from Data.gov.au](https://data.gov.au/data/dataset/2c79581f-600e-4560-80a8-98adb1922dfc/resource/33d822ba-138e-47ae-a15f-460279c3acc3)

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

