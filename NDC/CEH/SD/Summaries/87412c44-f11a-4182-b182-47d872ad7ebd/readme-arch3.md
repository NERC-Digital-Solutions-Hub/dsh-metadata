# Ozone flux, dynamic global vegetation, and carbon storage modelled data of tropical forests using the Joint UK Land Environment Simulator (JULES), 1900-2015

## Overview
- Spatially-explicit dataset from the Joint UK Land Environment Simulator (JULES) v5.6, describing ozone (O3) impacts on tropical forests from 1900 to 2014/2015.
- Includes input, output, and summary data: forest extents (current, secondary, potential-secondary) and O3 concentrations for preindustrial (1900–1910) and recent (2005–2014) periods at 1.25° × 1.875° resolution.
- Outputs quantify O3 effects on Net Primary Productivity (NPP) and the cumulative impact on global carbon cycling.
- Supported by NERC Trop-Oz project; designed to complement empirical O3 susceptibility data for tropical trees.

## Modelling framework
- Uses JULES as a land surface model to simulate soil–vegetation–atmosphere interactions with continuous, spatially explicit drivers (meteorology, O3, CO2, aerosols, etc.).
- O3 damage scheme modifies net photosynthesis (Anet) and stomatal conductance (gs) via a damage factor F that depends on an O3 flux threshold (y) and a sensitivity parameter (α).
  - F = 1 − α × (O3 flux > y)
  - A_mod = Anet × F
  - g_mod = gs × F
- Calibrations relate canopy-level processes to observed O3 susceptibilities by aligning model outputs with dose–response functions (DRFs) from empirical data.
- Calibration ties: JULES canopy-level fluxes are matched to DO3 SE measurements by focusing on the top canopy sunlit leaves for comparison.

## Calibration and scenarios
- Tropical broadleaf evergreen PFT (BET-Tr) calibrated to represent three susceptibility levels: low, moderate, and high.
- α (O3 response factor) adjusted iteratively to reproduce annual NPP (2009–2011) against observed DRF slopes.
- Other PFTs assigned α based on analogies:
  - C3 grasses: α equal to tropical trees
  - C4 grasses: α taken from Saccharum spontaneum cv. Mandalay (0.04 with a 2 nmol m⁻² s⁻¹ threshold)
- Calibration outputs documented in JULES_susceptibility.csv (relative NPP declines, POD1 values, susceptibility label).

## Simulation design
- Pan-tropical simulations from 1900-01-01 to 2014-12-31, with homogeneous O3 susceptibility across grid cells per scenario (low, moderate, high).
- Dynamic vegetation framework (Cox 2001; Harper et al. 2018) allows changes in PFT fractional cover and LAI under varying conditions.
- Forcing and inputs:
  - CO2 concentrations and land-use change from Global Carbon Budget 2020
  - Meteorology from CRU-JRA v2.3
  - O3 forcing from UKESM1 CMIP6 historical simulations
- Experimental design contrasts:
  - Fixed O3: average 1900–1909
  - Transient O3: 1900–2014 (hourly O3 from UKESM1)
- Long spin-up: 1900–1920 climatology repeated to initialize runs.

## Impacts assessed
- Changes in pan-tropical NPP under fixed vs transient O3 for BET-Tr by 2005–2014.
- Weighted regional outputs using 2015 ESA CCI forest extent data to reflect actual forest cover fractions.
- Cumulative impacts on terrestrial carbon pools (vegetation and soils) across 1900–2014 and post-2000.
- Evaluation of implications for nature-based climate solutions, using secondary forest regrowth and restoration area under the same O3 susceptibility spectrum.

## Nature-based solutions and spatial scaling
- Assessment of 2014 air quality effects in regions of forest regrowth and restoration potential.
- Original-resolution binary forest data regridded to JULES resolution to compute:
  - Existing forest area
  - Secondary forest regrowth
  - Potential forest restoration

## Data products and structure
- 19 data files (gridded data at 1.25° × 1.875°, plus CSV data summaries) plus descriptive metadata.
- Key data categories:
  - Forest cover and extents
    - Forest_type: Current_forest.nc, Secondary_forest.nc, Potential_forest.nc
    - grid_area.nc (cell area in m²)
    - Current_forest, Secondary_forest, Potential_forest fractions (CF, SF, PF)
  - O3 inputs and changes
    - O3_PI.nc (preindustrial 1900–1909), O3_PD.nc (2005–2014), O3_change (1900–2014)
    - SSP_2050.csv with present and 2050 O3 estimates across forest types under SSP scenarios
  - Model calibration and susceptibility
    - JULES_susceptibility.csv (Rel_NPP, POD1, Susceptibility levels Low/Mod/High)
  - NPP impacts and declines by susceptibility
    - Low_NPP.nc, Mod_NPP.nc, High_NPP.nc (NPP decline in kg C y⁻¹)
    - Low_NPP_per.nc, Mod_NPP_per.nc, High_NPP_per.nc (percentage decline)
  - Accumulated carbon impacts
    - Delta_carbon.csv (Year, Veg_low/Mod/High, Soils_low/Mod/High)
  - Forest-type-specific NPP details
    - Forest_types_NPP_Low.csv, Forest_types_NPP_Mod.csv, Forest_types_NPP_High.csv
- File-level details include units, variable definitions, and context for regridding and weighting.

## Quality control and data provenance
- Outputs checked against prior JULES CMIP6 applications to ensure consistency.
- Inputs drawn from established datasets (UKESM1 CMIP6, CRU-JRA v2.3, ESA CCI, Gridded forest datasets) with explicit regridding to model resolution.
- Clear documentation of variables, units, and data transformations to enable reproducibility and auditability.

## Relevance for monitoring frameworks
- Provides a transparent, well-documented modelling pipeline to monitor ozone-related risks to tropical forest productivity and carbon storage.
- Delivers a suite of interoperable data products (gridded outputs and summary CSVs) suitable for integration into policy monitoring dashboards, scenario analyses, and data governance processes.
- Highlights data dependencies (e.g., O3 forcing, forest extent datasets, meteorology inputs) and the need for metadata quality to support data sharing and verification across organisations.
- Demonstrates approach to calibrating ecosystem responses to pollutants, enabling scenario comparisons and sensitivity analyses essential for monitoring framework decisions.

## References
- Key sources covering JULES model descriptions, ozone damage representation, calibration approaches, and data inputs (Best et al., 2011; Clark et al., 2011; Cox, 2001; Eyring et al., 2016; Friedlingstein et al., 2020; Griscom et al., 2017; Harper et al., 2016–2023; Huntingford et al., 2017, 2022; Leung et al., 2022; Oliver et al., 2018, 2022; Mercado et al., 2009; Sitch et al., 2007; Sellar et al., 2019; Vancutsem et al., 2021).