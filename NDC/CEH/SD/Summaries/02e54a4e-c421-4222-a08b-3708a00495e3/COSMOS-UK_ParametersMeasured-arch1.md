# Daily and sub-daily hydrometeorological and soil data (2013-2016) [COSMOS-UK]

## Overview
- Dataset from the COSMOS-UK network covering 42 sites during Oct 2013–Dec 2016.
- Stored in the Environmental Information Data Centre (EIDC) as part of the COSMOS-UK data package.
- Data split into four CSV files: Hydrometeorological and soil; Potential evapotranspiration; Volumetric water content (daily); Volumetric water content (hourly).
- Information herein applies to sites installed before end of 2016; broader network data described in the COSMOS-UK User Guide.

## Data files and contents
- Hydrometeorological and soil (COSMOS-UK_Hydrometeorological&Soil.csv)
  - 30-minute resolution measurements across all sites.
  - Variables include: longwave and shortwave radiation (incoming/outgoing), net radiation; precipitation; atmospheric pressure; air temperature; wind speed and components; relative humidity; absolute humidity; snow depth; soil temperature at multiple depths; volumetric water content (VWC) at multiple sensors; soil heat flux.
  - Time stamps: yyyy-mm-dd hh:mm GMT.
  - Units: as specified (e.g., W/m² for radiation, mm for precipitation, hPa for pressure, °C for temperature, m/s for wind, % for humidity).

- Potential evapotranspiration (COSMOS-UK_PotentialEvapotranspiration.csv)
  - Derived daily from 30-minute hydrometeorological and soil data.
  - Variable: Potential Evapotranspiration (mm/day).
  - Calculation: Penman-Monteith method (FAO 56).

- Volumetric water content data (Daily) (COSMOS-UK_VolumetricWaterContent_Daily.csv)
  - Daily resolution; derived from hydrometeorological data and Cosmic-ray sensing probe.
  - Variables: Volumetric Water Content (VWC, %); D86 at 75 m (depth) data (cm).
  - D86 values derived per the methods in Evans et al. 2016.

- Volumetric water content data (Hourly) (COSMOS-UK_VolumetricWaterContent_Hourly.csv)
  - Hourly resolution; derived similarly to daily VWC.
  - Variables: Corrected COSMOS neutron counts (counts); Volumetric Water Content (VWC, %); D86 at 75 m (cm).

## Data resolution and time period
- Hydrometeorological and soil data: 30-minute temporal resolution (Oct 2013–Dec 2016).
- Potential evapotranspiration: daily resolution (derived from the 30-minute data).
- Volumetric water content: daily (primary) and hourly (alternative) resolutions for 42 sites (Oct 2013–Dec 2016).
- Spatial scope: 42 COSMOS-UK sites with site-specific calibration status and coordinates.

## Measurement, derivation, and instrumentation
- On-site data collection: range of instruments; data logged locally and telemetered to CEH Wallingford hourly.
- Volumetric water content: derived from COSMOS cosmic-ray neutron counts plus background neutron data (Jungfrau station, Switzerland); daily VWCs follow Evans et al. 2016; D86 adjustments follow Köhli et al. 2015.
- Potential evapotranspiration: calculated after daily data collection using Penman-Monteith (FAO-56) methodology.
- Instrumentation details and exact variable mappings are provided in the COSMOS-UK User Guide.

## Quality control and documentation
- All data undergo quality control tests; details of tests and variable-specific applications are in the COSMOS-UK User Guide.
- Supporting documentation and references provided for methods and corrections (e.g., Evans et al. 2016; Köhli et al. 2015; FAO 56).

## COSMOS-UK sites and metadata
- The dataset includes site metadata (Site_ID, START_DATE, CALIBRATED status, Easting, Northing, Altitude) for 42 sites (e.g., Alice Holt, Chimney Meadows, Easter Bush, Gisburn Forest, Plynlimon, Rothamsted, etc.).
- Site-specific calibration status and coordinates are provided; detailed site list and map are included in the accompanying documentation.
- Certain site-specific data nuances exist, such as snow depth measurements only at a subset of sites and absence of specific wind components at some sites.

## Access and usage notes
- Data available for sites installed before the end of 2016; for additional network data and data processing/availability beyond 2016, refer to the COSMOS-UK User Guide.
- Data processing workflows and instrumentation details are outlined in the User Guide; use these to interpret variables, calibrations, and derivation methods.
- References for methods: Evans et al. 2016 (COSMOS-UK soil moisture via cosmic-ray neutrons), FAO-56 (Penman-Monteith), Köhli et al. 2015 (D86 footprint corrections).

## References
- Evans J. G. et al. (2016). Soil water content in southern England derived from a cosmic-ray soil moisture observing system - COSMOS-UK. Hydrol. Process., 30, 4987-4999.
- FAO (1998). Crop evapotranspiration: Guidelines for computing crop water requirements. FAO Irrigation and drainage paper 56.
- Köhli M. et al. (2015). Footprint characteristics revised for field-scale soil moisture monitoring with cosmic-ray neutrons. Water Resour. Res., 51(7), 5772-5790.
- COSMOS-UK User Guide (and related documentation).