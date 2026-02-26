# Ozone exposure of Lolium perenne and Trifolium repens under solardome conditions

- Purpose: Evaluate environmental health monitoring aspects by examining how controlled ozone exposure affects pasture species, with monocultures and mixtures, using robust measurement and data handling methods to inform future policy and decision-making.

## Experimental design and setup

- Plant material: Vegetatively propagated Lolium perenne and Trifolium repens from turf pasture near Edinburgh, UK; plants from different parents randomized across treatments.
- Growth and arrangement: Each pot contained 12 plants (central four Trifolium repens surrounded by eight Lolium perenne). Three pots per monoculture and three pots per mixture per solardome.
- Solardomes and treatments: Four solardomes used; two controls and two ozone-exposed domes. Ozone regimes included continuous 30 ppb and two higher profiles (O3(30) controls, O3(30+peaks) episodic peaks) with maximum 80 ppb (days 1 and 4) and 100 ppb (days 2 and 3). Exposures occurred over 12 weeks starting July 26, 2002, with harvests on Sept 6 and Oct 16.
- Maintenance: Well-watered via mist irrigation; manual watering during warm periods.

## Measurements and data collection

- Visual injury and senescence:
  - Whole-pot assessments of injury and senescence (plants not separable); classification if >25% injured or senesced; measurement of senesced leaf length on 20 leaves per pot.
- Harvesting and biomass:
  - Plants harvested in layers: outside pot, >14 cm, 7–14 cm, and finally 0–7 cm above soil. Separate species and healthy vs ozone-injured leaves for Trifolium repens; Lolium perenne separated into healthy and senesced leaves. Drying at 65°C for at least 4 days to determine biomass.
- Physiological measurements:
  - Stomatal conductance: Measured on Trifolium repens using a porometer at upper (sunlit) and inner (shaded) canopy positions; six leaves per dome (two per canopy position).
  - Chlorophyll content: SPAD meter readings (chlorophyll a+b) taken at 1 and 10 weeks; calibration against acetone-extracted chlorophyll to convert SPAD units to mg g-1 fresh weight, with r^2 = 0.90 and the provided calibration equation.
- Data handling:
  - Per-dome means used for analyses; visually assessed data arcsine-transformed prior to analysis.

## Data analysis and structure

- Statistical approach:
  - One-way ANOVA for stomatal conductance.
  - Split-plot or split-split plot ANOVA in Genstat; main plot: ozone treatment; sub-plots: monoculture vs mixture; canopy-position sub-sub-plots as appropriate.
- Software:
  - Minitab v14 for stomatal conductance analyses; Genstat v8 for other comparisons.
- Data structure:
  - Injury_data.csv (Lolium_and_Trifolium_solardomes_Injury_data.csv): 24 rows, 7 columns including harvest, species, monoculture/mixture, canopy part, ozone treatment, percent leaves injured or senesced, and standard error.

## Notes on data quality and governance

- Emphasis on standardized measurement protocols (consistent harvesting layers, canopy-position sampling, calibration of chlorophyll measurements).
- Clear metadata and structure for data sharing (explicit data file format and column definitions); transformation of proportion data for analysis enhances interpretability and comparability.
- The study demonstrates rigorous design elements relevant to monitoring frameworks: replicable treatments, careful data cleaning and transformation, and transparent reporting of methods and data structure to facilitate external review and reuse.