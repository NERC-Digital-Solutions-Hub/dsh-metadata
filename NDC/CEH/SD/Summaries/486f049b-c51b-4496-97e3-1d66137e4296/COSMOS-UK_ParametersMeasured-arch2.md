# Supporting documentation for COSMOS-UK (2018). Daily and sub-daily hydrometeorological and soil data (2013-2016) [COSMOS-UK]. NERC Environmental Information Data Centre.

## Overview
- Dataset: Daily and sub-daily hydrometeorological and soil data from the COSMOS-UK network (2013–2016).
- Scope: Data from 42 sites across the COSMOS-UK network, with four related files.
- Availability: Data stored in the Environmental Information Data Centre (EIDC) for sites installed before end of 2016; Wytham Woods data ends 01/10/2016 due to decommissioning.
- Documentation: See COSMOS-UK_UserGuide.pdf for processing details and data availability across the network.

## Data files and contents
- Hydrometeorological and soil (COSMOS-UK_Hydrometeorological&Soil_2013-2016.csv)
  - Variables: site, datetime (UTC), longwave/shortwave radiation (incoming/outgoing, W/m2), net radiation, precipitation (mm), atmospheric pressure (hPa), air temperature (°C), wind speed (m/s), wind direction (°), absolute humidity (g/m3), relative humidity (%), snow depth (mm), wind components (X/Y/Z), soil temperature (TDT1/TDT2 and profile depths), volumetric water content (VWC) from TDT sensors, and D86 depth measurements.
  - Resolution: 30-minute measurements (variables recorded per 30-minute period; some values averaged over the period).
- Potential Evapotranspiration (COSMOS-UK_PotentialEvapotranspiration_2013-2016.csv)
  - Variables: site, datetime, potential evapotranspiration (mm); derived daily values from 30-minute hydrometeorological/soil inputs.
  - Derivation: Penman-Monteith method (FAO 56).
  - Resolution: Daily totals derived from 30-minute data.
- Volumetric Water Content Daily (COSMOS-UK_VolumetricWaterContent_Daily_2013-2016.csv)
  - Variables: site, datetime, volumetric water content (VWC, %), D86 at 75 m distance (cm).
  - Resolution: Daily (VWC average; D86 depth-averaged value).
  - Derivation: From hydrometeorological data and COSMOS-UK cosmic-ray sensor data, plus background neutron data from Jungfrau station. Daily VWC via Evans et al. (2016); D86 via Köhli et al. (2015).
- Volumetric Water Content Hourly (COSMOS-UK_VolumetricWaterContent_Hourly_2013-2016.csv)
  - Variables: site, datetime, corrected cosmic-ray neutron counts (counts), volumetric water content (VWC, %), D86 at 75 m distance (cm).
  - Resolution: Hourly (VWC average; counts total over preceding hour; D86 as hourly value).
  - Derivation: Similar data sources and methods as daily VWC; hourly values derived from corrected neutron counts and established equations.

## Variables and measurement details
- Hydrometeorological variables (per site across 42 sites):
  - Radiation: Incoming/outgoing longwave (W/m2), incoming/outgoing shortwave (W/m2), net radiation (W/m2).
  - Meteorology: Precipitation (mm), atmospheric pressure (hPa), air temperature (°C), relative humidity (%), absolute humidity (g/m3), wind speed (m/s), wind direction (°), snow depth (mm).
  - Wind components: X, Y, Z components (m/s) where measured.
  - Soil and temperature: Soil temperature (TDT1, TDT2, 2 cm/5 cm/10 cm/20 cm/50 cm profiles) in °C; VWC (TDT1, TDT2) in %; D86 depth data.
- Derived data:
  - Potential evapotranspiration: derived daily totals (mm) using Penman-Monteith FAO56.
  - Volumetric Water Content (VWC): derived from COSMOS cosmic-ray neutron counts plus hydrometeorological data; includes D86 depth-adjusted values.

## Data resolution and site coverage
- Hydrometeorological and soil data: 30-minute temporal resolution, across all sites (with some site-specific exceptions for snow depth and wind components).
- VWC data: daily (from daily file) and hourly (from hourly file) resolutions; D86 depth values accompany both.
- Snow depth: measured at a subset of sites (e.g., not universal across all 42 sites).
- Wind components (X, Y, Z) not measured at all sites (not at Alice Holt, Chimney Meadows, Harwood Forest, Sheepdrove, Waddesdon, or Wytham).

## Data collection, processing, and quality control
- Data collection: Measured by various instruments on site; data telemetered hourly to CEH Wallingford central system.
- Processing flow: On-site data logging, hourly telemetering, processing scripts run after daily data collection for derived metrics (evapotranspiration; VWC from neutron data).
- Quality control: All data subjected to quality control tests (details and tests documented in the COSMOS-UK User Guide).

## COSMOS-UK sites
- 42 calibrated sites listed with site IDs, coordinates, start dates, and calibration status.
- Example notes:
  - Some sites have calibration flag "Y" (Calibrated) and start dates ranging 2013–2016 (e.g., Chimney Meadows, Easter Bush, Plynlimon, etc.).
  - Cwm Garw marked as not calibrated (CALIBRATED = N) in start 29-Jun-2016.
- The site map (Figure 1) provides a visual of site distribution.

## Usage and references
- Primary references for methods:
  - Evans et al. (2016) COSMOS-UK: soil water content derived from cosmic-ray soil moisture observing system.
  - Köhli et al. (2015) vertical depth corrections for D86 derivations.
  - FAO 56 (1998) for crop evapotranspiration guidelines (Penman-Monteith).
- User Guide: COSMOS-UK User Guide for instrumentation, variable definitions, and site-specific details.

## Access and scope
- Data available via the NERC Environmental Information Data Centre (EIDC).
- Focused on sites installed before the end of 2016; Wytham Woods data ends 01/10/2016 due to decommissioning.
- Detailed instrument ownership, variable measurement, and site-by-site specifics are documented in the associated COSMOS-UK User Guide.