# Collection/generation methods

- RBRsolo3 pressure sensors were deployed between 2020 and 2023 in the upper regions of four UK estuaries: Conwy, Kent, Dyfi, and Milford Haven.
- Loggers were not operational continuously during the deployment period, resulting in intermittent data collection.

## Deployment locations and reference frames

- Location details (from Table 1):
  - Conwy: Eastings 278636.800, Northings 371878.877, vertical reference level (ODN) -0.686 m
  - Kent: Eastings 348111.700, Northings 483305.838, vertical reference level (ODN) 4.206 m
  - Dyfi: Eastings 267157.541, Northings 297651.400, vertical reference level (ODN) -0.295 m
  - Milford Haven: Eastings 198933.337, Northings 205215.959, vertical reference level (ODN) -0.476 m
- Note: Each estuary uses its own vertical reference level relative to Ordnance Datum Newlyn (ODN); coordinate values are given in Eastings/Northings, implying a local projected CRS.

## Measured parameters and units

- Time: date and time stamp
- Air pressure: measured in decibars (dbar)
- Sea pressure: measured in decibars (dbar)
- Depth: measured in meters (m), depth referenced to the sensor’s vertical reference level; negative depth values indicate water level above the vertical reference level
- Sea pressure values that are negative indicate the sensor was out of the water

## Quality control and data integrity

- Sensors arrived factory calibrated; no additional quality control was performed on the data post-deployment
- Data gaps are expected due to intermittent operation; this affects continuity and may require gap handling in analyses

## Data structure and file naming

- File format: CSV (.csv)
- File naming convention: Name_startdate_dataset.csv
  - Name: Estuary name (Conwy, Dyfi, Kent, MilfordHaven)
  - startdate: YYYYMMDD
  - dataset: dataset index, 1–N, ordered chronologically since the start date
- Example: Conwy_20201002_data1.csv

## Practical governance considerations for data stewards

- Ensure accompanying metadata captures CRS (projection) and the exact time zone used for timestamps
- Document the varying vertical reference levels by estuary and how depth should be interpreted relative to each reference
- Track data availability and gaps due to non-continuous operation to support proper data discovery and usage
- Include notes on the factory calibration status and the absence of post-deployment QA to inform users about potential quality considerations
- Maintain the prescribed file naming convention to support dataset discoverability and provenance across multiple estuaries and deployment periods