# Evaluating the Effectiveness of Conservation Investments in Reducing Deforestation and Fires in Ankeniheny-Zahemena Corridor, Madagascar

## Overview
- Describes data generation, metadata schema, analytical approach, and data structure used to assess deforestation and fire reduction in Madagascar.
- Integrates satellite imagery from Landsat 7 and Landsat 8 with collaborative data products from USAID, Conservation International, and Madagascar’s Ministry of Environment, Water, Forests and Tourism.
- Provides a reproducible workflow and a defined attribute schema to support transparency and re-use by data teams and partners.

## Data Generation Methods
- Comparison of Landsat 7 SLC-off imagery (15 m resolution) with Landsat 2005 imagery and the Change in Natural Forest Cover (1990–2005) product.
- Imagery sources:
  - Landsat data acquired from USGS Global Visualization Viewer (Glovis).
  - Years covered: p158r73 (2006, 2007, 2008, 2009, 2010) and p158r72 (2006, 2007, 2009, 2010).
- Preprocessing:
  - Landsat 7 data: gap-free composites generated using ENVI 4.7.
  - Landsat 8 data: preprocessed via Google Earth Engine.

## Attribute Table Definition
- Scene: Landsat imagery used; represented with date in the description.
- Baseline: Landsat imagery used for comparison.
- Year: Year of change (e.g., 2006 = change between 2005–2006).
- Area_ha: Area in hectares.
- X_utm / Y_utm: UTM coordinates (zone-specific).
- Zone: Classification within protected area (priority for conservation, sustainable use, controlled settlements).
- Code: Unique identifier.
- Data types: Scene (string), Baseline (string), Year (long), Area_ha (double), X_utm (long), Y_utm (long), Zone (string), Code (long).

## Analytical Methods
- Manual, visual interpretation and digitization of observed clearance using Esri software.
- Each observation enriched with attributes in the table; criteria for clearance identification relied on expert judgment.
- Distinguishing true clearings from phenological changes using shape, color, texture, and proximity to settlements.
- Outcome: 5,954 polygons identified; about 75% of observed clearings were ≥ 1 hectare; minimum recorded area ~ five pixels.

## Data Structure
- Format: Shapefile.
- Attribute table contains 8 relevant columns: scene, baseline, year, area_ha, x_utm, y_utm, zone, code.

## Data Provenance, Access, and Reuse
- Data generated through collaboration among USGS, USAID, Conservation International, and Madagascar’s government, enabling cross-organisational data sharing.
- Provenance indicates an integrated workflow from satellite acquisition to manual delineation and metadata-rich polygon features.
- Citation provided for traceability and academic reuse:
  Tabor, K., K. Jones, J. Hewson, A. Rasolohery, A. Rambeloson, T. Andrianjohaninarivo, and C. Harvey (submitted Nov 2016) Evaluating the Effectiveness of Conservation Investments in Reducing Deforestation and Fires in Ankeniheny-Zahemena Corridor, Madagascar.

## Data Quality and Limitations
- Subjectivity in clearance identification due to reliance on expert interpretation.
- Potential misclassification with phenology changes despite using multiple criteria.
- Dependence on 15 m Landsat resolution and SLC-off era data may influence detection sensitivity.
- Data gaps and alignment depend on preprocessing steps (ENVI for Landsat 7, Google Earth Engine for Landsat 8).