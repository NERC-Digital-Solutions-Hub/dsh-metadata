# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a cropland and a grassland on lowland peatland soils, East Anglia Fens, UK, 2016 to 2019

- Overview: A time series dataset of land-surface–atmosphere exchanges, including net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ), measured at two managed lowland peatland environments in the East Anglian Fens, UK. Ancillary weather and soil observations and turbulence-characterising variables are included.

## Study sites

- Location: East Anglian Fens (Fenland), UK; peat soils with historical drainage and agricultural use.
- Cropland (EF-SA): High-value horticultural crops (lettuce, celery, cereals); highly degraded fen peat overlying clay; drainage via subsurface pipes; peat depth 0.75–1.0 m; soil properties and land management details provided.
- Grassland (EF-GF): Former arable peatland restored to wetland; low-intensity grazing and occasional cutting; peat depth ~2.0 m; soil pH 5.2–6.0; residual drainage network present but not connected to regional system.

## Sampling regime

- Flux observations: Automated measurements above canopy at 2.6 m height.
- Time frame: EF-SA from 2016-11-17 to 2018-09-24; EF-GF from 2017-04-27 to 2019-03-31.
- Data granularity: 20 Hz raw data for turbulence and gas measurements; 30-minute summed/averaged fluxes.

## Flux data acquisition

- Instruments: Open-path eddy covariance systems with ultrasonic anemometer and LI-7500 CO2/HO2 sensor; two wind speed sensors (Gill WindMaster at EF-SA; Solent R3 at EF-GF).
- Data captured: U, V, W components, sonic temperature, density of water vapour and CO2; logged with CR3000 data loggers.

## Ancillary data acquisition

- Meteorology and soil sensors co-located with EC stations.
- Key variables: Air temperature (Ta), relative humidity (RH), net radiation (Rnet) and its components (SWin, SWout, LWin, LWout), soil heat flux (G) at two locations, water table/water level, soil moisture (VWC) at multiple depths, soil temperature (Tsoil) at several depths, precipitation (co-located rain gauges).
- Data cadence: Co-located measurements provided as 30-minute means or sums.

## Data processing

- Flux calculation: Turbulent flux densities computed from 20 Hz data using EddyPRO v6.1; 30-minute block-averaged fluxes.
- Corrections and QC: Quality control using standard procedures (outlier removal, non-stationarity checks, coordinate rotation, angle-of-attack correction, spectral corrections, density corrections for LE and CO2, etc.); uncertainty estimates for fluxes.
- Derived metrics: Footprint estimates, friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L), stability parameter (z/L); additional flux-related metrics produced.

## Quality control

- Outlier handling: Median absolute deviation method; removal of non-stationary turbulence periods; flux ranges filtered (H, LE, NEE); NEE filtered by night-time behavior and u* thresholds (EF-SA: 0.22 m s^-1; EF-GF: 0.16 m s^-1).
- Representativeness: Retained fluxes only if >75% of flux originated from within target ecosystem per footprint model.
- Visual checks: Weekly plots to identify and remove obvious errors.

## Data gap-filling and flux partitioning

- Gap-filling: Missing EC data (NEE, LE, H) filled with Marginal Distribution Sampling (Reichstein et al., 2005).
- Flux partitioning: NEE separated into GEP and TER using Ta-driven approach; implemented via REddyProc in R (Reichstein et al., 2016).
- Outputs: Gap-filled fluxes and partitioned components available for the full period of record.

## Details of data structure

- Data files: Two separate CSV files containing the time series data; gap-filled and partitioned data provided as complete series for each site.
- Missing data: Represented by -9999 for gaps due to failures or QC filtering.
- Variable references: Column names and units described in Table 1 of the dataset documentation.

## Nature and units of recorded values

- Core variables (sampled as 30-minute time series):
  - NEE: μmol CO2 m^-2 s^-1 (before gap-filling) and NEE_filled (gap-filled)
  - NEE_sd: standard deviation of NEE
  - LE: W m^-2 (latent heat) and LE_filled
  - LE_sd: SD of LE
  - H: W m^-2 (sensible heat) and H_filled
  - H_sd: SD of H
  - Tau: kg m^-1 s^-2 (momentum flux) and Tau_filled
  - Tau_sd: SD of Tau
  - Additional diagnostics: CO2_strg, LE_strg, H_strg, Pa, Ta, RH, VPD, SWin, SWout, LWin, LWout, Rnet, G1, G2, Tsoil1–3, VWC1–4, Precipitation, WaterLevel, Windspeed, Winddir, footprint parameters, u*, TKE, L, zL, NEE_filled_sd, GEP, TER
- Units and descriptions align with standard micrometeorological conventions and LI-COR outputs.

## Accessibility and usage

- Outputs are suitable for self-serve data exploration, dashboards, and further analyses by end users.
- Data quality and processing steps are documented, enabling reproducibility and appropriate interpretation of fluxes, gap-filled values, and partitioned components.
- Acknowledgments and references provide context on funding, site setup, and the processing methodology.