# Satellite-derived geomorphic river mobility for ten catchments in the Philippines, 1988-2019

## Overview
- Provides codes and data for analyzing satellite-derived geomorphic river mobility across ten catchments in the Philippines from 1988 to 2019.
- Includes worked examples and processed data to support reproducibility and GIS visualization.

## Data and Methods
- 01_Abulug_Example
  - GEE code to generate binary active channel images.
  - MATLAB code to calculate per-pixel locational probabilities.
  - MATLAB code to calculate and plot along-valley locational probabilities using TopoToolbox 2.4.
- 02_Processed_Locational_Probabilities
  - Raster images of per-pixel locational probabilities for the analysed catchments (for visualization in GIS).

## Data Components
- 01_Abulug_Example: worked example with executable workflows (GEE and MATLAB scripts) for generating and analyzing active channel and locational probability metrics.
- 02_Processed_Locational_Probabilities: ready-to-use raster datasets of per-pixel locational probabilities across catchments.

## Accessibility and Reuse
- Provides complete code and processed datasets to support reproducibility of river mobility analyses.
- Facilitates replication, auditing, and GIS-based visualization of results.

## Reproducibility and Workflow
- End-to-end workflow linking satellite data processing (GEE) with per-pixel probability calculations (MATLAB) and along-valley analyses (TopoToolbox).
- Datasets are organized to enable straightforward reuse for the Abulug catchment and other catchments in the study.

## Considerations for Monitoring Frameworks
- Demonstrates a transparent, reproducible approach to measuring river mobility that can inform monitoring frameworks.
- Uses widely adopted tools (GEE, MATLAB, TopoToolbox) to standardize methodologies and support governance, data sharing, and visualization.
- The structure supports evaluating and communicating spatially explicit environmental health indicators to stakeholders.