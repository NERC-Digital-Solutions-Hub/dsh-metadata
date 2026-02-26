# CONVERSION FROM STREM FLOW TO AREA-WEIGHTED RUNOFF

## Data overview
- Document describes rainfall measurement sites and Hafren catchment data, including coordinates, altitudes, soils, vegetation, land management, timing, and simple notes.
- Coordinate information uses lat/long in WGS84 and also provides easting/northing coordinates.
- Start and end dates indicate the measurement period for each site.

## Site details
- Rainfall site (Carreg Wen)
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
  - Comments: Volume measured using ground-level tipping-bucket rain gauge ~20 m away

- Lower Hafren (LHF)
  - Location code: LHF
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

- Upper Hafren (UHF)
  - Location code: UHF
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

## Catchment areas and notes
- Lower Hafren catchment area: 3.58 km^2
- Upper Hafren catchment area: 1.22 km^2
- Note: UHF drainage area is 122 ha to flow gauging point and 117 ha to chemistry sampling point

## Conversion formulas
- From Cumecs to mm/15min (flow): mm/15min = cumecs × 0.9 / (catchment_area_km^2)
- From mm/15min to Cumecs: cumecs = (mm/15min) × (catchment_area_km^2) / 0.9

## GIS considerations and potential uses
- Data are provided for three sites with consistent WGS84 coordinates, enabling integration into map-based visualisations and catchment-level analyses.
- Useful for hydrological modelling, linking rainfall measurements to streamflow, and performing area-weighted runoff calculations across the LHF and UHF catchments.
- Consider data harmonisation needs across datasets (resolution, timeframes, and measurement methods) and careful handling of units (km^2 vs ha) when integrating into GIS workflows.