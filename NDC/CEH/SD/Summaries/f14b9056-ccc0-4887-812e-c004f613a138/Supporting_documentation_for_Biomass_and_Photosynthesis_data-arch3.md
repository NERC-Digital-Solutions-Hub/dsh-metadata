Ozone exposure effects on Lolium perenne and Trifolium repens in monocultures and mixtures

## Overview
- This study investigates how ozone exposure affects growth and photosynthetic performance of two pasture species, Lolium perenne (ryegrass) and Trifolium repens (white clover), when grown in monocultures versus a mixed canopy.
- Plants were propagated from pasture turf near Edinburgh and exposed in controlled solardomes under varying ozone regimes for up to 12 weeks.
- Measurements encompass biomass, tissue carbon and nitrogen content, and detailed leaf-level photosynthetic responses to quantify ozone sensitivity and potential interaction effects between species and growth form (mono vs mix).

## Experimental design
- Plant material and setup
  - L. perenne and T. repens propagated from turf samples; randomised across competition (monoculture vs mixture) and ozone treatments.
  - Each pot contained 12 plants: 4 central T. repens within a surrounding ring of 8 L. perenne (in the mixture), enabling a defined canopy structure.
- Growing environment
  - Large pots (dimensions 35.5 cm × 45 cm × 25 cm) with drainage and root-containment liners.
  - Solardomes used to approximate ambient environmental conditions, except for rainfall, with consistent mist irrigation.
  - Two 3-pot setups for each species in monoculture and three pots for the mixed canopy per solardome.
- Experimental units and layout
  - Four solardomes in a randomized block design to manage ozone exposure.
  - Each solardome included: three L. perenne monoculture pots, three T. repens monoculture pots, and three L. perenne/T. repens mixture pots.
  - Two solardomes served as ozone-free controls; two provided elevated ozone regimes.

## Ozone exposure protocol
- Exposure regimes
  - Controls: continuous ozone at 30 ppb (O3(30)) using charcoal-filtered air.
  - Elevated ozone: a rural episodic profile with peaks, delivering up to 80 ppb on days 1–4 and 100 ppb on days 2–3, then returning to 30 ppb at other times (O3(30+peaks)).
- Monitoring and duration
  - Ozone concentrations measured every 30 minutes in each dome with an ozone analyzer; data managed via automated sample control.
  - Exposure period spanned 12 weeks, split into two harvest windows (6 weeks and 12 weeks).

## Harvesting and sample processing
- Harvest schedule
  - Two harvests: 6 weeks and 12 weeks after starting ozone exposure.
- Harvesting methodology
  - Plants cut to 7 cm height.
  - Layered harvesting: outside-canopy material, material above 14 cm, material between 7–14 cm, and an additional 0–7 cm layer for final harvest.
  - Tissue separated by species and canopy position; T. repens further partitioned into stolons, flowers, and leaves; L. perenne into leaves and stems (no stems present above 7 cm for the latter).
  - Material dried at 65°C for at least 4 days to determine dry biomass.
  - Subsamples of L. perenne leaf material analysed for carbon and nitrogen content via CHNS.
  
## Physiological measurements
- Leaf sampling strategy
  - Measurements on representative leaves at different ages: Leaf 1 (newest fully expanded) and Leaf 2 (second newest) on each plant.
  - A minimum of six leaves per measurement day at the same physiological stage.
- Photosynthetic analyses
  - A-Ci curves (net CO2 assimilation rate, A, vs substomatal CO2 concentration, Ci) to determine photosynthetic efficiency and capacity.
  - Equipment: PP-Systems CIRAS I with automatic cuvette; PAR set to 1000 μmol m^-2 s^-1.
  - CO2 steps: 0, 50, 100, 200, 400, 600, 800, 1000, 1500, 2000 ppm; Ci up to ~1600 ppm.
  - A and Ci calculated using CIRAS software and Farquhar model (1980) equations; Jmax estimated from A-Ci curve asymptote for Ci > 500 ppm using the Stirling et al. (1997) approach.
  - AQ curves (photosynthetic rate vs light response) performed with CO2 at 1000 ppm; light steps from 0 to 2000 μmol m^-2 s^-1 to derive Jmax and other light-limited responses.
- Derived parameters
  - Maximum rate of carboxylation (Vc,max) inferred from the initial slope of A vs Ci for Ci up to 300 ppm.
  - Jmax derived from A-Ci curves as described; both species evaluated under different ozone and canopy treatments.

## Data processing and modelling
- Data handling
  - Data averaged at the solardome level prior to analysis (one mean per solardome per parameter).
- Modelling and statistics
  - Primary comparison of Jmax across ozone treatments using one-way ANOVA.
  - For A-Ci relationships, regression comparisons between monoculture and mixture via GLM regression.
  - Additional analyses using Genstat (split-plot and split-split-plot ANOVA) with factors: ozone treatment, monoculture vs mixture, canopy position as a sub-factor, and, where relevant, harvest layer.
- Data structure and availability
  - Data files linked to the experiment include:
    - Lolium_and_Trifolium_solardomes_ACi_Curve_data.csv (220 rows, 7 columns) with Species, Leaf number, weeks, Treatment, dome.pot, Ci, A (area-corrected).
    - Lolium_and_Trifolium_solardomes_biomass_data.csv (16 rows, 6 columns) with Harvest, Species, Monoculture/mixture, Ozone treatment, dry weight per pot, standard error.
    - Lolium_and_Trifolium_solardomes_clover_distribution_data.csv (28 rows, 6 columns) with Harvest, Monoculture/mixture, part of canopy, Ozone treatment, dry weight per pot, standard error.
    - Lolium_and_Trifolium_solardomes_Lolium_distribution_data.csv (32 rows, 6 columns) with Harvest, Monoculture/mixture, part of canopy, Ozone treatment, dry weight per pot, standard error.

## Key considerations for monitoring frameworks
- Data quality and governance
  - The study relies on rigorous data collection, standardisation, and the ability to separate effects by species and canopy context; highlights the importance of detailed metadata and clear data provenance for cross-study comparability.
- Multilevel design and data integration
  - The combination of monoculture and mixed canopies under controlled ozone regimes demonstrates the value of factorial designs for isolating policy-relevant environmental stressors and their interactions.
- Measures aligned with policy evaluation
  - Biomass partitioning, carbon and nitrogen content, plus in-depth photosynthetic parameters (A, Ci, Jmax, Vcmax), provide a comprehensive suite of indicators to assess environmental stress and potential productivity impacts—informing decisions on land management, climate-oxidant interactions, and ecosystem service provisioning.
- Data transparency and sharing
  - The study's explicit data structures and willingness to share underlying data (with notes on potential barriers such as metadata completeness) align with best practices for openness and reproducibility in environmental monitoring.