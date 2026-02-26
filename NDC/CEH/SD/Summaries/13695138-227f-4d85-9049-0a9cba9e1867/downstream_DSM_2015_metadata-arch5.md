# Digital Surface Models for the South Saskatchewan River, Canada

## Overview
- A set of Digital Surface Models (DSMs) for two sections of the South Saskatchewan River near Outlook, Canada, constructed to document river morphology and its changes over time (erosion/deposition).
- Data span four acquisition dates (2015, 2016, 2017) and include separate DSMs for downstream and upstream sections, totaling eight DSMs.

## Data contents
- Eight DSM files:
  - downstream_DSM_2015.txt
  - downstream_DSM_2016.txt
  - downstream_DSM_2017a.txt
  - downstream_DSM_2017b.txt
  - upstream_DSM_2015.txt
  - upstream_DSM_2016.txt
  - upstream_DSM_2017a.txt
  - upstream_DSM_2017b.txt
- File format: each file contains three columns (UTM Easting, UTN Northing, UTM Elevation) in meters.
- Spatial reference: UTM zone 13N (EPSG:32613).
- Ground resolution: imagery at 0.06 m, with final DSMs in dry areas at 0.5 m resolution after processing.

## Acquisition and processing details
- Imagery collected from a fixed-wing aircraft with an UltraCamXp sensor at ~1500 m altitude.
- Dates of imagery: 13 May 2015; 2 Sept 2016; 8 Jun 2017; 12 Jun 2017.
- Processing workflow (three stages):
  - (1) Orthomosaic generation from up to 160 images using Pix4D with automated image matching and bundle adjustment; initial point cloud created after adjustment.
  - (2) Quality assurance of point cloud using Ground Control Points (RTK differential GPS). Reduced density to 0.5 m for dry areas and filtered with a Chauvenet-type criterion (MATLAB).
  - (3) For submerged areas: derive bed elevations with a depth-brightness model. Water surface elevations at dry/wet interface are interpolated; depth is predicted from pixel brightness via a log-linear regression; bed elevations in submerged areas calculated by subtracting depth from water surface; final DSM combines dry and submerged bed elevations.

## Spatial extent and coordinates
- Location: two river sections near Outlook, Canada.
- Coordinates provided: UTM Easting 356500, UTM Northing 5712400; latitude/longitude approximately 51.5 N, 107.07 W.

## Data access and citation
- Data and further details, including licensing, available at: https://doi.org/10.5285/13695138-227f-4d85-9049-0a9cba9e1867
- Required citation: Ashworth, P., Nicholas, A., Parsons, D., Sambrook Smith, G. (2019). Digital Surface Models for the South Saskatchewan River, Canada. NERC Environmental Information Data Centre. https://doi.org/10.5285/13695138-227f-4d85-9049-0a9cba9e1867

## Related references
- Strick, R.J.P., Ashworth, P.J., Sambrook Smith, G.H., Nicholas, A.P., et al. (2019). Quantification of bedform dynamics and bedload sediment flux in sandy braided rivers from airborne and satellite imagery. Earth Surf. Process. Landforms, 44: 953-972. https://doi.org/10.1002/esp.4558

## Data governance and stewardship considerations
- Metadata and standards: eight DSM files with explicit naming and date provenance; clearly defined coordinate system and units; documentation of processing steps to enable reproducibility.
- Sharing and updates: DSMs are produced from recurring imagery and combined to reflect morphological changes; data availability is governed via the DOI record and NERC EIDC framework.
- Usage notes relevant to data users and custodians: documentation of methods for dry vs. submerged bed derivation aids consistent interpretation and reuse; caution advised for submerged-area estimates due to depth-brightness modeling.