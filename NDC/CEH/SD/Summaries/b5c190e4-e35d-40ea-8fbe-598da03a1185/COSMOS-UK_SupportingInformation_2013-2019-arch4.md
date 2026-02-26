# Daily and sub-daily hydrometeorological and soil data (2013-2019) [COSMOSUK]. NERC Environmental Information Data Centre.

- Purpose and scope
  - Supporting documentation for the COSMOS-UK network (Stanley et al., 2021).
  - Provides daily and sub-daily time series of hydrometeorological and soil moisture data from 51 COSMOS-UK sites, covering 2013 to 2019.
  - Data intended to support analysis of water and energy balance, soil moisture dynamics, and related processes at multiple scales.

- Data content and structure
  - Total of 208 files including:
    - COSMOS-UK site metadata (site locations, coordinates, soil properties, land cover, etc.).
    - Sub-hourly (30-minute) hydro-soil data and corresponding QC flags and metadata for each site.
    - Hourly hydro-soil data (including volumetric water content, VWC) and metadata.
    - Daily hydro-soil data (including VWC, potential evapotranspiration, snow water equivalent).
    - QC flag files that mirror data files and flag data that failed quality tests.
    - Instrumentation and metadata documentation.
  - Data are organized by SITE_ID in filenames; missing values are encoded as -9999.

- Variables and data products
  - Sub-hourly data (30-minute resolution): radiation components, precipitation, air temperature, humidity, pressure, wind (speed and direction), absolute humidity (Q), relative humidity, snow depth, wind components, soil temperature (TDT sensors), soil moisture (VWC from TDT sensors), heat fluxes (G1, G2), and related TDT metadata.
  - Hourly data: VWC (from both hydrometeorological data and CRNS-derived measurements), air variables, and radiative components.
  - Daily data: VWC, potential evapotranspiration (PE), snow water equivalent (SWE), snow days indicator, and albedo.
  - Derived products and methods:
    - VWC derived from Cosmic-Ray Neutron Sensor (CRNS) counts, corrected for atmospheric pressure, humidity, and cosmic-ray intensity.
    - Daily VWC calculated as daily average of hourly corrected counts and converted to soil moisture via site-calibration parameters.
    - SWE estimation on days with snow cover using albedo-based snow detection and count-rate differences (Wallbank et al., 2020).
    - PE calculated using Penman-Monteith (FAO-56); inputs come from sub-hourly data (RN, G, TA, RH, WS, PA).
    - D86 depths: depth-specific metrics derived from VWC data following Köhli et al. (2015).

- Quality control and data integrity
  - Two-stage QC:
    - Automated QC tests applied on all relevant variables; data failing tests are flagged and removed.
    - Daily visual inspection using automatically generated plots.
  - QC flags:
    - Separate flag file COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2019_QC_Flags.csv with _QCFLAG suffix on column names.
    - Flags are additive and uniquely identify which tests were failed.
    - Table 3.2 in the documentation outlines tests (Missing, Zero data, Too few samples, Low power, Sensor fault, Diagnostic, Out of range, Secondary variable, Spike, Error) and their flag values.
  - Data handling during QC:
    - Missing data (represented as -9999) are removed from the QC-enabled datasets.
    - The QC process keeps a separate record of the flags to allow traceability of failures.
  - Completeness indicators:
    - Section 6 presents site-by-site completeness for combined Met, Soil, and VWC data; VWC completeness reflects CRNS-derived measurements.

- Methodology and processing notes
  - Data collected on-site via a range of instruments; logged and telemetered hourly to central system at UKCEH Wallingford.
  - Aggregation:
    - 30-minute data are end-stamped at the end of the period (e.g., 12:30 represents 12:00–12:30).
  - VWC and CRNS:
    - VWC derived from corrected CRNS counts; corrections account for NMDB reference data, altitude, atmospheric pressure, and absolute humidity.
    - Calibration methods include site-specific N0 calibration with corrections for lattice water and soil organic carbon.
    - In 2018, an extra correction factor was introduced to adjust for fluctuations in incoming cosmic rays.
  - Snow and albedo:
    - Snow presence inferred from albedo (average 10:00–14:00 GMT); snow days identified when albedo exceeds 50% (start) and falls below 35% (end).
    - SWE estimated from differences between observed and snow-free counts.
  - Derived daily albedo and snow-related metrics added to daily dataset (from 2019 updates).
  - Data updates and reprocessing:
    - Data are reprocessed when improvements are implemented; major changes include D86_75m update, VWC calibration updates, CRNS infilling, NMDB data infilling, precipitation recalculation, and PE updates.

- Instrumentation and site variability
  - COSMOS-UK instrumentation overview:
    - Cosmic-Ray Neutron Sensor (CRNS) for VWC estimation (Hydroinnova CRS-2000/B and CRS-1000/B).
    - Pluvio rain gauge for precipitation (on some sites with canopy-top installation considerations).
    - Time-domain reflectometry soil moisture sensors (TDT) at multiple depths for VWC and soil temperature.
    - Soil heat flux plates (HFP01SC) for soil heat flux.
    - Soil temperature sensors (STP01) at multiple depths.
    - Radiometer (NR01) for net radiation and shortwave/longwave components.
    - Automatic weather station (Rotronic HC2A-S3) for air temperature, humidity, etc.
    - Barometric pressure sensor (PTB110) and Vaisala HUMICAP humidity/temperature probes.
    - Anemometers (3D sonic and integrated 2D) for wind speed and direction.
    - Snow depth sensor (SR50A) and SnowFox CRNS-based SWE sensor.
    - Data logging and micrologger (CR3000).
  - Site-specific availability:
    - Some instruments are not installed at all sites; detailed site-by-site instrumentation variations are described in the documentation (Table 7.1).

- Accessibility and usage guidance
  - The dataset is provided via the NERC Environmental Information Data Centre.
  - Regular updates and user guides are available from the COSMOS-UK website.
  - The documentation emphasizes data provenance, processing steps, QA procedures, and the limitations/directions for data interpretation (e.g., snow effects on VWC, potential calibration uncertainties).

- Data governance and authorship
  - Primary authorship and data management coordination by S. Stanley and the COSMOS-UK team.
  - Clear delineation of contributions for site selection, field engineering, calibration, metadata, data presentation, and project management.

- References and foundational material
  - Key methodological references for calibration, data processing, and SWE/PE calculations are cited throughout (e.g., Baatz et al. 2014; Zreda et al. 2012; Evans et al. 2016; Wallbank et al. 2020; Köhli et al. 2015).