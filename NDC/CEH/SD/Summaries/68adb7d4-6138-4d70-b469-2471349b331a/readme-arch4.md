# Supporting documentation for plant biomass and leaf-level functional traits from four different genotypes of sugarcane plants grown under a range of ozone conditions

## Overview
- Experimental results investigating the impacts of ozone (O3) on four sugarcane genotypes using the TropOz facility in Queensland, Australia.
- Objective: develop O3 dose–response relationships for biomass and leaf traits, enabling integration with regional vegetation models.
- Data are tied to a companion paper (Cheesman et al., 2023) and related data deposit; viewable in conjunction with that work.

## Experimental facility and design
- Location: TropOz research facility at the Nguma-bada campus of James Cook University (Cairns, Queensland), a joint UoE–JCU project.
- Setup: Nine independently controlled Open Top Chambers (OTCs), each with internal volume of 22.2 m3.
- O3 exposure gradient: Each chamber receives a different O3 level to create a semi-continuous gradient (approximately 15–120 ppb daytime average), enabling investigation of nonlinear responses.
- Monitoring: O3 concentrations measured ~every 22 minutes; environmental variables (air temperature, VPD, PAR) logged at 5-minute intervals from a central meteorological station.
- Data systems: O3 and environmental data collected per chamber and date, with quality checks against standards and local references.

## Plant material and experimental runs
- Genotypes: Four Saccharum lines — Badila, Mandalay, Q240, and CTC4.
- Source and handling: Materials from SRA germplasm collection; germination and growth under controlled conditions before transfer to OTCs.
- Experimental setup: Four individuals per genotype per chamber; nine chambers total. 
- Timing: 
  - 1st set (Badila, Q240, CTC4) moved into OTCs around 10 cm height on 13 November 2021 (96 days exposure).
  - Mandalay delayed and moved into OTCs on 28 March 2022 (100 days exposure).
- Environmental notes: Two experimental runs experienced different environmental conditions; differences accounted for in subsequent dose–response calculations.

## Measurements and traits
- Biomass and partitioning: Plants harvested at end of exposure, oven-dried to constant mass to determine total biomass; partitioned into leaf, stalks, and roots.
- Leaf functional traits: Collected most recently emerged leaf (L+1) to determine leaf area, dry biomass, and leaf mass area (LMA).
- Gas exchange and stomatal conductance: 
  - gs measured on L+1 leaves for CTC4, Q240, Badila using a porometer; Mandalay not measured due to leaf traits.
  - Control-chamber measurements with a LI-6400XT for a broader set; data used to derive Relative Stomatal Conductance (RSC).
  - gs data converted to RSC and used to parameterize O3 flux model (g_o3 = 0.663 × g_s).
- O3 dose metrics:
  - Concentration-based: AOT40 (ppm h).
  - Flux-based: Phytotoxic Ozone Dose (POD_y) calculated with the DO3SE model v3.1, threshold y values from 0 to 8 nmol m−2 s−1; thresholds 0 and 2 nmol m−2 s−1 used for regional simulations.
  - Dose–response: Relative biomass decline modeled against POD_y to derive dose–response functions.
- Data integration: DO3SE-based flux calculations calibrated with gas-exchange data; model performance validated by comparing predicted gs with measured gs (R2 values 0.59–0.83 across genotypes).

## Data processing, modeling, and interpretation
- DO3SE modeling: 
  - Calibrated using measured gas-exchange data to estimate POD_y for each genotype × chamber combination (POD_y values 0–8).
  - Used two POD thresholds (POD_0 and POD_2) to enable comparability with literature and regional applications.
- Dose–response derivation: 
  - Biomass decline relative to maximum biomass (y-intercept of the linear relation between chamber-average biomass and POD_y) used to generate dose–response curves.
- Model validation: 
  - Modelled gs values compared with LI-6400XT measurements showed strong positive correlations during daylight hours.
- Data lineage and reproducibility: 
  - Data quality checks included meteorological validation against local station data and instrument calibration checks; final biomass data cross-validated by reweighing suspected outliers after additional drying.

## Data quality and quality control
- Instrument calibration: Factory-calibrated sensors; cross-validation with local meteorological station.
- O3 checks: Zero-air standard checks every sampling round.
- Biomass measurements: Annually calibrated scales; reweighing and additional drying when necessary.
- Run comparability: Acknowledgement of environmental differences between the two experimental runs; accounted for in dose–response calculations.

## Data files and contents
- Sugarcane_O3.csv: 10 columns with O3 concentration data from nine OTCs during the first experiment.
  - Columns: date, Chamber_1 … Chamber_9 (ppb)
- Sugarcane_Mandalay_O3.csv: 10 columns with O3 concentration data from nine OTCs during the second experiment.
  - Columns: date, Chamber_1 … Chamber_9 (ppb)
- Sugarcane_Met_5min.csv: 4 columns of environmental conditions (5-minute averages) during the first experiment.
  - Includes AirTC_Avg, RH, PAR_Den_Avg, Datetime
- Sugarcane_Mandalay_Met_5min.csv: Environmental conditions (5-minute averages) during the second experiment.
- Calculated_PODy.csv: 14 columns representing calculated POD_y for four genotypes (Badila, CTC4, Q240, Mandalay) across POD thresholds (0–8) and using different data sources (POD2_Porometer, POD6_Porometer, AOT40, POD0_LiCor, POD1_LiCor … POD8_LiCor).
  - Includes Cham_ID and Genotype identifiers.
- Sugarcane_Biomass.csv: 28 columns with final biomass partitioning and leaf-level traits for four genotypes.
  - Genotype, Plant_ID, Chamber_ID, Date
  - New_Leaf_Length, New_Leaf_FW, New_Leaf_DW, New_Leaf_Area, New_LMA
  - Old_Leaf_Length, Old_Leaf_FW, Old_Leaf_DW, Old_Leaf_Area, Old_LMA
  - Primary_Stems, Secondary_Stems, Final_height
  - Leaves_dw, Stems_dw, Roots_dw, AGB, Biomass
  - Flagged, Notes
- References: Documentation and related literature cited for methods and context (Agathokleous et al., Emberson, Kreyling, Pleijel, etc.).

## Notes for data users and reuse
- This dataset supports cross-genotype ozone-dose response studies, with both concentration-based (AOT40) and flux-based (POD_y) metrics.
- The DO3SE-calibrated flux approach accounts for stomatal behavior and environmental conditions, enabling integration with regional vegetation models.
- Data include comprehensive metadata on experimental setup, measurement methods, and quality checks, but readers should account for differences between the two experimental runs when applying dose–response relationships.
- Associated publication: Cheesman et al. (2023) for broader context on O3 impacts on sugarcane production.