# Satellite-derived geomorphic river mobility for ten catchments in the Philippines, 1988-2019

## Overview
- Documentation of codes and data associated with the study of satellite-derived geomorphic river mobility across ten catchments in the Philippines (1988–2019).
- Includes a worked example for the Abulug catchment and processed outputs to support visualization and analysis.

## Data and Code Included
- 01_Abulug_Example
  - GEE code to generate binary active channel images.
  - MATLAB code to calculate per-pixel locational probabilities.
  - MATLAB code to calculate and plot along-valley locational probabilities using TopoToolbox 2.4.
- 02_Processed_Locational_Probabilities
  - Raster images of per-pixel locational probabilities for the analysed catchments, designed for GIS visualization.

## Purpose and Use for Analysts Monitoring the Environment
- Provides standardized workflows to monitor river mobility over time (1988–2019) using satellite-derived metrics.
- Supports verification, quality assurance, cleaning, transformation, and analysis to produce outputs such as probability maps and active-channel classifications.
- Delivers GIS-ready and portal-uploadable datasets to enable consistent environmental monitoring and policy scrutiny.

## Methods and Outputs
- Tools: Google Earth Engine (GEE), MATLAB, TopoToolbox 2.4.
- Outputs:
  - Binary active channel images for each catchment.
  - Per-pixel locational probability rasters.
  - Along-valley locational probability plots.
  - Processed probability rasters suitable for GIS and further analysis.

## Data Accessibility and Reuse
- Structured to allow others to reproduce analyses and access underlying data behind final outputs, promoting transparency and reuse.

## Challenges and Opportunities for Analysts
- Increase the value of monitoring datasets by integrating with additional relevant data (beyond single-use applications).
- Improve accessibility of underlying data used to produce final outputs, ensuring datasets are stored and uploaded to the appropriate data portals.