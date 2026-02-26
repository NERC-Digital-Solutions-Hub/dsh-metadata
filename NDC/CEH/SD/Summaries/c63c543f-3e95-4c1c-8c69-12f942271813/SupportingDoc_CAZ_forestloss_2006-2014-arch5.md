# Evaluating the Effectiveness of Conservation Investments in Reducing Deforestation and Fires in Ankeniheny-Zahemena Corridor, Madagascar

## Overview
- Spatial dataset documenting observed forest clearances within the Ankeniheny-Zahemena Corridor (AZEC), Madagascar, used to evaluate conservation investments.
- Integrates Landsat imagery analysis from different periods (1990–2005 Change in Natural Forest Cover; and 2006–2010 imagery) to identify deforestation-related changes.
- Generated as a shapefile comprising 5,954 polygons of observed clearances, with 75% of clearings being at least 1 hectare.

## Data sources and timeline
- Imagery sources:
  - Landsat 7 SLC-off imagery at 15 m resolution (gap-filled composites) for p158r73 and p158r72 scenes.
  - Landsat 5/2005 baseline imagery used for comparison (Change in Natural Forest Cover, 1990–2005).
  - Landsat 8 imagery preprocessed via Google Earth Engine.
- Data provenance:
  - Imagery obtained from the USGS Global Visualization Viewer (Glovis).
  - Preprocessing steps to address SLC-off gaps and create gap-free composites.

## Data preprocessing and attribute schema
- Preprocessing:
  - Landsat 7 images processed with ENVI 4.7 to produce gap-free composites.
  - Landsat 8 images preprocessed through Google Earth Engine.
- Attribute table schema (8 relevant fields; described in detail below):
  - Scene: Landsat imagery used; followed by date (string).
  - Baseline: Landsat imagery used for comparison; string.
  - Year: Year of change (long/integer).
  - Area_ha: Area of the clearance in hectares (double).
  - X_utm: UTM Easting (long).
  - Y_utm: UTM Northing (long).
  - Zone: Delineation within protected area; categories include priority for conservation, sustainable use, and controlled settlements (string).
  - Code: Unique identifier (long).

## Analytical methods
- Detection approach:
  - Observed further clearances identified through visual interpretation and manual digitization using Esri software.
  - Based on expert judgment; criteria include shape, color, texture, and proximity to other clearings/settlements to distinguish true clearings from phenological or natural changes.
- Output:
  - 5,954 polygons depicting observed clearances.
  - Area distribution: 75% of clearings are ≥ 1 hectare.
  - Minimum area represented by approximately 5 pixels.

## Data structure and contents
- Format: Shapefile.
- Attribute table contains 8 key columns: scene, baseline, year, area_ha, x_utm, y_utm, zone, and code (with descriptive metadata for each field as noted above).

## Provenance and citation
- Primary study: Tabor, K., Jones, K., Hewson, J., Rasolohery, A., Rambeloson, A., Andrianjohaninarivo, T., and Harvey, C. (submitted Nov 2016). Evaluating the Effectiveness of Conservation Investments in Reducing Deforestation and Fires in Ankeniheny-Zahemena Corridor, Madagascar.

## Data quality, limitations, and governance
- Limitations:
  - Subjective, expert-judgment-based identification of clearances; potential for bias and inconsistency.
  - Use of historical Landsat data with SLC-off gaps addressed by gap-free composites, which may influence interpretation.
  - Observations derived from visual interpretation; not automatically detected.
- Governance and metadata considerations for Data Stewards:
  - Ensure clear documentation of preprocessing steps (ENVI gap-filling, GEE processing for Landsat 8) and data sources.
  - Preserve provenance details (scene identifiers, baselines, years) to support reproducibility.
  - Maintain the coordinate reference system (UTM) and zone information within the Zone field to support future integration with other datasets.
  - Capture limitations in metadata (subjectivity of delineation, data gaps) to inform data users.
  - Provide access to the dataset with accompanying methodology and citation to enable reuse for evaluating conservation outcomes.