# Environmental conditions, ozone concentrations, biomass and leaf level functional traits data for 10 tropical tree species grown across a range in ozone concentrations within nine Open Top Chambers in Cairns, Australia.

## Study purpose and scope
- Provides environmental, ozone, biomass, and leaf-level functional trait data for 10 tropical tree species exposed to a gradient of ozone concentrations in Open Top Chambers (OTCs) in Cairns, Australia.
- Spans July 2020 to November 2022 and includes final biomass, biomass partitioning, and leaf biochemical characteristics.
- Supports analysis of ozone impacts on tropical vegetation productivity and links to ozonetic dose–response modeling (POD) including DO3SE-based flux calculations.

## Experimental facility and design
- TropOz research facility at the University of Exeter (UoE) and James Cook University (JCU) in Cairns.
- Nine independently controlled OTCs with a gradient of nine ozone exposures, ambient CO2, and site-sourced measurements.
- On-site ozone generation with continuous monitoring (UV-absorption O3 analyzer) and high-resolution meteorological data collection; typical O3 exposure 25–112 ppb during fumigation hours (08:00–17:00).
- Data were collected at ~5-minute resolution per chamber and interpolated to continuous time series; 15-minute sampling cadence for gas and meteorological data.

## Plant material and cultivation
- Ten tropical tree species from nine families, representing a range of leaf morphologies and successional stages.
- Seedlings sourced locally; grown in 20–60 L pots with a garden mix and drainage amendment; acclimated to full sun before OTC transfer.
- O3 fumigation typically lasted 9 hours per day; plants grown for 61–191 days (mean ~150 days); daily drip irrigation and controlled-release fertilization.

## Data collected and measurements
- Biomass and partitioning: final dry weights for leaves, petioles, stems, roots; above-ground biomass (AGB) and total biomass.
- Leaf functional traits: leaf area, leaf mass per unit area (LMA) for whole leaf and lamina; lamina LMA; chlorophyll-related metrics not explicitly listed.
- Biochemical and elemental analyses: total carbon (TC) and nitrogen (TN); stable isotopes δ13C and δ15N; total antioxidant capacity (TAC) via FRAP; total phenolic content (TPC) via Folin–Ciocalteu; results expressed as Gallic or Ascorbic Acid equivalents per g dry weight as appropriate.
- Environmental conditions: air temperature, relative humidity, photosynthetically active radiation (PAR), vapor pressure deficit (VPD), atmospheric pressure, wind, precipitation; chamber-specific O3 concentrations.

## O3 dose, flux modeling and dose–response
- Ozone dose (POD) and flux calculated using the DO3SE model (v3.1) with two stomatal conductance representations: a combined photosynthesis-stomatal conductance model and an empirical-multiplicative model.
- Species-specific parameterization using photosynthetic traits (Vcmax, Jmax) and stomatal sensitivity (g1); leaf gas exchange data collected from control plants and youngest fully expanded leaves.
- DO3SE inputs include both model parameters (DOS3E_inputs.csv) and chamber-specific time-series data (species_merged_data.csv for each species; 17 columns including daily/hourly environmental data and O3 in nine chambers).
- Dose–response functions derived as linear declines in relative biomass against POD 1 (and POD 0) using both J (Jarvis) and P (photosynthesis-based) parameterizations; includes AOT40-based reference.
- The dataset provides POD- and O3-dose-based susceptibility metrics to support cross-species comparative analyses and integration into vegetation models.

## Data structure and file organization
- DO3SE model parameters: DOS3E_inputs.csv (15 columns: species code, m, g0, Vcmax, Jmax, gmax_O3, fmin, Tmin, etc.).
- O3 concentration and meteorology data: ten files named speciescode_merged_data.csv (each with 17 columns: Day_of_year, Hour_of_day, Temperature, VPD, PAR, Pa, Wind, ppt, Cham_1–Cham_9, etc.).
- Biomass and leaf traits dataset: Experimental_Biomass.csv (19 columns: Code, Plant_ID, Cham_ID, Leaves_dw, Petiole_dw, Stems_dw, Roots_dw, AGB, Biomass, LA_Av, LMA, LMA_lamina, etc.).
- Dose–response functions: Dose_response_functions.csv (6 columns: Code, POD0_J_DRF, POD1_J_DRF, POD0_P_DRF, POD1_P_DRF, AOT40_DRF).
- Accompanying methodological references and data provenance are included to support reuse and alignment with monitoring frameworks.

## Quality control and data validation
- Meteorological data quality checked against a local reference station; O3 concentrations validated against zero-air standards during each sampling round.
- Biomass measurements are tied to annually calibrated scales; suspicious outliers reweighed with extended drying time to confirm masses.
- DO3SE model parameterization validated through comparison of POD1 estimates from the two stomatal conductance approaches.

## Reuse potential and governance considerations
- Data are designed to inform environmental health monitoring frameworks, including the translation of ozone exposure to plant-level responses and potential ecosystem productivity impacts.
- Metadata quality and data sharing considerations are addressed, acknowledging potential barriers (e.g., dataset provenance, transparency of underlying datasets, and data governance standards at the source).

## References
- Key methodological and modeling references supporting DO3SE, stomatal conductance models, gas-exchange analysis, FRAP and Folin–Ciocalteu assays, and ozone-dose–response concepts.