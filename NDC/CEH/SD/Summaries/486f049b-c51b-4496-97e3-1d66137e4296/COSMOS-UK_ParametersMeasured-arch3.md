# Supporting documentation for COSMOS-UK (2018). Daily and sub-daily hydrometeorological and soil data (2013-2016) [COSMOS-UK]. NERC Environmental Information Data Centre.

## Overview
- Describes data stored in the Environmental Information Data Centre (EIDC) for the COSMOS-UK network (2013–2016).
- Data are organized into four CSV files and cover 42 sites with daily and sub-daily measurements.
- Wytham Woods data end on 01/10/2016 due to decommissioning; see COSMOS-UK_UserGuide.pdf for network-wide data processing and availability details.

## Data products and resolutions
- Hydrometeorological and soil data (30-minute resolution; Oct 2013–Dec 2016)
  - Filename: COSMOS-UK_Hydrometeorological&Soil_2013-2016.csv
  - Variables include: longwave and shortwave radiation (incoming/outgoing), net radiation; precipitation (mm); atmospheric pressure (hPa); air temperature (°C); wind speed (m/s) and direction (degrees); humidity (relative and absolute); snow depth; wind components (X, Y, Z); soil temperature at multiple depths; volumetric water content (VWC) sensors; cosmic-ray related measurements (for VWC derivation).
- Potential evapotranspiration (daily resolution; derived from 30-minute data)
  - Filename: COSMOS-UK_PotentialEvapotranspiration_2013-2016.csv
  - Variable: Potential Evapotranspiration (mm/day); derived via Penman-Monteith (FAO56).
- Volumetric water content (Daily, from COSMOS-UK neutron data)
  - Filename: COSMOS-UK_VolumetricWaterContent_Daily_2013-2016.csv
  - Variables: Volumetric water content (%, daily average); D86 at 75 m (depth-related parameter).
- Volumetric water content (Hourly)
  - Filename: COSMOS-UK_VolumetricWaterContent_Hourly_2013-2016.csv
  - Variables: Corrected cosmic-ray neutron counts; Volumetric water content (%; hourly average); D86 at 75 m.

## Data collection, processing and provenance
- Data are measured on-site using a range of instruments and logged locally, then telemetered hourly to a central system at CEH Wallingford.
- Hydrometeorological data feed subsequent processing steps to derive PET and VWC values.
- VWC daily data are derived from hydrometeorological data, cosmic-ray sensor data, and background neutron counts from the Jungfrau neutron monitoring station (Switzerland), using established methods (Evans et al. 2016; Köhli et al. 2015 for depth-specific calculations).
- Quality control (QC) tests are applied to all data; detailed QC procedures are described in the COSMOS-UK User Guide.

## Metadata and data governance
- Metadata and instrumentation details are documented in the COSMOS-UK User Guide.
- Data and variables are defined per site; full site metadata (location, calibration status, start dates) is provided in the COSMOS-UK sites section.
- Data are stored and accessible via the NERC Environmental Information Data Centre (EIDC); underlying data sharing and governance follow project and data centre standards.

## Site coverage and calibration
- 42 COSMOS-UK sites with varying start dates (2013–2016) and coordinates (Easting, Northing, Altitude).
- Calibration status (CALIBRATED = Y/N) varies by site; some sites (e.g., Cwm Garw) are not calibrated.
- Wytham Woods data end in 2016 due to decommissioning; other network data availability is described in the corresponding User Guide.

## Key methodological notes and caveats
- PET is derived daily from 30-minute hydrometeorological/soil data using the Penman-Monteith method (FAO-56).
- Daily VWC is derived from hydrometeorological data, cosmic-ray neutron counts, and background neutron data, with corrections and depth-specific calculations (including D86 at 75 m).
- Hourly VWC data are available and derived similarly at 1-hour resolution.
- Some variables have site-specific availability constraints:
  - Snow depth measured only at a subset of sites (e.g., Cwm Garw, Easter Bush, Gisburn Forest, Glensaugh, Moor House, Sourhope, etc.).
  - Wind components (X, Y, Z) not measured at certain sites (Alice Holt, Chimney Meadows, Harwood Forest, Sheepdrove, Waddesdon, Wytham).
- Data quality relies on calibration, instrument performance, and correction factors; see User Guide for details on instrumentation and variable-specific processing.
- Data include potential barriers related to metadata completeness and data sharing, which are acknowledged as general challenges in monitoring framework contexts.

## References
- Evans et al. (2016). Soil water content in southern England derived from a cosmic-ray soil moisture observing system - COSMOS-UK. Hydrological Processes, 30, 4987-4999.
- FAO (1998). Crop evapotranspiration: Guidelines for computing crop water requirements. FAO Irrigation and Drainage Paper 56.
- Köhli et al. (2015). Footprint characteristics revised for field-scale soil moisture monitoring with cosmic-ray neutrons. Water Resources Research, 51(7), 5772-5790.
- COSMOS-UK User Guide (as referenced for instrumentation and data processing details).