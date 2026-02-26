# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Meteorological Data for Cartmel Sands, Morecambe

## Overview
- Meteorological measurements at the Cartmel Sands site in Morecambe, part of the CBESS project.
- Data collected to support understanding of coastal biodiversity and ecosystem services across contrasting habitats.
- Timeframe: half-hourly mean values from 31/05/2013 to 26/01/2015.
- Two regional habitat comparisons represented: Essex and Morecambe Bay saltmarshes, plus mudflat sites with distinct sediment types.

## Location and Sampling
- Site: Cartmel Sands (CS) in Morecambe; coordinates 54°10'40"N, 003°00'05"W.
- Habitat contrasts:
  - Saltmarsh regions with clay soils (Essex) vs. sandy soils (Morecambe Bay).
  - Mudflat sites in Essex with cohesive clays vs. Morecambe mudflats with coarse, mobile sediments.
- Observation cadence:
  - Wind speed and direction at 10 Hz (CSAT3 anemometer on a 4.3 m lattice tower).
  - All other variables averaged to half-hourly means; wind data filtered for quality and shadowing.
  - Time references use the middle of each half-hour interval (e.g., 00:15 for 00:00–00:30).

## Variables and Measurements
- Observed/collected variables (with units):
  - Air temperature (T_air, degrees Celsius)
  - Soil temperature at 5 cm (T_soil_5cm, °C)
  - Soil temperature at 10 cm (T_soil_10cm, °C)
  - Relative humidity (RH, %)
  - Net radiation (Net_rad, W/m^2)
  - Photosynthetically active radiation (PAR, μmol m^-2 s^-1)
  - Precipitation (Precip, mm per 30 min)
  - Wind speed (Wind_Spd, m s^-1)
  - Wind direction (Wind_Dir, degrees)
  - Vapour pressure deficit (VPD, kPa)
- Instrumentation and data handling:
  - Primary datalogger: Campbell Scientific CR5000.
  - Wind: CSAT3 anemometer; 10 Hz measurements averaged to half-hourly.
  - Air temperature/humidity: Vaisala MP103A; conversions to VPD.
  - Precipitation: Environmental Measurements Limited ARG100 tipping bucket rain gauge.
  - Net radiation: Kipp and Zonen NR Lite.
  - PAR: Skye Instruments SKP215.
  - Soil temperatures: Type T thermocouples.
  - Data processing: Matlab used to compute mean half-hourly values.

## Data Processing and Quality Control
- Data processing:
  - 10 Hz wind data filtered for lattice wind shadowing and quality flags; averaged to half-hourly means.
  - Other meteorological measurements averaged to half-hourly means.
- Quality control:
  - Measurements screened using data quality flags from CS CSATA; wind shadowing corrections applied as needed.
  - NA values indicate missing measurements due to sensor malfunction or power loss.

## Data Formats and Gaps
- File format: CSV.
- Gaps:
  - Gaps attributable to sensor malfunction or power loss; NA values used to indicate non-measurement periods.

## Metadata and Field Descriptions
- Dataset fields include:
  - Row Number (sorting index)
  - Season (Winter W, Summer S)
  - Location (Morecambe M, Essex E)
  - Site (e.g., Morecambe: Cartmel Sands CS, etc.; Essex: AH, FW, TM)
  - Habitat (Mudflat MF, Saltmarsh SM)
  - Quadrat Number (1–22)
  - Scale (A: 1 m; B: 1–10 m; C: 10–100 m; D: 100 m+)
  - Year, Month, Day, Hour, Minute
  - Meteorological variables: T_air, T_soil_5cm, T_soil_10cm, RH, Net_rad, PAR, Precip, Wind_Spd, Wind_Dir, VPD
- Dataset field descriptions specify formats and units for each column, facilitating data discovery and reuse.

## Responsible Personnel
- Staff responsible: Timothy Hill.

## Relevance for Data Leaders
- Demonstrates end-to-end data stewardship:
  - Clear documentation of site contexts, contrasting habitats, and sampling design.
  - Detailed instrumentation metadata and data processing steps.
  - Explicit quality control procedures and data flags to aid trust and reusability.
  - Well-defined data formats (CSV) with comprehensive metadata fields enabling discoverability and integration.
- Aligns with key data leadership practices:
  - Understanding data availability and gaps across heterogeneous sites.
  - Documentation of data provenance, processing, and time alignment.
  - Emphasis on data quality and transparency in measurement methods.
  - Facilitation of data sharing and collaboration through standardized field descriptions and accessible formats.