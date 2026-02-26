Supporting documentation for COSMOS-UK (2018). Daily and sub-daily hydrometeorological and soil data (2013-2016) [COSMOS-UK]. NERC Environmental Information Data Centre.

## Overview
- Describes the COSMOS-UK dataset stored in the Environmental Information Data Centre (EIDC): Daily and sub-daily hydrometeorological and soil data from 2013-2016.
- Data cover COSMOS-UK network (42 sites) with four files: Hydrometeorological and soil, Potential evapotranspiration, Volumetric water content (daily), Volumetric water content (hourly).
- Timeframe: October 2013 to December 2016; sites installed before end-2016; note: Wytham Woods ends 01/10/2016.
- Data are telemetered to a central system (CEH Wallingford) and quality controlled. Detailed instrumentation and processing guidelines are in the COSMOS-UK User Guide.

## Data files and contents
- Hydrometeorological and soil (30-minute resolution)
  - Filename: COSMOS-UK_Hydrometeorological&Soil_2013-2016.csv
  - Variables include: radiations (longwave/shortwave, net), precipitation, atmospheric pressure, air temperature, wind speed/direction, humidity metrics, snow depth, wind components (X/Y/Z), soil temperatures, volumetric water content, soil heat flux, and site-level metadata.
  - Resolution: 30-minute intervals; 42 sites; some site-specific exceptions (e.g., snow depth measured only at a subset; X/Y/Z wind components not measured at certain sites).
  - Measurement: on-site instruments; data telemetered hourly to CEH Wallingford.
  - Quality control: data undergo quality control tests (details in COSMOS-UK User Guide).
- Potential Evapotranspiration (daily)
  - Filename: COSMOS-UK_PotentialEvapotranspiration_2013-2016.csv
  - Variable: Potential Evapotranspiration (mm/day) as total over the day.
  - Derivation: computed from 30-minute hydrometeorological and soil data using Penman-Monteith (FAO 56).
  - Coverage: derived for all sites.
  - Process: daily derivation after data collection; measurement inputs come from the hydrometeorological/soil data stream.
- Volumetric Water Content (Daily)
  - Filename: COSMOS-UK_VolumetricWaterContent_Daily_2013-2016.csv
  - Variables: Volumetric water content (percent); D86 at 75 m distance (depth) from the cosmic-ray sensor; timestamps (daily).
  - Resolution: daily data (with D86 depth component).
  - Derivation: from hydrometeorological data and cosmic-ray neutron data (plus background neutron data from Jungfrau station, Switzerland); method per Evans et al. 2016; D86 values per Köhli et al. 2015.
  - Notes: daily averages are derived from corrected neutron counts; D86-specific calculations use the referenced methods.
- Volumetric Water Content (Hourly)
  - Filename: COSMOS-UK_VolumetricWaterContent_Hourly_2013-2016.csv
  - Variables: Corrected cosmic-ray neutron counts; Volumetric water content (percent); D86 at 75 m depth.
  - Resolution: hourly; daily data also available via the Daily VWC file.
  - Derivation: hourly data derived from hydrometeorological and cosmic-ray sensor data, with background neutron data; method per Evans et al. 2016 and Köhli et al. 2015 for D86.
  - Telemetry and QA: as per the daily dataset; instrumentation and processing details in User Guide.
- COSMOS-UK sites (metadata)
  - Section lists 42 site entries (site_id, start_date, calibrations, coordinates, altitude, etc.).
  - Provides geospatial context and site-specific calibration status.

## Data resolution and coverage
- Hydrometeorological and soil: 30-minute resolution across 42 sites (Oct 2013–Dec 2016).
- Potential evapotranspiration: daily resolution, derived from 30-minute inputs.
- Volumetric water content: daily resolution (and hourly data available); D86 depth data included for both daily and hourly products.
- Note on site availability: Wytham Woods data ends 01-Oct-2016; others have data within the full period.

## Data derivation and methods
- Hydrometeorological/soil measurements: collected on-site via diverse instruments; data logged locally and telemetered hourly to CEH Wallingford.
- PET derivation: Penman-Monteith method (FAO-56) using daily hydrometeorological/soil inputs.
- Volumetric water content derivation:
  - Daily: derived from hydrometeorological data and cosmic-ray neutron counts; corrected counts for soil moisture estimation; uses Evans et al. 2016 methodology; D86 depth values from Köhli et al. 2015.
  - Hourly: similar process at hourly cadence; uses the same foundational methods.
  - Background neutron data from Jungfrau neutron monitoring station (Switzerland) is incorporated.
- Instrumentation and processing details: further specifics available in COSMOS-UK User Guide.

## Quality control and documentation
- All data are subject to quality control tests; specifics of tests and variable-level application are described in the COSMOS-UK User Guide.
- Documentation and metadata governance are centralized within the COSMOS-UK User Guide and related references.

## Data access, governance, and provenance
- Data housed in the NERC Environmental Information Data Centre (EIDC).
- Telemetry, processing, and updates are managed centrally (CEH Wallingford).
- Metadata include detailed site metadata (Section 6), instrument types, start dates, coordinates, and calibration status; consistent with COSMOS-UK User Guide for provenance and lineage.
- For governance and methodological details, refer to the COSMOS-UK User Guide and cited literature (Evans et al. 2016; Köhli et al. 2015; FAO 1998).

## References
- Evans J. G. et al. (2016). Soil water content in southern England derived from a cosmic-ray soil moisture observing system – COSMOS-UK.
- Köhli M. et al. (2015). Footprint characteristics revised for field-scale soil moisture monitoring with cosmic-ray neutrons.
- FAO (1998). Crop evapotranspiration: Guidelines for computing crop water requirements. FAO Irrigation and drainage paper 56.