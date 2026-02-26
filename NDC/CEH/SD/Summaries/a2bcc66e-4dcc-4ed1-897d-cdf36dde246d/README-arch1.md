# Satellite-derived geomorphic river mobility for ten catchments in the Philippines, 1988-2019

## Overview
- A dataset and code package examining river mobility in ten catchments in the Philippines over 1988–2019 using satellite-derived geomorphic signals.
- Aimed at enabling analysts to quantify spatial-temporal patterns, compute locational probabilities, and visualize mobility with GIS tools.

## Contents and how to use
- 01_Abulug_Example
  - Worked example for the Abulug catchment.
  - GEE code to generate binary active channel images.
  - MATLAB code to calculate per-pixel locational probabilities.
  - MATLAB code to calculate and plot along-valley locational probabilities using TopoToolbox 2.4.
- 02_Processed_Locational_Probabilities
  - Raster images of per-pixel locational probabilities for the analyzed catchments.
  - Designed for visualization in GIS to inspect spatial patterns of mobility.

## Data products and outputs
- Per-pixel locational probability rasters across the ten catchments.
- Along-valley probability analyses to characterize mobility along river corridors.
- Reproducible workflow snippets (GEE and MATLAB) enabling replication or adaptation to other regions.

## Reproducibility and accessibility
- Code assets include:
  - Google Earth Engine (GEE) scripts for binary active channel generation.
  - MATLAB scripts for per-pixel probability calculations and along-valley visualizations.
  - TopoToolbox 2.4 for along-valley probabilistic plotting.
- Raster probability maps compiled to support GIS-based analysis and further statistical work.

## Relevance for analysis and decision-making
- Provides a framework to quantify and compare river mobility across multiple catchments over a multi-decade period.
- Supports identifying correlations between geomorphic changes and environmental or anthropogenic factors.
- Facilitates reporting of findings through maps and probabilistic metrics suitable for informing planning and policy decisions.