Urban Heat Mapping and Vegetation-Based Priority Assessment of Indore

Project Overview

This project investigates the spatial distribution of Land Surface Temperature (LST) and vegetation patterns across a selected study area in Indore, Madhya Pradesh, India.

Using Landsat 8 and Landsat 9 satellite imagery, Google Earth Engine, and Python-based geospatial analysis, the project identifies relative heat hotspots, examines the relationship between vegetation and surface temperature, and develops a preliminary heat-priority classification.

Study Period: April–May 2025
Study Area: Indore, Madhya Pradesh, India

Objectives

* Estimate Land Surface Temperature using Landsat satellite imagery.
* Analyse vegetation distribution using NDVI.
* Identify relative surface-temperature hotspots.
* Examine the statistical relationship between vegetation and temperature.
* Develop a temperature-and-vegetation-based priority map.

Technologies Used

* Google Earth Engine
* Python
* Google Colab
* Rasterio
* NumPy
* Pandas
* Matplotlib
* SciPy

Data Sources

* Landsat 8 Collection 2 Level-2
* Landsat 9 Collection 2 Level-2

Satellite imagery was processed for April and May 2025 using cloud and saturation masking and median compositing.

Methodology

1. Define the study area around central Indore.
2. Filter Landsat 8 and Landsat 9 imagery by location and date.
3. Apply quality masks and generate a median composite.
4. Calculate Land Surface Temperature in Celsius.
5. Calculate the Normalized Difference Vegetation Index (NDVI).
6. Identify relative heat hotspots using the 90th percentile of LST.
7. Calculate Pearson correlation between LST and NDVI.
8. Generate a three-class heat-priority map.

Key Findings

Metric	Result
Mean LST	44.44°C
Maximum LST	57.50°C
Mean NDVI	0.2638
LST–NDVI Pearson correlation	-0.1910
High-priority pixels	1.09%
Moderate-priority pixels	17.82%
Lower-priority pixels	81.09%

The results indicate a weak negative association between vegetation greenness and land surface temperature.

Heat-Priority Classification

* High Priority: Relatively high temperature and low vegetation.
* Moderate Priority: Either relatively high temperature or low vegetation.
* Lower Priority: Neither condition.

Project Outputs

The repository includes:

* Land Surface Temperature map.
* NDVI vegetation map.
* Urban heat-priority map.
* Python analysis notebook.
* Statistical summaries.
* Research report.

Limitations

* Land Surface Temperature is not equivalent to air temperature.
* The Landsat thermal product has a coarser native spatial resolution than the 30 m output grid.
* The study covers only April–May 2025.
* The circular study boundary is an analytical buffer, not the official municipal boundary.
* Population and socioeconomic vulnerability have not been incorporated.
* The priority classification is exploratory and is not a validated public-health risk index.
* Spatial autocorrelation may affect conventional statistical significance tests.

Future Scope

* Integrate population density and demographic vulnerability indicators.
* Incorporate land-use and land-cover classification.
* Extend the analysis across multiple years and seasons.
* Investigate spatial autocorrelation and more advanced statistical methods.
* Evaluate potential urban greening and heat-mitigation interventions.

Author

Developed as an independent geospatial and environmental data analysis project.
