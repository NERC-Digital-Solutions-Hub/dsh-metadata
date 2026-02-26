# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a lowland valley fen, Anglesey, UK, 2015 to 2018

## Overview
- Time-series observations of net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ) fluxes measured via open-path eddy covariance (EC) at AF-LN site from 2015-01-01 00:30 to 2018-10-11 00:00.
- Includes ancillary meteorological and soil-physics variables and turbulence descriptors.
- Data processed to provide gap-filled, partitioned fluxes and extensive quality control and uncertainty estimates.

## Study site
- Location: AF-LN flux site, Cors Erddreiniog National Nature Reserve, Anglesey, North Wales (53° 18' 37.18'' N, 4° 17' 28.06'' W), elevation 63 m amsl.
- Habitat: Conservation-managed valley-head fen with low-intensity pony grazing.
- Climate: temperate maritime; mean 1981–2010 temp 10.4 ± 3.9 °C, precip 841 ± 41 mm yr⁻¹.
- Substrate: deep fen peat with marl bands; peat core data indicate uniform peat to ~2.5 m depth; peat bulk density ~0.17 g cm⁻³; carbon content ~45.3%.

## Data collected
- EC flux data: NEE (μmol CO2 m⁻² s⁻¹), H (W m⁻²), LE (W m⁻²), τ (kg m⁻¹ s⁻²) recorded at 20 Hz, aggregated to 30-min means.
- Instrumentation: CSAT3 ultrasonic anemometer and LI-7500 gas analyzer at 2.0 m height; data logger CR3000.
- Ancillary meteorology and soil observations: Ta, RH, Rnet, SWin, G (soil heat flux at two locations), Tsoil (0.05 m), precipitation (via tipping-bucket gauge), and wind metrics; logged as 30-min means or sums.
- Turbulence and footprint context: wind speed/direction, friction velocity (u*), TKE, Obukhov length (L), stability parameter z/L, and preliminary 1D flux footprint estimates (x_peak, x_70, x_90).

## Data processing
- Flux calculations: EddyPRO v6.1, with QC and corrections (angle-of-attack, rotation to local terrain, spectral attenuation, humidity and density corrections).
- Uncertainty: random uncertainties per flux estimated (per Reichstein et al.; Finkelstein & Sims).
- Footprint and turbulence metrics: from EddyPRO, including u*, TKE, L, z/L, and footprint estimates.

## Quality control
- Outlier detection: median absolute deviation; non-stationary turbulence removal; flux limits: H (-200 to 500 W m⁻²), LE (-60 to 500 W m⁻²), NEE (-50 to 30 μmol CO2 m⁻² s⁻¹).
- NEE flagged/removed when nighttime fluxes are negative and when u* below 0.18 m s⁻¹ (per Reichstein et al. 2016).
- Visual inspection: weekly plots of flux and ancillary data to remove clearly erroneous values.

## Gap-filling and flux partitioning
- Gap-filling: Marginal Distribution Sampling (MDS) approach (Reichstein et al., 2005) for NEE, LE, H.
- Partitioning: NEE partitioned into GEP (gross ecosystem production) and TER (total ecosystem respiration) using Ta-driven partitioning (Reichstein et al., 2005).
- Tools: REddyProc (R) for gap-filling and partitioning (Reichstein et al., 2016); meteorological gaps filled using a nearby station when possible.

## Data structure and units
- Format: a single CSV file with 30-minute time series; gap-filled and partitioned data provided as a complete series from 2015-01-01 00:30 to 2018-10-11 00:00.
- Missing data: represented by -9999.
- Table 1 variables (sampled/derived):
  - DateTime (dd-mm-yyyy HH:MM, UTC)
  - NEE, NEE_sd
  - LE, LE_sd
  - H, H_sd
  - Tau, Tau_sd
  - CO2_strg, CO2_strg_sd
  - LE_strg, LE_strg_sd
  - H_strg, H_strg_sd
  - Pa (kPa)
  - Ta (°C)
  - RH (%)
  - VPD (hPa)
  - SWin, Rnet
  - G1, G2 (soil heat flux)
  - Tsoil1 (°C)
  - Precipitation1 (mm, 0.5 h)
  - Precipitation2 (Total precipitation)
  - WS1, WS2 (wind speeds)
  - WD1, WD2 (wind directions)
  - Ustar (m s⁻¹)
  - TKE (m² s⁻²)
  - L (Obukhov length)
  - zL (stability parameter)
  - x_peak, x_70, x_90 (upwind distance metrics for flux footprint)
  - NEE_filled, NEE_filled_sd
  - LE_filled, LE_filled_sd
  - H_filled, H_filled_sd
  - TER, GEP

## Data availability and notes
- Data provenance: collected under Natural Environment Research Council (NE/R016429/1) and Defra SP1210; permission granted by National Resources Wales.
- Data product purpose: enables map-based data visualization and spatially-informed analyses of greenhouse gas fluxes on peatland habitats; includes footprint context for source-area interpretation.
- References and methodological sources provided for QA, processing, gap-filling, and flux partitioning.