# Supporting documentation for COSMOS-UK (2018). Daily and sub-daily hydrometeorological and soil data (2013-2016) [COSMOS-UK]. NERC Environmental Information Data Centre.

- Overview
  - Describes the COSMOS-UK dataset covering 2013–2016, stored in the Environmental Information Data Centre (EIDC).
  - Data come from 42 COSMOS-UK sites, installed before end of 2016; note that Wytham Woods ends on 01/10/2016.
  - Data are split into four CSV files and are intended for use in hydrometeorological and soil moisture analyses.

- Data files and formats
  - Hydrometeorological & Soil (COSMOS-UK_Hydrometeorological&Soil_2013-2016.csv)
    - 42 sites, 30-minute resolution, Oct 2013–Dec 2016.
    - Variables include: incoming/outgoing longwave and shortwave radiation, net radiation, precipitation, atmospheric pressure, air temperature, wind speed and direction, humidity (absolute and relative), snow depth, wind components (X/Y/Z), soil heat flux, soil temperature (TDT1, TDT2), volumetric water content (VWC) at multiple depths, and D86 depth data.
  - Potential Evapotranspiration (COSMOS-UK_PotentialEvapotranspiration_2013-2016.csv)
    - Daily resolution derived from 30-minute hydrometeorological and soil data.
    - Variable: Potential Evapotranspiration (mm/day), calculated via Penman–Monteith (FAO 56).
  - Volumetric Water Content (Daily) (COSMOS-UK_VolumetricWaterContent_Daily_2013-2016.csv)
    - Daily resolution; derived from hydrometeorological data and cosmic-ray sensor data.
    - Variables include: Volumetric Water Content (percent) and D86 at 75 m from the sensor (depth measurement in cm).
  - Volumetric Water Content (Hourly) (COSMOS-UK_VolumetricWaterContent_Hourly_2013-2016.csv)
    - Hourly resolution; derived from hourly processing of cosmic-ray neutron counts and hydrometeorological data.
    - Variables include: Corrected cosmic-ray neutron counts (counts) and Volumetric Water Content (percent), plus D86 (depth) at 75 m.

- Variables, units, and data derivation
  - Time stamps: DateTime in GMT (yyyy-mm-dd hh:mm).
  - Hydrometeorological & Soil: wide range of meteorological and soil variables measured on site by various instruments; data telemetered hourly to CEH Wallingford.
  - Volumetric water content (VWC):
    - Daily VWC: derived from hydrometeorological data and cosmic-ray data; uses Evans et al. (2016) methodology.
    - Hourly VWC: derived hourly from cosmic-ray counts using Köhli et al. (2015) methods; D86 depth data provided.
  - Potential Evapotranspiration: computed from daily aggregated inputs using Penman–Monteith (FAO-56) after daily data collection.
  - Cosmic-ray data: corrected neutron counts; data sourced with background counts from NMDB (Jungfraujoch, Switzerland).

- Resolution and coverage
  - Hydrometeorological & Soil: 30-minute resolution; 42 sites.
  - Potential Evapotranspiration: daily resolution (derived from 30-minute data).
  - Volumetric Water Content: daily and hourly resolutions (two separate files); all sites with calibrated VWC instruments.
  - Wytham Woods: decommissioned in Oct 2016; other sites remain active per site metadata.

- Site information and data provenance
  - Section 6 provides site metadata (site IDs, coordinates, start dates, calibration status, elevations).
  - Most sites are marked CALIBRATED = Y; a few have CALIBRATED = N or late start dates.
  - Data collection involved on-site instrumentation with data loggers, telemetered to a central system at CEH Wallingford.
  - VWC data incorporate background neutron counts from the Jungfrau NMDB station.

- Data quality and documentation
  - All data undergo quality control tests (specific tests detailed in the COSMOS-UK User Guide).
  - Processing scripts and methodologies referenced:
    - Evans et al., 2016 for daily VWC.
    - Köhli et al., 2015 for D86-based VWC depth correction.
    - FAO 56 (Penman–Monteith) for potential evapotranspiration.
  - Related documentation: COSMOS-UK User Guide (additional data processing and instrument details).

- Data availability and references
  - Data accessible via the NERC Environmental Information Data Centre (EIDC).
  - Key references include Evans et al. (2016) on COSMOS-UK soil moisture from cosmic-ray sensors, Köhli et al. (2015) on cosmic-ray footprints, and FAO (1998) guidelines for evapotranspiration calculations.