# Daily and sub-daily hydrometeorological and soil data (2013-2016) [COSMOS-UK]

- Overview
  - COSMOS-UK dataset containing hydrometeorological and soil data from 42 sites (2013–2016) at 30-minute resolution.
  - Data stored in the Environmental Information Data Centre (EIDC) and described across four files.
  - Documentation refers to sites installed before end of 2016; further network details in COSMOS-UK_UserGuide.rtf.

- Data files and structure
  - Hydrometeorological and soil.csv (COSMOS-UK_Hydrometeorological&Soil.csv)
  - Potential Evapotranspiration.csv (COSMOS-UK_PotentialEvapotranspiration.csv)
  - Volumetric Water Content Daily.csv (COSMOS-UK_VolumetricWaterContent_Daily.csv)
  - Volumetric Water Content Hourly.csv (COSMOS-UK_VolumetricWaterContent_Hourly.csv)

- Variables and resolution
  - Hydrometeorological and soil (30-minute resolution): incoming/outgoing/net radiation, precipitation, atmospheric pressure, air temperature, wind speed and direction, humidity (relative and absolute), snow depth (subset sites), wind components (X, Y, Z at most sites), soil temperatures, soil volumetric water content (VWC) at various sensors, and other site notes.
  - Potential evapotranspiration (daily resolution, derived): PET (mm/day).
  - Volumetric water content (VWC) daily (from COSMOS neutron data and sensors) and hourly (corrected COSMOS neutron counts and VWC; includes D86 depth data at 75 m from COSMOS sensor).
  - All sites except noted exceptions measure the same primary variables; snow depth and wind components have site-specific availability.

- Derivation and processing
  - PET: derived from 30-minute hydrometeorological and soil data using Penman-Monteith (FAO 56).
  - Daily VWC: derived from hydrometeorological data and COSMOS cosmic-ray neutron counts; uses Evans et al. 2016 methodology; D86 depth data derived via Köhli et al. 2015.
  - Hourly VWC: derived from hourly data using the COSMOS neutron counts method; daily values also available.

- Data collection, transmission, and governance
  - Data logged on-site and telemetered to CEH Wallingford every hour.
  - Quality control (QC) tests applied to all data; details of tests and variable-specific QC are described in the COSMOS-UK User Guide.
  - Datasets are documented and stored in EIDC; further instrumentation and processing details available in the COSMOS-UK User Guide.

- Site metadata and coverage
  - 42 calibrated sites listed with site IDs, coordinates (E/N), altitude, start dates, and calibration status.
  - Snow depth measured only at a subset of sites; X, Y, Z wind components not measured at several sites.
  - Comprehensive site map and metadata available in the COSMOS-UK documentation.

- Data quality and usability notes
  - All data undergo QC tests; processing methods and correction factors are described in the COSMOS-UK User Guide.
  - Some variables are location-specific (e.g., snow depth, wind components) and not uniformly available across all sites.
  - Data are suitable for hydrometeorological and soil moisture analyses at 30-minute, daily, and hourly scales, with derived PET and VWC products.

- References and related documentation
  - Evans et al., 2016. Soil water content in southern England derived from a cosmic-ray soil moisture observing system – COSMOS-UK.
  - Köhli et al., 2015. Footprint characteristics for field-scale soil moisture monitoring with cosmic-ray neutrons.
  - FAO, 1998. Crop evapotranspiration guidelines (FAO 56).
  - COSMOS-UK_UserGuide.rtf and 2018 COSMOS-UK Supporting Documentation.