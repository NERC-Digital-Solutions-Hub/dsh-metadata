# Ozone flux, dynamic global vegetation, and carbon storage modelled data of tropical forests using the Joint UK Land Environment Simulator (JULES), 1900-2015

## Overview
- A pan-tropical modelling study of ozone (O3) impacts on tropical forests from 1900 to 2014/2015 using JULES v5.6.
- Integrates spatially-explicit input, output, and summary data to assess how O3 exposure affects net primary productivity (NPP) and the global carbon cycle.
- Compares fixed (preindustrial) vs transient (historical) O3 forcing and explores implications for nature-based climate solutions.
- Data are designed to be used alongside empirical O3 susceptibility data for tropical trees.

## Modelling framework
- Tool: Joint UK Land Environment Simulator (JULES) v5.6, at 1.25° latitude × 1.875° longitude resolution.
- Features: Incorporates environmental drivers (meteorology, CO2, aerosols, O3), vegetation responses, nutrient cycling, drought, and climate-vegetation interactions.
- O3 damage scheme: Adjusts net photosynthesis (Anet) and stomatal conductance (gs) via a damage factor F, which depends on a sensitivity parameter α and a flux threshold y; A and gs decline with increasing O3 flux above the threshold.
  - F, Amod, and gmod defined by the referenced equations, with canopy-layer calculations for O3 flux to the top leaves to align with DO3 SE dose–response concepts.
- Calibration: Calibration of the O3 response factor α is performed to match observed dose–response functions (DRFs) for tropical broadleaf evergreen trees (BET-Tr) across three susceptibility levels (low, moderate, high).

## Calibration of O3 susceptibility
- BET-Tr PFT calibrated to reproduce one of three susceptibility levels by adjusting α to match annual NPP (2009–2011) against observed DRF slopes.
- For other tropical PFTs, α is set to values based on empirical analogues (e.g., C3 grasses aligned to C3 trees; C4 grasses to Saccharum spontaneum data in the cited study).
- Calibration outcome summarized in a figure showing the fit for low, moderate, and high susceptibility.

## Simulation design
- Time period: 1900–2014 (pan-tropical).
- Susceptibility: Homogeneous O3 susceptibility per simulation (low, moderate, high).
- Modelling framework: Dynamic vegetation (TRIFFID-style) with evolving PFT fractions and Leaf Area Index (LAI) under changing environmental conditions.
- Forcings:
  - CO2 variation and land-use/land-cover change as in Global Carbon Budget 2020.
  - Meteorology from CRU-JRA v2.3.
  - O3 forcing from UKESM1 CMIP6 historical simulations, with a 1000-year spin-up (1900–1920 climatology).
- Experimental design: Compare simulations with fixed preindustrial O3 (1900–1909 average) to simulations with transient, historically varying O3 (1900–2014).

## Impacts assessed
- Net Primary Productivity (NPP): Spatially-resolved responses under different O3 susceptibilities; analysis includes weighting by current forest extent.
- Terrestrial carbon pools: Time-series and cumulative impacts on vegetation and soils, accounting for NPP declines, vegetation dynamics, and soil biogeochemistry.
- Nature-based solutions: Examination of potential forest restoration and secondary forest regrowth regions in light of O3 susceptibility, using regridded outputs to match model resolution.
- Outputs are analyzed since 2000 and across the full 1900–2014 period to quantify changes in carbon stocks and productivity.

## Outputs and data products
A dataset collection comprising 19 data files (gridded) and accompanying CSV summaries at 1.25° × 1.875° resolution, including:

- Forest cover types and extents
  - Current_forest.nc: Fractional cover of tropical forest (BET-Tr) in 2015
  - Secondary_forest.nc: Fractional cover of secondary tropical forest
  - Potential_forest.nc: Fractional cover of potential secondary forest
  - Grid_area.nc: Grid cell area in m^2
- Ozone forcing and changes
  - O3_PI.nc: Preindustrial (1900–1909) average O3
  - O3_PD.nc: Present-day (2005–2014) average O3
  - O3_change: Change in O3 between preindustrial and present-day
  - SSP2050.csv: Present and 2050 O3 values by forest type, with uncertainties and SSP context
- O3 susceptibility calibration
  - JULES_susceptibility.csv: Relative NPP decline, POD1, and Susceptibility level (Low, Mod, High)
- NPP impacts under O3 scenarios
  - Low_NPP.nc, Mod_NPP.nc, High_NPP.nc: NPP declines (kg-C y-1)
  - Low_NPP_per.nc, Mod_NPP_per.nc, High_NPP_per.nc: NPP declines as percent of control
- Accumulated carbon impacts
  - Delta_carbon.csv: Yearly changes in vegetation and soils partitioned by susceptibility (Veg_high/mod/low; Soils_high/mod/low)
- Forest-type-level NPP declines
  - Forest_types_NPP_Low.csv, Forest_types_NPP_Mod.csv, Forest_types_NPP_High.csv: Daily NPP decline, area-weighting, and forest type (Current, Secondary, Potential)
- Data provenance notes
  - Descriptions align with data deposit accompanying the modelling exercise

## Data quality and validation
- Quality control checks compare outputs against prior JULES applications within CMIP6 experiments.
- Outputs validated for consistency with prescribed forcings and calibration targets.

## Data access and references
- Data deposit comprises 19 gridded NetCDF files and multiple CSV summaries; the spatial outputs are designed for integration with other data products on forest cover and ozone exposure.
- References accompany the dataset, detailing the JULES model descriptions, calibration approaches, and supporting literature on ozone impacts, plant physiology, and CMIP6 forcing data.

## How Data can be used
- Assess historical and future ozone impacts on tropical forest productivity and carbon storage.
- Quantify the contribution of O3 to changes in tropical carbon pools and productivity in the context of different policy Scenarios (SSP-based).
- Explore implications for nature-based climate solutions, including secondary forest regrowth and restoration planning under varying O3 susceptibility assumptions.
- Develop dashboards or reports to communicate spatial patterns of NPP decline and carbon stock changes across tropical regions.