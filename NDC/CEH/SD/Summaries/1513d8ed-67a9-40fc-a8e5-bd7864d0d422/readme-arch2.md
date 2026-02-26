# Supporting documentation for spatial outputs of modelled impacts of ambient ozone on sugarcane production in south-central Brazil

## Purpose and context
- Provides spatially-explicit model outputs of ambient ozone (O3) impacts on sugarcane production in south-central Brazil for 2010–2014.
- Coupled with Cheesman et al. (2023) and additional data deposits; intended to support environmental monitoring and policy evaluation through standardized, reviewable outputs.

## Modelling framework
- Uses the Joint UK Land Environment Simulator (JULES) v5.6 to simulate land-surface processes, soil-vegetation-atmosphere interactions, and vegetation responses to atmospheric composition.
- Gridcell-based approach with up to 13 plant functional types (PFTs); sugarcane represented by the C4 PFT, with area-weighted fraction in each gridcell to reflect observed sugarcane distribution.

## Sugarcane representation and parameterization
- Sugarcane modeled as C4 with tailored parameters (from Vianna et al. 2022) to improve carbon fixation, respiration, and stomatal conductance.
- Stomatal conductance via Medlyn model (g1 = 1.62 for C4); photosynthesis via Collatz model; O3 flux computed following Oliver et al. 2018.
- Vmax for photosynthesis calibrated to field-based nitrogen data; model calibrated to reproduce observed GPP in sugarcane.

## Ozone data and forcing
- O3 exposure derived from UKESM1 for 2000–2014; monthly surface O3 at 1.25° × 1.875°.
- To capture realistic diel and daily variation, a diurnal/daily pattern from 53 São Paulo sites (CETESB) is projected onto all gridcells, increasing annual O3 flux by ~40% versus using monthly means.

## O3 damage calibration and scheme
- O3 damage reduces net photosynthesis (A_net) and stomatal conductance (g_s) via a damage factor F, parameterized by α and flux above a threshold y.
- F = 1 − α × (Flux_O3 > y); A_mod = A_net × F; g_mod = g_s × F.
- Two thresholds, y = 0 and 2 nmol m−2 s−1, and eight α functions across four susceptibility levels (low, moderate, high, very high) were developed to capture diverse responses.
- α calibrated to reproduce relative NPP losses and aligned with dose–response for two sugarcane varieties (IACSP94-2094, IACSP95-5000).

## Model runs and outputs
- 10-year analysis period (2010–2014) after a 20-year spin-up.
- Meteorological forcing from CRUJRA v2.1 at 6-hour intervals (2005–2014); ozone climatology with hourly variation as described above.
- Outputs include both proportional declines and absolute NPP losses, under POD0 (threshold 0) and POD2 (threshold 2), across the different susceptibility scenarios.

## Data products and file structure
- Spatial resolution: 1.25° × 1.875°.
- sugarcane_cover.nc: cane_cover (fraction 0–1) from MapBiomass.
- control_frac.nc: NPP_sugarcane without O3 damage (kg C m−2 yr−1).
- NPP_risk_POD0_low/mod/high.nc, NPP_risk_POD2_low/mod/high.nc: NPP_loss (kg C m−2 yr−1) under POD0 and POD2 for each susceptibility level.
- per_loss_POD0_low/mod/high.nc, per_loss_POD2_low/mod/high.nc: NPP_loss as % of control.
- NPP_loss_POD0_low/mod/high.nc, NPP_loss_POD2_low/mod/high.nc: absolute NPP losses (kg C yr−1).
- NPP_risk_POD0_M2018.nc, NPP_risk_POD2_M2018.nc and their percentage counterparts: present-day risk calibrated to high-susceptibility varieties (Moura et al., 2018).

## Quality control and validation
- Outputs checked against previous JULES sugarcane applications (Vianna et al., 2022).
- Control yield benchmarks: up to ~3.1 kg C m−2 yr−1 (≈138 Mg ha−1), consistent with calibrated estimates (93.5–132 Mg ha−1; avg 109 Mg ha−1) for south-central Brazil (Dias & Sentelhas, 2018).

## Relevance for environmental monitoring and policy
- Delivers standardized, spatially explicit estimates of ozone-related production risk for a major crop, enabling comparison across regions and time.
- Facilitates data reuse and integration with other environmental datasets to enhance monitoring, assessment, and decision-making regarding air quality, agriculture, and climate impacts.