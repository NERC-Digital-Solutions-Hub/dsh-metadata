# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Meteorological Data for Cartmel Sands, Morecambe

## Overview
- Meteorological measurements at the Cartmel Sands site in Morecambe, as part of CBESS.
- Dataset covers half-hourly meteorological observations with detailed instrument and processing notes.

## Location and sampling design
- Location: Morecambe, Cartmel Sands (CS) at 54°10'40"N, 003°00'05"W.
- Sites chosen to represent contrasting habitats and sediment types:
  - Saltmarsh regions with two contrasting soil types (clay in Essex; sandy in Morecambe Bay).
  - Essex and Morecambe Bay saltmarsh regions differ in inundation frequency, creek structure, and dominant vegetation.
  - Essex mudflat sites consist of cohesive clays, mud and silt; Morecambe mudflat sites with coarser, more mobile sediments.

## Data collection and instrumentation
- Observation period: half-hourly mean values from 31/05/2013 to 26/01/2015.
- Variables observed: air temperature (T_air), soil temperature (T_soil_5cm; T_soil_10cm), relative humidity (RH), net radiation (Net_rad), photosynthetically active radiation (PAR), precipitation (Precip), wind speed (Wind_Spd), wind direction (Wind_Dir), vapour pressure deficit (VPD).
- Instruments and setup:
  - Datalogger: Campbell Scientific CR5000.
  - Wind: CSAT3 anemometer at a 4.3 m lattice tower, measuring at 10 Hz.
  - Other variables: recorded at 15-minute intervals.
  - Air temperature and humidity: Vaisala MP103A, converted to VPD.
  - Precipitation: Environmental Measurements Limited ARG100 tipping-bucket gauge.
  - Net radiation: Kipp and Zonen NR Lite.
  - PAR: Skye Instruments SKP215.
  - Soil temperatures: Type T thermocouples.
- Data processing: mean half-hour values computed in Matlab; time refers to the midpoint of the half-hour interval (e.g., 00:15).

## Data processing and quality control
- Calibration and quality procedures:
  - 10 Hz wind data filtered for wind shadowing and quality flags; averaged to half-hour means.
  - Remaining meteorological measurements averaged to half-hourly values.
  - Wind data filtered according to CS CSATA quality flags and wind shadowing.
- Data gaps: gaps occur due to sensor malfunctions or power loss.
- Quality assurance focus: filtering based on data quality flags to remove erroneous measurements.

## File formats and documentation
- File formats: CSV.
- Documentation notes:
  - Data gaps indicate non-availability from malfunctioning sensors or power issues.
  - Timekeeping aligned to the middle of half-hour periods.

## Metadata and field structure
- Dataset Field descriptions include:
  - Seasonal indicator (Winter W; Summer S).
  - Location codes (Morecambe M; Essex E).
  - Sites within regions (CS, WS, WP for Morecambe; AH, FW, TM for Essex).
  - Habitat types (Mudflat MF; Saltmarsh SM).
  - Quadrat numbers (1–22) and scale categories (A–D representing 1 m to upper limits).
  - Temporal fields: Year, Month, Day, Hour, Minute.
  - Observed variables with units:
    - T_air (°C), T_soil_5cm (°C), T_soil_10cm (°C)
    - RH (%)
    - Net_rad (W/m^2)
    - PAR (μmol m^-2 s^-1)
    - Precip (mm per 30 min)
    - Wind_Spd (m s^-1), Wind_Dir (degrees)
    - VPD (kPa)

## Roles and responsibilities
- Staff responsible for dataset: Timothy Hill.

## Data availability and governance considerations
- Coverage: 2013–2015 observational window; data described with detailed instrument provenance and processing steps.
- Data sharing readiness: CSV format with comprehensive variable definitions and metadata fields suitable for repository ingestion.
- Governance implications for data stewards:
  - Ensure metadata completeness and clarity around instrumentation, processing defaults (half-hour averaging), and QC procedures.
  - Maintain provenance of data transformations (e.g., Matlab averaging, filtering criteria).
  - Document data gaps and their causes (sensor malfunction, power loss) for users.
  - Align with dataset contribution standards for discovery, interoperability, and re-use, including clear notes on measurement frequency and site-specific context.