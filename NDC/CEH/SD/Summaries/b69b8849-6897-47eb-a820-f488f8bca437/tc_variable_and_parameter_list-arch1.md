# PLOT-SCALE SIMULATIONS WITH MAIN-FRAME

- A comprehensive data dictionary for a plot-scale, main-frame biogeochemical and ecohydrological model.
- Defines a large set of variables, parameters, and time-series outputs used to simulate vegetation dynamics, soil processes, and energy/wate budgets.

- Data structure and categories
  - Input time series: climate and environmental drivers (CO2 Ca, DeltaGMT, Lat, Lon, Zbas, precipitation Pr, PAR, RH, wind Ws, air/ocean variables, etc.), atmospheric deposition and fertilization (DepN, FertN, DepP, FertP, DepK, FertK), and plant/soil inputs (Ca, Datam, Date, Pre, U, PARB, PARD, U_SWE, SWE, etc.).
  - Assigned parameters: per-crown and per-vegetation type parameters governing structure, physiology, and allocation (e.g., Aice, Ared, Bfac_lo_H/L, Bharv_H/L, Ccrown, PFT_opt_H/L, gR_H/L, gcoef_H/L, Vmax_H/L, Nl_H/L, Sl_H/L, etc.).
  - Internal parameters: numerous model-internal constants and derived quantities (Asur, Bio_Zs, CT_H/L, Cbare, Cwat, Krock, Ks, Psi thresholds, dQ, fapar, q_runon, etc.) used during simulation.
  - Time-series outputs: daily and hourly records for albedo, gross/net primary production, leaf/wood/tissue pools, respiration (autotrophic, heterotrophic, microbial), litter dynamics, carbon and nutrient fluxes, soil moisture and temperature, energy fluxes (Q*, H, QE, Qv), water/ion fluxes, phenology states, and indices (NDVI, NEE, NPPI, NupI, TexN/L, TexP/L, etc.).
  - Structural organization: split by High Vegetation vs Low Vegetation, with per-Crown resolution for many variables; integration across 55 soil pools and multiple element cycles (C, N, P, K) and 18-component soil biogeochemistry exports in some sections.
  - Outputs and diagnostics: mass/energy closures (CkC_H/L, CkN_H/L, etc.), balance checks, and integrated indicators (NPPI, NEE, NPP_H/L, Nreserve_H/L, etc.).

- Model scope and processes represented
  - Vegetation physiology and carbon budgeting: net assimilation (An_H/L), photosynthetic capacity (Vmax_H/L, Jmax, fapar), leaf and canopy dynamics (LAI_H/L, LAIdead_H/L, SAI_H/L), and carbon allocation to pools (B_H/L, Bfac_dayH/L, Kreserve_H/L, Kuptake_H/L, TexN_H/L, TexP_H/L, TexK_H/L, etc.).
  - Growth, turnover, and respiration: growth respiration (Rg_H/L), maintenance respiration (Rmr_H/L, Rmc_H/L, Rg, Rb), fruit maturation, leaf/tissue turnover, and exudation (RexmyI/H/L, Rmyc_AM/EM).
  - Biogeochemistry and nutrient cycles: detailed N, P, and K pools and fluxes, mineralization/mineralization-related factors (Min_N, Min_P, SupN/P/K), nutrient uptake and suppression indices, and soil biogeochemistry pathways with many components (NupI, Nuptake, Nreserve, N2flx, NEE, etc.).
  - Hydrology and energy balance: soil moisture content and layers, interception storage, runoff (Rd, Rh, Rmc, Rg), infiltration, soil temperature (Tdp, Ts, TsV), energy fluxes (Q*, Qv, QE, Latent/Sensible heat), snow/ice processes (SWE, In_SWE, Csnow, e_relN, f, fapar, fLitter), and groundwater interactions.
  - Soil and plant hydraulics: multiple hydraulic conductances and potentials (Psi_l_H/L, Psi_s_H/L, Psi_x_H/L), interception and leaf/soil water relations, and root profiles (CASE_ROOT).
  - External controls and options: environment-limited growth (OPT_EnvLimitGrowth), soil biogeochemistry toggle (OPT_SoilBiogeochemistry), plant hydraulics toggles, and various tolerance/threshold parameters (TmaxS, TminS, Tlo_H/L, Tcold_H/L, Psi thresholds, etc.). Includes options and tolerances for numerical solving (OPT_PlantHydr, OPT_SM, OPT_VD, etc.).

- Granularity and local applicability
  - Per Crown and per Crown Type: many state variables and fluxes are tracked for High Vegetation and Low Vegetation, with explicit crown-level resolution.
  - Per soil layer and pool: extensive coverage of soil layers, pools, and biogeochemical compartments (e.g., 55 soil Pools, P, PHE_S_H/L, Slo_top, Slo_pot, Ks, Osat, Osat, etc.).
  - Temporal resolution: hourly and daily time steps, with some 18-day or 18xd references and 365-day integrations for annual nutrient uptake.
  - Rich metadata: each variable includes units, type (input, assigned parameter, internal, or time-series), and a description, facilitating data extraction and reproducibility.

- Practical implications for analysts
  - Enables comprehensive correlation and predictive analyses across carbon, nutrient, and water cycles, vegetation dynamics, and energy budgets at the plot scale.
  - Rich set of inputs and outputs supports model validation, sensitivity testing, and scenario analysis using per-crown and per-layer data.
  - Many features are optional or not active, allowing streamlined configurations while preserving the ability to enable advanced processes as needed.

- Overall impression
  - The document provides a detailed, highly structured schema for a sophisticated plot-scale ecosystem model, encapsulating climate inputs, vegetation structure, carbon/nutrient pools, soil biogeochemistry, and energy/hydrology with explicit metadata to support data-driven analysis and model-informed decision making.