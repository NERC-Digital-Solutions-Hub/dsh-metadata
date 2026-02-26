# Supporting documentation for COSMOS-UK (2019). Daily and sub-daily hydrometeorological and soil data (2013-2017) [COSMOS-UK]. NERC Environmental Information Data Centre.

## Overview
- Presents daily and sub-daily time series of hydrometeorological and soil moisture data from 46 COSMOS-UK sites spanning 2013–2017.
- Five data files are described:
  - Sub-hourly hydrometeorological and soil data
  - Sub-hourly hydrometeorological and soil quality control flags
  - Daily potential evapotranspiration
  - Hourly soil volumetric water content (VWC) from the cosmic-ray sensor
  - Daily soil volumetric water content (VWC) from the cosmic-ray sensor
- Data are provided in CSV format; missing values are coded as -9999.
- Data are managed and accessible via the NERC Environmental Information Data Centre (EIDC).

## COSMOS-UK sites and spatial context
- 46 sites across the COSMOS-UK network with site IDs, coordinates (E/N), altitude, soil type, bulk density, organic matter, and land cover.
- Figure 2.1 illustrates the geographical distribution; Table 2.1 lists site details (example entries included in document).
- Site coordinates (eastings/northings) support GIS integration; data include altitude and land cover to support spatial analyses.

## Data coverage and resolution
- Sub-hourly data: 30-minute resolution (2013–2017) for a range of hydrometeorological and soil variables.
- Daily data: Potential evapotranspiration and daily VWC derived from sub-hourly data.
- Hourly VWC: Derived from cosmic-ray neutron sensing (CRNS) with corrections; depth information (D86) included.
- Data are telemetered hourly to CEH Wallingford and pass through quality control processes.

## Data processing and quality control (QC)
- Two-stage QC:
  - Automatic QC with variable-specific tests; data failing tests are flagged and removed.
  - Daily visual inspection of data via automatically generated plots.
- QC flags are stored in a separate file: COSMOS-UK_Hydrometeorological&Soil_2013-2017_QC_Flags.csv; QC flags mirror the main data file with suffix _QCFLAG.
- Flag encoding is unique per combination, enabling traceability of failed tests (e.g., 72 could represent a combination of low power and out-of-range).
- Automatic QC tests cover multiple issues (missing data, zero data, too few samples, low power, sensor/diagnostic faults, out-of-range, secondary-variable reliability, spikes, and error codes).
- QC-compliant data are used for downstream products; flagged data are removed from the primary data file.

## Data files and content
- 3. COSMOS-UK_Hydrometeorological&Soil_2013-2017.csv
  - 46 sites, 30-minute resolution, Oct 2013–Dec 2017.
  - Variables include precipitation, radiation components, air temperature, humidity, pressure, wind components/direction, net radiation, soil/air moisture, soil temperatures, soil heat flux, etc.
  - Some site- or variable-specific exceptions (e.g., snow depth measured only at a subset of sites; wind components not measured at certain sites; Wytham Woods data ends 01/10/2016).
  - Timestamps refer to the end of the 30-minute period (e.g., 12:30 end time covers 12:00–12:30).
  - 3.4 File content provides a full variable table (names, units, aggregation, and notes).
- 4. COSMOS-UK_PotentialEvapotranspiration_2013-2017.csv
  - Daily potential evapotranspiration (mm/day) for all sites.
  - Calculated via Penman-Monteith (FAO-56) using net radiation, soil heat flux (mean of two G sensors), air temperature, absolute humidity, wind speed, and atmospheric pressure.
  - Timestamp at 00:00 for each day (covering the preceding 24-hour period).
- 5. COSMOS-UK_VolumetricWaterContent_Hourly_2013-2017.csv
  - Hourly VWC derived from CRNS and auxiliary site data.
  - Processing steps include correction of neutron counts for background cosmic ray intensity, altitude, atmospheric pressure, and absolute humidity.
  - VWC estimates can be derived via site-specific N0, universal hydrogen molar fraction (hmf), or neutron transport modelling; COSMOS-UK uses site-specific N0 calibration.
  - An additional 2018 correction applied to remove spurious trends (geomagnetic effects) via a site-specific factor Fi.
  - 30-minute counts are summed to hourly totals; D86 (depth) data provided at 75 m offset.
- 6. COSMOS-UK_VolumetricWaterContent_Daily_2013-2017.csv
  - Daily VWC derived by daily average of hourly corrected counts; D86_75m value provided.
  - Timestamp at 00:00 GMT for the day (covering the preceding 24-hour period).
- 7. Completeness
  - Provides completeness metrics by site for Met (meteorological) and Soil groups, and VWC data completeness.
  - Met: precipitation, humidity, air temperature, atmospheric pressure, short/longwave radiation, wind speed and direction.
  - Soil: soil heat flux, soil temperature, VWC from TDT sensors.
- 8. Instrumentation
  - Detailed description of sensors used (CRNS, rain gauge, soil moisture sensors, soil heat flux plates, soil temperature sensors, radiometers, automatic weather station, barometric pressure, temperature/humidity sensors, sonic anemometers, snow depth sensors, snow water equivalent, microloggers).
  - Section 8.2 notes that instrument availability varies by site (not all instruments installed at every site).
  - Models and brief descriptions provided for each instrument type (e.g., CRS-2000/CRS-1000/B, OTT Pluvio², Acclima TDT, Hukseflux HFP01SC, Hukseflux STP01, Hukseflux radiometer, Rotronic HC2A-S3, Vaisala PTB110, Vaisala HUMICAP HMP155, Gill WindMaster 3D, Gill Integrated WindSonic, Campbell SR50A, SnowFox, Campbell CR3000).
- 9 Author contributions
  - S. Stanley as primary author; data managers, calibration/maintenance teams, field engineering, site selection, project management, website maintenance, and network initiation acknowledged.
- 10 References
  - Cited methodological and calibration sources for cosmic-ray soil moisture sensing, calibration approaches, and FAO-56 evapotranspiration, among others.

## GIS and data usage considerations
- Data are amenable to GIS integration via site-level point features (site_ID with E/N coordinates and altitude) joined to time series data.
- 30-minute (sub-hourly) data enable high-temporal-resolution hydrometeorological and soil moisture mapping; daily products support climatology and trend analyses.
- Spatial analyses can leverage site metadata (soil type, land cover, bulk density, organic matter) alongside meteorological variables.
- Data quality flags enable selective filtering or confidence-based analyses across sites and time periods.
- Timestamp conventions differ between datasets (e.g., daily data timestamps refer to the start of the day; sub-daily timestamps refer to the end of the interval), which is important for temporal joins in GIS workflows.

## Access and provenance
- All data are described as part of COSMOS-UK and are hosted in the NERC Environmental Information Data Centre (EIDC).
- Data are provided as CSV files with clear metadata and file-level descriptions to support reproducibility and reuse in GIS and environmental analyses.