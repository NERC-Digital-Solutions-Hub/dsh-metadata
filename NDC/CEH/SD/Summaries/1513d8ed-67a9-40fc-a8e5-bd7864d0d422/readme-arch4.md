# Supporting documentation for spatial outputs of modelled impacts of ambient ozone on sugarcane production in south-central Brazil

## Overview
- Spatially-explicit dataset produced with the Joint UK Land Environment Simulator (JULES) v5.6 to predict ozone (O3) impacts on sugarcane production in south-central Brazil for 2010–2014; related to Cheesman et al. (2023).

## Modelling framework
- Uses JULES as a land-surface model with gridcell resolution; sugarcane represented as the C4 plant functional type (PFT) with sugarcane-specific parameter adaptations.
- Gridcells may contain multiple PFTs; sugarcane coverage is prescribed to reflect observed distribution across the region.
- Outputs are gridcell-averaged (not plant-scale) and do not explicitly model management actions (e.g., harvesting).

## Data inputs and parameterization
- O3 data:
  - Derived from the Earth System Model UKESM1 (2000–2014); monthly surface O3 at 1.25° × 1.875°.
  - Daily and diel cycles imposed to reflect regional variations using 53 São Paulo locations (CETESB, 2018), increasing annual O3 flux by ~40% vs. monthly means.
- Meteorology:
  - CRUJRA v2.1 reanalysis forcing at 6-hour intervals for 2005–2014.
- Sugarcane representation:
  - C4 PFT with Vianna et al. (2022) parameter tuning for sugarcane carbon fixation, respiration, and stomatal conductance.
  - Medlyn stomatal conductance model (g1 = 1.62 for C4) and Collatz photosynthesis model; O3 flux model follows Oliver et al. (2018); Vmax calibrated via Vianna et al. (2022).
- Data inputs for distribution:
  - Sugarcane coverage from MapBiomass v6.

## O3 susceptibility calibration
- O3 damage scheme reduces net photosynthesis and stomatal conductance using F, with thresholds y = 0 and 2 nmol m⁻² s⁻¹.
- Alpha (α) parameter tuned to reproduce relative NPP losses against a no-O3 baseline and to match dose–response data for two susceptible sugarcane varieties (IACSP94-2094, IACSP95-5000) from Moura et al. (2018b).
- Eight α functions created across four susceptibilities (low, moderate, high, very high) and two thresholds.

## Model runs and outputs
- Timeframe: 10-year run after a 20-year spin-up.
- Outputs for each susceptibility level and threshold:
  - Proportional decline in NPP (% of control) and absolute NPP losses (kg C m⁻² yr⁻¹).
  - Comparisons against a control model with no O3 damage.
- Outputs produced for a landscape-scale assessment of risk to C4 sugarcane production.

## Quality control and validation
- Outputs cross-checked against a prior sugarcane-focused JULES application (Vianna et al., 2022).
- Control NPP expectations align with literature, with maximum potential NPP around 3.1 kg C m⁻² yr⁻¹ (~138 Mg ha⁻¹), consistent with published yield estimates (93.5–132 Mg ha⁻¹).

## Data products deposited (files and what they contain)
- sugarcane_cover.nc: cane_cover (fraction 0–1), MapBiomass v6-based sugarcane coverage.
- control_frac.nc: NPP_sugarcane (kg C yr⁻¹) under the no-O3 baseline, scaled by sugarcane coverage.
- NPP_risk_POD0_low.nc, NPP_risk_POD0_mod.nc, NPP_risk_POD0_high.nc: NPP_loss (kg C m⁻² yr⁻¹) for POD0 threshold with low/mod/high susceptibility.
- NPP_risk_POD2_low.nc, NPP_risk_POD2_mod.nc, NPP_risk_POD2_high.nc: NPP_loss (kg C m⁻² yr⁻¹) for POD2 threshold with low/mod/high susceptibility.
- per_loss_POD0_low.nc, per_loss_POD0_mod.nc, per_loss_POD0_high.nc: NPP_sugarcane (% of control) for POD0 with varying susceptibility.
- per_loss_POD2_low.nc, per_loss_POD2_mod.nc, per_loss_POD2_high.nc: NPP_sugarcane (% of control) for POD2 with varying susceptibility.
- NPP_loss_POD0_M2018.nc, NPP_loss_POD2_M2018.nc: Absolute Risk of NPP loss under present-day-like conditions calibrated to very-high susceptibility (IACSP94-2094, IACSP95-5000) for POD0 and POD2.
- NPP_per_POD0_M2018.nc, NPP_per_POD2_M2018.nc: Percent risk of NPP loss under present-day calibration for POD0 and POD2.
- All files are at 1.25° × 1.875° spatial resolution and cover 2010–2014.

## Data use and interpretation notes
- Outputs are designed to produce spatially explicit risk maps of O3 impacts on sugarcane production in south-central Brazil.
- Important caveats:
  - Gridcell-averaged results; do not capture within-grid variability or management practices (e.g., harvest timing, ratooning).
  - Genotypic effects not explicitly modeled; eight α functions approximate a range of susceptibilities.
- Data suitable for integration with wider data networks to support data management, governance, and policy discussions around agricultural risks and ozone exposure.

## How this aligns with data leadership concerns
- Data provenance and lineage:
  - Clear linkage to input datasets (UKESM1 O3, CRUJRA meteorology, MapBiomass coverage) and calibration sources (Vianna et al. 2022; Moura et al. 2018b).
- Data quality and validation:
  - Validation against prior sugarcane modelling work and consistency with published NPP/yield ranges.
- Discoverability and structure:
  - NetCDF files with explicit variable definitions and units; descriptive file names and metadata tying outputs to POD0/POD2 thresholds and susceptibility levels.
- Governance and reuse:
  - Integrates modelling outputs with published literature; data designed for reuse in broader O3 impact assessments and cross-network collaborations.
- User-needs orientation:
  - Provides both absolute and relative risk metrics to support decision-making and cross-team discussion on data products, standards, and potential community of practice around ozone risk to crops. 

## References (not exhaustive)
- Vianna et al. 2022; Moura et al. 2018b; Best et al. 2011; Clark et al. 2011; Sitch et al. 2007; Oliver et al. 2018; Cheesman et al. 2023.