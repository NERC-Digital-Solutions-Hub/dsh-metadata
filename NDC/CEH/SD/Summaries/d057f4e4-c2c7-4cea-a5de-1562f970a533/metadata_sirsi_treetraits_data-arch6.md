# Western Ghats tree functional trait data

## Overview
- Dataset from a Farm near Sirsi, Karnataka, India (14.49 N, 74.75 E; ~538 m) with measurements collected in Summer 2021.
- Focus: functional traits across thermal, hydraulic, and leaf characteristics to enable cross-species comparisons and data products for exploration.

## Key trait categories

- Thermal traits
  - CO2 assimilation temperature relationship (A-T) derived from leaf A-T curves using LICOR 6400
  - Temperature limits of Photosystem II (PSII) functioning (T50) from fluorescence (Fv/Fm) versus temperature

- Hydraulic traits
  - Water potential at 50% loss of hydraulic conductivity (P50) from vulnerability curves using pneumatic method
  - Leaf water potential measurements alongside xylem embolism assessment
  - Leaf turgor loss point (TLP) estimated via bench-dry/pressure-volume approach

- Leaf traits
  - Leaf area (scanned images), leaf mass per area (LMA), leaf dry matter content (LDMC)
  - Descriptors of leaf morphology and related metrics

## Data file and structure

- File: Treetraits_Sirsi_WesternGhats.csv
- Core fields include:
  - Species and coding: species, spcode
  - Metadata: Season, cancat (canopy position/topography), leafhabit (deciduousness)
  - Thermal traits: Aopt, Aopt.se, Topt, Topt.se, omega_June2004model_param, omega.se, Tspan80%, Tair_at_Topt, Tleaf_at_Topt, VPD_at_Topt, Cond_at_Topt, Transp_at_Topt, wp, wpse
  - PSII trait: t50, t50.se, T50.com, T5.com, dw.com, dwslope.com, qymax.com
  - Hydraulic trait: P50, P50-related fields, plus leaf water potential metrics
  - Leaf traits: ldmc, ldmc.se, Leafarea.se, leafperimeter, leafperimeter.se, leafwidth, leafwidth.se, lma, lma.se, Turgor_loss_point, TLP_stdev, TLP_std_error, number_of_samples_TLP
  - Derived statistics for multiple replicates: 1 and 2 suffixes (e.g., Aopt, Topt for replicate 1 and 2)
- Units and explanations are provided alongside variables; many entries include standard errors (se) and combined-fit variants (com)

## Measurement methods and model details

- Thermal traits (1.1.1 A-T)
  - In situ measurements with IRGA Li-6400 XT and leaf chamber at ~1000 μmol m⁻² s⁻¹; CO2 400 μmol mol⁻¹; RH ~60%
  - Temperature steps typically: 20, 24, 28, 32, 36, 40, 44, 48°C; leaf temps ranged ~21.4–45°C in summer
  - Data modeled with A_net = A_opt × exp(−((T_leaf − T_opt)/Ω)²) to derive A_opt, T_opt, Ω, and related parameters

- PSII thermal limit (1.1.2 T50)
  - Leaf discs exposed to controlled temperatures (25, 40, 45, 47.5, 50°C) for 30 min, then dark-adapted 30 min
  - Fv/Fm measured with PAM fluorometer; five discs per temperature per individual
  - Four-parameter logistic model fitted to obtain T50 (50% loss of PSII potential)

- Hydraulic vulnerability (1.2.1 P50)
  - Pneumatic method with bench dehydration to generate air-discharge vs. leaf water potential curves
  - P50 is leaf water potential at 50% air discharge; leaf water potential measured with Scholander pressure chamber

- Leaf turgor loss point (1.2)
  - Bench-dry (pressure-volume) approach; plot Ψ_leaf vs (100 − RWC) to identify Turgor Loss Point

- Leaf traits (1.3)
  - Leaf area from scanned images via ImageJ
  - LMA and LDMC following standard protocols

## Data quality and notes for use

- Two replicates are recorded for many traits (suffix 1 and 2); combined-fit variants (com) available for some parameters
- Variables include a mix of directly measured values and model-derived estimates (e.g., Topt, Aopt, T50)
- Ensure consistent interpretation of units across replicates and properly handle standard errors (se) and combined estimates (com)
- Metadata (season, canopy position, leaf habit) supports cross-site or cross-species comparisons and data subsetting

## Potential data products and use cases (Data Support perspective)

- Self-serve dashboards or pivot-table views to compare species on:
  - Thermal tolerance (Aopt, Topt, Tspan80%, Tair_at_Topt)
  - PSII thermo-tolerance (T50)
  - Hydraulic vulnerability (P50) and leaf water potential metrics
  - Leaf structural traits (LMA, LDMC, leaf area)
- Cross-trait analyses and visualizations (e.g., relationships between Topt and P50, or leaf economics vs. thermal tolerance)
- Data curation workflows:
  - Harmonize units and naming conventions (replicate handling, com vs. se)
  - Validate model-derived fields against raw measurements
  - Document data lineage and measurement conditions for transparency

## References and data provenance

- June, T., Evans, J. R. and Farquhar, G. D. (2004) – A simple new equation for the reversible temperature dependence of photosynthetic electron transport
- Sastry A., Guha A., Barua D. (2018) – Leaf thermotolerance in dry tropical forest tree species
- Curtis EM, Knight CA, Petrou K, Leigh A. (2014) – Recovery from thermal stress
- Ritz C., Streibig J. (2005) – Bioassay analysis using R
- Hazir M., Gloor E., Galbraith D. (2022) – Hydraulic traits and drought tolerance
- Bittencourt PR., Pereira L., Oliveira RS (2018) – Pneumatic method for measuring xylem embolism
- Sperry JS., Donnelly JR., Tyree MT (1988) – Method for measuring hydraulic conductivity and embolism
- Bartlett MK., Scoffoni C., Sack L. (2012) – Leaf turgor loss point predictors
- Schneider CA., Rasband WS., Eliceiri K.W. (2012) – NIH Image to ImageJ
- Wilson PJ., Thompson KE.N., Hodgson JG. (1999) – Predictors of leaf economics