# PLOT-SCALE  SIMULATIONS  WITH  MAIN-FRAME

## Overview
- Presents a comprehensive data dictionary for a plot-scale, main-frame simulation model.
- Defines a large set of variables spanning energy balance, vegetation dynamics, carbon and nutrient cycles, water and soil processes, and biogeochemistry.
- Distinguishes High Vegetation vs Low Vegetation across many compartments and processes.
- Includes both inputs and internal/configuration parameters, with extensive time-series, scalar, and assigned-parameter entries.

## Data structure and types
- Variables are described with UNITS, TYPE, and DESCRIPTION for each item.
- TIME RESOLUTION: hourly, daily, or other time-step designations (e.g., Res. Time series [h], [d], [dx3], etc).
- DATA CATEGORIES: 
  - Input Time Series (e.g., Ca, Datam, Date, Pre, PARB, PARD, Pr, U, Ws, ea, esat, etc.)
  - Assigned Parameters (e.g., Aice, Ared, Bfac_lo_H, Bfac_lo_L, etc.)
  - Internal Parameters (e.g., Asur, CT_H/L, Bio_Zs, Damp_Zs, etc.)
  - Output/Derived Time Series (e.g., NEE, NPP_H/L, NPP_I, NPP sums, NPP over 7 days NPPI_H/L, etc.)
  - Case/Scenario Controls (CASE_ROOT, OPT_EnvLimitGrowth, OPT_PH, OPT_SoilBiogeochemistry, etc.)
  - Other structural/configuration fields (Datam, Date, j, I, O, PFT_opt_H/L, etc.)
- STRUCTURE: The document mixes two main blocks labeled "PLOT-SCALE  SIMULATIONS  WITH  MAIN-FRAME", with numerous subsections for variables, parameters, and options.

## Core variable categories and examples
- Energy balance and radiation
  - Albedo (ALB), G, H, Q, Qv, QE, QEV, dQ, dQVEG, Gfin
  - SIF, SIF_H/L, fapar_H/L (fraction of absorbed PAR)
  - Ts, TsV, Tdp, TdpI_H/L, T cold thresholds; surface and vegetation temperature contributions
- Atmosphere and inputs
  - Ca (CO2 atmospheric concentration), Ca_sno, Ca_snow (indirect references)
  - PARB, PARD, PAR radiation (direct/diffuse)
  - Pre (atmospheric pressure), U (relative humidity), Ws (wind speed), N (cloud cover or longwave), etc.
  - Date/time fields (Datam, Date) and DeltaGMT for solar integration timing
- Vegetation and phenology (two vegetation states)
  - NPP_H/NPP_L (net primary production by High/Low vegetation)
  - ANPP_H/ANPP_L (above-ground NPP)
  - NPP integral indicators NPPI_H/NPPI_L
  - NEE (net ecosystem exchange), N2flx, RA/RB (autotrophic/ respiration terms)
  - LAI_H/LAI_L (Leaf Area Index), LAIdead_H/L, SAI_H/L (Stem Area Index), SLL/L specifics
  - Nuptake/Uptake, Nuptake_H/L (N, P, K uptake for High/Low vegetation)
  - Xylem/leaf hydraulics and conductance terms (Kleas, Psi_l/x/s for various compartments)
  - PFT-related controls (PFT_opt_H/L), Stoich, OPT_VD, OPT_SM, OPT_VegSnow, etc.
- Carbon and nutrient pools
  - B_H/B_L (Carbon Pool Biomass for high/low vegetation across foliage, sapwood, roots, reserves, etc.)
  - Bfac_dayH/L, Bfac_lo_H/L, BfixN, Nreserve_H/L, NupI_H/L, Nuptake_H/L, P, K pools and related exports
  - CkC_H/L (Carbon Balance Closures by vegetation class), CkN_H/L, CkP_H/L, CkK_H/L
  - Rg/Rh/Rmc/Rmr/Rms, R_litter, R_microbe, R_bacteria, RexmyI/H/L (root exudates and mycorrhizal exports)
  - NPP/NPPI, N reserve, N uptake, soil biogeochemistry pools (PFTs and 55 soil pools)
- Soil, water, and hydrology
  - V (soil layer water storage), DQ and Q (energy fluxes and water balance residuals)
  - In/Out fluxes: Qi_in/out, Pr_liq/sno, Pr_runon, runoff terms Rd, Rdark_H/L, Rd (drainage, infiltration, percolation)
  - SWE, In_SWE, In_max_SWE (snow water equivalent and storage across vegetation states)
  - Soil properties and hydraulic parameters: Ks, Ks_Zs, Krock, Kbot, Slo_pot/top, Psi and water potential fields
  - Litter, litter fluxes, DOC/DON efflux (LEAK_DOC/DON/DOP/K/NH4/NO3/P)
- Phenology and growth controls
  - LDay_cr_H/L, LDay_min_H/L, Lmax_day (leaf onset and maximum day length)
  - mf_H/L, dmg_H/L (fruit maturation and leaf growth timing)
  - Case_root options for root profile (Exponential/Linear/Constant/Linear dose)
- Operational and diagnostic controls
  - OPT_EnvLimitGrowth, OPT_PH, OPT_PlantHydr, OPT_SM, OPT_VD, OPT_SoilTemp, OPT_ST, OPT_STh, OPT_SoilBiogeochemistry
  - HIST switch (deposition vs current deposition) and various quality-control flags (CK1/CK2 etc.)
  - I, j internal controls for hourly/daily stepping and time-step integration
- Miscellaneous
  - Spatial fractions and composition (Cbare, Ccrown, Crock, Curb, Cwat, Color_Class)
  - Plant and soil parameters for various components (Aice, Ared, Bio_Zs, CT_H/L, DSE_H/L, etc.)
  - PFT_opt_H/L structures for vegetation optics and parameters
  - jDay, mjDay_H/L for seasonal timing, Leaf onset thresholds, and related phenology

## Vegetation states, closures, and data products
- The document emphasizes two vegetation states (High vs Low Vegetation) with parallel sets of variables (e.g., NPP_H vs NPP_L, LAI_H vs LAI_L, NEE_H vs NEE_L, B_H vs B_L, etc.).
- Closure metrics and balance checks are included (CkC_H, CkC_L, CkN_H/L, CkP_H/L, CkK_H/L).
- Outputs and diagnostics likely feed dashboards or self-serve data products for end users to explore carbon, energy, and nutrient budgets across vegetation types.

## Data usage considerations for Data Support
- Data extracted includes extensive time-series across multiple compartments, enabling dashboards showing:
  - Carbon and nitrogen budgets by vegetation type and time scale
  - Energy balance residuals and flux components
  - Nutrient uptake and reserves (N, P, K) and their relation to deposition, fertilization, and case-root profiles
  - Soil moisture, temperature, sapwood/leaf hydraulics, and phenology-driven fluxes
- Data quality and formatting challenges to anticipate
  - Large, heterogeneous set of variables with many “not active” flags and numerous derived/intermediate fields
  - Patchy external inputs and multiple formats across inputs, time steps, and plant functional types
  - Need to map matrix-like time-series (per crown, per pool) to usable end-user datasets
- Potential data products
  - Self-serve dashboards for NEE, NPP, N balance closures, and water balance over time
  - Comparative analyses between High and Low Vegetation scenarios
  - Validation datasets via balance closures (CkC, CkN, CkP, CkK) and energy budget residuals (dQ, dQVEG)

## End notes and configuration
- The document ends with a collection of final parameter blocks and control flags (CASE_ROOT options, OPT_ flags, I/j internal controls).
- Includes extensive parameterization for root profiles, environmental limits on growth, soil biogeochemistry, and calculation steps (hourly vs daily vs internal time steps).