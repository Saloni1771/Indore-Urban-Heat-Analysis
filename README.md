# Urban Heat Mapping and Vegetation-Based Priority Assessment of Indore

## Project Overview

This project investigates the spatial distribution of **Land Surface Temperature (LST)** and vegetation patterns across a selected study area in **Indore, Madhya Pradesh, India**.

Using **Landsat 8**, **Landsat 9**, **Google Earth Engine**, and **Python-based geospatial analysis**, the project identifies relative heat hotspots, examines the relationship between vegetation and surface temperature, and develops a preliminary heat-priority classification.

**Study Period:** April-May 2025  
**Study Area:** Indore, Madhya Pradesh, India

---

## Objectives

- Estimate Land Surface Temperature (LST) using Landsat satellite imagery.
- Analyze vegetation distribution using NDVI.
- Identify relative surface-temperature hotspots.
- Examine the statistical relationship between vegetation and temperature.
- Develop a temperature-and-vegetation-based priority map.

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

The results indicate a **weak negative relationship** between vegetation greenness and land surface temperature. Areas with lower vegetation cover generally exhibit higher surface temperatures, though the relationship is not strong enough to explain all temperature variation across the study area.

---

## Project Outputs

The repository includes:

- Land Surface Temperature (LST) map
- NDVI vegetation map
- Urban heat-priority map
- Python analysis notebook
- Statistical summaries
- Research report

---

## Limitations

- Land Surface Temperature (LST) is not equivalent to air temperature.
- The Landsat thermal product has a coarser native spatial resolution than the 30 m output grid.
- The study covers only April-May 2025.
- The circular study boundary is an analytical buffer and not the official municipal boundary.
- Population and socioeconomic vulnerability indicators were not incorporated.
- The priority classification is exploratory and not a validated public-health risk index.
- Spatial autocorrelation may influence conventional statistical significance tests.

---

## Future Scope

- Integrate population density and demographic vulnerability indicators.
- Incorporate land-use and land-cover (LULC) classification.
- Extend the analysis across multiple years and seasons.
- Investigate spatial autocorrelation and advanced statistical methods.
- Evaluate potential urban-greening and heat-mitigation interventions.

---

## Author

Developed as an independent geospatial and environmental data analysis project.

---

## License

This project is intended for educational, research, and portfolio purposes. Users are encouraged to verify results independently before applying findings to planning or policy decisions.


This format is GitHub-ready and follows a professional README structure suitable for a portfolio, academic project, or public repository.
