# CONVERSION FROM STREM FLOW TO AREA-WEIGHTED RUNOFF

## Overview
- Contains rainfall and runoff data for three Hafren catchment sites and a rainfall site:
  - Carreg Wen rainfall site (Rainfall)
  - Lower Hafren (LHF)
  - Upper Hafren (UHF)
- For each site: location codes, coordinates (E/N, latitude/longitude), altitude, description, soil types, vegetation, land management, mining status, and observation periods.
- Also includes a method to convert streamflow (cumecs) to area-weighted runoff (mm/15min) and vice versa, using site catchment areas.

## Site Details

- Carreg Wen (Rainfall)
  - Location: LOCATION CODE = CR
  - Coordinates: EASTING 282869, NORTHING 288588; LATITUDE 52.4826, LONGITUDE -3.7263 (WGS84)
  - Altitude: 575 m
  - Description: Near met. site at Carreg Wen
  - Main soil types: Peat
  - Vegetation: Acid moorland
  - Land management: Rough sheep grazing
  - Mining: NA
  - Start date: 6-Mar-2007
  - End date: 27-Jan-2009
  - Comments: Volume measured using ground-level tipping-bucket rain gauge ~20 m away

- Lower Hafren (LHF)
  - Location: LOCATION CODE = LHF
  - Coordinates: EASTING 284281, NORTHING 287758; LATITUDE 52.4754, LONGITUDE -3.7052
  - Altitude: 352 m
  - Description: Main Hafren stream channel above lower flume
  - Main soil types: Podzol/Gley
  - Vegetation: 50% plantation Sitka spruce forest with semi-natural moorland headwaters
  - Land management: Phased felling / thinning since 1985
  - Mining: None
  - Start date: 6-Mar-2007
  - End date: 11-Mar-2008
  - Comments: 

- Upper Hafren (UHF)
  - Location: LOCATION CODE = UHF
  - Coordinates: EASTING 282842, NORTHING 289180; LATITUDE 52.4879, LONGITUDE -3.7269
  - Altitude: 550 m
  - Description: Main Hafren stream channel above forest boundary
  - Main soil types: Peat
  - Vegetation: Semi-natural acid moorland
  - Land management: Very low intensity sheep grazing
  - Mining: None
  - Start date: 6-Mar-2007
  - End date: 27-Jan-2009
  - Comments: 

## Runoff Conversion (Area-Weighted)

- Site catchment areas:
  - Lower Hafren (LHF): 3.58 km²
  - Upper Hafren (UHF): 1.22 km²
  - Note: UHF drainage area is 122 ha to flow gauging point and 117 ha to chemistry sampling point

- Conversion formulas:
  - From cumecs to mm/15min (flow): mm/15min = cumecs × 0.9 / catchment_area_km²
  - From mm/15min to cumecs: cumecs = mm/15min × catchment_area_km² / 0.9

## Data Use and Considerations

- Use the site-specific catchment areas to convert measured streamflow to area-weighted runoff for hydrological modelling or comparative analyses between sites.
- The Carreg Wen rainfall data provide anchoring rainfall measurements near peat soils and rough grazing conditions, which can be relevant for rainfall-runoff studies in moorland catchments.
- Ensure alignment of drainage area when applying conversions for LHF and UHF, especially for UHF where gauging and chemistry sampling areas differ (122 ha vs 117 ha).
- Observational periods indicate data primarily from 2007–2009, which may influence model calibration and validation windows.