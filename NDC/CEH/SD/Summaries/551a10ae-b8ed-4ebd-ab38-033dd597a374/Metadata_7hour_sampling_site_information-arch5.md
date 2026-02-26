# Rainfall and Catchment Data with Conversion from Stream Flow to Area-Weighted Runoff

## Overview
- Multi-site dataset covering rainfall and catchment data for three sites: Rainfall (CR), Lower Hafren (LHF), Upper Hafren (UHF).
- Time span:
  - Rainfall: 6-Mar-2007 to 27-Jan-2009
  - Lower Hafren: 6-Mar-2007 to 11-Mar-2008
  - Upper Hafren: 6-Mar-2007 to 27-Jan-2009
- Measurement detail for Rainfall: volume measured using a ground-level tipping-bucket rain gauge located ~20 m away from the site.

## Site Metadata (by site)

- Rainfall (CR)
  - Location code: CR
  - Coordinates: Easting 282869, Northing 288588; Latitude 52.4826, Longitude -3.7263
  - Altitude: 575 m
  - Description: Near met. site at Carreg Wen
  - Main soils: Peat
  - Vegetation: Acid moorland
  - Land management: Rough sheep grazing
  - Mining: NA
  - Start date: 6-Mar-2007; End date: 27-Jan-2009
  - Comments: Volume measured with a tipping-bucket rain gauge ~20 m away

- Lower Hafren (LHF)
  - Location code: LHF
  - Coordinates: Easting 284281, Northing 287758; Latitude 52.4754, Longitude -3.7052
  - Altitude: 352 m
  - Description: Main Hafren stream channel above lower flume
  - Main soils: Podzol/Gley
  - Vegetation: 50% plantation Sitka spruce forest with semi-natural moorland headwaters
  - Land management: Phased felling/thinning since 1985
  - Mining: None
  - Start date: 6-Mar-2007; End date: 11-Mar-2008
  - Comments: (none)

- Upper Hafren (UHF)
  - Location code: UHF
  - Coordinates: Easting 282842, Northing 289180; Latitude 52.4879, Longitude -3.7269
  - Altitude: 550 m
  - Description: Main Hafren stream channel above forest boundary
  - Main soils: Peat
  - Vegetation: Semi-natural acid moorland
  - Land management: Very low intensity sheep grazing
  - Mining: None
  - Start date: 6-Mar-2007; End date: 27-Jan-2009
  - Comments: (none)

## Data conversions and calculations

- Conversion from stream flow (cumecs) to area-weighted runoff (mm/15 min):
  - mm/15min (flow) = cumecs × 0.9 ÷ catchment area (km^2)
- Inverse conversion:
  - cumecs = (mm/15min) × catchment area (km^2) ÷ 0.9
- Catchment areas:
  - Lower Hafren: 3.58 km^2
  - Upper Hafren: 1.22 km^2
- Note: UHF drainage area is 122 ha to the flow gauging point and 117 ha to the chemistry sampling point

## Data governance considerations

- Ensure consistent coordinate reference system (WGS84) across all sites (lat/long provided in WGS84).
- Metadata completeness: capture site metadata, measurement methods, data scope, and time coverage.
- Standardize units (mm/15min, cumecs, km^2, ha) and document the conversion formulas within the data dictionary.
- Attach conversion methodology and catchment areas to dataset provenance; enable traceability of calculations.
- Record data status and update procedures; manage versions and any embargoes.
- Document data quality checks and known limitations (e.g., Rainfall gauge location relative to site).

## Risks and data quality considerations

- Some metadata fields may be incomplete (e.g., UHF Comments are empty).
- Time windows vary by site; ensure alignment when integrating datasets.
- Site-specific context (soil/vegetation/land management) may influence runoff interpretation; note these for analytics.

## Recommendations for Data Stewards

- Create a comprehensive dataset metadata entry capturing all fields above; align with standard metadata schemas (e.g., ISO 19115 where possible).
- Verify and enforce consistent coordinate reference frames and units across all records.
- Include detailed data provenance for measurement methods (gauge type, distance to site) and the runoff conversion rules.
- Store explicit data processing notes and the catchment-area figures within the dataset's data dictionary.
- Define data access, sharing rights, and update/versioning policies; plan for ongoing ingestion and end-date updates.
- Maintain linkage between site metadata and corresponding data files in data portals for discoverability.