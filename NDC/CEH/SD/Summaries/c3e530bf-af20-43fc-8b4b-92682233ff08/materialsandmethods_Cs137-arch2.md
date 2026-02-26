# Prediction of 137 Cs deposition from atmospheric nuclear weapons tests within the Arctic

- Objective: Estimate 137 Cs deposition in the UK from atmospheric nuclear weapons tests (1955–1985) using a precipitation-linked approach and produce a spatially resolved deposition map at 5 × 5 km resolution.

## Data sources

- Deposition records: UK Atomic Energy Authority (AEA/AERE) stations (1955–1997) with quarterly deposition data; Milford Haven (Wales, UK) chosen as representative site due to complete records (1955–1985) alongside Gibraltar and Singapore.
- Precipitation data: 
  - Milford Haven quarterly deposition/precipitation data (1955–1985) to derive deposition-to-precipitation ratios.
  - UK Meteorological Office gridded baseline precipitation data representing UK-wide spatial variability (derived from a 30-year window, 1961–1990; 5 × 5 km resolution; UKCIP framework).
  - UKCIP monthly total precipitation data for spatial variability across the UK.
- Reference data: Wright et al. (1999) for methodology on Arctic deposition prediction.

## Methodology

- Derive quarterly deposition-to-precipitation ratios for Milford Haven using deposition and precipitation records (1955–1985).
- Apply these ratios to the UK-wide average quarterly precipitation to estimate spatially variable quarterly 137 Cs input across the UK at 5 × 5 km resolution.
- Accumulate deposition over time by adding the quarterly predicted deposition to the existing predicted 137 Cs deposition and apply decay correction.
- Apply decay correction using a 30.2-year half-life to obtain cumulative decay-corrected 137 Cs deposition for the UK for 1955–1985.
- Output a spatially resolved (5 × 5 km) deposition dataset representing cumulative deposition over the period.

## Outputs and applications

- A spatially explicit UK-wide map of cumulative, decay-corrected 137 Cs deposition from atmospheric nuclear weapons tests for 1955–1985 at 5 × 5 km resolution.
- Useful for environmental modelling, monitoring, and policy evaluation related to fallout deposition and radiological health assessments.

## Assumptions and caveats

- Milford Haven deposition/precipitation ratio is representative of the UK-wide deposition-precipitation relationship.
- UKCIP precipitation data (1961–1990 baseline) accurately captures spatial variability for the UK during the study period.
- Decay correction assumes a 30.2-year half-life for 137 Cs.
- The approach relies on combining historical station data with modeled precipitation to interpolate nationwide deposition.

## Reference

- Wright, S.M., Howard, B.J., Strand, P., Nylen, T., & Sickel, M.A.K. (1999). Prediction of 137 Cs deposition from atmospheric nuclear weapons tests within the Arctic. Environmental Pollution, 104, 131-143. doi:10.1016/S0269-7491(98)00140-7