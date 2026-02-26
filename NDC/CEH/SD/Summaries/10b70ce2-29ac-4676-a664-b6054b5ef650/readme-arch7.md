# Environmental conditions, ozone concentrations, biomass and leaf level functional traits data for 10 tropical tree species grown across a range in ozone concentrations within nine Open Top Chambers in Cairns, Australia.

## Overview
- A dataset documenting ozone concentrations, environmental conditions, biomass and leaf-level functional traits for 10 tropical tree species exposed to nine O3 concentrations in Open Top Chambers (OTCs) from July 2020 to November 2022.
- Includes final biomass, biomass partitioning, leaf traits (e.g., leaf mass per unit area, LMA; lamina LMA), and biochemical characteristics (total antioxidant capacity FRAP; total phenolic content; δ13C and δ15N).
- Contains calculated phytotoxic ozone dose (POD) for each species using the DO3SE model with two stomatal conductance (gs) parameterizations; selects the combined photosynthesis-stomatal conductance approach for calibration.
- Part of the NERC Trop-Oz project (NE/R001812/1) and to be viewed alongside accompanying data.

## Experimental setup and facility
- Conducted at the TropOz research facility (UoE/JCU) in Cairns, Australia, comprising nine independently controlled OTCs with a gradient of nine O3 exposures.
- Chambers: internal volume ~22.2 m3, fumigated 08:00–17:00 with O3 concentrations typically ranging 25–112 ppb.
- O3 monitoring: continuous measurements with a single UV-absorption O3 analyzer; data averaged to five-minute resolution.
- Meteorology: high-resolution air temperature, relative humidity, shortwave radiation, and PAR recorded at a central station; data averaged to 5–10 minute intervals.
- Plant material: ten tropical tree species from nine families; grown in 20 or 60 L pots; 61–191 days (average ~150) under varying O3 exposures; irrigation and controlled-release fertilizer used.
- Harvest: plants harvested for total biomass and partitioned into leaves, stems, roots; dry biomass determined at 70°C.

## Data collected
- Ozone concentrations by chamber and time; meteorological conditions (temperature, RH, PAR, solar radiation); experimental biomass (leaf, stem, root weights; AGB; total biomass); leaf-level morphometrics (LA_Av, LMA, LMA_lamina) and morphology.
- Leaf biochemistry: total antioxidant capacity (FRAP, expressed as mg AAE g-1 dry weight) and total phenolic content (TPC, expressed as mg GAE g-1 dry weight).
- Isotopic composition: δ13C and δ15N from leaf lamina tissue.
- POD and dose-response: computed phytotoxic ozone dose (POD_y) using DO3SE with two gs schemes (combined photosynthesis-stomatal conductance model and empirical-multiplicative gs model); POD1 and POD0 values used for dose-response functions.
- Experimental design: rolling introduction of species into OTCs; data include per-species and per-chamber ozone exposures and biomass outcomes.

## Data files and structure
- DO3SE model inputs (DOS3E_inputs.csv): 15 columns detailing species-specific parameters (e.g., m, g0, Vcmax, Jmax, gmax_O3, fmin, Tmin) required to parameterize DO3SE.
- Species-specific data files: multiple merged data files named by species code (e.g., Ba_merged_data.csv) containing 17 columns such as Day_of_year, Hour_of_day, Temperature, VPD, PAR, Pa, Wind, precipitation, and O3 concentrations in each chamber (Cham_1 to Cham_9); includes biomass and exposure indicators with NA where data are missing.
- Experimental_Biomass.csv: 19 columns including Species code, Plant_ID, Cham_ID, Leaves_dw, Petiole_dw, Stems_dw, Roots_dw, AGB, Biomass, LA_Av, LMA, LMA_lamina; captures final harvest metrics.
- Dose_response_functions.csv: 6 columns per species (Code) detailing relative biomass decline per unit POD0 and POD1 for Jarvis (J) and photosynthesis (P) parameterizations, plus AOT40-based DRF.
- Leaf biochemical and isotopic data: stored in associated files as part of the leaf sampling protocol (FRAP/TAC, TPC, δ13C, δ15N).
- References: comprehensive list of methodological and modelling sources supporting DO3SE, gs modelling, and analytical assays.

## Methods and modeling
- DO3SE ozone flux and POD calculation:
  - Two gs modelling approaches used: (i) combined photosynthesis-stomatal conductance model (optimal gs behavior) and (ii) empirical-multiplicative gs model.
  - gs parameterization for species derived from gas-exchange measurements; Vcmax and Jmax estimated from ACi curves using specialized fitting tools.
  - POD1 used to calibrate dose-response relationships; relative biomass vs. POD1 analyzed via linear decline (not accounting for hormesis in this dataset).
  - DO3SE inputs prepared per species and per chamber data; final selection of model calibration based on consistency with existing DGVMs.
- Gas exchange and leaf traits:
  - Gas-exchange data collected from newest fully developed leaves; night-time gs (g0) and day-time gs (g1) estimated; Vcmax and Jmax derived from ACi curves.
  - Leaf traits measured: leaf area, fresh/dry mass, LMA (whole leaf and lamina), and biochemical traits (FRAP, TPC).
- Quality control:
  - Meteorological data cross-validated against a local weather station; ozone monitors calibrated against zero-air standards; biomass weights rechecked to confirm accuracy.

## GIS and data integration considerations
- Spatial-temporal alignment: chamber-level O3 exposures linked to chamber positions within the OTC array; high-resolution meteorology enables time-resolved exposure mapping.
- Potential map-based products:
  - O3 exposure gradients across OTCs and over time.
  - POD flux and dose maps by species and chamber.
  - Biomass and leaf-trait distributions by species and O3 treatment, enabling spatially informed impact assessments.
- Data interoperability: per-species merged data files enable cross-species spatial analyses when combined with OTC geometry and chamber coordinates; DO3SE parameter file provides a reusable set of inputs for exposure modelling in GIS workflows.

## Quality, limitations, and usage notes
- Quality controls implemented for meteorology and O3 measurements; final biomass measurements validated with recalibration checks.
- Limitations:
  - Hormesis not modelled in the primary dose-response; linear decline approach used for dose-response.
  - Trials span 10 species with varying exposure durations; NA entries indicate missing data.
  - Data are facility- and chamber-specific; spatial generalization beyond OTC layout should be done cautiously.
- Usage:
  - Suitable for GIS-based visualization of ozone exposure and dose-response across species.
  - Can be used to link environmental conditions to biomass outcomes and leaf chemistry for spatially informed forest productivity analyses.

## References
- DO3SE modelling and plant gas-exchange literature (e.g., Emberson et al., Jarvis; Ball et al.; Medlyn et al.), assay methods for FRAP and TPC, isotopic analysis, and TropOz project documentation.