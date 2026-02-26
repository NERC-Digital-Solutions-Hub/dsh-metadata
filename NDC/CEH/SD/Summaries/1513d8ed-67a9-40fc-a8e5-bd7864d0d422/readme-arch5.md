# Supporting documentation for spatial outputs of modelled impacts of ambient ozone on sugarcane production in south-central Brazil

## Overview
- Spatially explicit model outputs (2010–2014) assessing potential ozone (O3) impacts on sugarcane production in south-central Brazil.
- Based on the Joint UK Land Environment Simulator (JULES) v5.6 with sugarcane represented as a C4 PFT adapted for Brazilian conditions.
- Data deposited to accompany Cheesman et al. (2023) and related data materials.

## Modelling framework and data lineage
- Modelling tool: JULES v5.6, a land surface model with gridcell-averaged outputs and up to 13 plant functional types.
- Sugarcane representation: C4 PFT with parameters tuned to Brazilian field data (Vianna et al. 2022) to better capture carbon fixation, respiration, stomatal conductance, and GPP.
- Photosynthesis and stomatal models:
  - Stomatal conductance using Medlyn model (g1 = 1.62 for C4 plants).
  - Photosynthesis via Collatz model; ozone flux calculated per Oliver et al. (2018).
  - O3 damage scheme modifies net photosynthesis (Anet) and stomatal conductance (gs) through a damage factor F dependent on flux and a sensitivity parameter α.
- Ozone forcing data:
  - O3 fields simulated with UKESM1 (2000–2014), monthly resolution (0–40 m above ground, 1.25° × 1.875°).
  - Diel and daily variability projected onto gridcells using diel patterns from 53 sites in São Paulo (CETESB, 2018), yielding ~40% higher annual O3 flux than using monthly means alone.
- Calibration of O3 susceptibility:
  - Eight α functions across four susceptibility levels (low, moderate, high, very high) and two dose-thresholds (y = 0 and y = 2 nmol m−2 s−1).
  - α tuned to match relative NPP losses in a year-long run against a no-damage baseline and to fit dose–response functions for two susceptible sugarcane varieties (IACSP94-2094, IACSP95-5000; Moura et al., 2018).
- Forcing and spin-up:
  - Meteorology: CRUJRA v2.1 reanalysis, 6-hour intervals, 1.25° × 1.875°.
  - Simulation period: 10-year runs after a 20-year spin-up.
  - Outputs averaged for 2010–2014 to compare with observed/contextual baselines.
- Outputs are gridcell-scale (not individual plant scale) and do not include explicit management practices (e.g., harvesting, ratooning).

## Data products and file catalogue
- Spatial resolution: 1.25° × 1.875°.
- Primary dataset components and variables:
  - sugarcane_cover.nc: variable cane_cover, units 0–1 (fraction of gridcell covered by sugarcane). Coverage from MapBiomass v6.
  - control_frac.nc: variable NPP_sugarcane, units kg C m−2 yr−1. Predicted average NPP of sugarcane (C4 PFT) over 2010–2014.
  - NPP_risk_POD0_low/mod/high.nc, NPP_risk_POD2_low/mod/high.nc: variable NPP_loss, units kg C m−2 yr−1. Predicted NPP losses under O3 flux accumulation thresholds POD0 (0 nmol m−2 s−1) or POD2 (2 nmol m−2 s−1) and susceptibility levels.
  - per_loss_POD0_low/mod/high.nc, per_loss_POD2_low/mod/high.nc: variable NPP_sugarcane, units % of control. Predicted percent loss under POD thresholds.
  - NPP_loss_POD0_M2018.nc, NPP_loss_POD2_M2018.nc: NPP_loss at present-day (2010–2014) calibration against very high-susceptibility varieties (Moura et al., 2018) for POD0 and POD2.
  - NPP_per_POD0_M2018.nc, NPP_per_POD2_M2018.nc: Percent risk of NPP loss under present-day calibration for POD0 and POD2.
- Metadata notes:
  - All files document the gridcell-scale outputs, definitions of NPP and NPP_loss, and the two O3 accumulation thresholds (0 and 2 nmol m−2 s−1).
  - Data are intended to be used alongside Cheesman et al. (2023) and related deposit materials for interpretation and reproducibility.

## Data quality, calibration, and validation
- Calibration approach:
  - α parameters adjusted so modeled NPP loss per gridcell matches dose–response expectations, including calibration to two sugarcane varieties.
  - Four susceptibility classes and two thresholds cover a range of potential responses.
- Quality control:
  - Outputs cross-checked against prior JULES-sugarcane applications (Vianna et al., 2022); reported control NPP without O3 damage peaks near 3.1 kg C m−2 yr−1, aligning with field-modelled ranges (93.5–132 Mg ha−1; average ~109 Mg ha−1; Dias & Sentelhas, 2018).
  - Appendix and supplementary information provide additional methodological detail (Appendix A).
- Reproducibility aids:
  - Detailed model setup, parameter choices, and data processing steps referenced to the associated paper and supplementary materials.

## Provenance, governance, and metadata considerations for Data Stewards
- Provenance and transparency:
  - Full documentation of model version, PFT mapping, parameter tuning (Vianna 2022; Moura 2018), and O3 flux formulation (Oliver et al. 2018) to enable traceability.
  - Clear data lineage from UKESM1 O3 fields, CRUJRA meteorology, to JULES outputs and final risk products.
- Metadata and documentation:
  - File names and variable definitions explicitly document content and units.
  - Appendix and referenced literature provide calibration details and context for interpretation.
- Data formats and interoperability:
  - NetCDF format with standardized variables (e.g., cane_cover, NPP_sugarcane, NPP_loss) suitable for integration into other GIS or climate-data platforms.
  - Spatial resolution and grid alignment documented; ensure consistent coordinate reference system and grid handling for downstream use.
- Data availability and updates:
  - Outputs are tied to a specific period (2010–2014 for baseline results; present-day calibration in M2018 files).
  - If future modelling or data updates occur (new O3 datasets, updated sugarcane parameters, or refined forcing), consider versioning and clear release notes.

## Usage considerations and limitations
- Model scope and assumptions:
  - JULES models gridcell-averaged responses and does not simulate management practices (harvest, ratooning) or genotype-level dynamics beyond the defined susceptibility classes.
  - O3 exposure is driven by modeled climatologies rather than direct, site-by-site measures; diel variation is approximated from São Paulo locations and applied region-wide.
- Spatial and temporal resolution:
  - Outputs at 1.25° × 1.875° resolution; regional aggregation or downscaling may be needed for local decision-making.
  - Temporal window focuses on 2010–2014 (with 2005–2014 meteorology driving the simulations); extrapolations beyond this period should be treated with caution.
- Data interpretation:
  - NPP_loss and percentage losses are model-derived estimates of potential production reductions due to O3 flux interactions with sugarcane physiology; not direct yield measurements.
  - Calibration against specific susceptible varieties informs relative risk but may not capture all varietal responses across Brazil.

## References (key sources)
- Best et al. 2011; Clark et al. 2011; SITCH/JULES model descriptions and parameterizations.
- Moura et al. 2018; Moura et al. 2018b (sugarcane O3 dose–response data).
- Vianna et al. 2022 (improving sugarcane representation in JULES).
- Oliver et al. 2018; Medlyn et al. 2011; Collatz photosynthesis model.
- Cheesman et al. 2023 (impacts of ground-level ozone on sugarcane production).
- Dias & Sentelhas 2018; Dias et al. (yield analyses).
- CETESB 2022; Harris et al. 2020; UKESM1 model data.
- Related supplementary materials (Appendix A).