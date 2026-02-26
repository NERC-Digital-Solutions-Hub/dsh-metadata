# Codes and data associated with "Satellite-derived geomorphic river mobility for ten catchments in the Philippines, 1988-2019."

## Overview
- A data and code package accompanying a study on satellite-derived geomorphic river mobility across ten catchments in the Philippines (1988–2019).
- Provides executable tools and processed data to reproduce and extend analyses.

## Data assets and contents
- 01_Abulug_Example
  - GEE code to generate binary active channel images.
  - MATLAB code to calculate per-pixel locational probabilities.
  - MATLAB code to calculate and plot along-valley locational probabilities using TopoToolbox 2.4.
- 02_Processed_Locational_Probabilities
  - Raster images of per-pixel locational probabilities for the analyzed catchments, intended for GIS visualization.

## Purpose and value
- Enables reproducibility of the river-mobility analysis by delivering both the processing scripts and the resulting probability rasters.
- Provides practical data products (per-pixel and along-valley probabilities) that support GIS-based interpretation and further research.

## Tools, formats, and accessibility
- Software/tools referenced: Google Earth Engine (GEE), MATLAB, TopoToolbox 2.4.
- Data formats include executable code (GEE and MATLAB) and raster probability images suitable for GIS work.

## Data governance and reuse considerations
- Clear folder structure and naming support discoverability and reuse.
- Facilitates extension to additional catchments or different timeframes by reusing the provided code and rasters.
- Metadata details are not described here; users should verify provenance and provide appropriate documentation when reusing.

## Implications for data leadership
- Demonstrates a end-to-end data workflow: from code-based analysis to ready-to-use spatial data products.
- Highlights the importance of providing both analytical tooling and resulting data outputs to enable co-ownership, collaboration, and broader application in policy or planning contexts.