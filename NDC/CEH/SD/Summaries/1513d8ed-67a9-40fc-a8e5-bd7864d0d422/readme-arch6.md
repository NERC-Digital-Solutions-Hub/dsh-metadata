# Supporting documentation for spatial outputs of modelled impacts of ambient ozone on sugarcane production in south-central Brazil

## Overview
- Spatially explicit data from a dynamic global vegetation model (JULES v5.6) used to model predicted impacts of ambient ozone (O3) on sugarcane production in south-central Brazil for 2010–2014.
- Intended to accompany Cheesman et al. (2023) and related data deposit; enables assessment of potential risks to sugarcane yields under current O3 levels.
- Outputs are gridcell-averaged (1.25° x 1.875°) and integrate environmental drivers, vegetation dynamics, and O3 damage.

## Modelling framework
- JULES framework: land surface model with gridcell-based vegetation across up to 13 plant functional types (PFTs); sugarcane represented as the C4 PFT.
- Modifications for sugarcane: adapted carbon fixation and physiology parameters based on Vianna et al. (2022) to better represent sugarcane (GPP, respiration, stomatal conductance).
- C4 PFT used; sugarcane interspersed with other PFTs and non-vegetation cover per gridcell.
- Outputs provide gridcell-average vegetation responses and fluxes, not individual plant-scale management (e.g., harvesting/ratooning).

## Data inputs and parameterization
- Stomatal conductance: Medlyn model with g1 from Oliver et al. (2022) for C4 plants.
- Photosynthesis: Collatz model; ozone flux calculated per Oliver et al. (2018); Vmax calibrated via Vianna et al. (2022).
- O3 damage scheme: reduces net photosynthesis (Anet) and stomatal conductance (gs) via a damage factor F dependent on O3 flux and a sensitivity parameter α.
- O3 data: simulated with UKESM1 (2000–2014) and downscaled to reflect diel and daily variations; regional diel patterns mapped from 53 São Paulo locations to all gridcells, increasing annual O3 flux by about 40% versus using monthly means alone.
- Calibration: eight α functions across four susceptibility levels (low, moderate, high, very high) and two thresholds (0 and 2 nmol m^-2 s^-1) to capture range of potential O3 impacts on sugarcane.

## Ozone data and exposure settings
- O3 climatology with diel/daily variation applied to model gridcells to drive O3 damage in the simulations.
- Two damage thresholds examined: POD0 (0 nmol m^-2 s^-1) and POD2 (2 nmol m^-2 s^-1) for flux accumulation and damage modeling.

## Model runs and scenarios
- Time period: 10-year simulation window after a 20-year spin-up; meteorological forcing from CRUJRA v2.1 (2005–2014) at 6-hour intervals.
- O3 forcing: yearly climatology with hourly/diel variation; based on UKESM1 data.
- Outputs compare scenarios with and without O3 damage, across four susceptibility levels and two POD thresholds.
- Metrics produced: proportional decline relative to control, absolute NPP losses (kg C m^-2 yr^-1), and percent of control production.

## Outputs and data products
- Spatial granularity: 1.25° x 1.875° gridcells.
- Data files and variables include:
  - sugarcane_cover.nc: cane_cover (fraction 0–1), sugarcane distribution from MapBiomas v6.
  - control_frac.nc: NPP_sugarcane (kg C yr^-1) under no O3 damage.
  - NPP_risk_POD0_low.nc, NPP_risk_POD0_mod.nc, NPP_risk_POD0_high.nc: NPP_loss for POD0 at low/moderate/high susceptibility.
  - NPP_risk_POD2_low.nc, NPP_risk_POD2_mod.nc, NPP_risk_POD2_high.nc: NPP_loss for POD2 at low/moderate/high susceptibility.
  - per_loss_POD0_low.nc, per_loss_POD0_mod.nc, per_loss_POD0_high.nc: % of control NPP for POD0.
  - per_loss_POD2_low.nc, per_loss_POD2_mod.nc, per_loss_POD2_high.nc: % of control NPP for POD2.
  - NPP_loss_POD0_low.nc, NPP_loss_POD0_mod.nc, NPP_loss_POD0_high.nc: absolute NPP loss (kg C yr^-1) for POD0.
  - NPP_loss_POD2_low.nc, NPP_loss_POD2_mod.nc, NPP_loss_POD2_high.nc: absolute NPP loss (kg C yr^-1) for POD2.
  - NPP_risk_POD0_M2018.nc, NPP_risk_POD2_M2018.nc: present-day risk of NPP loss (absolute) for POD0/2, calibrated to highly susceptible varieties (IACSP94-2094, IACSP95-5000).
  - NPP_per_POD0_M2018.nc, NPP_per_POD2_M2018.nc: present-day risk of NPP loss as a percentage of control.
- Outputs enable assessment of O3 risk to sugarcane production, spatially explicit risk mapping, and comparison across susceptibility classes and thresholds.

## Data quality and validation
- QC against previous sugarcane-focused JULES applications (Vianna et al. 2022); control NPP baselines consistent with literature, with potential NPP up to ~3.1 kg C m^-2 yr^-1 (≈138 Mg ha^-1) in control runs, aligning with published yield estimates (93.5–132 Mg ha^-1).
- Model integration of multiple data sources (climate forcing, ozone climatology, sugarcane distribution) designed to produce robust spatial risk outputs.

## How this data supports data use
- Enables data users to:
  - Explore spatial patterns of ozone risk to sugarcane across south-central Brazil under present-day O3 conditions.
  - Compare impacts across different sugarcane susceptibilities and O3 damage thresholds.
  - Use gridded outputs to create dashboards, maps, or summary reports showing absolute and relative yield risks.
  - Integrate with other data layers (e.g., management practices, regional policies) to support decision-making and risk communication.

## References
- Best et al. 2011; Clark et al. 2011; Sitch et al. 2007; Moura et al. 2018; Vianna et al. 2022; Oliver et al. 2018; CETESB 2022; and Cheesman et al. 2023, among others cited in the deposit.