# Urban Heat Mapping and Vegetation-Based Priority Assessment of Indore

## Project Overview

This project investigates the spatial distribution of **Land Surface Temperature (LST)** and vegetation patterns across a selected study area in **Indore, Madhya Pradesh, India**.

Using **Landsat 8**, **Landsat 9**, **Google Earth Engine**, and **Python-based geospatial analysis**, the project identifies relative heat hotspots, examines the relationship between vegetation and surface temperature, and develops a preliminary heat-priority classification.

As an extension, the project incorporates a **management engineering and resource-allocation framework** that translates spatial heat priorities into illustrative urban heat-mitigation investment scenarios.

**Study Period:** April-May 2025  
**Study Area:** Indore, Madhya Pradesh, India

---

## Objectives

- Estimate Land Surface Temperature (LST) using Landsat satellite imagery.
- Analyze vegetation distribution using NDVI.
- Identify relative surface-temperature hotspots.
- Examine the statistical relationship between vegetation and temperature.
- Develop a temperature-and-vegetation-based priority map.
- Explore budget-based urban heat-mitigation planning scenarios.

---

## Technologies Used

- Google Earth Engine (GEE)
- Python
- Google Colab
- Rasterio
- NumPy
- Pandas
- Matplotlib
- SciPy

---

## Data Sources

- Landsat 8 Collection 2 Level-2
- Landsat 9 Collection 2 Level-2

Satellite imagery was processed for **April-May 2025** using cloud masking, radiometric saturation masking, and median compositing.

---

## Methodology

1. Define the study area around central Indore.
2. Filter Landsat 8 and Landsat 9 imagery by location and date.
3. Apply cloud and quality masks.
4. Generate a median composite image.
5. Calculate Land Surface Temperature (°C).
6. Calculate Normalized Difference Vegetation Index (NDVI).
7. Identify relative heat hotspots using the 90th percentile of LST.
8. Calculate Pearson correlation between LST and NDVI.
9. Generate a three-class heat-priority map.
10. Aggregate results into planning zones for intervention prioritization.
11. Develop illustrative resource-allocation scenarios under a fixed budget.

---

## Spectral Bands Used

| Band | Purpose |
|--------|---------|
| ST_B10 | Land Surface Temperature |
| SR_B4 | Red Reflectance |
| SR_B5 | Near-Infrared Reflectance |
| QA_PIXEL | Cloud and Atmospheric-Quality Masking |
| QA_RADSAT | Radiometric Saturation Masking |

---

## Land Surface Temperature Statistics

| Metric | Result |
|----------|----------|
| Mean LST | 44.44°C |
| Median LST | 44.26°C |
| Minimum LST | 27.96°C |
| Maximum LST | 57.50°C |
| 10th Percentile | 40.69°C |
| 90th Percentile | 48.63°C |
| Valid Paired Pixels | 845,072 |

---

## NDVI Statistics

| Metric | Result |
|----------|----------|
| Mean NDVI | 0.2638 |
| Median NDVI | 0.2434 |
| Minimum NDVI | -0.2194 |
| Maximum NDVI | 0.7802 |

---

## Heat-Priority Classification

### Classification Rules

| Class | Classification Rule |
|---------|---------------------|
| High Priority | Both high temperature and low vegetation |
| Moderate Priority | Either high temperature or low vegetation |
| Lower Priority | Neither condition |

### Priority-Class Distribution

| Priority Class | Pixel Count | Percentage |
|----------------|------------:|-----------:|
| High Priority | 9,234 | 1.09% |
| Moderate Priority | 150,580 | 17.82% |
| Lower Priority | 685,258 | 81.09% |
| **Total** | **845,072** | **100%** |

---

## Key Findings

| Metric | Result |
|----------|----------|
| Mean LST | 44.44°C |
| Maximum LST | 57.50°C |
| Mean NDVI | 0.2638 |
| LST-NDVI Pearson Correlation | -0.1910 |
| High-Priority Pixels | 1.09% |
| Moderate-Priority Pixels | 17.82% |
| Lower-Priority Pixels | 81.09% |

### Interpretation

The results indicate a **weak negative relationship** between vegetation greenness and land surface temperature. Areas with lower vegetation cover generally exhibit higher surface temperatures, although vegetation alone does not explain all observed temperature variation.

---

# Management Engineering Extension: Investment Planning and Resource Allocation

To extend the geospatial analysis into a management decision-support application, the project incorporates a preliminary resource-allocation framework for urban heat mitigation.

The analysis uses **791 planning zones** and identifies the **20 highest-priority zones** based on the temperature-and-vegetation priority assessment.

## Planning Approach

The framework translates spatial priority scores into illustrative intervention allocations across three categories:

- **Urban tree plantation** to increase vegetation cover.
- **Pocket green spaces** to create localized cooling zones.
- **Cool-roof interventions** to reduce heat absorption from built surfaces.

### Illustrative Intervention Costs

| Intervention | Assumed Unit Cost |
|--------------|------------------:|
| Urban Tree Plantation | ₹2,500 per tree |
| Pocket Green Space | ₹1,50,000 per 100 m² |
| Cool-Roof Treatment | ₹80,000 per 100 m² |

---

## ₹1 Crore Budget Allocation Scenarios

Three alternative investment strategies were evaluated under an illustrative budget of **₹1 crore**.

| Intervention | Balanced | Vegetation-Led | Built-Environment-Led |
|-------------|---------:|--------------:|---------------------:|
| Trees | 1,600 | 2,000 | 800 |
| Green-Space Units (100 m²) | 20 | 23 | 13 |
| Cool-Roof Units (100 m²) | 37 | 18 | 75 |
| Total Expenditure | ₹99.60 lakh | ₹98.90 lakh | ₹99.50 lakh |
| Remaining Budget | ₹40,000 | ₹1,10,000 | ₹50,000 |

### Management Insights

- The **Balanced Scenario** distributes investments across vegetation and built-environment interventions.
- The **Vegetation-Led Scenario** prioritizes tree plantation and green-space development.
- The **Built-Environment-Led Scenario** allocates a larger share of resources to cool-roof interventions.
- Priority-score-based allocation offers a preliminary framework for directing investments toward the areas identified by the spatial analysis as most vulnerable to urban heat.

> **Important:** These scenarios are illustrative planning exercises. Unit costs are assumed values rather than verified local market quotations. The proposed allocations do not represent confirmed implementation locations or measured cooling outcomes. Field validation, feasibility assessment, and stakeholder consultation would be required before implementation.

---

## Results and References

### Maps and Visualizations

| Output | Description |
|----------|-------------|
| LST Map | Spatial distribution of Land Surface Temperature |
| NDVI Map | Vegetation greenness distribution |
| Heat-Priority Map | Priority classification based on temperature and vegetation |
| Hotspot Map | Areas exceeding the 90th-percentile temperature threshold |
| LST Histogram | Distribution of land surface temperature values |
| NDVI Histogram | Distribution of NDVI values |
| LST-NDVI Scatter Plot | Relationship between vegetation and temperature |

### Reports and Documentation

| Document | Description |
|----------|-------------|
| Research Report | Detailed methodology, results, discussion, and conclusions |
| Statistical Summary | Summary statistics and correlation analysis |
| Python Notebook | Complete analysis workflow and code implementation |

### Data Sources

- Landsat 8 Collection 2 Level-2
- Landsat 9 Collection 2 Level-2
- Google Earth Engine Data Catalog
- United States Geological Survey (USGS) Landsat Program

### References

1. Google Earth Engine Documentation  
   https://developers.google.com/earth-engine

2. USGS Landsat Program Documentation  
   https://www.usgs.gov/landsat-missions

3. Landsat Collection 2 Surface Temperature Product Guide

4. Tucker, C.J. (1979). *Red and Photographic Infrared Linear Combinations for Monitoring Vegetation*. Remote Sensing of Environment.

---

## Project Outputs

The repository includes:

- Land Surface Temperature (LST) Map
- NDVI Vegetation Map
- Urban Heat-Priority Map
- Hotspot Analysis Outputs
- Python Analysis Notebook
- Statistical Summaries
- Research Report
- Budget Allocation and Planning Framework

---

## Repository Structure

```text
Indore-Urban-Heat-Mapping/
│
├── data/
│   ├── lst_indore.tif
│   ├── ndvi_indore.tif
│   └── priority_map.tif
│
├── figures/
│   ├── lst_map.png
│   ├── ndvi_map.png
│   ├── heat_priority_map.png
│   ├── hotspot_map.png
│   ├── lst_histogram.png
│   ├── ndvi_histogram.png
│   └── lst_ndvi_scatter.png
│
├── notebooks/
│   └── urban_heat_analysis.ipynb
│
├── reports/
│   ├── research_report.pdf
│   └── statistical_summary.pdf
│
└── README.md
```

---

## Limitations

- Land Surface Temperature (LST) is not equivalent to air temperature.
- The Landsat thermal product has a coarser native spatial resolution than the 30 m output grid.
- The study covers only April-May 2025.
- The circular study boundary is an analytical buffer and not the official municipal boundary.
- Population and socioeconomic vulnerability indicators were not incorporated.
- The priority classification is exploratory and not a validated public-health risk index.
- Spatial autocorrelation may influence conventional statistical significance tests.
- Cost assumptions used in the planning scenarios have not been validated through procurement or engineering studies.

---

## Future Scope

- Integrate population density and demographic vulnerability indicators.
- Incorporate land-use and land-cover (LULC) classification.
- Extend the analysis across multiple years and seasons.
- Investigate spatial autocorrelation and advanced statistical methods.
- Evaluate potential urban-greening and heat-mitigation interventions.
- Incorporate cost-benefit analysis and optimization models for intervention planning.
- Integrate field observations and measured cooling outcomes.

---

## Author

Developed as an independent geospatial, environmental analytics, and management engineering project.

---

## License

This project is intended for educational, research, and portfolio purposes. Users are encouraged to verify results independently before applying findings to planning, investment, or policy decisions.


This version reads like a professional GitHub portfolio project and clearly highlights both the remote sensing analysis and the management engineering/resource allocation component, which makes it stronger for recruiters and academic reviewers.
