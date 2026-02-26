# Rainfall and Runoff Data for Hafren Catchments

## Overview
- Document lists rainfall measurement sites with detailed metadata and observational context.
- Includes site-specific coordinates, topography, soil types, vegetation, land management, and project dates.
- Provides a method to convert stream flow (cumecs) to area-weighted runoff (mm/15min) and vice versa for two catchments.

## Site Metadata

- Carreg Wen (Rainfall)
  - Location code: CR
  - Easting/Northing: 282869 / 288588
  - Latitude/Longitude (WGS84): 52.4826, -3.7263
  - Altitude: 575 m
  - Description: Near met. site at Carreg Wen
  - Main soil types: Peat
  - Vegetation: Acid moorland
  - Land management: Rough sheep grazing
  - Mining: NA
  - Start date: 6-Mar-2007
  - End date: 27-Jan-2009
  - Comments: Volume measured using a ground-level tipping-bucket rain gauge ~20 m away

- Lower Hafren (Runoff/Stream data)
  - Site code: LHF
  - Easting/Northing: 284281 / 287758
  - Latitude/Longitude (WGS84): 52.4754, -3.7052
  - Altitude: 352 m
  - Description: Main Hafren stream channel above lower flume
  - Main soil types: Podzol/Gley
  - Vegetation: 50% plantation Sitka spruce forest with semi-natural moorland headwaters
  - Land management: Phased felling / thinning since 1985
  - Mining: None
  - Start date: 6-Mar-2007
  - End date: 11-Mar-2008
  - Comments: (none)

- Upper Hafren (Runoff/Stream data)
  - Site code: UHF
  - Easting/Northing: 282842 / 289180
  - Latitude/Longitude (WGS84): 52.4879, -3.7269
  - Altitude: 550 m
  - Description: Main Hafren stream channel above forest boundary
  - Main soil types: Peat
  - Vegetation: Semi-natural acid moorland
  - Land management: Very low intensity sheep grazing
  - Mining: None
  - Start date: 6-Mar-2007
  - End date: 27-Jan-2009
  - Comments: (none)

## Runoff Conversion (Area-Weighted)

- Catchment information
  - Lower Hafren (LHF): Catchment area 3.58 sq km
  - Upper Hafren (UHF): Catchment area 1.22 sq km
  - Note: UHF drainage area is 122 ha to flow gauging point and 117 ha to chemistry sampling point

- Conversion formulas
  - From cumecs to mm/15min (flow):
    - mm/15min = cumecs × 0.9 / catchment_area_km2
  - From mm/15min (flow) to cumecs:
    - cumecs = mm/15min × catchment_area_km2 / 0.9

## Data Use and Potential Outputs
- Data can be combined across sites to enable self-serve dashboards of rainfall and runoff.
- Metadata supports data quality checks, unit consistency, and conversion between flow and area-weighted runoff.
- Possible outputs include site-specific and aggregate rainfall/runoff profiles, along with guidance for end users on interpreting the data and applying the conversion factors.

## Considerations for Data Support
- Ensure consistent unit handling across datasets (cumecs, mm/15min, catchment areas).
- Integrate site metadata with observational data for richer self-serve products.
- Address potential data gaps or alignment issues between sites (e.g., differing start/end dates, formats, or observation methods).