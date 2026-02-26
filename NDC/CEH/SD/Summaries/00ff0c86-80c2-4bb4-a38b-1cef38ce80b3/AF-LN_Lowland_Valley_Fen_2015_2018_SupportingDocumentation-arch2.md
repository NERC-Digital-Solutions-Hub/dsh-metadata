# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a lowland valley fen, Anglesey, UK, 2015 to 2018

## Overview
- Time series of land surface–atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum flux (τ) measured at AF-LN fen, Anglesey, UK.
- Monitoring period: 2015-01-01 00:30 to 2018-10-11 00:00.
- Includes ancillary meteorological and soil-physics observations and turbulence-characterising variables.
- Data processed with standardized, published methodologies; dataset designed for assessment of environmental health and ecosystem carbon balance.

## Study Site
- Location: AF-LN flux site, Cors Erddreiniog National Nature Reserve, Anglesey, North Wales (53° 18' 37.18'' N, 4° 17' 28.06'' W, 63 m amsl).
- Habitat: High-quality lowland valley-head fen with low-intensity pony grazing; peat-dominated with marl bands.
- Climate: Temperate maritime; mean annual air temperature ~10.4°C and precipitation ~841 mm (1981–2010).
- Peat characteristics: Deep peat to ~2.5 m, low bulk density (0.17 g cm^-3), high carbon content (45.3%).
- Land management and permissions: Managed for conservation; permission granted by Natural Resources Wales.

## Data Collection and Instrumentation

### Flux data acquisition
- Eddy covariance (EC) measurements above grass canopy at 2.0 m height.
- Instruments: CSAT3 ultrasonic anemometer + LI-7500 CO2/H2O infrared analyser.
- Raw data: 20 Hz measurements of wind components, sonic temperature, H2O and CO2 densities.
- Data logging: CR3000 Micrologger.

### Ancillary data acquisition
- Meteorology and soil physics co-located with EC station.
- Measurements at 2.0 m: air temperature (Ta), relative humidity (RH).
- Net radiation (Rnet), incoming shortwave radiation (SWin), soil heat flux at two locations (G1, G2), soil temperature (Tsoil1 at 0.05 m), precipitation (ARG10 gauge).
- Data reported as 30-minute means (and sums for precipitation).

## Data Processing and Quality Control

- Flux calculations: Turbulent flux densities computed with EddyPRO v6.1; 30-minute block averages.
- Processing steps included: QC of 20 Hz data, angle-of-attack correction, 2D rotation to align with local terrain, corrections for co-spectral attenuation, humidity effects on H, density corrections on LE and CO2, and random uncertainty estimates.
- Derived turbulence metrics: wind speed/direction, friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L), stability parameter z/L, and flux footprint estimates.
- Quality control (QC): 
  - Outliers removed with median absolute deviation criteria.
  - Non-stationary turbulence periods excluded.
  - Flux ranges applied: H [-200, 500] W m^-2, LE [-60, 500] W m^-2, NEE [-50, 30] μmol CO2 m^-2 s^-1.
  - NEE omitted when nighttime fluxes were negative or when u* < 0.18 m s^-1.
  - Weekly visual checks for additional outliers, manually removed as needed.

## Gap-filling and Flux Partitioning

- Gap filling: Marginal Distribution Sampling (MDS) approach (Reichstein et al., 2005).
- Flux partitioning: NEE partitioned into Gross Ecosystem Production (GEP) and Total Ecosystem Respiration (TER) using Ta-driven algorithms (Reichstein et al., 2005).
- Tools: REddyProc (R package) for gap-filling and partitioning (Reichstein et al., 2016).
- Meteorological gaps: Filled where possible using observations from a nearby second EC station within 1 km.

## Data Structure and Variables

- Output: Single CSV file with 30-minute time steps from 2015-01-01 00:30 to 2018-10-11 00:00.
- Missing data marker: -9999.
- Recorded variables (examples):
  - NEE, NEE_sd, NEE_filled, NEE_filled_sd
  - LE, LE_sd, LE_filled, LE_filled_sd
  - H, H_sd, H_filled, H_filled_sd
  - Tau, Tau_sd
  - CO2_strg, LE_strg, H_strg, Pa, Ta, RH, VPD, SWin, Rnet, G1, G2, Tsoil1
  - Precipitation, WS, WD, Ustar, TKE, L, zL, x_peak, x_70, x_90 (footprint metrics)
  - GEP, TER (partitioned fluxes)
- Units and descriptions follow standardized formats (Table 1 in the dataset documentation).

## Data Quality and Documentation

- Data processing and QC follow established micrometeorological protocols (Papale et al.; Mauder et al.; Moncrieff et al.; Reichstein et al.; Wilczak et al.).
- Uncertainty estimates included for flux measurements.
- Data provenance and processing chain documented, enabling reproducibility and cross-study comparability.

## Context, Access and Acknowledgments

- Funding and support: Natural Environment Research Council (NE/R016429/1) under UK-SCAPE; Defra SP1210 project. Acknowledgement of permission from Natural Resources Wales.
- Relevance: Provides standardized, quality-controlled measurements of GHG fluxes and energy exchanges in peatland ecosystems—valuable for environmental health assessment, carbon balance studies, and policy-relevant environmental monitoring.
- References include foundational methodological papers and dataset-specific sources cited in the documentation.