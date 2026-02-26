# Water temperature measurements from Durleigh Reservoir 2018 - RBR SoloT

## Overview
- Temperature metadata file for Durleigh Reservoir in 2018
- Location: latitude 51.1210, longitude -3.0403
- Temperature chain: RBR SoloT thermistors at depths from surface (0 m) to bottom (6 m) in 1 m increments
- Temporal resolution: every 10 minutes
- Time period: 22/02/2018 to 05/10/2018
- Date/time format: dd/mm/yyyy HH:MM
- Temperature units: degrees Celsius (°C)
- Data gaps: missing data for thermistors at 1 m, 2 m, and 3 m depths due to corrupted files on download

## Data Content and Structure
- Deep profile: temperatures recorded at depths 0 m, 1 m, 2 m, 3 m, 4 m, 5 m, 6 m
- Each timestamp includes temperature values for each depth (subject to data availability)
- Metadata file accompanies the dataset; exact file formats not specified in the excerpt

## Data Quality and Gaps
- Missing data specifically at depths 1 m, 2 m, and 3 m due to corrupted download files
- Temperature data available for other depths (0 m, 4 m, 5 m, 6 m) and timestamps within the date range

## Provenance
- Deployment researchers: Emily Slavin and Danielle Wain
- Citation: Slavin, E.I., Wain, D.J. 2018. Water temperature measurements from Durleigh Reservoir 2018

## Considerations for GIS Applications
- Suitable for time-series and multi-depth analyses, as well as profile visualizations
- For map-based products, consider creating layered raster/vector representations per depth or multi-layer time-enabled datasets
- Plan for handling missing values at 1 m, 2 m, and 3 m depths during analysis and visualization
- Coordinate reference is based on geographic coordinates (lat/lon); ensure appropriate CRS handling in GIS workflows