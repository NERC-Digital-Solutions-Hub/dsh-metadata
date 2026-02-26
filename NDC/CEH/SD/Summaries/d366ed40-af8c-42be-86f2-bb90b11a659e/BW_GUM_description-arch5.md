# This document describes the dataset submitted under filename BW_GUM_2018_2020.csv

## Overview
- Continuous time-series dataset of heat (latent and sensible) and trace gas (CO2 and CH4) fluxes obtained by eddy-covariance, gas concentrations, and ancillary meteorological data.
- Location: Guma Lagoon, Okavango Delta, Botswana (18°57'53.01"S; 22°22'16.20"E); over a Cyperus papyrus stand.
- Period and cadence: 01/01/2018 to 31/12/2020; measurements reported at half-hourly intervals.
- Data gaps: missing data encoded as -9999 due to instrumentation downtime.
- File reference: BW_GUM_2018_2020.csv.

## Data content and variables
- Primary flux variables (half-hourly):
  - H (sensive heat flux), LE (latent heat flux), co2_flux (CO2 flux), ch4_flux (CH4 flux).
- Quality flags for fluxes:
  - qc_H, qc_LE, qc_co2_flux, qc_ch4_flux (0 = good, 1 = fair, 2 = poor).
- Ancillary gas and environmental variables:
  - co2_mole_fraction, h2o_mole_fraction, ch4_mole_fraction
  - VPD (vapour pressure deficit), wind_speed, wind_dir
  - ustar (friction velocity), stability
  - PAR (photosynthetically active radiation), Rg (total incoming radiation)
  - RH (relative humidity), Pair (air pressure), Tair (air temperature)
- Metadata for variables provided in Table 1 (names, units, and descriptions).

## Instrumentation and data processing
- Eddy-covariance instrumentation:
  - IRGASON (3D ultrasonic anemometer + open-path CO2 and H2O gas analyzer)
  - LI-COR 7700 open-path CH4 analyser
  - Orientation aligned with prevailing wind
- Meteorological sensors:
  - Vaisala WXT520 (air temperature, pressure, RH, wind speed/direction)
  - Skye Instruments pyranometer (PAR) and quantum detector
- Data logging:
  - Campbell Scientific CR3000; EC data at 10 Hz, meteorological data at 10 s
- Site setup:
  - Mounted on a 3 m tripod on a 3 m platform; effective measurement height ~5.5 m
  - Location relative to papyrus mat: ~30 m west; canopy height ~2.5 m
  - Flux footprint restricted to wind sector 60°–190°
- Data processing and quality control:
  - Processed into half-hourly fluxes using EddyPro software v7.0.6
  - Quality controlled by Dr. Helfter
- Personnel:
  - Installation by Dr Carole Helfter; monthly maintenance/data collection by Dr Mangaliso Gondwe

## Data quality, provenance, and metadata
- Clear documentation of instrument models, heights, and processing workflow to support reproducibility.
- Quality flags accompany flux variables to indicate data reliability (0 = good, 1 = fair, 2 = poor).
- provenance includes: site description, sensor arrangement, processing software, and responsible researchers.

## Data governance considerations for reuse
- Access and sharing:
  - Dataset submitted as BW_GUM_2018_2020.csv; no explicit embargo or access restrictions stated.
- Currency and updates:
  - Data cover 2018–2020; ongoing updates or reprocessing not described.
- Interoperability and standards:
  - Uses standard flux conventions (H, LE, co2_flux, ch4_flux) with explicit units; quality flags enable filtering for analyses.
- Completeness and limitations:
  - Gaps present (represented as -9999); footprint limitation means data from wind sectors outside 60°–190° should be treated with caution or excluded.
  - Specific to a Cyperus papyrus stand at a single site; spatial generalizability limited.
- Documentation needs:
  - Metadata includes coordinates, measurement heights, instrumentation, data processing version, and quality flags; consider providing a data catalog entry with variable descriptions, units, and QC criteria for broader discoverability.

## Limitations and caveats
- Data restricted to a defined footprint; other wind sectors may not represent homogeneous conditions.
- Some data quality is flagged as fair or poor (qc values 1 or 2), requiring careful filtering for robust analyses.
- Missing data encoded as -9999; users should apply appropriate gap-filling or QC filtering.

## References
- Background on the Okavango Delta hydrology and related literature cited, indicating broader context for the data site and environmental conditions.