# Lolium and Trifolium solardomes

- Objective: Assess the effects of ozone on Lolium perenne (ryegrass) and Trifolium repens (white clover) when grown in monoculture or in mixture, under controlled solardome conditions, using standardized data collection to support environmental health monitoring and policy evaluation.
- Study context: Plants originated from pasture near Edinburgh, vegetatively propagated, and randomized across competition (monoculture vs mixture) and ozone treatments. Exposed for approximately 12 weeks after an eight-week establishment.

## Experimental design and treatments

- Setup: Large containers (pots) with drainage, containing 12 plants per pot (4 central, 8 surrounding). Each solardome contained:
  - 3 pots of L. perenne monoculture
  - 3 pots of T. repens monoculture
  - 3 pots of a L. perenne and T. repens mixture (central plants: T. repens; surrounding plants: L. perenne)
- Environment: Solardomes provided conditions close to ambient air, with controlled irrigation and temperature.
- Exposure period: 12 weeks, starting 26 July 2002, divided into two harvest periods (6 Sept and 16 Oct).

## Ozone exposure protocol

- Design: Randomised block with four solardomes; two domes as controls and two with ozone exposure.
- Ozone regime:
  - Controls: Continuous ozone 30 ppb (O3(30)).
  - Treatment domes: Episodic rural ozone profile (O3(30+peaks)).
- Concentrations: Max 80 ppb on days 1 and 4; max 100 ppb on days 2 and 3; ramp up from 30 ppb to max over 2 hours, hold 6 hours, then return to 30 ppb over 2 hours; otherwise 30 ppb.

## Harvesting and biomass analysis

- Harvests: Two harvests (6 Sept and 16 Oct) after 6 and 12 weeks of exposure.
- Procedures: Plants cut to 7 cm; harvested in layers:
  - Outside pot perimeter
  - >14 cm above soil
  - 7–14 cm above soil
  - At final harvest, 0–7 cm layer included
- Sorting: Material sorted by species; T. repens separated into stolons, flowers, leaves; L. perenne into leaves and stems (no stems in the lower section; above 7 cm all material counted as leaves).
- Drying: Biomass dried at 65°C for at least 4 days.
- Chemical analysis: Subsamples of L. perenne leaf material ground and dried; C and N content measured via CHNS analyzer (Leco).

## Physiological measurements

- Leaf sampling: Representative leaves from different ages; “Leaf 1” = newest fully expanded leaf; “Leaf 2” = second newest; minimum six leaves per measurement day.
- Photosynthesis assessments:
  - A-Ci curves: Net CO2 assimilation rate (A) vs substomatal CO2 (Ci) to determine photosynthetic efficiency and capacity; conditions: 1000 μmol m−2 s−1 PAR; CO2 series from 0 to 2000 ppm; calculations with CIRAS software and Farquhar model.
  - AQ curves: Similar approach for additional parameters; CO2 at 1000 ppm; PAR ramp from 10 to 2000 μmol m−2 s−1.
  - Parameters: Maximum electron transport rate (Jmax) estimated from A-Ci curve; Vc,max derived from initial slope of A vs Ci for Ci up to 300 ppm.
- Data per plant: Each A-Ci and AQ curve generated for a single plant.

## Data handling and analysis

- Data aggregation: For each parameter, values averaged per solardome before analysis.
- Statistical analyses:
  - One-way ANOVA (Minitab v14) to test ozone effects on Jmax (no monoculture vs mixture comparison in this analysis).
  - GLM regression (SPSS v12) for A vs Ci comparisons across treatments.
  - Genstat (v8) split-plot and split-split-plot ANOVA with main factor ozone and subplot monoculture vs mixture; canopy position included as sub-subplot for biomass partitioning.
- Data structure (examples of included datasets):
  - Lolium_and_Trifolium_solardomes_ACi_Curve_data.csv: 220 rows, 7 columns (Species, Leaf number, Weeks, Treatment, dome.pot, Ci, A_corr)
  - Lolium_and_Trifolium_solardomes_biomass_data.csv: 16 rows, 6 columns (Harvest, Species, Monoculture or mixture, Ozone treatment, dry weight, standard error)
  - Lolium_and_Trifolium_solardomes_clover_distribution_data.csv: 28 rows, 6 columns (Harvest, Monoculture/mixture, part of canopy, Ozone treatment, Dry weight, SE)
  - Lolium_and_Trifolium_solardomes_Lolium_distribution_data.csv: 32 rows, 6 columns (Harvest, Monoculture/mixture, part of canopy, Ozone treatment, Dry weight, SE)

## Data quality, access, and monitoring considerations

- Calibration and validation: Ozone analyzers calibrated prior to exposure; randomised block design with replication to support robust comparisons.
- Standardized data practices: Clear data structures and metadata, with explicit variable definitions to facilitate secondary analyses and reproducibility.
- Data stewardship: Results organized into clearly defined CSV datasets suitable for upload to shared data portals, supporting transparency and reuse for environmental monitoring and policy evaluation.