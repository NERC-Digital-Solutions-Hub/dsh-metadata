# Ozone exposure of Lolium perenne and Trifolium repens in monoculture and mixture under solardome conditions

## Study purpose and organisms
- Investigates the effects of ozone exposure on two forage species, Lolium perenne (ryegrass) and Trifolium repens (white clover).
- Plants propagated from pasture near Edinburgh, then randomized between monoculture and mixed (L. perenne and T. repens) competition structures.
- Aimed to understand how ozone interacts with plant composition (monoculture vs mixture) and how data on growth, allocation, and physiology can be collected and analyzed.

## Experimental design and setup
- Pots: large containers with drainage, 35.5 cm x 45 cm x 25 cm, lined to prevent root escape; each pot contains 12 plants (4 central, 8 surrounding).
- Treatments per solardome: three pots of L. perenne monoculture, three pots of T. repens monoculture, and three pots of a mixed canopy (4 central T. repens, 8 surrounding L. perenne).
- Environment: four solardomes acting as blocks in a randomised design; environmental conditions similar to ambient air aside from rainfall exclusion.
- Ozone regimes:
  - Two domes: controls with charcoal-filtered air delivering ~30 ppb (O3(30)).
  - Two domes: episodic rural ozone profile (O3(30+peaks)).
  - Maximum ozone concentrations reached 80 ppb on days 1 and 4, and 100 ppb on days 2 and 3; elevated from 30 ppb to max over 2 hours, held for 6 hours, then returned to 30 ppb over 2 hours.
- Exposure period:
  - Initiation on 26 July 2002.
  - Two harvest windows: 26 July–6 September (6 weeks) and 7 September–16 October (12 weeks).

## Treatments and timing
- Harvesting schedule:
  - First harvest: 6 September; plants cut back to 7 cm.
  - Second harvest: 16 October; same height.
- Plant material collection:
  - Layered harvests to separate spatial zones: outside pot, >14 cm, 7–14 cm above soil; final harvest additionally collected 0–7 cm.
  - Sorting by species at harvest; T. repens subdivided into stolons, flowers, leaves; L. perenne subdivided into leaves and stems (all material >7 cm considered leaves).
- Plant maintenance:
  - Regular mist irrigation (04:00) with supplemental hand watering during warm periods.
- Biomass and tissue analysis:
  - Biomass dried at 65°C for ≥4 days.
  - Subsamples of L. perenne leaf analyzed for carbon and nitrogen content (CHNS via automated analyzer).

## Physiological measurements
- Leaf selection: Leaf 1 (newest fully expanded) and Leaf 2 (second newest) on a given tiller/stolon; minimum six leaves per measurement day.
- Photosynthetic measurements (A-Ci curves):
  - Instrument: CIRAS I with automatic cuvette; PAR set at 1000 μmol m⁻² s⁻¹.
  - CO2 steps: 0, 50, 100, 200, 400, 600, 800, 1000, 1500, 2000 ppm; data used to derive A vs Ci.
  - Calculations: net photosynthesis (A) and intercellular CO2 concentration (Ci) using standard equations; also modeled using Farquhar framework.
  - Jmax estimation: derived from A-Ci curve asymptote (Ci > 500 ppm) using established method.
  - Vc,max comparison: based on initial slope of A vs Ci for Ci up to 300 ppm.
- Light-response (AQ) curves:
  - CO2 fixed at 1000 ppm; light response from 10 to 2000 PAR.
- Data processing: per-plant curves analyzed to estimate photosynthetic capacity and related parameters.

## Data handling, structure, and analysis
- Data aggregation:
  - Values averaged per solardome (block) for subsequent analyses.
- Statistical analyses:
  - Jmax: one-way ANOVA to assess ozone effects (no monoculture vs mixture comparison in this analysis).
  - A-Ci relationships: GLM regression to compare slopes between treatments.
  - Other parameters: split-plot and split-split-plot ANOVA (Genstat) with main factor ozone treatment and subplot of cultivation type (monoculture vs mixture); canopy position included as a sub-sub plot for biomass partitioning.
- Data structure and datasets:
  - Lolium_and_Trifolium_solardomes_ACi_Curve_data.csv
    - 220 rows, 7 columns: Species, Leaf number, weeks since start, Treatment, dome.pot, Ci (ppm), A corrected for leaf area (μmol m⁻² s⁻¹)
  - Lolium_and_Trifolium_solardomes_biomass_data.csv
    - 16 rows, 6 columns: Harvest, Species, Monoculture or mixture, Ozone treatment, dry weight (g per pot at 7 cm), standard error
  - Lolium_and_Trifolium_solardomes_clover_distribution_data.csv
    - 28 rows, 6 columns: Harvest, Monoculture or mixture, part of canopy, Ozone treatment, Dry weight per pot (g), standard error
  - Lolium_and_Trifolium_solardomes_Lolium_distribution_data.csv
    - 32 rows, 6 columns: Harvest, Monoculture or mixture, part of canopy, Ozone treatment, Dry weight per pot (g), standard error
- Overall scope:
  - Combines growth, tissue composition, and physiological measurements to evaluate ozone effects on both species in different community contexts.
  - Provides structured datasets suitable for modeling photosynthetic responses and biomass allocation under ozone stress.

## Practical implications for data management
- Clear experimental design with replication and blocking (solardomes as blocks) supports robust ozone effect estimation.
- Detailed metadata and explicit data structures (including leaf age, canopy position, and measurement type) enhance reusability and comparability.
- Data outputs cover both whole-plant biomass and leaf-level physiology, enabling integrated analyses of growth and function under environmental stress.
- The datasets are organized to support reproducible analyses of photosynthetic capacity (Jmax, Vc,max) and carbon/nitrogen content, with explicit documentation of measurement protocols and processing steps.