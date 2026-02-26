# Rainfall, LOCATION CODE = CR.

## Overview
- Dataset describing rainfall measurement at three sites with detailed metadata.
- Timeframe spans 2007–2009 for the sites, with start and end dates provided per site.
- Measurement method noted for the Rainfall site: volume measured using a ground-level tipping-bucket rain gauge ~20 m away.
- Site attributes include location, altitude, soil types, vegetation, and land management practices.
- Includes a separate section on converting stream flow to area-weighted runoff.

## Site Details
- Rainfall (CR)
  - Location: Easting 282869, Northing 288588; Latitude 52.4826, Longitude -3.7263 (WGS84)
  - Altitude: 575 m
  - Description: Near met. site at Carreg Wen
  - Main soil types: Peat
  - Vegetation: Acid moorland
  - Land management: Rough sheep grazing
  - Mining: NA
  - Start date: 6-Mar-2007; End date: 27-Jan-2009
  - Comments: Volume measured with a ground-level tipping-bucket rain gauge ~20 m away
- Lower Hafren (LHF)
  - Location: Easting 284281, Northing 287758; Latitude 52.4754, Longitude -3.7052 (WGS84)
  - Altitude: 352 m
  - Description: Main Hafren stream channel above lower flume
  - Main soil types: Podzol/Gley
  - Vegetation: 50% plantation Sitka spruce forest with semi-natural moorland headwaters
  - Land management: Phased felling/thinning since 1985
  - Mining: None
  - Start date: 6-Mar-2007; End date: 11-Mar-2008
  - Comments: (none)
- Upper Hafren (UHF)
  - Location: Easting 282842, Northing 289180; Latitude 52.4879, Longitude -3.7269 (WGS84)
  - Altitude: 550 m
  - Description: Main Hafren stream channel above forest boundary
  - Main soil types: Peat
  - Vegetation: Semi-natural acid moorland
  - Land management: Very low intensity sheep grazing
  - Mining: None
  - Start date: 6-Mar-2007; End date: 27-Jan-2009
  - Comments: (none)

## Data and Methods
- Catchment areas:
  - Lower Hafren: 3.58 sq km
  - Upper Hafren: 1.22 sq km
  - Note: UHF drainage area is 122 ha to the flow gauging point and 117 ha to the chemistry sampling point
- Unit conversion between stream flow and rainfall-derived runoff:
  - From Cumecs to mm/15 min (flow): mm/15min = cumecs × 0.9 / catchment_area_km2
  - From mm/15 min (flow) to Cumecs: cumecs = (mm/15min) × catchment_area_km2 / 0.9

## Data Use and Accessibility (Analyst perspective)
- Data are collected, verified, quality-assured, cleaned, and transformed to standard outputs (e.g., clear formats, maps, charts).
- Datasets are stored and uploaded to appropriate portals to support long-term environmental monitoring and policy performance evaluation.
- Key challenges include increasing dataset value by combining with other relevant data and enabling access to underlying data used to generate final outputs.