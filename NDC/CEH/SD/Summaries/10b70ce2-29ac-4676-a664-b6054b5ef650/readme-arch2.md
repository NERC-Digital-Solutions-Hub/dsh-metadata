# Environmental conditions, ozone concentrations, biomass and leaf level functional traits data for 10 tropical tree species grown across a range in ozone concentrations within nine Open Top Chambers in Cairns, Australia

## Aim
- Provide a standardised, time-series dataset to assess ozone impacts on tropical vegetation and forest productivity, enabling scrutiny of environmental health and policy performance over time.
- Combine ozone exposure data with plant biomass, leaf traits, and biochemical characteristics to evaluate species-specific responses.

## What is included
- Measurements of ozone concentrations and environmental conditions (air temperature, relative humidity, PAR) across nine Open Top Chambers (OTCs) in Cairns, Australia, from July 2020 to November 2022.
- Final plant biomass (total and partitioned into leaves, stems, roots) and leaf-level functional traits (leaf area, leaf mass per unit area, lamina-only LMA).
- Biochemical leaf traits: total antioxidant capacity (FRAP assay) and total phenolic content (Folin-Ciocalteau method).
- Isotopic composition: δ13C and δ15N in leaf tissue, via EA-IRMS.
- Calculated phytotoxic ozone dose (POD) per species using the DO3SE model with two stomatal conductance parameterisations.

## Experimental facility and design
- TropOz facility (University of Exeter and James Cook University) at JCU Environmental Research Complex, Nguma-bada campus, Australia.
- Nine independently controlled OTCs (internal volume 22.2 m3) delivering ambient CO2 and nine distinct O3 concentrations in a gradient design.
- O3 concentrations typically 25–112 ppb during fumigation (08:00–17:00); continuous O3 monitoring with a single UV-absorption analyser; data interpolated to five-minute resolution.
- Meteorological data (temperature, relative humidity, shortwave radiation, PAR) collected at a central station and averaged for model inputs.

## Plant material and experimental setup
- Ten tropical tree species from nine families, selected to span a range of successional stages and leaf traits (e.g., leaf mass per area 58.1–142.5 g m-2).
- Seedlings sourced locally; planted in 20–60 L pots with local soil mix; acclimatised to full sun before transfer to OTCs.
- fumigation: typically 9 hours per day; 61–191 days (average ~150 days) of exposure.
- Replication: 3–4 plants per treatment per species; watering and fertilisation standardised.

## Measurements and analyses
- Harvest and biomass: leaves, stems, roots dried at 70°C to constant weight; total and above-ground biomass recorded; biomass partitioning calculated.
- Leaf traits: leaf area (via scanning), fresh/dry masses, whole-leaf and lamina LMA (g m-2).
- Biochemical analyses: TAC via FRAP assay (as mg AAE g-1 dry weight) and total phenolics via Folin-Ciocalteau (as mg GAE g-1).
- Isotopes: δ13C and δ15N from leaf lamina tissue using EA-IRMS.
- Data organisation includes a comprehensive set of derived metrics and standardized columns in each data file.

## DO3SE ozone dose calculations
- POD (phytotoxic ozone dose) calculated per species using the DO3SE model v3.1 with two stomatal conductance (gs) parameterisations:
  - Combined photosynthesis-stomatal conductance model (optimal stomatal behaviour), parameterised from gas-exchange data (Vcmax, Jmax, g1, etc.).
  - Empirical-multiplicative gs model.
- Leaf gas exchange data collected from the youngest fully expanded leaf of control plants to estimate gs: nocturnal g0 (night) and daytime g1 (day) via FitBB and plantecophys tools.
- DO3SE inputs include species-specific parameters and environmental inputs; outputs include POD1 and related metrics used for dose–response analyses.

## Data structure and key files
- DO3SE parameters: a species-specific parameter file detailing sensitivity to assimilatory demand, g0, Vcmax, Jmax, gmax_O3, fmin, Tmin, etc.
- DO3SE inputs and datasets:
  - "DOS3E_inputs.csv" — 15 columns with species code and physiology parameters.
  - Ten data files named "speciescode_merged_data.csv" containing: Julian day, hour, temperature, VPD, PAR, pressure, wind, precipitation (0 when irrigated), and O3 concentrations in each chamber (Cham_1 to Cham_9).
- Experimental_Biomass.csv — 19 columns including species code, Plant_ID, Cham_ID, biomass components (Leaves_dw, Petiole_dw, Stems_dw, Roots_dw), AGB, Total Biomass, Leaf Area (LA_Av), LMA, LMA_lamina.
- Dose_response_functions.csv — 6 columns per species: POD0_J_DRF, POD1_J_DRF, POD0_P_DRF, POD1_P_DRF, AOT40_DRF (relative biomass decline per unit dose).
- Data sources and references included to support DO3SE modelling and dose–response interpretation.

## Quality control
- Meteorological data: factory-calibrated sensors cross-checked against a local reference station.
- O3 concentrations: validated against zero-air standards every sampling round (~22 min).
- Biomass measurements: annually calibrated scales; outliers re-weighed after longer drying where needed.

## Use and relevance for environmental monitoring
- Delivers a harmonised, auditable dataset linking ozone exposure to plant growth, leaf physiology, and biochemical responses across multiple tropical species.
- Supports cross-study comparisons and integration with larger policy- and monitoring-focused frameworks by providing standardised data formats, DO3SE-based ozone flux estimates, and dose–response relationships.
- Enables exploration of species- and trait-based sensitivity to ozone, informing forest productivity assessments and ozone policy impact analyses.
- Data housed as part of the Trop-Oz project (NE/R001812/1) and accessible alongside related datasets for broader ecological interpretation.