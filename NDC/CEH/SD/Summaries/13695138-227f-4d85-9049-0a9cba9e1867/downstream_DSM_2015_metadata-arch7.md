# Digital Surface Models for the South Saskatchewan River, Canada

## Overview
- DSM dataset of two river sections near Outlook, Canada, designed to reveal river morphology and its changes over time (erosion/deposition).
- Eight DSMs across four dates (2015, 2016, 2017) for two sections (downstream and upstream).

## Data files and structure
- File names:
  - downstream_DSM_2015.txt
  - downstream_DSM_2016.txt
  - downstream_DSM_2017a.txt
  - downstream_DSM_2017b.txt
  - upstream_DSM_2015.txt
  - upstream_DSM_2016.txt
  - upstream_DSM_2017a.txt
  - upstream_DSM_2017b.txt
- Each file contains three columns:
  - Column 1: UTM Easting (m)
  - Column 2: UTM Northing (m)
  - Column 3: UTM Elevation (m)
- Coordinate system: UTM Zone 13N, EPSG:32613.
- Spatial reference coordinates provided: Easting 356500, Northing 5712400; latitude/longitude 51.5 N, 107.07 W.
- Resolution: 0.06 m ground resolution; data points previously resampled to 0.5 m for the dry bed processing.
- File format: text files with three columns.

## Data collection and processing
- Date of imagery: 13 May 2015; 2 Sept 2016; 8 Jun 2017; 12 Jun 2017.
- Platform and sensor: fixed-wing aircraft with UltraCamXp; nadir imagery at ~1500 m altitude; up to 160 images per date.
- Processing workflow:
  - (1) Generate orthomosaic and dense point cloud using Pix4D; bundle adjustment with calibration certificates; derive point cloud.
  - (2) Validate and refine point cloud with RTK differential GPS Ground Control Points; reduce density to 0.5 m; apply MATLAB-based filtering to produce DSM in dry areas.
  - (3) For submerged (wet) areas, derive bed elevations using a depth-brightness model: extract water surface elevations, interpolate, perform log-linear regression between water depth and pixel brightness, and convert to bed elevations. Combine dry and wet bed elevations to produce final DSM.

## Spatial scope and methodology
- Two river sections near Outlook, Saskatchewan (South Saskatchewan River) in Canada.
- DSMs constructed to quantify bed morphology and changes over time via photogrammetric approaches and depth-water relationships for submerged areas.

## Data quality and standards
- Uses a combination of photogrammetry, ground control, and depth-brightness modeling to handle dry and submerged bed areas.
- Data are designed for GIS-based analysis of river morphology over time.

## Access, licensing, and citation
- Data access and licensing information available at: https://doi.org/10.5285/13695138-227f-4d85-9049-0a9cba9e1867
- Required citation:
  Ashworth, P., Nicholas, A., Parsons, D., Sambrook Smith, G. (2019). Digital Surface Models for the South Saskatchewan River, Canada. NERC Environmental Information Data Centre. https://doi.org/10.5285/13695138-227f-4d85-9049-0a9cba9e1867

## References
- Strick, R.J.P., Ashworth, P.J., Sambrook Smith, G.H., Nicholas, A.P., Best, J.L., Lane, S.N., Parsons, D.R., Simpson, C.J., Unsworth, C.A., and Dale, J. (2019). Quantification of bedform dynamics and bedload sediment flux in sandy braided rivers from airborne and satellite imagery. Earth Surf. Process. Landforms, 44: 953-972. https://doi.org/10.1002/esp.4558