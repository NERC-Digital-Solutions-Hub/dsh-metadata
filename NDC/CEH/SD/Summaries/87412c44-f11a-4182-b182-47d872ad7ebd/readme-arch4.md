# Ozone flux, dynamic global vegetation, and carbon storage modelled data of tropical forests using the Joint UK Land Environment Simulator (JULES), 1900-2015

## Overview
- Dataset modeling ozone (O3) impacts on tropical forests using JULES v5.6 (1.25° × 1.875° resolution) for 1900–2014/2015.
- Combines input, output, and summary data on forest extents (current, secondary, potential) and O3 concentrations (preindustrial and 2005–2014) to assess O3 effects on net primary productivity (NPP) and global carbon cycle.
- Supports analysis of historical O3 exposure, its impact on nature-based climate solutions, and regional forest restoration/regrowth scenarios.

## What is included
- Spatial data at 1.25° × 1.875° resolution:
  - Forest cover types: Current, Secondary, Potential; grid_area, fractional covers (CF, SF, PF).
  - O3 concentrations: O3_PI (1900–1909), O3_PD (2005–2014), O3_change (1900–2014 difference).
  - SSP2050 projections: SSP_2050.csv (forest-type O3 levels under various SSPs).
- Model calibration and susceptibility data:
  - JULES_susceptibility.csv: relative NPP decline, POD1, and Susceptibility levels (Low, Mod, High).
- Model outputs for NPP and biomass:
  - Low_NPP.nc, Mod_NPP.nc, High_NPP.nc: predicted NPP declines under respective O3 susceptibilities.
  - Low_NPP_per.nc, Mod_NPP_per.nc, High_NPP_per.nc: percent declines.
- Carbon storage impacts:
  - Delta_carbon.csv: yearly changes in vegetation and soils (Pg-Carbon) under different susceptibilities.
- Per-forest-type NPP declines:
  - Forest_types_NPP_Low.csv, Forest_types_NPP_Mod.csv, Forest_types_NPP_High.csv: daily (% NPP decline) by forest type with area weights.
- Outputs under model validation and context:
  - Quality-controlled JULES outputs and supporting data used for CMIP6-style analyses.

## Modeling framework
- Tool: Joint UK Land Environment Simulator (JULES) v5.6, a land-surface model for soil-vegetation-atmosphere interactions.
- O3 damage representation:
  - A damage factor F adjusts Anet and gs at each time step (Eq. 1–3), dependent on a sensitivity parameter α and O3 flux above a threshold y.
  - A_mod = A_net × F; g_mod = g_s × F.
  - F causes instantaneous damage at uptake and a coordinated reduction in stomatal conductance.
- Calibration approach:
  - BET-Tr tropical broadleaf evergreen PFT calibrated to three O3 susceptibility levels (low, moderate, high) to match observed DRF-derived biomass declines and annual NPP (2009–2011).
  - α values adjusted per susceptibility to reproduce target DRF slopes.
- Model behavior:
  - JULES computes canopy-layer O3 fluxes for all leaves; DO3SE-based susceptibilities are represented using top-canopy sunlit leaf flux to align with calibration data.
- Inputs and forcing:
  - Meteorology and forcing from CRU-JRA v2.3; land-use change from Global Carbon Budget 2020; dynamic vegetation and Carbon Cycle configuration for pan-tropical simulations.

## Calibration and scenarios
- Calibration:
  - Adjusted α to replicate low, moderate, and high O3 susceptibilities for BET-Tr with observed dose–response functions (DRFs) and NPP targets.
- Simulation design:
  - Period: 1900–2014 (1900–2014; spin-up 1900–1920).
  - Scenario contrast: fixed (preindustrial) vs transient (1900–2014) O3 exposures.
  - Susceptibility levels applied globally across tropical tree types; C3 grasses tied to tree-derived α where data are lacking; C4 grasses tied to a specified reference value.
- Outputs and analysis:
  - Assess 10-year mean NPP differences (2005–2014) under fixed vs transient O3.
  - Track changes in total terrestrial carbon pools (vegetation and soils) over 1900–2014, including post-2000 trends.
  - Examine potential impacts on nature-based climate solutions: secondary forest regrowth and restoration areas under different O3 susceptibilities.

## Data structure and accessibility
- Gridded data files describe forest extents, O3 inputs, and modeled responses; accompanied by CSV summaries for accessibility and interoperability.
- Key file groups:
  - Forest cover and area: Current_forest.nc, Secondary_forest.nc, Potential_forest.nc, Forest_area metadata (grid_area.nc, CF, SF, PF).
  - O3 inputs: O3_PI.nc, O3_PD.nc, O3_change.csv (and related projections SSP_2050.csv).
  - Susceptibility and NPP outputs: JULES_susceptibility.csv; Low_NPP.nc, Mod_NPP.nc, High_NPP.nc; Low_NPP_per.nc, Mod_NPP_per.nc, High_NPP_per.nc.
  - Carbon impacts: Delta_carbon.csv.
  - Forest-type granularity: Forest_types_NPP_Low.csv, Forest_types_NPP_Mod.csv, Forest_types_NPP_High.csv.
- Data are designed for discoverability and reuse in CMIP6-style analyses, with explicit units and spatial-temporal resolution.

## Implications for data strategy and governance
- Demonstrates end-to-end data lifecycle: from model inputs (forest extents, O3 concentrations) to calibrated outputs (NPP, carbon pools) and scenario analyses (nature-based solutions under O3 stress).
- Highlights importance of:
  - Clear metadata and unit definitions to enable cross-study reuse.
  - Documentation of calibration procedures (α adjustments, target DRFs) for transparency and reproducibility.
  - Inclusion of multiple susceptibility levels to capture species- and forest-type variability.
  - Data packaging that supports weightings by forest area and daily temporal detail (Julian day indexing) for nuanced impact assessments.
- Useful for researchers and policy teams evaluating historical ozone impacts on tropical forests and future nature-based climate strategies, with opportunities for collaboration and data integration across networks.