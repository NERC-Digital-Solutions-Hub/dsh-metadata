# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a pasture, Yorkshire, UK, 2021-2023

- The dataset provides 30-minute observations of land-atmosphere exchange, including net ecosystem CO2 exchange (NEE) and sensible (H) and latent heat (LE) fluxes, collected over about 1.5 years at an agriculturally managed pasture in Yorkshire, UK.
- In addition to fluxes, the dataset includes weather and soil physics measurements collected with automated instruments.

## Study site and context

- Location: field at the University of Leeds Research Farm (coordinates provided in the dataset).
- Management: grazed by sheep since 2012; occasionally cut for silage; no irrigation or chemical fertilisers applied.
- Climate and soil: temperate oceanic climate; typical air temperature around 9.5°C and rainfall ~885 mm annually; soil is loamy calcareous brown earth (pH ~6.8) with 0–30 cm carbon and nitrogen ~27.7 g kg^-1 and 2.3 g kg^-1.
- Land use during measurement: silage cut in July 2022; periodic grazing throughout the period.

## Data collection and instrumentation

- Measurement period: 01/09/2021 to 01/01/2023.
- Flux measurements: automated eddy covariance (EC) method above the canopy at 2 m height; closed-path CO2/H2O analyser (LI-7200RS) and 3D sonic anemometer (Gill Windmaster).
- Data acquisition: sampled at 10 Hz and aggregated to 30-minute means; loggers used include CR1000X and Smartflux 2.
- Ancillary measurements (CO2, heat, and radiation flux context): net radiation, short- and long-wave radiation, air temperature, relative humidity, soil temperature and soil moisture (5 cm depth) using SN-500, HMP155, and TEROS-11 sensors.
- Data processing workflow and software: EddyPro 7 for flux calculation; alignment and corrections for instrument angle of attack, time lags, and spectral attenuation.

## Data processing and quality control

- Processing steps: conditioning of raw data, angle-of-attack correction, cross-correlation for time lags, high- and low-frequency attenuation corrections; random uncertainty estimated following established methods.
- Quality control (QC): performed in R; data removal criteria include statistical outliers, GLI-CO2 signal anomalies (>10% above baseline), nonrepresentative footprint (>20% outside site boundaries), unrealistic flux thresholds (H, LE, NEE ranges), and friction velocity threshold (u* < 0.14 m s^-1).
- Gap-filling and flux partitioning: NEE gaps filled using marginal distribution sampling; uncertainty of filled values estimated from the contributing data; partitioning performed with REddyProc (to obtain Reco and GPP components).

## Data structure and contents

- Primary data file: Yorkshire_Pasture_2021_2023.csv.
- Columns include:
  - Time: Date (dd/mm/yyyy) in GMT and Time (HH:MM:SS) in GMT.
  - Fluxes (before gap-filling): NEE (μmol m^-2 s^-1), LE (W m^-2), H (W m^-2) with corresponding uncertainties.
  - Storage terms: CO2_strg, LE_strg, H_strg (μmol CO2 m^-2 s^-1 or W m^-2 as specified).
  - Meteorology: Pa (kPa), Tair (°C), RH (%), VPD (various units), SWin/SWout/LWin/LWout/Rnet (W m^-2), PAR (W m^-2), windspeed (m s^-1), winddir (degrees), Ustar (m s^-1), TKE, Tstar, L, (z-d)/L (stability parameter).
  - Soil and moisture: Tsoil (°C), VWC (%), G (soil heat flux, W m^-2).
  - Sensor and structural data: NEE_f (gap-filled NEE), NEE_f_sd (uncertainty of gap-filled NEE), Reco (ecosystem respiration), GPP (gross primary productivity).
- Notes: NA values indicate missing data; the dataset provides both pre-gap-filled and gap-filled outputs.

## Outputs and data products

- The dataset supports end-user exploration and self-service analysis of carbon, energy, and water fluxes in a temperate pasture environment.
- Includes gap-filled fluxes and partitioned components (GPP and Reco) for straightforward interpretation and model validation.
- Suitable for analyses requiring data provenance, quality flags, and uncertainty estimates.

## Acknowledgements and references

- Funding: Leeds-York-Hull Natural Environmental Research Council (NERC) DTP Panorama grant NE/S007458/1.
- Acknowledges field site access and management information.
- Key references relate to EddyPro processing, gap-filling algorithms, QC criteria, and footprint considerations.