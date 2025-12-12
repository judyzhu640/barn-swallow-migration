# Barn Swallow Migration Patterns in Northeast China (2023)

This project visualizes the seasonal migration patterns of barn swallows (*Hirundo rustica*) across Northeast China using weekly relative abundance data from eBird.

By aggregating weekly raster data into monthly averages and mapping them spatially, the project illustrates how barn swallow presence shifts throughout the year, highlighting migration timing, routes, and seasonal concentration.

---

## Data Source

- **Dataset:** eBird Status and Trends – Relative Abundance
- **Species:** Barn Swallow (*Hirundo rustica*)
- **Year:** 2023
- **Temporal resolution:** Weekly (52 weeks)
- **Data format:** GeoTIFF (.tif)
- **Source:** Cornell Lab of Ornithology, eBird  
  https://science.ebird.org/en/status-and-trends

The relative abundance values represent modeled estimates of the expected number of individuals detected per checklist, rather than raw counts.

---

## Methodology

### 1. Data Preparation (R)

- Downloaded 52 weekly GeoTIFF files for barn swallow relative abundance in 2023.
- Used **R** to:
  - Read and stack weekly raster files
  - Extract temporal metadata
  - Aggregate weekly rasters into **monthly mean relative abundance** layers
- Monthly averages were calculated to reduce short-term noise and highlight seasonal movement patterns.

### 2. Spatial Mapping (QGIS)

- Imported monthly averaged raster layers into **QGIS**.
- Ensured consistent coordinate reference systems (CRS) across all layers.
- Applied a uniform color scale to allow month-to-month comparison.
- Exported each monthly map as a **PNG** image.

### 3. Visualization

- Combined monthly PNG maps into an **animated GIF**.
- The animation shows:
  - Spring arrival
  - Summer breeding distribution
  - Autumn migration
  - Winter absence or low abundance

This visualization helps illustrate the spatial and temporal dynamics of barn swallow migration across Northeast China.

---

## Outputs

- Monthly raster maps (PNG)
- Animated GIF showing 2023 migration patterns
- R scripts for data processing
- QGIS project files for map styling and export

---

## Tools Used

- **R** (raster processing and aggregation)
- **QGIS** (spatial visualization)
- **eBird Status & Trends data**
- Image tools for GIF creation

---

## Limitations

- Relative abundance is a modeled estimate and depends on observer effort and environmental covariates.
- Monthly averaging smooths variability and may obscure short-term migration events.
- Results should be interpreted as broad migration patterns rather than precise population counts.

---

## Author

Ziyue Zhu  
Data journalism project
