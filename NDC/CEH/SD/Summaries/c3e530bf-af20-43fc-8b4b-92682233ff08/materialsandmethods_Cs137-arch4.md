# Estimation of the deposition of 137 Cs from atmospheric nuclear weapons tests in the UK prior to the Chernobyl accident uses the approach outlined in Wright et al. (1999)

## Overview
- Objective: Estimate cumulative deposition of 137 Cs in the UK from atmospheric nuclear weapons tests before the Chernobyl accident.
- Core idea: Deposition rates correlate with precipitation; use this relationship to map UK-wide deposition at a fine spatial resolution.

## Data sources
- UK Atomic Energy Authority (AEA/AERE) network: 19 UK stations and 20 international stations (1955–1997) monitoring radionuclides from weapons tests.
- Complete quarterly 137 Cs deposition records (1955–1985) available from Gibraltar, Singapore, and Milford Haven (Wales, UK); Milford Haven used as representative UK record.
- Milford Haven provides quarterly 137 Cs deposition and precipitation data (1955–1985).
- UK precipitation data: gridded baseline climate data from the UK Met Office (spatial resolution 5 × 5 km; derived from a 1961–1990 30-year period). UKCIP2009 data referenced for baseline precipitation (monthly totals used to reflect UK spatial variability).
- UK total precipitation (terrestrial areas) used to scale deposition spatially.

## Method
- For each quarter, compute the 137 Cs deposition/precipitation ratio using Milford Haven records.
- Apply this ratio to the UK-wide average total precipitation for that quarter to derive spatial variability in 137 Cs input at 5 × 5 km resolution.
- Sum the quarterly deposition with the pre-existing predicted 137 Cs deposition and apply decay correction (137 Cs half-life = 30.2 years) to estimate cumulative deposition for 1955–1985 at 5 × 5 km resolution.

## Data processing and calculations
- Spatial variability: 5 × 5 km grid across the UK.
- Temporal scope: 1955–1985 (pre-Chernobyl period).
- Decay correction: adjust deposition figures to account for radiological decay over time.
- Data integration: combine Milford Haven-based deposition/precipitation ratios with UK-wide precipitation to produce spatially explicit deposition estimates.

## Assumptions and limitations
- Milford Haven’s quarterly deposition/precipitation ratio is representative of UK-wide conditions.
- Use of 1961–1990 baseline precipitation to model spatial variability may not capture all temporal changes outside this window.
- Data quality depends on the consistency and comparability of historic deposition records across stations.
- Spatial resolution limited to 5 × 5 km.

## Outputs and relevance
- Produces cumulative, decay-corrected 137 Cs deposition maps for the UK at 5 × 5 km resolution for 1955–1985.
- Methodology linked to Wright et al. (1999) for deposition predictions within the Arctic, providing a published approach endorsement.

## Reference
- Wright, S.M., Howard, B.J., Strand, P., Nylen, T., & Sickel, M.A.K. 1999. Prediction of 137 Cs deposition from atmospheric nuclear weapons tests within the Arctic. Environmental Pollution, 104, 131-143. doi:10.1016/S0269-7491(98)00140-7