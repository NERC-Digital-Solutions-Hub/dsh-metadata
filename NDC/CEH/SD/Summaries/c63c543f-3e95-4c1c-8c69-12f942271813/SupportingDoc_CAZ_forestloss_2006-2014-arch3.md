# Evaluating the Effectiveness of Conservation Investments in Reducing Deforestation and Fires in Ankeniheny-Zahemena Corridor, Madagascar

## Purpose and monitoring relevance
- Documents a methodological approach to generate and structure spatial data for assessing how conservation investments influence deforestation and fire dynamics.
- Focuses on producing comparable, area-based metrics (deforestation changes) across time and zones within the Ankeniheny-Zahemena Corridor.

## Data generation and sources
- Imagery and data sources:
  - Landsat 7 SLC-off imagery (15 m) used for change detection, with comparisons to Landsat 2005 imagery.
  - Change in Natural Forest Cover (1990–2005) framework developed by USAID, Conservation International, and Madagascar’s Ministry.
  - Imagery acquired from USGS Global Visualization Viewer (Glovis).
  - Landsat 7 composites preprocessed with ENVI 4.7; Landsat 8 preprocessed via Google Earth Engine.
- Temporal coverage:
  - Scene p158r73: 2006, 2007, 2008, 2009, 2010.
  - Scene p158r72: 2006, 2007, 2009, 2010.
- Observational approach:
  - Visual interpretation and manual digitization to identify further clearance.
  - Extra observation details recorded in the attribute table; criteria for clearance identification are expert-driven and subjective.
- Dataset scope:
  - 5954 polygons identified as clearings; about 75% of observed clearings are ≥ 1 hectare.
  - Minimum recorded area corresponds to ~5 image pixels.

## Attribute table and data structure
- Data format: shapefile.
- Eight key attribute columns:
  - scene (string): Landsat imagery used.
  - baseline (string): Baseline imagery used for comparison.
  - year (long): Year of observed change (e.g., 2006 for 2005–2006 change).
  - area_ha (double): Area in hectares of the clearing.
  - x_utm (long): UTM easting.
  - y_utm (long): UTM northing.
  - zone (string): Delineation within the protected area; zones include priority for conservation, sustainable use, and controlled settlements.
  - code (long): Unique identifier.

## Analytical methods
- Change detection through manual digitization of clearings based on visual interpretation.
- Recording detailed metadata for each observation to support verification and future review.
- Spatial data produced as 5954 polygon features with accompanying attribute data.

## Data management, sharing, and governance considerations
- Data are organized in a shapefile with clearly defined metadata fields (scene, baseline, year, area_ha, location, zone, code).
- Underlying observations are documented, enabling traceability for monitoring of conservation investments.
- The documentation emphasizes the need for data provenance and the ability to share data publicly, but specific governance mechanisms or sharing policies are not detailed within the document.

## Limitations and challenges (implications for monitoring)
- Subjectivity in clearance identification due to reliance on expert judgment.
- Dependence on image quality and preprocessing steps to discern true clearings from phenological changes.
- Spatial and temporal gaps inherent in the imagery and processing workflows (e.g., SLC-off gaps, 1–2 year gaps in some years).
- Metadata completeness and transformation requirements may pose barriers to reuse without careful provenance tracking.

## Citation
- Tabor, K., K. Jones, J. Hewson, A. Rasolohery, A. Rambeloson, T. Andrianjohaninarivo, and C. Harvey (submitted Nov 2016 PlosOne). Evaluating the Effectiveness of Conservation Investments in Reducing Deforestation and Fires in Ankeniheny-Zahemena Corridor, Madagascar.