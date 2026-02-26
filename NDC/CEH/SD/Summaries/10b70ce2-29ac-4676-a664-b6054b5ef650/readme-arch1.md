Environmental conditions, ozone concentrations, biomass and leaf level functional traits data for 10 tropical tree species grown across a range in ozone concentrations within nine Open Top Chambers in Cairns, Australia.

# Overview
- Dataset from ozone exposure experiments (July 2020 – November 2022) at the TropOz facility (UoE-JCU) in Cairns, Australia.
- Ten tropical tree species across nine families grown under nine O3 concentration treatments in Open Top Chambers (OTCs).
- Includes environmental conditions, ozone exposure, final biomass, and leaf-level functional traits.
- Aims to quantify ozone effects on tropical vegetation productivity and physiology using DO3SE-based ozone flux and POD metrics.

# Experimental Facility and Design
- Nine independently controlled OTCs (internal volume ~22.2 m3) enabling a gradient of nine O3 exposures.
- Ambient CO2 with O3 generated on-site; fumigation 08:00–17:00 each day.
- Typical chamber mean O3 concentrations ranged from 25 to 112 ppb during exposure hours.
- Continuous O3 monitoring with a dedicated UV-absorption analyzer; data averaged to 5-minute resolution and interpolated to a continuous dataset.
- Meteorological data (air temperature, relative humidity, shortwave radiation, PAR) recorded at a central station and averaged for model inputs.
- Experimental design included staggered introduction of species, with independent replication per species per chamber and plant growth periods ranging from 61 to 191 days (average 150 days).

# Plant Material and Growth Conditions
- Ten tropical tree species from nine families:
  - Brachichyton acerifolius, Carallia brachiata, Calophyllum inophyllum, Chionanthus ramiflorus, Darlingia darlingiana, Flindersia pimenteliana, Homalanthus novoguineensis, Inga edulis, Syzygium gustavioides, Theobroma cacao.
- Seedlings sourced locally; grown in 20 or 60 L pots with a garden-topsoil/Quincan mix.
- Plants acclimated to full sun prior to OTC transfer; irrigation daily and controlled-release fertilizer as needed.
- Harvest at experiment end: above-ground and total biomass, plus partitioning into leaves, stems, roots.

# Measurements and Biochemical Traits
- Biomass and partitioning:
  - Leaves, petiole, stems, roots biomass; total above-ground biomass and total biomass.
  - Leaf area (LA_Av), whole-leaf mass per unit area (LMA), lamina-specific LMA (LMA_lamina).
- Leaf biochemical traits (from lamina tissue):
  - Total carbon (TC) and nitrogen (TN) and stable isotopes (δ13C, δ15N) via EA-IRMS.
  - Total antioxidant capacity (TAC) via FRAP assay; expressed as mg ascorbic acid equivalents per g dry weight.
  - Total phenolic content (TPC) via Folin-Ciocalteu assay; expressed as mg gallic acid equivalents per g dry weight.
- Sampling details:
  - Leaf measurements taken from the newest fully developed leaves at the end of O3 exposure.
  - Biochemical analyses performed on freeze-dried lamina tissue.

# Calculating O3 Flux and POD
- O3 flux and phytotoxic dose (POD) computed using DO3SE v3.1:
  - Two stomatal conductance (gs) models:
    - Combined photosynthesis–gs model assuming optimal stomatal behavior (Ball–Berry–Woodrow framework) with gs parameterization (g1, g0, Vcmax, Jmax, Tmin, fmin, etc.).
    - Empirical-multiplicative gs model.
  - Parameterization:
    - Gas exchange data from control plants (lowest O3) used to estimate Vcmax, Jmax, g1, etc., via LI-6400XT measurements and the plantecophys package.
    - Night-time gs (g0) and day-time gs (to estimate g1) derived from leaf gas exchange data and modeled with FitBB.
  - DO3SE inputs require species-specific parameters (15 columns) and chamber- and weather-aligned data.
- POD metrics:
  - POD1: phytotoxic ozone dose above a threshold of 1 nmol O3 m-2 s-1.
  - POD0: dose above threshold 0, used for comparison.
  - Linear dose-response relationships linking relative biomass decline to POD1 (and POD0) for each species, calibrated using the combined photosynthesis–gs model or the empirical-multiplicative gs model.
  - Relationship for dose-response also considers AOT40-based metric in DRFs.

# Ozone Dose-Response Functions
- Species-level linear dose-response functions derived from chamber-averaged relative biomass versus POD1 (and POD0) using:
  - Jarvis (J) parameterization.
  - Photosynthesis (P) model parameterization.
  - AOT40-based DRF included for reference.
- DO3SE-based DRFs allow assessment of ozone sensitivity across species, acknowledging that hormesis is not explicitly modeled in the primary linear approach.

# Data Structure and Files Included
- DO3SE model parameter file:
  - DOS3E_inputs.csv: 15 columns per species describing sensitivity to An, g0, Vcmax, Jmax, gmax_O3, fmin, Tmin, and related parameters.
- DO3SE inputs (ten data files):
  - Species-specific merged data files named as "speciescode_merged_data.csv" (e.g., Ba_merged_data.csv for Brachiochyton acerifolius).
  - Each file contains 17 columns including Day_of_year, Hour_of_day, Temperature, VPD, PAR, Pa, Wind, Cham_1…Cham_9 O3 concentrations, etc.
- Experimental_Biomass.csv:
  - 19 columns including Species code, Plant_ID, Cham_ID, Leaves_dw, Petiole_dw, Stems_dw, Roots_dw, AGB, Biomass, LA_Av, LMA, LMA_lamina.
- Dose-Response Functions summary:
  - Dose_response_functions.csv: 6 columns including Code, POD0_J_DRF, POD1_J_DRF, POD0_P_DRF, POD1_P_DRF, AOT40_DRF.
- References section includes key methodological papers and datasets supporting the DO3SE modeling, gs parameterization, and biochemical assays.

# Quality Control and Validation
- Meteorological data vetted against a local meteorological station to ensure consistency.
- O3 concentrations checked against zero-air standards (activated charcoal filtered air) every sampling round (~22 minutes).
- Biomass measurements validated with annually calibrated scales and outlier rechecks after additional drying.

# Context and Access
- Part of the Trop-Oz project: Ozone impacts on tropical vegetation; implications for forest productivity (NE/R001812/1).
- Related dataset available alongside TropOz companion data: https://catalogue.ceh.ac.uk/documents/87412c44-f11a-4182b182-47d872ad7ebd.