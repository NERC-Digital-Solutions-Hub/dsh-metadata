# Supporting documentation for plant biomass and leaf-level functional traits from four different genotypes of sugarcane plants grown under a range of ozone conditions

## Overview
- Experimental study examining ozone (O3) impacts on four Saccharum sugarcane genotypes using a gradient of O3 exposures across Open Top Chambers (OTCs) at the TropOz facility.
- Data intended to support O3 dose–response functions for biomass and leaf traits, including flux-based metrics (POD) and regional-scale modelling.
- Data deposit accompanies Cheesman et al. (2023) and related data.

## Experimental facility and exposure design
- Location: TropOz research facility, JCU/UoE, Cairns, Queensland, Australia; Nguma-bada campus, JCU.
- Setup: Nine independently controlled OTCs (internal volume 22.2 m3) with charcoal-filtered air, each receiving O3 to create a semi-continuous gradient (average daytime 15–120 ppb).
- O3 delivery and monitoring: On-site O3 generation, sampling ~every 22 minutes per chamber; centralized hub for air delivery and UV-absorption O3 measurements.
- Environmental monitoring: Temperature, vapor pressure deficit (VPD), and photosynthetically active radiation (PAR) recorded at five-minute resolution from a central meteorological station in the OTC area.
- Experimental runs: Two runs with nine chambers each; slight environmental differences between runs due to staggered planting dates (Badila, Q240, CTC4 exposed ~Nov 2021; Mandalay exposed Mar 2022). Environmental differences between runs accounted for in analyses.

## Plant material and experimental design
- Genotypes: Badila (Saccharum officinarum L.), Mandalay (Saccharum spontaneum), Q240 and CTC4 (commercial hybrids).
- Source: Germplasm from SRA collection (Meringa, Queensland) under licence (Oct 2021).
- Establishment: ~60 one-eye sets per genotype; fungicide-treated; germinated under ambient shadehouse conditions; transferred to 30-L pots with high organic matter mix and drainage adjusters; regular irrigation and biweekly fertilization.
- Allocation to OTCs: Four plants per genotype per chamber (total nine chambers) for dose–response assessment.
- Experimental duration: 96 days for Badila, Q240, CTC4; 100 days for Mandalay due to delayed start.
- Drought/heat stress: Plants exposed to full sun, not subjected to drought; residual environmental differences between runs were accounted for in analyses.

## O3 dose–response methods and measurements
- Biomass assessment: Post-harvest, plants oven-dried at 70°C; biomass partitioned into leaves, stalks, and roots. Leaf area and leaf mass per area (LMA) derived from the most recently emerged leaf (L+1).
- O3 metrics:
  - AOT40 (ppm h) for concentration-based exposure.
  - DO3SE model v3.1 to estimate phytotoxic O3 dose (PODy, mmol m-2) using stomatal conductance and flux-based calculations.
  - PODy thresholds used: y = 0 and y = 2 nmol m-2 s-1 for regional simulations; additional POD values (0–8) calculated for each genotype/chamber.
  - stomatal conductance (gs) measurements: leaft-level gas exchange using LI-COR LI-6400XT; porometer readings on L+1 leaves for most genotypes; Mandalay relied on control chamber data due to narrow leaf blades.
  - gs data processed to Relative Stomatal Conductance (RSC) and used to parameterize DO3SE; g_o3 estimated as 0.663 × gs.
  - Model validation: Modelled gs compared with measured values; R^2 ranged from 0.59 (CTC4) to 0.83 (Mandalay) for daylight hours (5:30–19:00).
- Dose–response relationship: Relative biomass decline modeled against PODy; maximum biomass used as y-intercept from chamber-level regressions.

## Data collection, quality control and structure
- Meteorological QA: OTC sensor data cross-validated against local JCU station data.
- O3 QA: Chamber O3 readings checked against zero-air standards every sampling round (~22 min).
- Biomass QA: Final biomass determined with annually calibrated scales; suspected outliers reweighed after extra drying time.
- Data types: Six CSV files containing O3 concentrations, environmental conditions, calculated POD values, and biomass/leaf trait measurements.

## Data files and contents
- Sugarcane_O3.csv
  - Contents: O3 concentration data (ppb) for nine OTCs during the first experiment.
  - Columns: date (dd/mm/yyyy HH:MM); Chamber_1 … Chamber_9 (ppb).
- Sugarcane_Mandalay_O3.csv
  - Contents: O3 concentration data (ppb) for nine OTCs during the Mandalay experiment.
  - Columns: date (dd/mm/yyyy HH:MM); Chamber_1 … Chamber_9 (ppb).
- Sugarcane_Met_5min.csv
  - Contents: Environmental conditions (5-min averages) during the first experiment.
  - Columns: AirTC_Avg (°C), RH (%), PAR_Den_Avg (µmol m-2 s-1), Datetime (dd/mm/yyyy HH:MM).
- Sugarcane_Mandalay_Met_5min.csv
  - Contents: Environmental conditions (5-min averages) during the Mandalay experiment.
  - Columns: AirTC_Avg (°C), RH (%), PAR_Den_Avg (µmol m-2 s-1), Datetime (dd/mm/yyyy HH:MM).
- Calculated_PODy.csv
  - Contents: Calculated POD values (phytotoxic ozone dose) for all genotypes (Badila, CTC4, Q240, Mandalay) across chambers and thresholds (0–8 nmol m-2 s-1) using porometer or LICOR data.
  - Columns: Cham_ID, Genotype, POD2_Porometer, POD6_Porometer, AOT40, POD0_Licor, POD1_Licor, ..., POD8_Licor.
- Sugarcane_Biomass.csv
  - Contents: Final biomass and leaf-trait measurements for four genotypes across chambers.
  - Columns: Genotype, Plant_ID, Chamber_ID, Date, New_Leaf_Length, New_Leaf_FW, New_Leaf_DW, New_Leaf_Area, New_LMA, Old_Leaf_Length, Old_Leaf_FW, Old_Leaf_DW, Old_Leaf_Area, Old_LMA, Primary_Stems, Secondary_Stems, Final_height, Leaves_dw, Stems_dw, Roots_dw, AGB, Biomass, Flagged, Notes.

## Data usage and interpretation for environment monitoring
- The gradient O3 design and flux-based POD metrics enable cross-genotype comparisons under varied environmental conditions, supporting nonlinear dose–response analysis and regional-scale modelling.
- The dataset aligns with standardized monitoring outputs (biomass, leaf traits, gas exchange, and flux-based ozone dose) to scrutinize environmental health and the impact of ozone on crop productivity.
- Data quality practices ensure traceability and comparability with other monitoring efforts and can be used to inform policy performance assessments related to ozone exposure and agricultural resilience.

## References
- Key sources underpinning methods and interpretation, including: Agathokleous et al. (2019, 2020), Braga Junior et al. (2021), Cheesman et al. (2023), Emberson (2020), Kreyling et al. (2018), Pleijel et al. (2022).