# Supporting documentation for COSMOS-UK (2018). Daily and sub-daily hydrometeorological and soil data (2013-2016) [COSMOS-UK]. NERC Environmental Information Data Centre.

## Overview
- Framework: COSMOS-UK network data collected between Oct 2013 and Dec 2016.
- Scope: 42 sites with both hydrometeorological and soil measurements.
- Data access: Stored at the Environmental Information Data Centre (EIDC); site installations prior to end of 2016; Wytham Woods ends 01-Oct-2016.
- Data products: Four CSV files (hydrometeorological & soil; potential evapotranspiration; daily volumetric water content; hourly volumetric water content).
- Reference material: COSMOS-UK User Guide for data processing and availability.

## Data files and structure
- File 1: Hydrometeorological and Soil ( COSMOS-UK_Hydrometeorological&Soil_2013-2016.csv )
  - Resolution: 30-minute data.
  - Variables include: Wm-2 incoming/outgoing longwave and shortwave radiation, net radiation; Precipitation (mm, total); Atmospheric Pressure (hPa); Air Temperature (°C); Wind speed (m/s) and Wind direction (degrees); Relative Humidity (%); Snow depth (mm; measured at a subset of sites); Wind components (X, Y, Z) at selected sites; Soil temperature (TDT1, TDT2, profile depths) and Volumetric Water Content (VWC) at sensor depths; D86 (soil measurement depth) at 75 m distance from cosmic-ray sensor; and corrected neutron counts data used for VWC.
  - Metadata: Site, DateTime (yyyy-mm-dd hh:mm GMT), units, and notes.
  - Data flow: Measured on-site, telemetered hourly to CEH Wallingford central system.

- File 2: Potential Evapotranspiration ( COSMOS-UK_PotentialEvapotranspiration_2013-2016.csv )
  - Resolution: Daily (derived from 30-minute data).
  - Variable: Potential Evapotranspiration (mm/day), calculated for all sites.
  - Derivation: Penman-Monteith method (FAO 56) using on-site hydro data.

- File 3: Volumetric Water Content Daily ( COSMOS-UK_VolumetricWaterContent_Daily_2013-2016.csv )
  - Resolution: Daily (avg values).
  - Variables: Volumetric Water Content (%) and D86 at 75 m from cosmic-ray sensor (cm).
  - Derivation: From hydro data and cosmic-ray neutron data; daily averages per Evans et al. 2016; D86 values per Köhli et al. 2015.

- File 4: Volumetric Water Content Hourly ( COSMOS-UK_VolumetricWaterContent_Hourly_2013-2016.csv )
  - Resolution: Hourly.
  - Variables: Corrected cosmic-ray neutron counts (counts); Volumetric Water Content (%) and D86 at 75 m (cm).
  - Derivation: Hourly VWC derived from hydro and neutron data; correction factors per Evans et al. 2016 and Köhli et al. 2015.

## Temporal resolution and access
- Hydro data: 30-minute intervals.
- PET: Daily totals derived from 30-minute data.
- VWC: Daily (primary) and hourly (secondary) derived datasets.
- Access notes: Data reside in EIDC; refer to COSMOS-UK_UserGuide.pdf for instrumentation details, processing, and data availability.

## Variables, measurement, and site coverage
- All sites provide hydro and soil variables except:
  - Snow depth: measured only at a subset (e.g., Cwm Garw, Easter Bush, Gisburn Forest, Glensaugh, Moor House, Plynlimon, Sourhope).
  - X, Y, Z wind components: not measured at all sites (e.g., Alice Holt, Chimney Meadows, Harwood Forest, Sheepdrove, Waddesdon, Wytham).
- Data are measured by on-site instruments and logged locally, then telemetered hourly to the CEH Wallingford system.
- Instrumentation details and variable mappings per instrument are documented in the COSMOS-UK User Guide.
- Quality control: All data subjected to QC tests; details in COSMOS-UK User Guide.

## Spatial coverage and site metadata
- 42 COSMOS-UK sites with precise coordinates and identification (Site_ID, Easting/Northing, Altitude, Start Date, Calibrated status).
- A map (Figure 1) provides site locations.
- Example notes:
  - Wytham Woods decommissioned after 01-Oct-2016.
  - Start dates and calibration status vary by site.

## Derived data methods and references
- PET: Penman-Monteith method (FAO 56).
- VWC Daily: derived from corrected cosmic-ray neutron counts and hydro data (Evans et al. 2016); D86 depths from Köhli et al. 2015; corrections as per COSMOS-UK User Guide.
- VWC Hourly: derived hourly from similar inputs; uses background neutron counts (Jungfrau station data) and Najor correction factors.

## GIS-focused implications and usage
- Spatially aligns with site coordinates, enabling regional mapping of hydrometeorological conditions, soil moisture proxies (VWC), and PET across 42 UK sites.
- Useful for creating time-series, heat-maps, or animated maps showing spatial-temporal patterns (30-min to daily resolution).
- Data can be joined to GIS layers using Site_ID or geographic coordinates; be mindful of time zone (GMT) and differing resolutions when synchronizing layers.

## Notes and caveats for users
- Data availability pertains to sites installed before end of 2016; some sites have partial measurements or decommissioning dates.
- Snow depth and high-frequency wind components may be missing for certain sites; verify site-specific metadata.
- Derived data rely on multiple data streams and correction factors; consult the COSMOS-UK User Guide for full methodology and latest corrections.

## References
- Evans et al., 2016. Soil water content in southern England derived from a cosmic-ray soil moisture observing system - COSMOS-UK. Hydrol. Process.
- Köhli et al., 2015. Footprint characteristics revised for field-scale soil moisture monitoring with cosmic-ray neutrons. Water Resour. Res.
- FAO, 1998. Crop evapotranspiration: Guidelines for computing crop water requirements. FAO Irrigation and drainage paper 56.
- COSMOS-UK User Guide (supplementary documentation).