# Ozone flux, dynamic global vegetation, and carbon storage modelled data of tropical forests using the Joint UK Land Environment Simulator (JULES), 1900-2015

## Overview
- Dataset modelling the impacts of ozone (O3) on tropical forests over 1900–2014/2015 using JULES v5.6.
- Includes input, output, and summary data for forest extents (current, secondary, potential), and O3 concentrations (preindustrial and 2005–2014), at 1.25° x 1.875° resolution.
- Aims to quantify O3 effects on tropical forest net primary productivity (NPP) and the global carbon cycle, and to assess implications for nature-based climate solutions.
- Supported by NERC Trop-Oz project; should be used alongside empirical data on O3 susceptibility of tropical trees.

## Modelling framework and data inputs
- Uses Joint UK Land Environment Simulator (JULES) v5.6 to simulate soil–vegetation–atmosphere interactions with continuous, spatially explicit environmental drivers (meteorology, O3) and plant responses to CO2, aerosols, O3, temperature, drought, and nutrient cycling.
- O3 damage scheme: modifies net photosynthesis (Anet) and stomatal conductance (gs) via a damage factor F, governed by a sensitivity parameter α and a threshold y for O3 flux.
  - F = 1 − α × (Flux_O3 > y)
  - Amod = Anet × F
  - gmod = gs × F
- Calibration considerations:
  - JULES typically uses canopy-layer O3 flux; DO3SE uses uppermost sunlit leaves. For comparability, top-canopy sunlit leaf flux is used.
- Calibration targets:
  - Tropical broadleaf evergreen (BET-Tr) PFT calibrated to replicate three observed O3 susceptibilities (low, moderate, high) by adjusting α to match dose–response functions (DRF) against observed annual NPP (2009–2011) and biomass decline.
  - Other tropical PFTs set α values based on observed data from related species (e.g., C3 grasses; Saccharum spontaneum for C4 grasses).

## Simulation design and scenarios
- Time period: Pan-tropical simulations from 1900-01-01 to 2014-12-31 (1900–2014) with a 1000-year spin-up (1900–1920 climatology repeated).
- Forcing and inputs:
  - Meteorology and land-use forcing from CRU-JRA v2.3.
  - CO2 fertilization and land-use changes from Global Carbon Budget 2020.
  - O3 forcing from UKESM1 CMIP6 historical simulations; simulations include:
    - Fixed (preindustrial) O3 concentrations (1900–1909 average).
    - Transient O3 concentrations (1900–2014, hourly UKESM1 data).
- Forest cover context:
  - Baseline fractional forest cover weighted by ESA CCI landcover fractions (2015) regridded to JULES PFTs.
- O3 susceptibility scenarios:
  - Low, Moderate, High susceptibilities applied to BET-Tr and propagated to other PFTs as described.
- Outputs focus:
  - Impacts on NPP (current forest cover) under fixed vs transient O3 across the three susceptibilities.
  - Cumulative effects on terrestrial carbon pools (vegetation and soils) over 1900–2014 and since 2000.
- Nature-based solutions assessment:
  - Impacts on regions of secondary forest regrowth and potential forest restoration using 2014 wind-down data, regridded to JULES resolution.

## Outputs and data files (data structure)
- Total of 19 data files at 1.25° x 1.875° resolution plus CSV summaries.
- Forest cover and grid geometry:
  - Current_forest.nc (fractional current tropical forest cover)
  - Secondary_forest.nc (fractional secondary forest)
  - Potential_forest.nc (fractional potential secondary forest)
  - Grid_area.nc (area per grid cell)
- Ozone and change over time:
  - O3_PI.nc (preindustrial average annual O3, 1900–1909)
  - O3_PD.nc (present-day average annual O3, 2005–2014)
  - O3_change (difference between 1900s and 2005–2014)
  - SSP_2050.csv (2050 O3 projections by forest type and SSP scenario)
- Calibration and susceptibility:
  - JULES_susceptibility.csv (Rel_NPP decline, POD1, Susceptibility Low/Mod/High)
- NPP impacts by susceptibility:
  - Low_NPP.nc, Mod_NPP.nc, High_NPP.nc (kg-C y−1)
  - Low_NPP_per.nc, Mod_NPP_per.nc, High_NPP_per.nc (percent of control)
- Carbon stock impacts:
  - Delta_carbon.csv (yearly changes in vegetation and soils by susceptibility; Pg-C)
- Forest-type specifics:
  - Forest_types_NPP_L.csv, Forest_types_NPP_Mod.csv, Forest_types_NPP_High.csv
    - Columns include: index (Julian day), NPP_decline (%), weights (area weighting), Type (Current Forest, Secondary Forest, Potential Forest)
- Summary and references:
  - Data quality checks; model outputs aligned with prior JULES applications (CMIP6 context)
- Data deposit and access:
  - Acknowledges data deposition with CEH (catalogue CEH documents link provided in text)

## Data governance, provenance, and usage notes
- Provenance:
  - Model version: JULES v5.6
  - Forcing data: CRU-JRA v2.3; UKESM1 CMIP6 historical simulations
  - Spin-up and scenario design clearly documented
- Reproducibility and transparency:
  - Clear calibration process for BET-Tr PFT across three susceptibility levels
  - Explicit equations and methodology for O3 damage and its effects on photosynthesis and stomatal conductance
- Spatial and temporal coverage:
  - Global tropics with 1.25° x 1.875° resolution; 1900–2014 (or 2015) scope
- Data limitations and caveats:
  - O3 susceptibility is applied homogeneously to tropical forest types due to limited species-level data
  - O3 damage is treated as instantaneous at uptake with a linear decrease beyond a threshold
  - Potential uncertainties from forcing data, spin-up, and model parameterization
  - Regridding to model resolution introduces additional spatial uncertainty
- Accessibility and reuse:
  - Data are deposited with accompanying CSVs and NetCDFs; intended for use alongside empirical ozone sensitivity data and other Earth-system model outputs
  - Provides a framework for assessing past ozone exposure effects on tropical carbon dynamics and for exploring nature-based climate solutions under ozone change

## Limitations and considerations for data stewards
- Ensure clarity on the homogeneous susceptibility assumption when integrating with other datasets or performing cross-biome analyses.
- Note the distinction between top-canopy flux calibration (JULES) and leaf-level DO3SE comparisons in interpretation.
- When updating or extending, consider incorporating more species- or PFT-specific O3 sensitivity data to reduce ensemble uncertainties.
- Maintain traceability of forcing data versions (CRU-JRA v2.3, UKESM1 CMIP6) and calibration parameters (α values) for reproducibility.

## References
- Key model descriptions, calibration studies, and data sources are listed, including works on JULES, O3 damage schemes, and CMIP6 data, plus supporting literature for plant functional types and climate forcings.