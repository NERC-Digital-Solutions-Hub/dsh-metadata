# Turbulent fluxes of sensible heat and momentum at an ancient deciduous broadleaved forest in southern England

## Overview
- Time series of turbulent surface-atmosphere exchanges of sensible heat (H) and momentum (τ) measured at a 27 m forest canopy tower in Wytham Woods, Oxfordshire, UK.
- Data collected via eddy covariance (EC) between 2014-06-13 13:00 and 2016-01-04 22:00.
- Includes ancillary weather and soil physics observations, plus turbulence-related variables and quality metrics for the flux observations.
- Processed with standardized methods, providing QC flags and uncertainties to support monitoring and policy evaluation over time.

## Study site
- Location: Wytham Woods flux site (approx. 51.7667° N, -1.3333° W), within ~400 ha of ancient broadleaved deciduous forest, ~5 km NW of Oxford.
- Climate: temperate maritime; mean annual temperature ~10.1°C; mean annual precipitation ~730 mm.
- Soils: range from poorly to well-drained clays over sandstone.
- Vegetation: ancient woodland; canopy-dominated by Pedunculate Oak, Ash, Sycamore; average canopy height ~20 m.
- Flux tower situated on the north-facing slope; site described as disturbed ancient forest in the surrounding area.

## Sampling regime
- Automated flux measurements from 2014-06-13 13:00 to 2016-01-04 22:00.
- EC and micrometeorological data collected 27 m above ground using a Windmaster sonic anemometer; raw data at 20 Hz.
- Ancillary meteorological and soil measurements from a co-located COSMOS-UK station; data merged with the EC observations.
- Half-hourly (30 min) averaging for fluxes and ancillary variables; precipitation recorded at base of tower with an inlet at the top.

## Data processing
- Fluxes calculated with EddyPRO software (v6.1) using 30-minute averages.
- Preprocessing corrections for a known Gill sonic anemometer issue (boost-bug) and standard EC corrections (angle of attack, rotation, spectral corrections, humidity effects).
- Random uncertainties estimated for H and τ.
- Quality control (QC) flags implemented: high (0), acceptable (1), poor (2).
- Derived diagnostics included wind speed/direction, friction velocity (u*), Turbulent Kinetic Energy (TKE), temperature scaling (T*), Obukhov length (L), stability parameter (z/L), and flux footprint estimates.
- Dataset includes both fluxes and QC metrics along with ancillary diagnostic variables.

## Quality control
- Outlier detection for H using median absolute deviation; flagged values (H) outside plausible range (-200 to 600 W m^-2) excluded.
- Fluxes with QC flag > 1 removed from the primary dataset; users may apply their own filtering criteria.
- Weekly visual checks of flux and ancillary data performed; clearly erroneous values removed manually.
- Users can decide to retain or exclude flagged data based on their quality requirements (e.g., u*, footprint considerations).

## Data structure
- Single CSV file: WythamWoodsMicromet_v1.0.csv; covers 201406-13 13:00 to 2016-01-04 22:00.
- Missing records denoted by -9999.
- Column descriptions and units (adapted from Li-COR Biosciences) include:
  - DateTime, H, rand_err_H, qc_H, Tau, rand_err_Tau, qc_Tau
  - Wind metrics: wind_speed, max_wind_speed, wind_dir
  - Derived flux metrics: Ustar, TKE, Tstar, L, zL
  - Footprint and upwind distance metrics: X_peak, X_10, X_30, X_50, X_70, X_90 (and corresponding location values)
  - Radiation and energy balance: SW in, SW out, LW in, LW out, R net
  - Soil and surface variables: SHF_1/SHF_2 (soil heat flux), Ta, RH, Pa, Ts_1/Ts_2 (soil temperatures), VWC_1/VWC_2 (volumetric water content), Precip
- Ancillary data are provided as 30-minute means; data merged with COSMOS-UK observations for completeness.

## Accessibility and usage
- Funded by NERC; COSMOS-UK data integrated for enhanced hydrometeorological and soil context.
- Dataset designed for standardized reporting of environmental health and policy-relevant monitoring over time.
- Clear documentation of data processing, QC procedures, and uncertainties supports reproducibility and inter-site comparisons.
- Data users should consider applying QC-based filters (flag, footprint, u*, etc.) to suit analysis goals.

## Acknowledgments and references
- Acknowledges NERC funding, COSMOS-UK data, Oxford University access, and technical support.
- References include methodological papers on EC processing, QC standards, footprint modeling, instrument corrections, and related site studies.