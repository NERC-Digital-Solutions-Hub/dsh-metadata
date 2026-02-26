# PLOT-SCALE  SIMULATIONS  WITH  MAIN-FRAME

## Overview
- Describes a comprehensive plot-scale simulation framework implemented on a mainframe, capturing environmental processes across energy, water, carbon, and nutrient cycles.
- Provides a dense set of state variables, inputs, parameters, and diagnostics for monitoring environmental health and biogeochemical/policy performance over time.

## Data Components and Structure
- Two vegetation strata: High Vegetation (HV) and Low Vegetation (LV), with many variables defined per C crown and per pool.
- Large set of input time series and assigned/internal parameters, including atmospheric drivers, deposition/fertilization, uplift, and soil-plant interactions.
- Core data categories include:
  - Albedo and surface energy balance (ALB, G, H, Q, Rn, Qv, QE, dQ, etc.)
  - Carbon fluxes and pools (NPP_H/NPP_L, ANPP_H/ANPP_L, NEE, N reserve/uptake, carbon pools B_H/B_L and sub-pools, litter, respiration, root exudates, etc.)
  - Above- and below-ground biology (LAI_H/LAI_L, LAIdead_H/L, SAI_H/SAI_L, NPP/NPPi, N allocation/uptake, phenology states PHE_S_H/L, C crown counts, Crown Area/Ccrown, leaf/root/wood turnover)
  - Nutrient cycles (N, P, K pools and balances; C/N/P/K uptake, suppression indices SupN/SupP/SupK, mineralization Min_N/Min_P, fertilization FertN/FertP/FertK, deposition DepN/DepP/DepK)
  - Soil biogeochemistry and hydrology (P, O, Psi-related variables; Ks/soil hydraulic parameters; soil water content and potentials; interception, infiltration, runoff, and drainage)
  - Plant hydraulics and optics (Psi_l/Psi_s/Psi_x, K/leaf conductances, stomatal resistance rs, gsr, r_soil, ri, fapar, fPAR absorption, Vmax, Rubisco capacities)
  - Phenology, structure, and stoichiometry (Stoich_H/L, NITs, Slo_top, a1/aR/aTop, crown-specific and layer-specific parameters)
- Time resolution includes hourly and daily series, with some components using multi-day aggregations (e.g., 18xd exports) and per-Crown outputs.

## Outputs and Analysts’ Key Metrics
- Carbon balance and fluxes:
  - NEE (Net Ecosystem Exchange), NPP_H/NPP_L, ANPP_H/ANPP_L, NUP uptake metrics, and maintenance/growth respiration components.
  - Total and per-pool carbon budgets (CkC_H, CkC_L, CkC_ALL) and nitrogen/phosphorus/potassium balance closures.
- Vegetation structure and function:
  - LAI_H/LAI_L, LAIdead_H/L, SAI_H/SAl_L, leaf area and leaf turnover metrics, leaf phenology states (PHE_S_H/L).
- Energy and water budgets:
  - Surface albedo (ALB), net and latent/sensible heat fluxes, radiation terms (Rn, Q, QE, QEV), soil heat and temperature terms, snow/ice interactions (Csnow, SWE, In_SWE).
- Soil and biogeochemistry:
  - 55 soil biogeochemistry pools with associated exports/exports to litter, root exudates, and mycorrhizal pathways; nutrient mineralization and uptake indices; interception and soil moisture dynamics.
- Hydrology and disturbance:
  - Runoff (Rd), infiltration, drainage, interception storage (In_H/L), Snow/ice dynamics, groundwater interactions, and related hydrological fluxes.
- Phenology and disturbance regimes:
  - Fruit maturation, leaf onset/sh shedding thresholds, drought mortality factors, temperature thresholds for phenology, and leaf/sapwood turnover parameters.
- Data provenance and structure indicators:
  - Explicitly defined inputs (Ca CO2, Pre, PARB/PARD, Pr, U, Ws, N, Lat/Lon, DepN/DepP/DepK, FertN/FertP/FertK) and internal/assigned parameters (Aice, Ared, CT_H/L, Cbare, PFT_opt_H/L, etc.), with clear mappings to model components.

## Temporal and Spatial Structure
- Plot-scale scope with per-Crown resolution for HV and LV groups.
- Time-stepped simulation governed by hourly and daily inputs and internal calculations, enabling detailed tracking of short-term processes and longer-term trends.
- Outputs intersect multiple domains (biogeochemistry, physiology, hydrology, energy balance) to support integrated environmental monitoring.

## Data Management and Accessibility
- Datasets are designed for storage and upload to appropriate portals, aligning with standard monitoring practices.
- The model’s rich, multi-variable output requires careful data management to maximize re-use, including combining with other datasets and ensuring underlying data accessibility for transparency and scrutiny.

## Relevance for Environmental Monitoring and Policy Analysis
- Enables consistent, time-series-based assessment of environmental health indicators and policy performance at the plot scale.
- Supports multi-pactor analyses (carbon, water, nutrient cycles) and cross-dataset integration to improve understanding of ecosystem responses to climate and anthropogenic factors.
- The extensive balance checks (CkC_ALL, CkC_H, CkC_L; N balance; P balance) provide diagnostics for model fidelity and potential policy-relevant insights on ecosystem functioning.

## Notable Features and Capabilities
- Comprehensive representation of both High and Low Vegetation scenarios with numerous crown- or layer-specific parameters.
- Detailed energy, water, and biogeochemical budgeting with explicit balance closures and flux decompositions.
- Flexible input structure including deposition, fertilization, tectonic uplift, and environmental limitation options.
- Embedded phenology, nutrientups, and root-match parameters enabling nuanced simulation of vegetation dynamics and soil interactions.

## Potential Challenges for Analysts
- Highly complex and voluminous variable set; requires careful data curation, validation, and documentation.
- Many parameters are per-Crown or per-soil-layer and may necessitate robust data handling and calibration to avoid overfitting or misinterpretation.
- Interdependencies across energy, hydrology, and biogeochemistry mean small input changes can propagate nonlinearly through multiple outputs.