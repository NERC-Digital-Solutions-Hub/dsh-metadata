Supporting documentation for COSMOS-UK (2019). Daily and sub-daily hydrometeorological and soil data (2013-2017) [COSMOS-UK]. NERC Environmental Information Data Centre.

## Overview
- A dataset of daily and sub-daily hydrometeorological and soil moisture data from 46 COSMOS-UK sites, covering 2013–2017.
- Comprises five files: sub-hourly data, QC flags, daily potential evapotranspiration, hourly VWC (cosmic-ray sensor), and daily VWC (cosmic-ray sensor).
- Extensive site metadata detail (location, altitude, soil type, bulk density, organic matter, land cover) and instrument descriptions.

## Data files and contents
- Sub-hourly hydrometeorological and soil data
  - COSMOS-UK_Hydrometeorological&Soil_2013-2017.csv
  - 30-minute resolution; missing values coded as -9999.
- Quality control flags
  - COSMOS-UK_Hydrometeorological&Soil_2013-2017_QC_Flags.csv
  - Flags data that failed automatic QC tests; combined flag value tracks multiple failures.
- Daily potential evapotranspiration
  - COSMOS-UK_PotentialEvapotranspiration_2013-2017.csv
  - Daily PE calculated with Penman-Monteith using RN, G, TA, Q, WS, PA; timestamp at 00:00 for each day; -9999 for missing.
- Hourly volumetric water content (VWC)
  - COSMOS-UK_VolumetricWaterContent_Hourly_2013-2017.csv
  - Derived from cosmic-ray neutron sensor (CRNS); corrected counts accounting for atmospheric conditions, altitude, and humidity; 30-minute counts aggregated to hourly; D86_75m alongside VWC.
  - 2018 introduced site-specific correction factor for cosmic-ray fluctuations; reprocessing applied.
- Daily volumetric water content
  - COSMOS-UK_VolumetricWaterContent_Daily_2013-2017.csv
  - Daily average VWC derived from hourly corrected counts; D86_75m provided; timestamp at 00:00 daily.

## Data provenance, processing, and quality control
- Data collection
  - Instruments include CRNS (cosmic-ray neutron sensor), rain gauge (OTT Pluvio²), soil moisture sensors (TDT), soil heat flux plates (HFP01SC), soil temperature sensors (STP01), radiometer, automatic weather station, barometer, temperature/humidity sensors, and sonic anemometers.
  - Data logged on-site, then telemetered hourly to CEH Wallingford.
- Quality control
  - Two-stage QC: automated QC tests applied on arrival (with unique flags per test); failing data are flagged and removed; results archived in QC flag file.
  - Daily visual QC via plots over 1–10 day windows.
  - Flag values are additive, enabling traceability of which tests failed.
  - Notation: -9999 for missing data; some site-specific exceptions apply (see Completeness).
- Calibration and methodology
  - VWC via CRNS processing: background correction, site altitude, atmospheric pressure, and absolute humidity adjustments; three processing methods exist (N0, hmF, neutron transport); COSMOS-UK uses site-specific N0 calibration with standard silica soil parameters; corrections for lattice/bound water and soil organic carbon applied.
  - 2018 update adds a correction factor to counts to remove spurious trends; site-specific gamma factors derived for VWC reprocessing.
- Completeness and site-specific notes
  - Snow depth measured only at a subset of sites; some wind components not measured at several sites; Wytham Woods data end on 2016-10-01 due to site decommission.
  - Completeness summarized in Section 7 of the documentation (Met, Soil, and VWC groups).

## Variables and site metadata
- Site metadata includes 46 COSMOS-UK sites with details such as altitude, soil type, bulk density, organic matter content, informal soil description, and land cover (e.g., grassland, arable, woodland, moorland).
- Variable details:
  - Sub-hourly file: RN (net radiation), SWIN/SWOUT (shortwave), LWIN/LWOUT (longwave), precipitation, pressure, air temperature, wind speed/direction, humidity, VWC (TDT sensors, D86 distance), soil temperatures at multiple depths, soil heat flux (G1, G2), etc.
  - QC flags correspond to tests like missing data, zero data, too few samples, low power, sensor fault, diagnostic flags, out of range, secondary variable consistency, spikes, and error codes.
  - POTENTIAL evapotranspiration file: PE (mm/day).
  - VWC files (hourly and daily): corrected CRNS counts and VWC, plus D86_75m metadata.
- Instrumentation and site variability
  - Instrument types and deployment vary by site and over time; Section 8 provides consolidated instrument descriptions and a site-by-site table of installed instruments (with some sites lacking certain sensors).

## Completeness and limitations
- Some data gaps due to site decommissioning, instrument availability, and partial instrumentation across sites.
- Snow depth is not universally available; wind component measurements (X, Y, Z) not present at all sites; some sites lack certain sensors or have partial deployments.
- Completeness quantified in the documentation (Section 7) to guide data quality assessment and gap analyses.

## Data governance, access, and stewardship notes
- Data hosted and documented in the NERC Environmental Information Data Centre (EIDC).
- Clear data lineage: on-site measurements, 30-minute aggregation, hourly transmission, two-stage QC, flagging, and reprocessing in 2018 for cosmic-ray data.
- Versioning considerations: post-2018 VWC corrections imply the need to reference data version when reusing VWC data.
- Metadata richness: extensive site metadata enables proper data discovery, discovery-usage alignment, and governance across large datasets.
- Authorship and responsibilities: explicit author contributions and data management roles are described (data managers, calibration/maintenance teams, field engineering, project management).

## Practical implications for data stewardship
- Ensure consistent use of QC flags and documentation when sharing or reusing the data.
- Maintain versioned records of VWC data, especially post-2018 reprocessing for cosmic-ray counts.
- Preserve site metadata alongside data to support discoverability and correct interpretation of variable availability and instrumentation.
- Monitor and document data gaps or changes in instrumentation over time to inform users about potential discontinuities.
- Align data sharing with the NERC EIDC repository requirements, including proper citation and metadata completeness.

## Author contributions and references
- Primary author: S. Stanley; data managers: H. M. Cooper, O. Hitt, M. Fry, O. Swain; instrument calibration and maintenance teams; field engineering; site selection; COSMOS-UK project management; website and outreach; network inception.
- Key references include foundational papers on cosmic-ray soil moisture sensing and calibration methods (e.g., Baatz et al. 2014; Zreda et al. 2012; Franz et al. 2012/2013; Evans et al. 2016).