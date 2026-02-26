# Evaluating the Effectiveness of Conservation Investments in Reducing Deforestation and Fires in Ankeniheny-Zahemena Corridor, Madagascar

## Overview
- Uses Landsat-derived data to evaluate conservation investments by identifying deforestation/clearance events and producing standardized outputs for monitoring environmental health and policy performance over time.
- Focuses on the Ankeniheny-Zahemena Corridor in Madagascar, comparing imagery and a Change in Natural Forest Cover dataset to track changes from 2005 onwards.

## Data Generation Methods
- Data sources:
  - Landsat 7 SLC-off imagery (15 m) compared with Landsat 2005 imagery and the Change in Natural Forest Cover dataset (USAID, Conservation International, Madagascar’s Ministry of Environment, Water, Forests and Tourism).
  - Imagery coverage for map sheets p158r73 (2006–2010) and p158r72 (2006, 2007, 2009, 2010).
- Preprocessing:
  - Landsat 7 imagery preprocessed with ENVI 4.7 to create gap-free composites.
  - Landsat 8 imagery preprocessed via Google Earth Engine.

## Attribute Table Definition
- Scene, Description: Landsat imagery used; date (underscore).
- Scene, Type: string.
- Baseline, Description: Imagery used for comparison.
- Baseline, Type: string.
- Year, Description: Year of change (e.g., 2006 = change between 2005-2006).
- Year, Type: long.
- Area_ha: Area in hectares.
- X_utm: UTM Easting (long).
- Y_utm: UTM Northing (long).
- Zone: Delineation within protected areas (types: priority for conservation, sustainable use, controlled settlements).
- Code: Unique identifier (long).

## Analytical Methods
- Observed clearance areas identified via visual interpretation and manually digitized using Esri software.
- Additional attributes recorded in the attribute table.
- Clearance criteria were subjective, based on expert experience.
- Distinguishing true clearings vs natural phenology changes using shape, color, texture, and proximity to other clearings/settlements.
- Result: 5,954 polygons; about 75% of observed clearings are ≥ 1 ha; minimum area around 5 pixels.

## Data Structure
- Format: Shapefile.
- Attribute table contains 8 columns: scene, baseline, year, area_ha, x_utm, y_utm, zone, and code.

## Data Quality and Reproducibility
- Relies on expert interpretation for identifying clearings, indicating potential subjectivity.
- Documentation of preprocessing steps and attribute definitions supports reproducibility and data integration.

## Usage and Purpose for Monitoring
- Provides a standardized, geo-referenced dataset to monitor changes in forest cover and deforestation/clearance in the corridor.
- Enables assessment of the effectiveness of conservation investments in reducing deforestation and fires.

## Citation
- Tabor, K., K. Jones, J. Hewson, A. Rasolohery, A. Rambeloson, T. Andrianjohaninarivo, and C. Harvey (submitted Nov 2016). Evaluating the Effectiveness of Conservation Investments in Reducing Deforestation and Fires in Ankeniheny-Zahemena Corridor, Madagascar.