# Daily climate data combines data from several different sources for the Siksik catchment. Explanation of data sheet - meteo_data.csv

## Overview
- Meteorological and hydrological data for the Siksik catchment, North West Territories, Canada.
- Site details: Longitude 133°26′26″W, Latitude 68°44′17″N, Elevation 85 m, watershed ≈1 km², time zone Mountain Standard Time.
- Data assembled from multiple sources; includes both observed climate variables and derived measures (evapotranspiration, thaw depth/volume, runoff, and stream temperature).

## Data content and structure
- The meteo_data.csv data sheet documents:
  - Column headings (variable name), units, and methodology for each variable.
  - Three source blocks (1, 2, 3) indicating data from different sources or methods.
- Key variables include:
  - date: Date of record (dd/mm/yy).
  - Tair: Mean daily air temperature (°C); Tmin/Tmax: min/max daily air temperature (°C).
  - RHmin/RHmax: Daily relative humidity (%).
  - u2: Wind speed at 10 m height (km/s; note unit column).
  - Tdew: Dew point temperature (°C).
  - ea: Estimated actual vapour pressure (kPa) via FAO methods.
  - P: Precipitation (mm).
  - Rs: Estimated surface resistance (s m⁻¹) via FAO method.
  - albedo: Estimated albedo (only in source 1; absent in sources 2–3).
  - PET: Estimated potential evapotranspiration (Penman method; units mm d⁻¹).
  - Other derived indicators: degree-days above 0°C (ddt), mean thaw depth (m), thaw volume (mm), flow_m3s (m³/s), flow_mm (mm), stream_temp (°C).
- Remarks on data structure:
  - Each variable provides a 1–3 source block (1, 2, 3) with corresponding units and methodology.
  - NA indicates not applicable or missing data.

## Data sources and methodology
- Primary data source for temperature, humidity, wind, and precipitation: http://climate.weather.gc.ca.
- Derived variables:
  - ea and Rs calculated using FAO methods.
  - PET estimated using the Penman-Monteith approach.
  - Thaw depth and thaw volume derived from a day-degree method; measured thaw depth referenced to Lorna Street.
- Notes emphasize the presence of multiple sources and the need to align units and methods across datasets.

## Metadata and governance
- The dataset includes explicit metadata for each variable: name, units, and methodology.
- Repeated source blocks (1–3) facilitate provenance tracking and interoperability across systems.
- NA entries mark missing or inapplicable values, underscoring data completeness considerations.

## Data quality and limitations
- Data may come from several sources with potential interoperability challenges.
- Some variables have data only in certain source blocks (e.g., albedo present only in source 1).
- Missing data are indicated by NA, which may affect analyses requiring complete time series.

## Access, sharing and updates
- Data is organized in a CSV data sheet (meteo_data.csv) with documented provenance and update rules implied by the source blocks.
- Sharing should maintain source attribution; updates should preserve the documented methodology (FAO for ea and Rs, Penman-Monteith for PET, day-degree for thaw metrics).

## Data steward considerations
- Ensure consistent unit handling and metadata alignment across sources 1–3.
- Maintain clear provenance by preserving source-specific methodology notes for each variable.
- Monitor and document data gaps; create guidance for imputation or exclusion where appropriate.
- Manage potential embargoes or access restrictions if any derived variables (e.g., thaw measurements) originate from controlled sources.
- Consider publishing-ready documentation to facilitate reuse by researchers and data users with diverse needs.