# Supporting documentation for COSMOS-UK (2019). Daily and sub-daily hydrometeorological and soil data (2013-2017) [COSMOS-UK]. NERC Environmental Information Data Centre.

## Overview
- Describes a dataset of daily and sub-daily hydrometeorological and soil moisture data from 46 COSMOS-UK sites (2013–2017).
- Five files cover sub-hourly data, QC flags, daily potential evapotranspiration, hourly VWC from cosmic-ray sensors, and daily VWC.
- Data are quality-controlled and archived at the NERC Environmental Information Data Centre (CEH data system centralization).

## Data Coverage
- 46 COSMOS-UK sites across Great Britain with site-level metadata (location, altitude, soil type, bulk density, organic matter, land cover).
- Time period: October 2013 to December 2017.
- Temporal resolution: sub-hourly data at 30-minute intervals; hourly and daily aggregations for VWC; daily PET.

## File Structure and Content
- COSMOS-UK_Hydrometeorological&Soil_2013-2017.csv
  - Sub-hourly hydrometeorological and soil data at 30-minute resolution; missing values coded as -9999.
  - Timestamps end of each 30-minute period (e.g., 12:30 represents 12:00–12:30 data).
- COSMOS-UK_Hydrometeorological&Soil_2013-2017_QC_Flags.csv
  - QC flags corresponding to data in the main file; column names end with _QCFLAG.
  - Flags indicate failures of automated QC tests; multiple flags sum to a unique final value.
- COSMOS-UK_PotentialEvapotranspiration_2013-2017.csv
  - Daily potential evapotranspiration (PET) at all sites; units in millimetres per day; timestamp at start of the day (00:00 GMT).
- COSMOS-UK_VolumetricWaterContent_Hourly_2013-2017.csv
  - Hourly VWC derived from cosmic-ray neutron sensor (CRNS) data; corrected counts account for atmospheric pressure, humidity, and cosmic-ray intensity.
  - Data can be derived using site-specific N0, universal calibration (hmf), or neutron transport methods; COSMOS-UK uses site-specific N0.
  - 2018 reprocessing applied an additional correction factor to address spurious trends; 30-minute counts are summed to hourly and converted to VWC.
- COSMOS-UK_VolumetricWaterContent_Daily_2013-2017.csv
  - Daily VWC derived from hourly corrected counts; daily aggregation is the average of daily values; timestamp at 00:00 GMT for each day.

## Methodology and Processing
- Sub-hourly data (30-minute) collected on site via instruments, logged locally, telemetered to CEH Wallingford hourly; subjected to two QC stages:
  - Automatic QC tests (per-variable relevance) with unique flag values; failed data removed; accumulated flag value stored in QC Flags file.
  - Daily visual QC via plots for 1–10 day ranges.
- Quality Control flags describe failures such as missing data, zero data, too few samples, low power, sensor faults, diagnostics, out of range, secondary variable dependency, spikes, and error codes.
- VWC processing overview:
  - CRNS counts corrected for background cosmic rays (Junfraujoch reference), atmospheric pressure, and absolute humidity.
  - Three possible VWC derivation methods; COSMOS-UK uses a site-specific N0 calibration approach with a reference soil water content from field calibration.
  - 2018 correction introduces a factor F_i to account for geomagnetic effects and differences between CRNS and reference counters.
  - Hourly VWC generated from corrected counts; D86 depth corrections applied to obtain VWC at ~86 cm or equivalent depth per methodology.
- PET calculation:
  - Derived from sub-hourly data using Penman-Monteith (FAO 56, 1998) with RN, mean soil heat flux (G1 and G2), TA, absolute humidity (Q), wind speed (WS), and atmospheric pressure (PA).

## Completeness and Completeness Notes
- Section 7 provides completeness metrics for Met (precipitation, humidity, air temperature, pressure, radiation, wind speed/direction) and Soil (soil heat flux, soil temperature, VWC from TDT sensors); VWC completeness also covered for CRNS-derived data.
- Some measurements have site-specific limitations:
  - Snow depth measured only at a subset of sites.
  - Wind components not measured at several sites (e.g., Alice Holt, Chimney Meadows, Harwood Forest, Sheepdrove, Waddesdon, Wytham).
  - Wytham Woods decommissioned after 01/10/2016.
  - Snow depth measurements limited by site availability.

## Instrumentation (Overview)
- Cosmic-Ray Neutron Sensor (CRNS) – Neutron counts corrected to derive soil moisture; field calibration and background corrections applied.
- Rain gauge – OTT Pluvio² for precipitation amounts and intensity.
- Point soil moisture sensors – Time Domain Transmissometry (TDT) sensors for VWC and soil temperature at various depths.
- Soil heat flux plates – Hukseflux HFP01SC at 0.03 m depth (two plates per site).
- Soil temperature sensors – Hukseflux STP01 at multiple depths (2, 5, 10, 20, 50 cm).
- Radiometer – Four-component radiation measuring shortwave and longwave components; net radiation computed.
- Automatic weather station – Measures air temperature, humidity, and barometric pressure (Rotronic HC2A-S3 with Gill MetPak Pro base).
- Barometric pressure sensor – Vaisala PTB110.
- Temperature and humidity sensor – Vaisala HUMICAP HMP155A.
- Wind measurement – 3D sonic anemometer and integrated 2D sonic anemometer (wind speed and direction).
- Snow depth – Campbell Scientific SR50A; Snow Water Equivalent via SnowFox sensor.
- Data logger – Campbell Scientific CR3000.

## Data Governance and Access
- Primary contact: S. Stanley; data managers include H. M. Cooper, O. Hitt, M. Fry, O. Swain.
- Institutions responsible for data management, calibration, field engineering, site selection, project management, and website/network outreach.
- Data and documentation are publicly archived at the NERC Environmental Information Data Centre; regular updates and user guide references are provided on the COSMOS-UK website.

## Notes for Data Leaders
- The dataset enables cross-site, high-resolution hydrometeorological and soil moisture analysis with robust QC and provenance trails.
- Important to account for site heterogeneity in instrumentation, missing data, and completeness when designing analyses or dashboards.
- The VWC data rely on CRNS methodology with site-specific calibration; ensure proper interpretation of VWC values, especially in peat or organic-rich soils.
- 2018 reprocessing indicates potential revisions to CRNS-derived data; consider versioning and reprocessing history in longitudinal studies.
- Metadata richness (soil type, bulk density, organic matter, land cover) supports advanced data governance and contextual analysis across networks.