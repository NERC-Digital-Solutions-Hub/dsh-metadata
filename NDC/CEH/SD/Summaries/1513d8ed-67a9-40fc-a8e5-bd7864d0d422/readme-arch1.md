# Supporting documentation for spatial outputs of modelled impacts of ambient ozone on sugarcane production in south-central Brazil

- Purpose and scope
  - Provides spatially explicit data from a JULES v5.6 model to quantify the potential impacts of ambient ozone (O3) on sugarcane production in south-central Brazil.
  - Covers the period 2010–2014, aligned with the associated Cheesman et al. (2023) paper and supplementary data.
  - Aims to support risk assessment and interpretation of O3 effects on sugarcane yield at landscape scale.

- Modeling framework and sugarcane representation
  - Uses the Joint UK Land Environment Simulator (JULES) v5.6 to simulate gridcell-scale vegetation responses and carbon fluxes.
  - Sugarcane represented as the C4 plant Functional Type (PFT); parameters tuned to sugarcane physiology via Vianna et al. (2022) to improve carbon fixation, respiration, and stomatal conductance.
  - Photosynthesis modeled with the Collatz framework; stomatal conductance with Medlyn et al. formulation (g1 = 1.62 for C4 plants); ozone damage to net photosynthesis and stomatal conductance implemented via a damage factor F.

- Ozone exposure data and climatology
  - Ozone (O3) flux and exposure driven by UKESM1 Earth System Model data (2000–2014) at monthly resolution (0–40 m a.s.l.; 1.25° × 1.875° grid).
  - Due to limited direct O3 measurements in rural sugarcane regions, the monthly O3 fields are adjusted to reflect diel cycles and daily variation observed at 53 sites in São Paulo (CETESB, 2022), producing a more realistic O3 climatology and ~40% higher annual O3 flux than using raw monthly means.

- Calibration of sugarcane susceptibility to O3
  - O3 damage scheme follows Sitch et al. (2007): F reduces Anet and gs in proportion to O3 flux above a threshold y (0 or 2 nmol m-2 s-1), controlled by a sensitivity parameter α.
  - α is calibrated by:
    - Matching relative NPP losses per grid cell to dose–response expectations from the study when compared to a no-O3-damage scenario.
    - Fitting to observed dose–response relationships for two sugarcane varieties (IACSP94-2094 and IACSP95-5000) from Moura et al. (2018).
  - Result: eight α functions across four susceptibility levels (low, moderate, high, very high) for two thresholds (0 and 2 nmol m-2 s-1), capturing a full range of potential O3 impacts.

- Simulation design and outputs
  - Timeframe: 10-year model runs (after a 20-year spin-up) to develop spatial risk maps of O3 impacts on sugarcane production.
  - Meteorological forcing: CRUJRA v2.1 reanalysis, 6-hourly, for 2005–2014 (1.25° × 1.875° grid).
  - Outputs: gridcell-level data at 1.25° × 1.875° resolution, including both baseline and O3-damaged scenarios, with and without considering sugarcane susceptibility.
  - Key derived metrics:
    - Proportional decline relative to no-O3 (percent of control).
    - Absolute NPP impact (kg C m^-2 yr^-1) or NPP_loss.
    - Percent of control production (NPP_sugarcane).
  - Susceptibility scenarios and POD (pollution dose) thresholds:
    - POD0 (0 nmol m^-2 s^-1) and POD2 (2 nmol m^-2 s^-1) thresholds.
    - Low, moderate, high, and very-high susceptibility combinations.

- Data files and variables
  - sugarcane_cover.nc: cane_cover, fraction of gridcell covered by sugarcane (from MapBiomass v6), resampled to model grid.
  - control_frac.nc: NPP_sugarcane, predicted average NPP of sugarcane (C4 PFT) 2010–2014 multiplied by cane coverage.
  - NPP_risk_POD0_low/mod/high.nc, NPP_risk_POD2_low/mod/high.nc: NPP_loss (kg C m^-2 yr^-1) under POD0/POD2 with low/mod/high susceptibility.
  - per_loss_POD0_low/mod/high.nc, per_loss_POD2_low/mod/high.nc: NPP_sugarcane as percentage of control under POD0/POD2.
  - NPP_loss_POD0_low/npp_loss_POD2_high.nc: additional NPP_loss files under POD0/POD2 for various susceptibilities.
  - NPP_risk_POD0_M2018.nc, NPP_risk_POD2_M2018.nc: modelled risk of NPP loss under present-day conditions, referencing very-high susceptibility calibrations (Moura et al., 2018) for POD0 or POD2.
  - NPP_per_POD0_M2018.nc, NPP_per_POD2_M2018.nc: percentage risk of NPP loss under present-day calibrations.
  - All files provide variables with units specified in the dataset descriptions (e.g., NPP_sugarcane in kg C yr^-1; NPP_loss in kg C m^-2 yr^-1; cane_cover as a fraction 0–1).
  - Spatial outputs are intended for mapping landscape-scale risks and potential production losses across south-central Brazil.

- Quality control and validation
  - Outputs benchmarked against previous JULES-based sugarcane applications (Vianna et al., 2022), ensuring plausible NPP ranges.
  - Control model yields estimated up to ~3.1 kg C m^-2 yr^-1 (≈138 Mg ha^-1), consistent with calibrated sugarcane production ranges reported in the region (e.g., 93.5–132 Mg ha^-1; average ~109 Mg ha^-1).
  - The approach includes cross-checks against observed dose–response patterns for susceptible varieties (IACSP94-2094 and IACSP95-5000).

- Important caveats and scope limitations
  - JULES outputs reflect gridcell-averaged responses and do not include management decisions such as harvesting or ratooning.
  - Scales: outputs are provided at a coarse grid resolution (1.25° × 1.875°) suitable for landscape-level assessment, not field-scale management.
  - Genotypic variation is not explicitly modeled beyond the eight α-susceptibility functions; no explicit genotype-by-environment interactions are represented.
  - O3 exposure is based on model simulations with adjustments to reflect diel cycles, which introduces uncertainties inherent to model-based ozone climatologies.

- Data use and documentation
  - Data are designed to support spatial risk assessment of ambient O3 on sugarcane production in south-central Brazil and to inform policy, adaptation planning, and further research.
  - Detailed model setup, parameterizations, and supplementary information are referenced (Appendix A; Vianna et al., 2022; Moura et al., 2018), enabling reproducibility and critical evaluation.

- References
  - Best et al. (2011); Clark et al. (2011); Sitch et al. (2007); Moura et al. (2018); Vianna et al. (2022); Cheesman et al. (2023); and related methodological papers listed in the deposit.