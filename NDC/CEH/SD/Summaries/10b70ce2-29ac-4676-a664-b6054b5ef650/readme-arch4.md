# Environmental conditions, ozone concentrations, biomass and leaf level functional traits data for 10 tropical tree species grown across a range in ozone concentrations within nine Open Top Chambers in Cairns, Australia.

## Aim and scope
- Presents a dataset from experiments exposing 10 tropical tree species to nine different O3 concentrations using Open Top Chambers (OTCs) from July 2020 to November 2022.
- Includes ozone concentrations, environmental conditions, final biomass, and leaf-level functional traits.
- Supports analysis of O3 impacts on tropical vegetation, with calculated phytotoxic ozone dose (POD) and dose–response relationships.

## Experimental design and facility
- Facility: TropOz research facility (University of Exeter and James Cook University) with nine independently controlled OTCs (22.2 m3 each) at the JCU Environmental Research Complex, Far North Queensland, Australia.
- Design: Gradient exposure to nine O3 concentrations (mean chamber concentrations 25–112 ppb during exposure hours 08:00–17:00); controlled CO2 and environmental conditions.
- Data collection cadence: High-resolution meteorological data (temperature, relative humidity, PAR) and O3 measurements at ~5-minute resolution; linearly interpolated to continuous five-minute datasets for model inputs.
- O3 monitoring: On-site O3 generation with charcoal-filtered ambient air; UV-absorption O3 analyzer with regular zero-air checks.

## Plant material and growing conditions
- Ten tropical tree species representing diverse families and leaf traits (LMA range 58.1–142.5 g m-2).
- Seedlings sourced locally; potted in 20–60 L pots with garden mix and scoria; acclimated to full sun.
- Exposure: 9 hours per day of O3 fumigation (08:00–17:00); duration per plant between 61 and 191 days (average ~150 days).
- Maintenance: Daily drip irrigation; fertilized as needed with controlled-release fertilizer.
- Harvest: Plants harvested for total biomass with partitioning into leaves, stems, and roots; dry biomass measured at 70°C to constant weight.

## Data collected and key variables
- O3 and environment: O3 concentrations in each chamber; air temperature; relative humidity; shortwave radiation; PAR.
- Biomass and morphology: Final dry weights of leaves, petioles, stems, and roots; total above-ground biomass (AGB) and total biomass; leaf area (LA_Av); leaf mass per area (LMA) including lamina-specific LMA (LMA_lamina).
- Leaf chemistry and biochemistry: Whole-le leaf C and N; δ13C and δ15N; total antioxidant capacity (TAC) via FRAP assay; total phenolic content (TPC) via Folin-Ciocalteau; sample preparation and analysis details provided.
- Data-structure outputs: Species-specific biomass data, chlorophyll-related traits, and biogeochemical metrics for each plant and chamber.

## Calculating ozone dose and models used
- Phytotoxic O3 dose (POD) calculated using the DO3SE model (v3.1), integrating stomatal conductance (gs) dynamics via two approaches:
  - Combined photosynthesis-stomatal conductance model with optimal gs behavior (Ball–Berry–Woodrow framework) to derive gs parameters (e.g., Vcmax, Jmax, g1) and night/day conductance.
  - Empirical-multiplicative gs model.
- Data for gs parameterization:
  - Gas-exchange measurements (ACi curves and light-response) on youngest fully expanded leaf of control plants using LI-6400XT.
  - Gs values from measurements performed during the study period; night-time (g0) and day-time (g1) parameters estimated.
- POD1 and POD0:
  - Relative biomass vs POD (POD1) used to derive species-specific dose–response functions.
  - Linear dose–response approach used to estimate susceptibility (slope coefficients) for each species, with calibration to JULES when used in DGVMs.
- Additional dose metrics:
  - POD0 and POD1 responses also characterized using Jarvis and photosynthesis-based parameterizations (P and J).

## DO3SE inputs and data files
- DO3SE parameters (DO3SE_inputs.csv): 15 columns per species including:
  - m (sensitivity to An), g0 (minimum stomatal conductance), Vcmax, Jmax, gmax_O3, fmin, Tmin, and other species-specific parameters.
- DO3SE input data files (ten species):
  - Naming convention: speciescode_merged_data.csv (e.g., Ba_merged_data.csv).
  - Each file contains 17 columns with hourly/interval data: Julian day, hour, temperature, VPD, PAR, Pa, wind, precipitation, and nine chamber O3 concentrations (Cham_1 to Cham_9). Missing data represented as NA.
- Experimental biomass dataset (Experimental_Biomass.csv): 19 columns including species code, plant ID, chamber, biomass components (Leaves_dw, Petiole_dw, Stems_dw, Roots_dw), AGB, Biomass, LA_Av, LMA, and LMA_lamina.

## Dose–response functions and references
- Dose_response_functions.csv: 6 columns per species including
  - POD0_J_DRF, POD1_J_DRF (Jarvis-based DRFs for POD0 and POD1)
  - POD0_P_DRF, POD1_P_DRF (photosynthesis-based DRFs for POD0 and POD1)
  - AOT40_DRF (relative biomass decline per unit AOT40)
- DRFs support cross-model comparisons of O3 susceptibility across species.

## Quality control and data integrity
- Meteorological data quality checked against a local meteorological station; sensors factory-calibrated.
- O3 concentration validation via zero-air standard checks at every sampling round (~22 minutes).
- Final biomass measurements validated with annually calibrated scales; outliers reweighed after additional drying time.

## Data accessibility and references
- Accompanying data set available at CEH data catalog: https://catalogue.ceh.ac.uk/documents/87412c44-f11a-4182b182-47d872ad7ebd
- Core methodological and modeling references for DO3SE, gs parameterization, and dose–response analyses are provided, including key works by Büker et al., Ball et al., Medlyn et al., Jarvis, and Hayes et al.