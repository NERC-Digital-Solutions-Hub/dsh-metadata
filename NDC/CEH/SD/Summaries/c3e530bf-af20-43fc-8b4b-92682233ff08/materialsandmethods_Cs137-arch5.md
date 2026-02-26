# Prediction of 137 Cs deposition from atmospheric nuclear weapons tests within the Arctic

## Overview
- Estimates UK-wide deposition of 137Cs from atmospheric nuclear weapons tests conducted 1955–1985, prior to the Chernobyl accident.
- Builds on the approach described by Wright et al. (1999).
- Aims to map cumulative, decay-corrected 137Cs deposition at 5 × 5 km resolution across the UK.

## Data Sources
- Deposition data
  - UK Atomic Energy Authority (AEA/AERE) network: 19 UK stations, 20 international stations (1955–1997).
  - Complete quarterly deposition records (1955–1985) available for Gibraltar, Singapore, Milford Haven (UK); Milford Haven used as representative UK site.
- Precipitation data
  - Milford Haven: quarterly precipitation records (1955–1985) used to derive deposition/precipitation ratios.
  - UK-wide precipitation: UK Met Office gridded data (5 × 5 km) representing spatial variability; based on baseline climate data for 1961–1990 (UKCIP framework). UKCIP2009 data used for spatial variability of annual precipitation.

## Methods
- For each quarter:
  - Derive deposition/precipitation ratio from Milford Haven 1955–1985 records.
  - Apply this ratio to UK-wide average total precipitation to estimate spatially varying 137Cs input at 5 × 5 km resolution.
  - Add quarterly deposition to previously predicted deposition; correct for decay of 137Cs (half-life 30.2 years) to obtain cumulative deposition.
  - Produce UK-wide, decay-corrected deposition estimates for 1955–1985 at 5 × 5 km resolution.

## Temporal and Spatial Details
- Temporal coverage: 1955–1985 (pre-Chernobyl period).
- Spatial resolution: 5 × 5 km grid across terrestrial UK.
- Temporal resolution: quarterly (January–March, April–June, July–September, October–December).

## Key Considerations and Limitations
- Reliance on Milford Haven as a representative UK deposition site due to incomplete complete records from all stations.
- Potential uncertainties from using a single-site ratio to project UK-wide deposition.
- Assumes consistency between Milford Haven deposition/precipitation behavior and broader UK precipitation patterns.
- Requires careful handling of data provenance, calibration, and potential updates if additional datasets become available.

## Provenance and Reproducibility
- Method follows Wright et al. (1999) framework for predicting 137Cs deposition within the Arctic, adapted for the UK.
- Data inputs drawn from historical measurement networks (AEA/AERE) and UKCIP/Met Office gridded precipitation datasets.
- Decay correction applied using a fixed half-life of 30.2 years.

## Reference
- Wright, S.M., Howard, B.J., Strand, P., Nylen, T., & Sickel, M.A.K. 1999. Prediction of 137 Cs deposition from atmospheric nuclear weapons tests within the Arctic. Environmental Pollution, 104, 131-143. doi:10.1016/S0269-7491(98)00140-7