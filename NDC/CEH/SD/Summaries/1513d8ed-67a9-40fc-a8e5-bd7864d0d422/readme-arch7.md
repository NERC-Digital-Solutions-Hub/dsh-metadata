# Supporting documentation for spatial outputs of modelled impacts of ambient ozone on sugarcane production in south-central Brazil

- Spatially-explicit data from using the dynamic global vegetation model JULES v5.6 to model predicted impacts of ozone on sugarcane production across south-central Brazil for 2010–2014, intended to be viewed with Cheesman et al. (2023) and related data deposit.
- Data support maps of potential ozone risks to sugarcane production and are accompanied by methodological details, data sources, and file specifications.

## Overview and purpose
- Aim to generate map-based data products showing how ambient ozone (O3) exposure could affect sugarcane yields in south-central Brazil.
- Uses JULES to simulate vegetation responses at the gridcell level, integrating environmental conditions, ozone flux, and sugarcane-specific physiology.
- Results serve as a basis for spatial risk assessment and visualization of potential production impacts.

## Modelling framework and domain
- Model: Joint UK Land Environment Simulator (JULES) v5.6; gridcell-based land surface model with multiple plant functional types (PFTs).
- Sugarcane representation: modeled as a C4 PFT; parameters adapted from Vianna et al. (2022) to better reflect sugarcane physiology (carbon fixation, respiration, stomatal conductance).
- Key physiological components:
  - Stomatal conductance via Medlyn model (g1 = 1.62 for C4 plants).
  - Photosynthesis via Collatz model; ozone flux and damage incorporated as per Oliver et al. (2018) and related work.
  - Outputs at gridcell scale without explicit management decisions (e.g., no harvesting or ratooning).
- Purpose: produce spatially explicit projections of NPP and sugarcane production under ozone stress, including interactions with temperature, CO2, aerosols, drought, and nutrient cycling.

## Ozone data and forcing
- O3 exposure data come from the UKESM1 Earth System Model (2000–2014); monthly resolution, 0–40 m above orography, 1.25° × 1.875° grid.
- To reflect biological realism, the monthly O3 values were adjusted to reproduce diel cycles and daily variation using data from 53 sites in São Paulo (2018), producing a climatology that increases annual O3 flux by about 40% compared to using monthly means alone.

## Calibration of ozone damage (alpha)
- Damage scheme: F = 1 − α × (Flux_O3 > y) with A_mod = A_net × F and g_mod = g_s × F, linking ozone flux to photosynthesis and stomatal conductance changes.
- Calibration process:
  - Used thresholds y = 0 and 2 nmol m−2 s−1; tuned α so modelled NPP loss matches a no-damage reference and aligns with observed dose–response for sugarcane (Moura et al., 2018).
  - Calibrated against two susceptible sugarcane varieties (IACSP94‑2094, IACSP95‑5000).
  - Resulted in eight α functions across four susceptibility categories (low, moderate, high, very high) and two thresholds, capturing a range of potential O3 impacts.

## JULES runs and outputs
- Temporal scope: 10-year period (after a 20-year spin-up) for 2005–2014 forcing.
- Meteorological forcing: CRUJRA v2.1 reanalysis at 6-hour intervals.
- O3 forcing: yearly climatology with hourly variation as described above.
- Spatial outputs: calculated annual yields with/without O3 susceptibility; produced both proportional decline (% of control) and absolute NPP losses (kg C m−2 yr−1).
- Scenarios: four susceptibility levels and two POD thresholds (POD0 and POD2) to reflect different ozone dose-response assumptions.

## Data products and file specifications
- Spatial resolution: 1.25° latitude × 1.875° longitude grid.
- Sugarcane cover: sugarcane_cover.nc (variable: cane_cover; units: fraction 0–1). Derived from MapBiomass v6 and resampled to JULES grid.
- Control NPP: control_frac.nc (variable: NPP_sugarcane; units: kg C yr−1). Predicted average NPP for sugarcane across 2010–2014 (no O3 damage) scaled by sugarcane coverage.
- O3 risk files (NPP_loss and NPP_sugarcane): 
  - NPP_risk_POD0_low/mod/high.nc and NPP_risk_POD2_low/mod/high.nc (variable: NPP_loss; units: kg C m−2 yr−1).
  - per_loss_POD0_low/mod/high.nc and per_loss_POD2_low/mod/high.nc (variable: NPP_sugarcane; units: % of control).
  - NPP_loss_POD0_low/mod/high.nc, NPP_loss_POD2_low/mod/high.nc (variable: NPP_loss; units: kg C yr−1).
- Present-day risk files (M2018 calibration against very-high susceptibility):
  - NPP_risk_POD0_M2018.nc and NPP_risk_POD2_M2018.nc (variable: Risk of NPP loss; units: kg C m−2 yr−1).
  - NPP_per_POD0_M2018.nc and NPP_per_POD2_M2018.nc (variable: Risk of NPP loss; units: % of control).
- File-level notes: each file contains gridcell-scale outputs appropriate for map-based visualization of both absolute production losses and relative risk across the landscape.

## Quality control and interpretation
- Model outputs were checked against previous sugarcane-based calibrations (Vianna et al., 2022) to ensure plausible NPP ranges and yield estimates.
- Control NPP values for sugarcane without ozone damage align with published yield estimates for south-central Brazil (roughly 93.5–132 Mg ha−1; average ~109 Mg ha−1).
- The data are designed for spatial risk interpretation and cross-reference with Cheesman et al. (2023) for broader context and validation.

## Usage notes and references
- These spatial outputs complement the associated paper Cheesman et al. (2023) and the broader data deposit.
- Sugarcane cover information is anchored to MapBiomass v6 data (Souza et al., 2020); ozone climatology relies on UKESM1 and region-specific site data for diel variation (CETESB 2022).
- References include key JULES descriptions, ozone risk studies, and sugarcane-specific model adaptations (see detailed references in the deposit).