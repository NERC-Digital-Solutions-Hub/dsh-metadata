# PLOT-SCALE  SIMULATIONS  WITH  MAIN-FRAME

- A detailed parameter and variable dictionary for plot-scale simulations driven by a main-frame model, covering vegetation, soil, hydrology, energy, and biogeochemical processes.
- Supports two vegetation schemes (High Vegetation HV and Low Vegetation LV) with per-C Crown representations and numerous carbon/nutrient pools, processes, and state variables.
- Outputs are time-series (hourly to daily) of many ecological and biogeochemical metrics, suitable for generating map-based data products after appropriate aggregation.

## What the document contains

- Structure and scope
  - Two primary sections: plot-scale simulations with main-frame; and associated parameter sets (Assigned Parameters, Internal Parameters, Input Time Series, etc.).
  - Extensive lists of variables with units, data types, and narrative descriptions describing their role in the model (e.g., albedo, net primary production, leaf area index, carbon pools, nutrient pools, soil and water variables, energy balance terms, radiative fluxes, and stress/uptake factors).

- Key variable families (high-level grouping)
  - Vegetation state and production
    - Above-ground production: NPP_H, NPP_L; ANPP_H, ANPP_L
    - Net ecosystem exchanges: NEE; Net assimilation metrics; NDVI
    - Leaf area and foliage metrics: LAI_H, LAI_L; LAIdead_H, LAIdead_L; leaf/foliage-related rates
    - Biomass pools and allocation: B_H, B_L across carbon pools; growth and maintenance respiration
    - Phenology and stress indicators: PHE_S_H/L; FNC_H/L; OPT_VegSnow and related switches
  - Carbon, nitrogen, phosphorus, potassium pools and fluxes
    - Numerous pool and flux variables (NupI_H/L, Nuptake_H/L, Nreserve_H/L, PHE_S_H/L, Potassium pools; LEAK_* fluxes; mineralization terms)
  - Soil, water, and hydrology
    - Soil moisture and storage: V (soil water volume), Osat, Osat-related parameters, SWE (snow water equivalent), SP_wc, SPAR, Ks/ Ks_Zs, Psi_l/H, Psi_s/H, Psi_x/H/L
    - Infiltration, runoff, drainage: Qi_in, Qi_out, Rd (drainage), Rh (infiltration/runoff), Rdark_H/L (leaf dark respiration), Rg (growth respiration)
    - Interactions with snow and ice: Csnow, Csno, SWE, snow interception, snow age, albedo-related terms
  - Energy and radiation
    - Net radiation, latent/ sensible heat fluxes: Rn, Qv, QE, QEV, HV, H, G, Gfin, Lvarious terms
    - Evaporation and interception fluxes: EIn_*, EICE, ELitter, Evaporation from surfaces and litter
  - Litter, litter- and soil-derived processes
    - Litter pools, leak fluxes (LEAK_*), litter respiration, litter/soil exports
  - Nutrient deposition and fertilization inputs
    - DepN, FertN, FertP, FertK, DepP, DepK, Upl
  - External drivers and inputs
    - CO2 concentration Ca; date/time data Datam/Date; atmospheric inputs Pre (pressure), PARB/PARD, Pr (precipitation), U (relative humidity), Ws (wind), Ca, Lat/Lon, Zbas (elevation)
  - Model configuration and options
    - PFT_opt_H/L, OPT_* controls (environmental limits, plant hydraulics, soil biogeochemistry, soil temp, etc.)
    - Case_root, CT_H/L, PFT_opt_H/L, HIST switch, j (time step), dQ/dQVEG residuals, OPT_SoilBiogeochemistry, OPT_VegSnow, etc.
  - Time step and data structure details
    - Time-series formats include hourly (h), daily (d), or multi-day aggregations; per-C crown and per-pool breakdowns; some fields marked as not active or not used in certain configurations.

- Inputs and configuration
  - Core input streams required to drive simulations: Ca (CO2), Datam/Date, Pre, PARB, PARD, Pr, U, Ws, ea/esat/VD relations, Lat/Lon, Zbas, Lmax_day, DeltaGMT, and various deposition/fertilization/uptake inputs (DepN/DepP/DepK, FertN/FertP/FertK, Upl).
  - Internal and assigned parameters for vegetation, soil, canopy, interception, root profiles, hydraulic conductances, and biogeochemical pathways.

- Outputs and potential GIS applications
  - Time-series outputs for map-based products: NDVI, NPP_H/NPP_L, NEE, LAI_H/LAI_L, SWE, NDVI, Albedo, soil moisture and water balance terms, energy fluxes (Rn, G, H, LE, Qv, QE, QEV), litter and organic matter fluxes, and various nutrient uptake and allocation metrics.
  - Spatial GIS use-case potential by aggregating plot-scale outputs to larger extents (e.g., per-pixel or per-plot layers) to produce maps of productivity, carbon balance, leaf area, soil moisture, snowpack, and energy fluxes across landscapes.
  - Time-series to seasonal/annual summaries suitable for thematic mapping (e.g., annual NEE, cumulative NPP, mean LAI, peak SWE, cumulative precipitation effects).

## Spatial and temporal considerations for GIS

- Scale and resolution
  - The model is described as plot-scale with per-C crown detail and HV/LV differentiation; GIS use would typically involve aggregating to landscape or gridded cells for maps.
- Temporal granularity
  - Numerous variables are time-series at hourly or daily granularity; for mapping, summarize to daily, monthly, seasonal, or annual values as needed.
- Data integration
  - Requires integration of climate inputs (Ca, Pre, PAR, radiation, humidity, wind) and deposition/fertilization streams from external data sources, with careful unit standardization.
- Data management
  - Large and complex datasets with many pools and fluxes; consider data packaging, naming conventions, and consistent units when exporting to GIS-ready formats (e.g., netCDF, HDF, or CSV/GeoTIFF derivatives).

## Practical considerations for GIS specialists

- Relevance to map products
  - Key map-ready outputs include: NDVI, LAI (high/low vegetation), NPP (high/low), NEE, albedo, SWE, soil moisture proxies, surface energy fluxes (QE, QEV, H, G), and precipitation/soil- moisture related stresses.
- Data preparation and quality
  - Ensure consistency of units across inputs; address not-active fields and deprecated options; validate time-series alignment with calendar dates; handle missing data and deposition/fertilization scenarios.
- Workflow suggestions
  - Preprocess inputs to a uniform spatial grid; run simulations per plot or per grid cell; post-process to derive seasonal/annual statistics; generate map layers for each target variable; document the aggregation method and time-steps used.
- Potential challenges
  - Managing data volume from hourly to multi-year horizons; aligning many input streams from different sources; varying data standards across inputs; ensuring computational efficiency for large-area applications.

## Summary for GIS-focused use

- The document defines a comprehensive, parametric plot-scale biogeochemical model with HV/LV vegetation schemes, detailed carbon/nutrient pools, soil and hydrology processes, and an extensive set of inputs (climate, deposition, fertilization) and outputs (NDVI, LAI, NPP, NEE, SWE, energy fluxes, soil moisture, etc.).
- For GIS applications, treat the model as a producer of rich, time-resolved map layers that require careful upfront data harmonization and post-processing to generate landscape-scale products.
- Effective GIS workflows will involve: standardizing inputs, executing the model per spatial cell/plot, aggregating hourly/daily outputs to map-ready intervals, and producing thematic layers of productivity, carbon balance, and hydrology/energy fluxes across the study area.