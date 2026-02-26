# Turbulent fluxes of sensible heat and momentum at an ancient deciduous broadleaved forest in southern England

## Overview
- Time series of turbulent surface–atmosphere exchanges: sensible heat (H) and momentum flux (τ) measured via eddy covariance at Wytham Woods, Oxfordshire, UK.
- Coverage: 2014-06-13 13:00 to 2016-01-04 22:00.
- Includes ancillary meteorological and soil physics observations, plus turbulence and quality-of-flux metrics.
- Dataset designed for integration with a broader data system (QC, metadata, footprints) to support data-driven decision making and research on land–atmosphere exchanges.

## Study site
- Wytham Woods flux observation site (approx. 400 ha ancient broadleaved forest), ~5 km NW of Oxford.
- Climate: temperate maritime; mean annual temp ~10.1°C, precipitation ~730 mm.
- Flux tower mounted on a canopy of ~20 m, located on a north-facing slope.
- Surrounding land use: arable agriculture; soils range from poorly to well drained clays over sandstone.

## Sampling regime and flux data acquisition
- Measurements taken above the canopy at 27 m height using a 20 Hz sonic anemometer; 30-minute flux means used for analysis.
- Raw EC data: three velocity components and sonic temperature; log at 20 Hz.
- Ancillary data: air temperature, relative humidity, net radiation and components, soil heat flux at two locations, soil moisture and soil temperature at two depths, precipitation.
- Co-located data from COSMOS-UK station merged with site observations for a comprehensive dataset.

## Data processing
- Flux calculations performed with EddyPRO® v6.1; corrections include:
  - Boost-bug correction for wind measurements.
  - Angle-of-attack correction for Gill sonic anemometers.
  - 2D coordinate rotation to align with local terrain.
  - Correcting for spectral attenuation and humidity effects.
  - Random uncertainties for H and τ estimated.
- Quality control (QC) flags for 30-minute fluxes with a high (0), acceptable (1), and poor (2) scheme.
- Derived variables: wind speed/direction, friction velocity (u*), Turbulent Kinetic Energy (TKE), temperature scaling (T*), Obukhov length (L), stability parameter (z/L), and flux footprint estimates (X_peak, X_10, X_30, X_50, X_70, X_90).

## Quality control
- Outliers removed using median absolute deviation; further checks ensure EC method validity.
- H and τ fluxes with QC > 1 excluded; H flux range checked (-200 to 600 W m^-2).
- Daily/weekly visual checks to identify and remove clearly erroneous values.
- Users decide whether to exclude QC > 0 fluxes or apply additional filters (e.g., u*, footprint).

## Data structure and access
- Data provided as a single CSV file: WythamWoodsMicromet_v1.0.csv.
- Time series begin 2014-06-13 13:00 and end 2016-01-04 22:00.
- Missing records denoted by -9999.
- Variables and units described in Table 1; names/units adapted from Li-COR Biosciences guidance.

## Variables and units (selected)
- DateTime; H (W m^-2); rand_err_H; qc_H; τ (kg m^-1 s^-2); rand_err_Tau; qc_Tau.
- Wind speed (ms^-1); max_wind_speed; wind_dir (degrees); Ustar (ms^-1); TKE (m^-2 s^-2); Tstar (K); L (m); zL (dimensionless).
- Footprint metrics: X_peak, X_10, X_30, X_50, X_70, X_90 (m).
- Radiation: SW in/out, LW in/out, R net.
- Soil/air heat flux: SHF_1, SHF_2 (W m^-2).
- Atmospheric/soil sensors: Ta (°C), RH (%), Pa (kPa); Ts_1, Ts_2 (soil temperatures, °C); VWC_1, VWC_2 (%).
- Precip (mm per 0.5 h).
- Table 1 notes: units and descriptions follow Li-COR conventions.

## Data provenance and acknowledgments
- Funded by the Natural Environment Research Council (NERC).
- Ancillary data contributed by the COSMOS-UK network; site access permissions provided by University of Oxford.
- Technical support and installation/maintenance acknowledged.

## Relevance for data leadership and strategy
- Demonstrates a coherent, end-to-end data product: raw observations, rigorous processing, quality control, and derived analytics (footprints, turbulence metrics).
- Emphasizes documentation, metadata, and data governance (QC flags, missing value coding, processing provenance).
- Highlights challenges for data systems: fragmented ancillary data sources, need for harmonized metadata, and clear data quality indicators to enable reuse across teams and networks.
- Provides a ready-to-integrate case study for cross-organization data strategy: standardized processing pipelines, traceable lineage, and transparent data quality metrics to support policy, science, and stakeholder collaboration.