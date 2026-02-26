# Digital Surface Models for the South Saskatchewan River, Canada

## Overview
- A set of Digital Surface Models (DSMs) for two sections of the South Saskatchewan River near Outlook, Canada.
- Time series covers four dates: 13 May 2015; 2 Sept 2016; 8 Jun 2017; 12 Jun 2017.
- Purpose: quantify river morphology and its changes over time due to processes like erosion and sediment deposition.

## Data content
- Eight DSM files total:
  - downstream_DSM_2015.txt, downstream_DSM_2016.txt, downstream_DSM_2017a.txt, downstream_DSM_2017b.txt
  - upstream_DSM_2015.txt, upstream_DSM_2016.txt, upstream_DSM_2017a.txt, upstream_DSM_2017b.txt
- Each DSM contains three columns: 
  - Column 1: UTM Easting (m)
  - Column 2: UTM Northing (m)
  - Column 3: UTM Elevation (m)
- Coordinates and reference system:
  - UTM zone 13N (EPSG:32613)
  - Specific location: Easting 356500, Northing 5712400; Lat 51.5 N, Lon -107.07 W
- Resolution and method:
  - Ground resolution: 0.06 m
  - DSM combines dry-bank elevations and submerged-bed elevations to cover both dry and wet river-bed areas

## Data collection and processing
- Imagery captured from ~1500 m altitude using a fixed-wing aircraft with an UltraCamXp sensor.
- Photogrammetric workflow (three stages):
  1) Orthomosaic generation from up to 160 images using Pix4D with fixed camera calibration; produce a point cloud after bundle adjustment.
  2) Quality assurance using Ground Control Points (RTK differential GPS); derive DSM in dry areas at 0.5 m resolution after MATLAB-based Chauvenet filtering.
  3) Wet areas: derive bed elevations with a depth–brightness model. Water surface elevations are inferred from the point cloud; depth is estimated via a log-linear regression between brightness and measured depths, then bed elevations in submerged areas are computed and combined with the dry-area elevations.

## Data structure and accessibility
- Data are organized as separate files per section and date; designed for straightforward time-series analysis and comparison across periods.
- Intended to support monitoring of river morphology changes and related hydrodynamic interpretation.

## Licensing and citation
- Data and details, including licensing, are accessible via https://doi.org/10.5285/13695138-227f-4d85-9049-0a9cba9e1867.
- Required citation: Ashworth, P., Nicholas, A., Parsons, D., Sambrook Smith, G. (2019). Digital Surface Models for the South Saskatchewan River, Canada. NERC Environmental Information Data Centre. https://doi.org/10.5285/13695138-227f-4d85-9049-0a9cba9e1867

## References
- Strick, R.J.P., Ashworth, P.J., Sambrook Smith, G.H., Nicholas, A.P., Best, J.L., Lane, S.N., Parsons, D.R., Simpson, C.J., Unsworth, C.A., and Dale, J. (2019). Quantification of bedform dynamics and bedload sediment flux in sandy braided rivers from airborne and satellite imagery. Earth Surf. Process. Landforms, 44: 953-972. https://doi.org/10.1002/esp.4558