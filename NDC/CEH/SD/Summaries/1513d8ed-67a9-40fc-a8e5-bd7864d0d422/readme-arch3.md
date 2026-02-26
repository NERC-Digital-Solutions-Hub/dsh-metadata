# Supporting documentation for spatial outputs of modelled impacts of ambient ozone on sugarcane production in south-central Brazil

- Purpose: Provide spatially explicit data on predicted ozone (O3) impacts on sugarcane production across south-central Brazil (2010–2014) to support the associated Cheesman et al. (2023) study and related data deposit.
- Context: Supplements a modelling study using JULES v5.6 to assess current O3 risk to sugarcane yields and to generate risk maps for policy and monitoring.

## Modelling framework and key methods

- Model: Joint UK Land Environment Simulator (JULES) v5.6; a land-surface model with gridcell-level vegetation types (PFTs).
- Sugarcane representation: C4 PFT adapted to better represent sugarcane physiology (via Vianna et al., 2022) with tuned parameters for carbon fixation, respiration, and stomatal conductance (Medlyn model; g1 = 1.62 for C4).
- Photosynthesis and fluxes: Collatz photosynthesis model; ozone flux and damage scheme modify net photosynthesis (Anet) and stomatal conductance (gs) via a damage factor F.
- O3 damage scheme: F = 1 − α × (FluxO3 > y); two dose thresholds used (y = 0 and y = 2 nmol m⁻² s⁻¹); α is calibrated to match observed dose–response relationships.
- Calibration across varieties: eight α functions across four susceptibilities (low, moderate, high, very high) and two thresholds, capturing a range of potential O3 sensitivities.

## Data inputs and ozone data

- O3 data: Simulated surface O3 from the Earth System Model UKESM1 for 2000–2014; monthly resolution, 1.25° × 1.875° grid.
- Temporal refinement: Daily diel cycle and daily variation inferred from 53 locations in São Paulo (CETESB, 2022) applied to all grid cells, producing a realistic O3 climatology.
- Flux adjustment: This approach yields ~40% higher annual O3 flux than using monthly mean concentrations alone.

## Model runs and outputs

- Simulation setup: 10-year runs (after a 20-year spin-up); meteorology from CRUJRA v2.1 forcing at 6-hour intervals (2005–2014); O3 climatology with hourly variation.
- Outputs: Spatially explicit metrics of O3 impact on sugarcane including:
  - Proportional declines relative to a no-O3-damage control
  - Absolute NPP losses (kg C m⁻² yr⁻¹)
- Scenarios: O3 susceptibility levels (low, moderate, high, very high) and two flux thresholds (POD0 and POD2).

## Data products and file formats

- Data resolution: 1.25° × 1.875° grid cells.
- Provided files (examples):
  - sugarcane_cover.nc: cane_cover (0–1 fraction)
  - control_frac.nc: NPP_sugarcane (kg C m⁻² yr⁻¹) under control
  - NPP_risk_POD0_low/mod/high.nc, NPP_risk_POD2_low/mod/high.nc: NPP_loss (kg C m⁻² yr⁻¹) under POD0/ POD2 for different susceptibilities
  - per_loss_POD0_low/mod/high.nc, per_loss_POD2_low/mod/high.nc: NPP_sugarcane as percentage of control
  - NPP_loss_POD0_M2018.nc, NPP_loss_POD2_M2018.nc: present-day risk calibrations
  - NPP_per_POD0_M2018.nc, NPP_per_POD2_M2018.nc: corresponding percentage risks
- Metadata and provenance: Detailed variable definitions, units, and descriptions provided; reference to MapBiomass for sugarcane cover.

## Quality control and validation

- Compatibility checks: Outputs compared with prior JULES sugarcane work (Vianna et al., 2022); control yields align with expected ranges (up to ~3.1 kg C m⁻² yr⁻¹; ~138 Mg ha⁻¹) and with published sugarcane yield estimates (93.5–132 Mg ha⁻¹).
- Model documentation: Supporting Appendix A and related references provide further methodological specifics.

## Data accessibility, governance, and use in monitoring

- Purpose for monitoring: Delivers spatial indicators of O3 risk to sugarcane production, suitable for policy scrutiny, scenario planning, and adaptation decision-making.
- Data sharing considerations: Data deposited to accompany the Cheesman et al. (2023) paper; includes a suite of gridded outputs and extensive methodological detail.
- Metadata and transparency: Clear documentation of model setup, calibration, inputs, and output variables to support verification and reuse.
- Practical considerations: Gridcell-averaged outputs; does not model on-farm management (e.g., harvesting, ratooning); relies on simulated O3 data and calibrated susceptibility functions.

## Key takeaways for monitoring frameworks

- Provides spatially explicit indicators of ozone risk to sugarcane production in south-central Brazil, enabling regional risk assessment and policy targeting.
- Demonstrates a rigorous calibration approach to match observed O3 dose–response relationships across cultivars, with multiple susceptibility scenarios.
- Highlights data governance considerations relevant to monitoring: need for complete metadata, data accessibility, and transparent data provenance to support reuse in policy analysis.
- Useful as a data source for building or validating environmental health indicators, subject to its assumptions (gridcell homogeneity, lack of management practices, modeled ozone flux).