# Digital elevation models (DEMs) of difference (DoD)

## Overview
- DoD rasters (raster format, .tif) quantify vertical (z) topographic change between two dates.
- Used in GIS for analysis or supporting other geospatial analyses; negatives indicate surface lowering (erosion), positives indicate surface gain (deposition).

## Purpose and applicability
- Created to support analysis of landscape change after the avalanche-debris flow on 7 February 2021 in Chamoli District, Uttarakhand, India.
- Also supports numerical modelling with CAESAR-Lisflood.

## Spatial and temporal coverage
- Spatial extent described by bounding box (WGS 84 / UTM Zone 44):
  - Top left: 352,312 m E, 3,385,209 m N
  - Lower right: 384,787 m E, 3,358,896 m N
- DoDs span periods defined by pairs of dates; raw DEMs were generated between 10 February 2021 and 27 April 2022 and DoDs were created on a rolling basis within this window.
- Coordinate system and area are consistent across the dataset.

## Data collection and processing
- DoDs created in QGIS (versions 3.18 and 3.24) using the Raster Calculator.
- For each DEM pair, the later DEM is subtracted from the earlier DEM:
  - Negative values = surface lowering (erosion)
  - Positive values = surface gain (deposition)

## Responsibility
- The project principal investigator (PI) created all DoDs and interpreted the results.

## Completeness and reproducibility
- The dataset contains all DoDs generated as part of this research.
- Other DoDs could be generated using additional input DEMs from this data collection; the method can be replicated to estimate significant change thresholds (described in section 5).

## Quality control and uncertainty
- Gaps/holes in input DEMs propagate into the DoDs (caused by photogrammetric reconstruction issues such as cloud cover, occlusion, or large view-angle offsets).
- Statistically significant change thresholds are defined per DoD using 16 stable hillside areas adjacent to the valley floor:
  - Thresholds are based on the standard deviation of DoD values within these stable areas, applying a two-sigma uncertainty.
  - DoD significance thresholds (uncertainties):
    - ±1.11 m for 2015-09 to 2021-02-10 DoD
    - ±0.91 m for 2021-02-10 to 2021-06-06 DoD
    - ±0.61 m for 2021-06-06 to 2021-12-25 DoD
    - ±1.14 m for 2021-02-10 to 2021-12-25 DoD
    - ±1.06 m for 2021-02-10 to 2022-01-27 DoD
- Stable area polygons used for threshold estimation are provided as part of the resource.

## Dataset contents and structure
- DoD raster files:
  - 1509_composite_210210_DoD.tif (Sept 2015 – Feb 2021)
  - 210210_210606_DoD.tif (Feb 2021 – Jun 2021)
  - 210606_211225_DoD.tif (Jun 2021 – Dec 2021)
  - 210210_211225_DoD.tif (Feb 2021 – Dec 2021)
  - 210210_220127_DoD.tif (Feb 2021 – Jan 2022)
- Stable areas:
  - stable_areas.shp (plus auxiliary files: .cpg, .dbf, .prf, .qmd, .shx)
- Naming convention:
  - File names reflect the dates spanning each DoD (YY-MM-DD); 1509 denotes September 2015 due to composite origin.

## Usage notes
- Values represent net elevation change between the two input DEMs; use the provided significance thresholds to identify statistically meaningful changes.
- Users can reproduce or explore additional DoDs and estimate corresponding significant-change thresholds using the methods described.