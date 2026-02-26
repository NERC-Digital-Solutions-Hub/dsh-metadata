# Ozone flux, dynamic global vegetation, and carbon storage modelled data of tropical forests using the Joint UK Land Environment Simulator (JULES), 1900-2015

- Purpose and scope
  - Spatially-explicit input, output, and summary data from JULES V5.6 modeling of tropical forests (extant, current-secondary, and potential-secondary) and ozone (O3) concentrations from 1900 to 2014/2015.
  - Assesses impact of O3 on tropical forest net primary productivity (NPP) and the global carbon cycle, including cumulative carbon pool changes.
  - Data complement empirical O3 susceptibility data for tropical trees; linked to the NERC Trop-Oz project.

- Modelling framework
  - Uses JULES v5.6 (1.25° x 1.875° resolution) to simulate soil–vegetation–atmosphere interactions with environmental drivers (meteorology, CO2, aerosols, O3, drought, nutrients).
  - O3 damage scheme: modifies net photosynthesis (Anet) and stomatal conductance (gs) via damage factor F, defined by a sensitivity parameter α and a flux threshold y.
  - Equations (conceptual):
    - F = 1 − α × (O3 flux > y)
    - A_mod = Anet × F
    - g_mod = gs × F
  - O3 flux to the canopy is calculated per canopy layer (sunlit vs shaded); comparisons to DO3-SE use top-of-canopy sunlit-leaf flux.

- Calibration of O3 susceptibility
  - Tropical broadleaf evergreen PFT (BET-Tr) calibrated to replicate three susceptibilities (low, moderate, high) by adjusting α to match observed dose–response functions (DRFs) from biomass decline data (2009–2011).
  - α values for BET-Tr: low around 0.03, moderate around 0.05, high around 0.12 (with corresponding DRF slopes matching targets).
  - For other PFTs: C3 grasses adopt the tree’s α; C4 grasses adopt α = 0.04 at a 2 nmol m−2 s−1 threshold (per species analogs).

- Simulation design and forcing
  - Pan-tropical simulations from 1900-01-01 to 2014-12-31, with homogeneous O3 susceptibility fixed to one of three levels (low, moderate, high).
  - Forcing inputs: CO2 and land-use/land-cover changes from Global Carbon Budget 2020; meteorology from CRU-JRA v2.3.
  - O3 scenarios:
    - Fixed: average O3 ~1900–1909.
    - Transient: 1900–2014, hourly O3 from UKESM1 CMIP6 historical runs; includes a 1000-year spin-up (1900–1920 climatology cyclically repeated).
  - Forest extent weighting: results weighted by current forest extent (ESA CCI, 2015).

- Analyses conducted
  - Impacts of changing O3 over the 20th century on current pan-tropical NPP (comparing fixed vs transient O3 across BET-Tr and weighted by forest extent).
  - Cumulative impacts on terrestrial carbon pools (NPP declines, vegetation shifts, soil biogeochemistry) across 1900–2014 and since 2000.
  - Implications for nature-based climate solutions: effects of O3 susceptibility on secondary forest regrowth and potential forest restoration, using regridded data to JULES resolution.

- Data products and file catalogue
  - 19 data files at 1.25° x 1.875° resolution plus CSV summaries, including:
    - Forest cover types and area metrics:
      - Current_forest.nc (fractional current tropical forest cover, BETTr)
      - Secondary_forest.nc (secondary forest cover)
      - Potential_forest.nc (potential secondary forest cover)
      - Grid_area.nc (grid cell areas, m²)
    - O3 concentrations and changes:
      - O3_PI.nc (pre-industrial 1900–1909)
      - O3_PD.nc (present-day 2005–2014)
      - O3_change (1900–1909 vs 2005–2014)
      - SSP_2050.csv (Forestry O3 levels by SSP scenarios for 2050)
    - JULES calibration and outputs:
      - JULES_susceptibility.csv (relative NPP decline, POD1, susceptibility level)
      - Low_NPP.nc, Mod_NPP.nc, High_NPP.nc (NPP declines under each susceptibility level)
      - Low_NPP_per.nc, Mod_NPP_per.nc, High_NPP_per.nc (percent changes)
      - Delta_carbon.csv (yearly changes in vegetation and soils under each susceptibility)
      - Forest_types_NPP_Low.csv, Forest_types_NPP_Mod.csv, Forest_types_NPP_High.csv (NPP declines by forest type with day-indexed columns, weights, and type)
  - Documentation and references embedded within the data deposition (model descriptions, calibration figures, and methodological notes).

- Quality control and data provenance
  - Outputs checked against prior JULES applications in CMIP6 contexts.
  - Data designed to be interpretable alongside empirical O3 susceptibility data for tropical species.

- Related references and external resources
  - Key methodological and data sources for JULES v5.6, ozone damage schemes, plant functional types, and CMIP6 UKESM1 forcing, plus supporting studies on tropical vegetation and carbon cycling.

- Usage note for analysts
  - Use the Jacobian-like calibration to select a plausible O3 susceptibility level for BET-Tr in your analysis, and compare fixed vs transient O3 scenarios to isolate potential impacts on tropical carbon stocks.
  - Leverage the forest-type NPP and Δcarbon datasets to quantify regional or global shifts under different O3 exposure assumptions.
  - Integrate with empirical O3 sensitivity data to validate model projections and to ground-truth interpretations for policy and management contexts.