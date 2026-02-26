# Lolium_and_Trifolium_solardomes

## Aim
- Use controlled ozone exposure to assess environmental health impacts on two pasture species (Lolium perenne and Trifolium repens) in monocultures and mixtures, using standardized data collection to enable monitoring of ecological responses over time.

## Plant material
- Lolium perenne and Trifolium repens propagated vegetatively from pasture turf near Edinburgh, UK.
- Plants from different parents randomized across competition (monoculture vs mixture) and ozone treatments.
- Establishment period of ~8 weeks before potting into experimental setups.

## Experimental design
- Large pots (containers) with drainage; 12 plants per pot (4 center, 8 surrounding).
- Each solardome contained:
  - Three pots of L. perenne monoculture
  - Three pots of T. repens monoculture
  - Three pots of a L. perenne and T. repens mixture (central T. repens, surrounding L. perenne)
- Four solardomes used for exposure in a randomized block design; two additional domes as controls (filtered air) and two domes with episodic rural ozone profile.
- Ozone regime:
  - Background ozone 30 ppb; maximums of 80 ppb on days 1 and 4, and 100 ppb on days 2 and 3.
  - Ramp up to maximum over 2 hours, hold 6 hours, then decrease over 2 hours; remaining times at 30 ppb.
- Exposure period: 12 weeks total (start 26 July 2002), split into two harvest windows.

## Harvesting and biomass measurements
- Harvested in two rounds: 6 September and 16 October.
- Material harvested in layers:
  - Outside pot perimeter
  - >14 cm above soil
  - 7–14 cm above soil
  - Final harvest also included 0–7 cm layer
- Species-specific sorting:
  - Trifolium repens: stolons, flowers, leaves
  - Lolium perenne: leaves and stems (all material >7 cm considered leaf)
- Drying: 65°C for at least 4 days; biomass measured per layer and per plant.
- Subset analysis: L. perenne leaf material ground and dried for C and N content (CHNS analyzer).

## Physiological measurements
- Leaf sampling: representative leaves at different ages; at least six leaves per measurement day.
- A-Ci curves:
  - Using CIRAS I (PP-Systems) with 1000 μmol m⁻² s⁻¹ PAR.
  - CO2 concentrations: 0 to 2000 ppm in steps, steady-state measurements.
  - Outputs: net photosynthesis (A) and intercellular CO2 concentration (Ci).
- A-Q (light response) curves:
  - PAR steps from 10 to 2000 μmol m⁻² s⁻¹ with CO2 fixed at 1000 ppm.
- Photosynthetic parameters:
  - Fitted to Farquhar et al. model to derive maximum carboxylation velocity (Vc,max) and maximum electron transport rate (Jmax) from A-Ci and A-Q data.
  - Jmax estimated from A-Ci curve using Ci > 500 ppm data.
- Data processing uses standard equations, with specific handling for leaf age and canopy position.

## Data management and structure
- Data generated per solardome and per plant, stored in structured CSV files:
  - Lolium_and_Trifolium_solardomes_ACi_Curve_data.csv: 220 rows, 7 columns (Species, Leaf number, weeks, Treatment, dome.pot, Ci, A corrected for leaf area)
  - Lolium_and_Trifolium_solardomes_biomass_data.csv: 16 rows, 6 columns (Harvest, Species, Monoculture or mixture, Ozone treatment, dry weight, standard error)
  - Lolium_and_Trifolium_solardomes_clover_distribution_data.csv: 28 rows, 6 columns (Harvest, Monoculture or mixture, part of canopy, Ozone treatment, Dry weight per pot, standard error)
  - Lolium_and_Trifolium_solardomes_Lolium_distribution_data.csv: 32 rows, 6 columns (Harvest, Monoculture or mixture, part of canopy, Ozone treatment, Dry weight per pot, standard error)
- Data structure supports longitudinal and comparative analyses across ozone levels, plant compositions, and canopy positions.

## Statistical analysis
- Data aggregated to solardome means for analyses.
- Anova and regression:
  - One-way ANOVA (Minitab) for Jmax across ozone treatments.
  - GLM regression (SPSS) comparing A vs Ci relationships between monoculture and mixture.
  - Split-plot and split-split-plot ANOVA (Genstat) with ozone as main factor and monoculture vs mixture as subplot factors; canopy position included for biomass partitioning analyses.
- Software details:
  - Minitab 14, SPSS 12, Genstat 8.

## Key points for environmental monitoring and data value
- The study provides a standardized, repeatable framework for assessing plant physiological and biomass responses to ozone under near-natural canopy configurations (mixtures vs monocultures).
- Data are organized for re-use and cross-study comparison, with explicit metadata on treatments, pot design, harvest layers, and measurement protocols.
- Challenges highlighted in environmental data monitoring align with this work:
  - Increasing the value of datasets by integrating with other data sources (e.g., additional environmental variables, remote sensing, or longer-term monitoring).
  - Facilitating access to underlying data to support transparency and secondary analyses.