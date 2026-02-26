# Meteorological and atmospheric dust data from Kangerlussuaq, southwest Greenland, 20172019

## Overview
- Describes meteorological and atmospheric dust data collected at two locations in southwest Greenland: Ridge and SS85, across 2017–2019 (seasonal sampling periods noted).
- Data collected using multiple instruments and protocols to capture dust concentration, weather conditions, and dust deposition.
- Includes data management details, data file naming conventions, and processing steps (e.g., LOI and ashing for deposition, particle-size analysis).

## Datasets Included
- DUSTY_DustTrak.csv: Atmospheric dust concentrations (PM1, PM2.5, RESP, PM10, Total) at Ridge and SS85; 1-minute averages every 5 minutes; mg/m3; partial data missing due to power/instrument issues.
- DUSTY_Weather_Station_Temperature_and_Humidity_Data.csv: Temperature, relative humidity, absolute humidity, dew point; two sites; readings every 10 minutes; units: Degrees C, %, gm-3.
- DUSTY_Weather_Station_Wind_Data.csv: Wind speed (mean, max, min) and wind direction; two sites; readings every 5 minutes; units: m/s and degrees.
- HDT_Deposition_Data.csv: Dust deposition measurements at five locations; seasonal sampling (Spring 2017 to Autumn/Winter 2018/19); deposition in gm-2 day-1; LOI-based mass estimation after filter ashing; data per trap (locations listed) and per season.
- Data Files (data provenance): PSA906_DUST_HDT.csv, PSAR_DUST_HDT.csv, PSA17b_DUST_HDT.csv, PSA1590_DUST.csv, PSA85_DUST_HDT.csv (data per location).
- 1 = Particle-size data (size distribution) from HDT traps; locations include SS906, Ridge, SS17b, SS1590, SS85; includes season-specific operational dates; particle sizes measured with laser sizer (0.375–2000 µm) with 93 class intervals.

## Measurement Characteristics
- Instruments:
  - DustTrak DRX Environmental Monitor (DUSTY_DustTrak.csv) at 2.5 m above ground.
  - Omega OMYL-RH20 (for temperature, humidity) at ~1 m above ground.
  - RMYoung 5013 (wind) at 2.5 m above ground.
- Deposition measurements:
  - Hall Deposition Trap; trap heads 1.5–1.8 m above ground.
  - Protocol involves collecting, filtering (0.45 µm nylon or 0.7 µm glass fibre), drying, reweighing, ashing at 500°C for 4 hours, and calculating inorganic (minerogenic) dust masses; final areal deposition calculated accounting for trap dimensions and collection period.
- Particle-size data:
  - Be measured from deposited dust using Beckman Coulter LS 230 laser sizer (size range 0.375–2000 µm).
  - In some sites, data are aggregated across traps to produce site-level distributions due to low dust mass.

## Data Quality, Gaps, and Limitations
- Missing data:
  - Dust concentration: 63.9–99.9% data retrieval per sampling period (power loss, auto-zero, equipment malfunction).
  - Temperature/Humidity: 98.4–100% retrieval per period, with some missing due to power/equipment issues.
  - Wind: 66.4–99.9% retrieval per period (power/equipment issues).
  - Deposition/particle-size: some traps yield no data (noted as n/d) due to trap loss or damage.
- Data structure details:
  - CSV format with clear column labels per dataset (e.g., Date/Time, Site, pollutant concentrations, meteorological variables, deposition data, trap numbers, particle-size classes).
  - Units clearly specified (e.g., mg/m3 for particulates, °C for temperature, % for humidity, gm-3 for absolute humidity, m/s for wind).
- Metadata and provenance:
  - Location coordinates and site names explicitly documented.
  - Sampling heights and instrument models documented.
  - Seasonal/operational date ranges provided for each dataset.

## Data Structure and Access
- Data Files: multiple CSVs, each corresponding to a specific measurement category or site.
- Data organization:
  - Per-site and per-season data files for deposition and particle-size datasets.
  - Per-variable datasets for dust concentration, weather (temperature/humidity), and wind.
- Descriptive documentation embedded in the dataset descriptions (sampling frequency, measurement protocols, and data processing steps).

## Governance, Reuse, and Integration Considerations
- Data discoverability: clearly named files and detailed metadata facilitate discovery and integration with broader environmental datasets.
- Data quality management: evident data gaps and instrumentation issues; plan for data quality assessment, imputation strategies, or usage limitations due to missing periods.
- Data lineage and processing: deposition data include LOI-based mass estimation and ashing steps; deposition results depend on trap geometry and seasonal sampling; particle-size data rely on laser sizing with specified class intervals.
- Potential uses for data leaders:
  - Integrating atmospheric dust concentrations with meteorological conditions to study transport and deposition processes.
  - Assessing spatial variability across multiple sites and seasons.
  - Supporting model validation for dust/aerosol transport and deposition studies in polar/subpolar environments.
  - Informing data governance by aligning these datasets with broader data standards and metadata schemas for environmental monitoring.