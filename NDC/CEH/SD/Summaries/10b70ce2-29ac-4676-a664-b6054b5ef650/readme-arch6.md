# Environmental conditions, ozone concentrations, biomass and leaf level functional traits data for 10 tropical tree species grown across a range in ozone concentrations within nine Open Top Chambers in Cairns, Australia

## Overview
- Dataset documenting ozone concentrations, environmental conditions, biomass, and leaf-level functional traits for 10 tropical tree species grown under nine gradient ozone exposures in Open Top Chambers (OTCs) in Cairns, Australia, from July 2020 to November 2022.
- Includes final biomass data, biomass partitioning, and leaf traits such as leaf mass per unit area (LMA) and lamina-specific LMA, plus biochemical metrics (total carbon and nitrogen, δ13C, δ15N, antioxidant capacity, and total phenolics).
- Contains calculated phytotoxic ozone dose (POD) for each species using the DO3SE model with two stomatal conductance formulations, enabling ozone-sensitivity assessment.
- Data are intended to support cross-species analyses of ozone-vegetation interactions and to facilitate model calibration and data-driven decision making.

## Experimental setup and facility
- Location: TropOz research facility, joint University of Exeter (UoE) and James Cook University (JCU) at JCU Environmental Research Complex, Nguma-bada campus, Cairns.
- Facility: Nine independently controlled OTCs (internal volume 22.2 m3) with a gradient of nine O3 exposures; chambers ventilated with charcoal-filtered air and on-site O3 generation; fumigation from 08:00 to 17:00.
- O3 monitoring: Continuous measurements with a UV-absorption ozone analyzer; data averaged to ~5-minute resolution and used for model inputs.
- Meteorology: Central monitoring station capturing temperature, relative humidity, shortwave radiation, and PAR; data averaged to align with model inputs.

## Plant material and cultivation
- Ten tropical tree species from nine families representing a range of successional stages and leaf morphologies.
- Seedlings (~20 cm) grown in pots with a garden mix/Quincan substrate; acclimated to full sun; transferred to OTCs with ~3–4 replicates per chamber.
- Exposure protocol: Approximately 61–191 days of ozone fumigation (average ~150 days); daily irrigation and controlled-release fertilization.

## Measurements and analyses
- Biomass and tissue separation: Harvested at experiment end; partitioned into leaves, stems, and roots; dry biomass determined at 70°C to constant weight; dry above-ground biomass (AGB) and total biomass recorded.
- Leaf functional traits: Collected 6–12 fully expanded leaves per plant; measured leaf area, fresh mass, dry mass; calculated whole-leaf and lamina LMA.
- Biochemical characterization: Freeze-dried lamina tissue analyzed for total carbon and nitrogen, δ13C and δ15N; Total Antioxidant Capacity (TAC) via FRAP assay; Total Phenolic Content (TPC) via Folin-Ciocalteau method; results expressed as mg AAE g-1 DW and mg GAE g-1 DW respectively.
- Gas exchange and stomatal conductance: Youngest fully expanded leaves measured for photosynthetic traits using LI-6400XT; ACi curves and 24-hour measurements used to derive Vcmax and Jmax; day and night stomatal conductance (gs) data collected with a porometer to parameterize DO3SE.

## Ozone flux modelling and POD
- Phytotoxic Ozone Dose (POD) calculated using DO3SE model version 3.1 to quantify ozone flux into leaves above specified flux thresholds.
- Two gs parameterisations used:
  - Combined photosynthesis-stomatal conductance model (optimal gs, Ball–Berry–Woodrow; using Vcmax, Jmax, and g1)
  - Empirical-multiplicative gs model (gs parameterized from porometer measurements)
- DO3SE inputs include species-specific parameters (m, g0, Vcmax, Jmax, gmax_O3, fmin, Tmin) and per-species data files with chamber O3 concentrations and meteorological variables.
- POD calculations focused on POD1 (threshold 1 nmol m-2 s-1) and POD0 (threshold 0 nmol m-2 s-1) as part of dose-response analyses.

## Data structure and contents
- DO3SE parameter file:
  - DOS3E_inputs.csv: 15 columns including species code, m, g0, Vcmax, Jmax, gmax_O3, fmin, Tmin, etc.
- Per-species data:
  - Ten files named speciescode_merged_data.csv (e.g., Ba_merged_data.csv) containing 17 columns with time-resolved environmental and ozone data:
    - Day_of_year, Hour_of_day, Temperature, VPD, PAR, Pa, Wind, ppt, Cham_1–Cham_9 (chamber O3 in ppb)
- Experimental biomass data:
  - Experimental_Biomass.csv: 19 columns including Code, Plant_ID, Cham_ID, Leaves_dw, Petiole_dw, Stems_dw, Roots_dw, AGB, Biomass, LA_Av, LMA, LMA_lamina.
- Dose-response functions:
  - Dose_response_functions.csv: 6 columns including Code, POD0_J_DRF, POD1_J_DRF, POD0_P_DRF, POD1_P_DRF, AOT40_DRF.
- References linked to methods and models used (DO3SE, stomatal conductance models, FRAP, Folin-Ciocalteau, isotopic analysis, etc.).

## Quality control and data provenance
- Meteorological and O3 data validated against factory-calibrated sensors and local reference station; zero-air checks performed on O3 measurements; final biomass data cross-checked with re-weighing after extended drying.
- Data collected with standardized protocols across species, with careful documentation of exposure periods and chamber conditions.
- Data deposited as a structured set including model inputs and processed outputs to enable replication, re-analysis, and integration with DGVMs or other data products.

## Potential uses and value
- Enables cross-species analysis of ozone sensitivity and dose-response relationships using POD and DO3SE parameters.
- Facilitates calibration and validation of ecosystem and vegetation models (e.g., DGVMs) under tropical O3 stress.
- Supports development of data products such as dashboards or reports that allow researchers to explore species-specific ozone responses, biomass outcomes, and leaf trait changes.
- Provides a rich repository for linking physiological traits (Vcmax, Jmax, gs dynamics, LMA, δ13C, δ15N) with ozone exposure and biomass performance.

## Limitations and considerations
- Hormetic responses are not explicitly accounted for in the linear dose-response framework.
- Nine OTCs and site-specific conditions may limit direct extrapolation to other tropical contexts.
- Temporal coverage varies by species due to staggered exposure initiation and harvest timing.

## References
- Methods and models underlying DO3SE, stomatal conductance, gas exchange analyses, and biochemical assays are cited within the dataset documentation.