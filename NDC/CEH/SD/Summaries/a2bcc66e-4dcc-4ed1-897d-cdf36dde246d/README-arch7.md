# Codes and data associated with "Satellite-derived geomorphic river mobility for ten catchments in the Philippines, 1988-2019."

## Overview
- Provides codes and data linked to the study on satellite-derived geomorphic river mobility across ten Philippine catchments (1988–2019).
- Includes a worked example for the Abulug catchment with:
  - GEE code to generate binary active channel images
  - MATLAB code to calculate per-pixel locational probabilities
  - MATLAB code to calculate and plot along-valley locational probabilities using TopoToolbox 2.4
- Supplies raster images of per-pixel locational probabilities for the analyzed catchments to visualize in GIS.

## What’s Included
- 01_Abulug_Example
  - 01 - GEE code to generate binary active channel images
  - 02 - MATLAB code to calculate per-pixel locational probabilities
  - 03 - MATLAB code to calculate and plot along-valley locational probabilities (TopoToolbox 2.4)
- 02_Processed_Locational_Probabilities
  - Raster images of per-pixel locational probabilities for the catchments analyzed (for GIS visualization)

## GIS and Data Utilization
- Produces GIS-ready raster outputs to map spatial probability of river mobility.
- Enables reproducibility of analyses via embedded code (GEE and MATLAB).

## How to Use
- Run GEE script in 01_Abulug_Example to generate binary active channel images.
- Execute MATLAB scripts to compute:
  - Per-pixel locational probabilities
  - Along-valley locational probabilities (with TopoToolbox 2.4)
- Load the processed locational probability rasters into GIS for visualization and analysis.