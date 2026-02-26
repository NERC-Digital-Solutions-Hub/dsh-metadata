# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Derwent Water 1990 to 2013

## Overview
- Long-term monitoring dataset from Derwent Water, Cumbria, England (fortnightly sampling 1990–2013).
- Variables include: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3/L), pH (PH), ammonium (NH4N, µg N/L), nitrate (NO3N, µg N/L), soluble reactive phosphate (PO4P, µg P/L), total phosphorus (TOTP, µg P/L), dissolved reactive silicon (SIO2, µg/L), phytoplankton chlorophyll a (TOCA, µg/L).
- Water samples integrated from 0–5 m; typically collected from a boat at the deepest point buoy; shore samples used when buoy access was not possible.
- Data are raw (not quality controlled or calibrated) but visually checked; some data are missing due to events (e.g., 2001 FMD outbreak, 2009 weather).

## Sampling regime and collection methods
- Fortnightly sampling regime; measurement date recorded as Date.
- Sampling location flags:
  - Flag 1: sample taken at the marked buoy location.
  - Flag 2: sample taken from the shore when buoy visit was not possible.
- Detection limits indicated with sign_if_LT_LOD (< sign for below detection limit).
- Water samples reflect conditions from the lake’s 0–5 m depth layer.

## Quality control and data quality
- Data are raw and have not undergone quality control or calibration (except for some duplicate entries from 2005 onwards).
- Visual checks performed; known data gaps noted (e.g., March–June 2001 due to foot-and-mouth disease, 2009 weather-related gaps).

## Data structure and formats
- Data provided as a comma-separated values (CSV) file with columns:
  - Date: Date of measurement.
  - Description: Date of measurement.
  - Variable, Description: Variable name and description (e.g., TEMP – surface temperature in °C; OXYG – surface oxygen saturation in % air-saturation; etc.).
  - Value, Description: Measured value for each variable.
  - Sign_if_LT_LOD, Description: Indicates below detection limit with a < sign when applicable.
  - Flag, Description: 1 = sample at buoy; 2 = sample from shore.

## GIS and data-use considerations
- Suitable for map-based visualization of spatially implicit time-series data from a single lake; requires external spatial context (Derwent Water location, buoy position) for mapping.
- To create maps, consider pairing measurements with point locations representing buoy sampling (and shore samples with their implied location) and timestamps for temporal analysis.
- Data are raw; cleaning, normalization, and calibration would be needed for cross-dataset comparisons or integration with other datasets.
- Be mindful of gaps (2001, 2009) and detection-limit indicators when modeling or aggregating data.

## Reuse and related literature
- Dataset has supported research on climate change impacts and lake productivity:
  - Examples include studies on climate effects on lake physics and catchment productivity’s influence on CO2 emissions, among others.
- Recent publications citing the dataset:
  - George et al. (2007)
  - Maberly et al. (2013)
  - Winfield et al. (various years, 2006–2017)
  - Woolway et al. (2016)

## Access implications for GIS work
- Data are provided in a structured CSV suitable for ingestion into GIS workflows as time-stamped point data.
- Requires alignment with a spatial reference for the sampling site(s) and clear handling of flags to distinguish buoy versus shore samples.
- Consider creating a spatial-temporal database or layer with fields for all variables, dates, and quality flags to support interactive maps and time-enabled visualizations.