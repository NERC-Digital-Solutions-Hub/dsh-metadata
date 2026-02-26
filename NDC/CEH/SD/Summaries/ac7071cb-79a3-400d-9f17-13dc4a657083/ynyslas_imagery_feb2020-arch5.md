# RGB aerial imagery dataset collected with DJI Mavic Pro 2 (5 February 2020)

## Overview
- High-resolution RGB aerial imagery collected for dune area using a DJI Mavic Pro 2 UAV.
- Ground pixel resolution: 0.01 m.
- Data processed to produce an orthomosaic via automated Structure-from-Motion photogrammetry.

## Collection Method
- Platform: DJI Mavic Pro 2 UAV
- Flight duration: 6 minutes
- Date: 5 February 2020
- Flight planning: Pix4DCapture
- Ground pixel resolution: 0.01 m
- Image overlap: 80% (lateral and longitudinal)
- Ground Control Points (GCPs): 8 evenly distributed across the dune; GCP locations surveyed using Trimble R8 DGPS

## Data Characteristics
- Recorded values: RGB pixel values
- Resolution: 0.01 m
- Processing: Orthorectification and mosaicking performed with Pix4Dmapper using Structure-from-Motion (SFM) algorithms
- Output format: GeoTIFF
- Coordinate system: WGS84 30N (EPSG:32630)

## Quality Control
- GCP identification and alignment checked in Pix4Dmapper
- Accuracy assessment: RMSE of 0.003 m in X, Y, and Z directions, indicating high relative accuracy

## Data Structure and Metadata
- Data format: GeoTIFF imagery
- Coordinate reference system: EPSG:32630 (WGS84 30N)
- Processing workflow: Fully automated Pix4Dmapper pipeline based on SFM

## Stewardship and Usage Considerations
- Ensure metadata captures: collection date, platform, sensor, processing software, GCP details, and CRS
- Maintain consistency of CRS and resolution for interoperability with other datasets
- Document any updates or reprocessing steps to preserve traceability of the orthomosaic dataset
- Data is suitable for analyses requiring high-resolution RGB imagery and precise geolocation alignment due to demonstrated low RMSE in validation.