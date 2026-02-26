# Turbulent fluxes of sensible heat and momentum at an ancient deciduous broadleaved forest in southern England

## Overview
- Time-series dataset of turbulent surface-atmosphere exchanges of sensible heat (H) and momentum (τ) measured above a 27 m forest canopy using eddy covariance (EC) at Wytham Woods, Oxfordshire, UK.
- Observation period: 2014-06-13 13:00 to 2016-01-04 22:00.
- Includes ancillary meteorological and soil-physics observations, plus turbulence and data-quality indicators.
- Aims aligned with monitoring framework needs: produce useful environmental health metrics, ensure data quality, and enable policy-relevant interpretation.

## Study site
- Location: Wytham Woods flux site (approximately 400 ha ancient broadleaved forest), ~5 km NW of Oxford.
- Climate: temperate maritime; mean annual temperature ~10.1°C; precipitation ~730 mm.
- Canopy/land cover: ~20 m canopy height; dominant tree species include Pedunculate Oak, Ash, Sycamore; site on a moderate slope with northerly exposure.
- Surrounding land use: nearby arable agriculture; soils range from poorly to well-drained clays over sandstone.
- Site context: part of ancient woodland with disturbance history; data sourced from established references (e.g., Thomas et al. 2011).

## Sampling regime
- Automated flux measurements conducted on a 27 m tower above the canopy.
- Flux sampling interval: 30 minutes for computed fluxes; raw data at 20 Hz for EC components.
- Ancillary meteorological and soil data collected concurrently from a co-located COSMOS-UK station; data merged to create a unified dataset.

## Flux data acquisition and processing
- Instruments: Windmaster sonic anemometer for turbulence; HMP45 for Ta and RH; CR3000 Micrologger for data logging.
- Processing: EddyPRO v6.1 used to compute fluxes and perform quality control; corrections applied include:
  - Boost-bug correction for vertical wind velocity
  - Angle-of-attack correction for Gill sonic anemometers
  - Two-dimensional tilt/coordinate rotation to align with terrain
  - Corrections for high/low-frequency co-spectral attenuation
  - Humidity-related correction for H
- Outputs include: H, τ with associated random uncertainties; derived metrics (u*, TKE, T*, L, z/L) and footprint/upslope diagnostics.

## Quality control and data quality
- QC workflow: identify and remove statistical outliers (median absolute deviation) for H; exclude any H/τ with QC flag > 1.
- Acceptable ranges: H restricted to -200 to 600 W m^-2; τ values flagged if outside expected ranges.
- Visual inspection: weekly checks of flux and ancillary data; clearly erroneous values removed.
- QC flag semantics: 0 = high quality, 1 = acceptable, 2 = poor; decisions on filtering left to data user.
- Uncertainty and data integrity: includes random error estimates for H and τ; provides data provenance and processing steps to aid reproducibility.

## Data structure and content
- Data file: single CSV (WythamWoodsMicromet_v1.0.csv) containing complete 2014-06-13 13:00 to 2016-01-04 22:00 time series.
- Missing data: denoted by -9999 for any missing records.
- Variables and units: 30-minute time-series with fields including DateTime, H, rand_err_H, qc_H, Tau, rand_err_Tau, qc_Tau, wind_speed, max_wind_speed, wind_dir, Ustar, TKE, Tstar, L, zL, X_peak, X_10/30/50/70/90 (upwind footprint metrics), radiation components (SW in/out, LW in/out), net radiation (R net), soil heat flux (SHF_1, SHF_2), Ta, RH, Pa, Ts (soil temperatures at two depths/locations), VWC (volumetric water content), Precip.
- File format details: Table 1 describes variables and their units; data are columnar and aligned with standard micrometeorological conventions.

## Data provenance, access, and governance
- Data collection funded by NERC; ancillary weather data provided by COSMOS-UK network.
- Dataset designed to support open-data sharing and transparent governance, with clear metadata on processing steps and QC.
- Data user guidance: decide on including/excluding data based on QC flags and footprint metrics; complete traceability from raw 20 Hz data to final 30-minute fluxes.
- Acknowledgments reflect collaboration and permissions for site access; references document methodological foundations and quality-control standards.

## Implications for monitoring frameworks
- Demonstrates end-to-end workflow from raw EC measurements to curated, QA/QC’d flux products suitable for policy-relevant environmental health assessments.
- Highlights the importance of:
  - Standardized processing pipelines (EddyPRO-based workflows) and documented corrections
  - Comprehensive QC flags and uncertainty estimates to inform decision-making
  - Rich ancillary data and footprint analysis to contextualize flux measurements
  - Clear data structure, sentinel values for missing data, and metadata for reproducibility and governance
- Highlights potential governance challenges relevant to monitoring frameworks:
  - Data access and sharing barriers due to metadata gaps or data ownership
  - Maintaining up-to-date datasets and ensuring interoperability across networks (e.g., COSMOS-UK)
  - Ensuring data quality through ongoing validation, outlier management, and transparent QC criteria

## References and supporting material
- References to methodological standards and related datasets underpinning processing, QC, and interpretation (e.g., Mauder et al., Moncrieff et al., Papale et al., Wilczak et al., Vickers & Mahrt).