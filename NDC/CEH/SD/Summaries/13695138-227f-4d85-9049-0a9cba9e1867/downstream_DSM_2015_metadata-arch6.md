# Digital Surface Models for the South Saskatchewan River, Canada

## Overview
- Dataset comprising Digital Surface Models (DSM) for two sections of the South Saskatchewan River near Outlook, Canada.
- Temporal coverage across four dates: 13 May 2015; 2 Sept 2016; 8 Jun 2017; 12 Jun 2017.
- Eight DSMs in total (two river sections x four dates) stored as separate files.
- Purpose: to provide information on river morphology and changes over time due to erosion and sediment deposition.

## Data files
- downstream_DSM_2015.txt
- downstream_DSM_2016.txt
- downstream_DSM_2017a.txt
- downstream_DSM_2017b.txt
- upstream_DSM_2015.txt
- upstream_DSM_2016.txt
- upstream_DSM_2017a.txt
- upstream_DSM_2017b.txt

## Data content and structure
- Each file contains three columns:
  - Column 1: UTM Easting (m)
  - Column 2: UTM Northing (m)
  - Column 3: UTM Elevation (m)
- Coordinate reference system: UTM Zone 13N (EPSG:32613).
- Study area coordinates (reference): UTM13N Easting 356500, Northing 5712400; Latitude/Longitude ~ 51.5 N, 107.07 W.

## Data collection and processing
- Source imagery: photogrammetric quality aerial photographs captured at ~1500 m altitude using a fixed-wing aircraft with an UltraCamXp sensor; ground resolution 0.06 m.
- Processing workflow (three stages):
  1) Orthomosaic generation from up to 160 images with Pix4D, including bundle adjustment and point cloud creation.
  2) Point cloud quality check using Ground Control Points (RTK-DGPS); final dry-area DSM density reduced to 0.5 m; MATLAB filtering (Chauvenet-type) applied.
  3) Wet/submerged bed elevations derived via a depth-brightness model:
     - Water surface elevations at the interface between wet/dry areas extracted from the corrected point cloud.
     - Water depth at known locations inferred from image brightness; a log-linear regression links depth to brightness.
     - Bed elevations in submerged areas obtained by subtracting predicted depth from water surface elevations.
     - Final DSM formed by merging dry-bed elevations with submerged-bed elevations.

## Data use and licensing
- Full data access and licensing information available at the provided DOI: https://doi.org/10.5285/13695138-227f-4d85-9049-0a9cba9e1867
- Citation required for use: Ashworth, P., Nicholas, A., Parsons, D., Sambrook Smith, G. (2019). Digital Surface Models for the South Saskatchewan River, Canada. NERC Environmental Information Data Centre. https://doi.org/10.5285/13695138-227f-4d85-9049-0a9cba9e1867

## References
- Ashworth, P., Nicholas, A., Parsons, D., Sambrook Smith, G. (2019). Digital Surface Models for the South Saskatchewan River, Canada. NERC Environmental Information Data Centre. https://doi.org/10.5285/13695138-227f-4d85-9049-0a9cba9e1867
- Strick, R.J.P., et al. (2019). Quantification of bedform dynamics and bedload sediment flux in sandy braided rivers from airborne and satellite imagery. Earth Surf. Process. Landforms, 44: 953-972. https://doi.org/10.1002/esp.4558