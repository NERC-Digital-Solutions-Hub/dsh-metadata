# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Meteorological Data for Cartmel Sands, Morecambe

## Overview
- Meteorological dataset collected at Cartmel Sands, Morecambe (CBESS) to support coastal biodiversity and ecosystem service analyses.
- Observation period: half-hourly mean values from 31 May 2013 to 26 Jan 2015.
- Primary variables: air temperature (T_air), soil temperature (T_soil_5cm, T_soil_10cm), relative humidity (RH), net radiation (Net_rad), photosynthetically active radiation (PAR), precipitation (Precip), wind speed (Wind_Spd), wind direction (Wind_Dir), vapour pressure deficit (VPD; derived).
- Staff: Timothy Hill.

## Location and Habitat Context
- Observation site: Cartmel Sands, Morecambe (CS) in Morecambe Bay.
- Comparative site descriptions note contrasting habitats used for study design, including differences in sediment types, inundation frequency, creek structure, and vegetation between Essex and Morecambe saltmarsh regions.
- Related substrates include mudflats with cohesive clays/mud/silt (Essex) and mudflats with coarse, mobile sediments (Morecambe).

## Data Collection and Instrumentation
- Instrumentation:
  - Campbell Scientific CR5000 datalogger.
  - Wind: CSAT3 anemometer mounted on a 4.3 m lattice tower, sampling at 10 Hz.
  - Other variables: measured with appropriate sensors (e.g., Vaisala MP103A for air temperature/humidity, EML ARG100 tipping bucket rain gauge for Precip, Kipp and Zonen NR Lite for Net_rad, Skye Instruments SKP215 for PAR, soil thermocouples for T_soil).
- Sampling rates:
  - Wind: 10 Hz; all wind measurements averaged to half-hourly values.
  - Other meteorological variables: recorded/averaged at 15-minute intervals, then averaged to half-hourly means.
  - Time reference: values correspond to the middle of the half-hour period (e.g., 00:15 covers 00:00–00:30).
- Data processing:
  - Mean half-hourly values calculated in Matlab.
  - VPD derived from T_air and RH.

## Quality Assurance and Calibration
- Calibration and data quality handling:
  - 10 Hz wind data filtered for wind shadowing effects and quality flags; averaged to half-hourly means.
  - Other meteorological measurements averaged to half-hourly.
  - Data checked against quality flags (CSATA) and wind shadowing considerations.
- Data quality notes:
  - Gaps occur due to sensor malfunction or power loss.
  - NA values indicate periods when measurements were not performed.

## File Formats and Data Structure
- Primary file format: CSV.
- Dataset field descriptions:
  - Temporal fields: Year, Month, Day, Hour, Minute (and associated Season).
  - Spatial/Grouping fields: Location (e.g., Morecambe, Essex), Site (e.g., Cartmel Sands, other Essex sites), Habitat (Mudflat, Saltmarsh), Quadrat Number, Scale (grid resolution).
  - Variables with units: T_air (°C), T_soil_5cm (°C), T_soil_10cm (°C), RH (%), Net_rad (W/m²), PAR (μmol m⁻² s⁻¹), Precip (mm/30 min), Wind_Spd (m s⁻¹), Wind_Dir (degrees), VPD (kPa).
- Data semantics:
  - Field descriptions and formats accompany the dataset to support interpretation and reuse, including explicit categorizations for Season (Winter/Summer), Location (M/Essex), Site, and Habitat.
  - Quadrat numbers and scale denote spatial resolution of measurements.

## Data Usage and Outputs
- Designed to enable end users to “self-serve” analyses by providing clean, well-documented meteorological data.
- Supports integration with other Coastal Biodiversity and Ecosystem Service datasets for broader analyses.
- Potential outputs include dashboards, pivot tables, and reports; outputs can be promoted and iterated based on user feedback.
- Documentation includes details enabling data re-use, provenance, and cross-site comparisons.

## Practical Considerations for Data Support
- Ensure awareness of site/contextual differences between Essex and Morecambe habitats when integrating data.
- Account for occasional data gaps and missing values in analyses; consider data quality flags and flag-based filtering.
- Leverage the detailed field descriptions to map variables to analytical models and visualization tools.