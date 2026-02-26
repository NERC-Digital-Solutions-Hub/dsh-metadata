# Plant material

## Overview
- Describes a controlled study of ozone effects on Lolium perenne (ryegrass) and Trifolium repens (white clover) grown in monocultures or mixtures.
- Plants were propagated from pasture turf near Edinburgh, randomized across competition (monoculture vs mixture) and ozone treatments.
- Exposed in solardomes for 12 weeks with two harvest periods; multiple biometric and physiological measurements collected, plus carbon and nitrogen analyses.

## Experimental design and data collection
- Setup
  - Large containers (drainage holes) lined to prevent root escape; filled with multipurpose compost.
  - Each pot had 12 plants (4 central, 8 surrounding) with different parental lines; randomised blocks for competition and ozone.
  - Exposed in solardomes that mimic ambient environmental conditions except rainfall; irrigation via mist system.
- Ozone exposure
  - Four solardomes in a randomized block design; two controls with filtered air, two with episodic rural ozone peaks.
  - Concentrations: 30 ppb baseline, rising to 80–100 ppb on days 1–4; maintenance at 30 ppb otherwise; continuous monitoring every 30 minutes.
- Harvests
  - Two harvests: 6 Sept (6 weeks exposure) and 16 Oct (12 weeks).
  - Harvest layers: outside pot, >14 cm above soil, 7–14 cm, and later 0–7 cm for final harvest.
  - Tissue sorted by species and plant part (e.g., T. repens stolons, leaves, flowers; L. perenne leaves/stems with stems absent above 7 cm).
  - Biomass dried at 65°C for at least 4 days; subset of L. perenne leaves analysed for C and N via CHNS.
- Physiological measurements
  - Leaf sampling: “Leaf 1” (newest fully expanded) and “Leaf 2” from tillers/stolons; minimum six leaves per measurement day.
  - A-Ci curves: net CO2 assimilation (A) vs substomatal CO2 (Ci) using CIRAS I; PAR = 1000 μmol m−2 s−1; CO2 steps from 0 to 2000 ppm.
  - AQ curves: CO2 fixed at 1000 ppm; PAR stepped from 10 to 2000 μmol m−2 s−1.
  - Parameters estimated per leaf: A, Ci; Jmax from A-Ci, Vcmax from initial slope; models based on Farquhar et al. (1980) and related methods; temperature-adjusted I* for estimating Jmax.
- Data processing
  - For A-Ci curves: data restricted to Ci > 500 ppm for Jmax estimation; averaged per plant.
  - Vcmax derived from the initial slope of A vs Ci up to Ci = 300 ppm.
  - Data handled with CIRAS software; specific equations and empirical constants applied as described.

## Data structure and datasets
- Lolium_and_Trifolium_solardomes_ACi_Curve_data.csv
  - 220 rows, 7 columns
  - Columns: Species, Leaf number, number of weeks since start of exposure, Treatment, dome.pot, Ci (ppm), A corrected for leaf area (μmol m−2 s−1)
- Lolium_and_Trifolium_solardomes_biomass_data.csv
  - 16 rows, 6 columns
  - Columns: Harvest, Species, Monoculture or mixture, Ozone treatment, dry weight (g per pot, cutting height 7 cm), standard error
- Lolium_and_Trifolium_solardomes_clover_distribution_data.csv
  - 28 rows, 6 columns
  - Columns: Harvest, Monoculture or mixture, part of canopy, Ozone treatment, Dry weight per pot (g), standard error
- Lolium_and_Trifolium_solardomes_Lolium_distribution_data.csv
  - 32 rows, 6 columns
  - Columns: Harvest, Monoculture or mixture, part of canopy, Ozone treatment, Dry weight per pot (g), standard error

## Data quality, verification, and analysis
- Data validation
  - Ozone concentrations continuously monitored in each dome; instrument calibration prior to exposure.
  - Replicated dome design with two control domes and two treatment domes to account for variability.
- Statistical analysis
  - Data averaged per solardome prior to analysis.
  - One-way ANOVA (Jmax) to test ozone effects; GLM regression for A vs Ci across treatments and canopy types.
  - Split-plot and split-split-plot ANOVA used with main factor: ozone treatment; subplot: monoculture vs mixture; canopy position as sub-sub plot.
  - Software: Minitab for ANOVA, SPSS for GLM, Genstat for other analyses.
- Data provenance and lineage
  - Clear linkage between physiological measurements and biomass data via harvest/timepoints and canopy position.
  - Datasets document experimental context (species, treatment, canopy structure, harvest stage).

## Data management and metadata considerations
- Datasets are explicitly structured with descriptive column headers and documented data structures.
- Data capture spans multiple measurement modalities (biomass, tissue composition, leaf physiology) and multiple timepoints.
- Metadata captured includes treatment, canopy type, harvest timing, and dome/pot identifiers to enable re-use and cross-study comparisons.

## Implications for data leaders
- Data assets are organized into separate, well-documented CSV files corresponding to different measurement domains (physiological curves, biomass, canopy distribution).
- Clear data lineage: from experimental setup (species, pot arrangement, ozone regime) to measurements (A-Ci/AQ curves, biomass, C and N content) and analyses (Jmax, Vcmax).
- Opportunities for data governance improvements:
  - Ensure consistent metadata for cross-study integration (e.g., standardize species naming, treatment coding, and canopy segmentation conventions).
  - Maintain a central data dictionary describing each column, units, and measurement methods for long-term discoverability.
  - Facilitate data reuse by preserving raw data alongside processed outputs and analysis scripts.
- Validation considerations for future studies:
  - Maintain robust calibration records for instruments (ozone analyser, CIRAS system).
  - Preserve per-dome aggregations to enable reproducibility of the statistical analyses.