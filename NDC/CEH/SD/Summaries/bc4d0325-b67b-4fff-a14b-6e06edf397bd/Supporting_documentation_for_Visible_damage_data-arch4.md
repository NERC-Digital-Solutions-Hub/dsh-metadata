# Plant material

## Overview
- Study of ozone effects on two grass species (Lolium perenne and Trifolium repens) grown from turf samples near Edinburgh, UK.
- Plants were randomised across competition (monoculture vs mixture) and ozone treatments.
- Experiment started with eight weeks of establishment before forming monocultures and mixtures for ozone exposure over 12 weeks.

## Experimental design
- Large pots (35.5 x 45 x 25 cm) with drainage holes, lined to keep roots contained.
- Each pot contained 12 plants: 4 central Trifolium repens surrounded by 8 Lolium perenne.
- Three pots per monoculture (Lolium or Trifolium) and three pots per mixture were allocated to each of four solardomes.
- Exposures ran from 26 July 2002, with two harvests (intermediate 6 Sept; final 16 Oct).
- Well-watered via mist irrigation and additional hand watering during warm periods.

## Ozone exposure
- Four solardomes: two controls, two ozone-exposed.
- Ozone generated from oxygen; concentrations measured every 30 minutes per dome.
- Control domes received ozone-poisoned air with continuous 30 ppb (O3(30)).
- Two domes simulated episodic rural ozone (O3(30+peaks)).
- Regime: maximum 80 ppb on days 1 and 4; maximum 100 ppb on days 2 and 3; increases from 30 ppb to max over 2 hours, sustained 6 hours, then declines to 30 ppb over 2 hours; otherwise 30 ppb.

## Visual assessments
- Whole-pot assessments for senescence and ozone-specific injury (white/pale-yellow leaf stippling).
- Classification: leaves with >25% senesced or injured deemed unhealthy.
- Senescence progression in Lolium perenne documented from leaf tip along blade.
- A subsample of 20 leaves per pot measured for senesced length.

## Harvests
- Plants cut to 7 cm on 6 Sept and 16 Oct.
- Harvested in layers: outside pot, >14 cm above soil, 7–14 cm, and finally 0–7 cm for the final harvest.
- Material separated by species and health status (healthy vs ozone-injured for Trifolium repens; healthy vs senesced for Lolium perenne).
- Drying: 65°C for at least 4 days prior to biomass determination.

## Stomatal conductance
- Measured on Trifolium repens with a porometer after ~10–11 weeks of exposure.
- Readings from upper (sunlit) and inner (shaded) canopy positions.
- Six leaves per dome position (two per pot) per canopy position.

## Chlorophyll content
- SPAD-based chlorophyll index measured after 1 and 10 weeks of exposure.
- Calibration using acetone extraction and spectrophotometry (470, 646, 663 nm) per Lichtenthaler and Wellburn.
- Reported relationship: Chlorophyll content (mg g-1 FW) = (SPAD index * 30.448) + 417; r^2 = 0.90.

## Statistical analysis
- Data aggregated to dome means before analysis; visible injury and senescence arcsine transformed.
- Analyses:
  - Stomatal conductance: one-way ANOVA (Minitab).
  - Other parameters: split-plot or split-split plot ANOVA (Genstat).
- Experimental factors:
  - Main plot: ozone treatment.
  - Sub-plots: monoculture vs mixture.
  - Sub-sub-plots: canopy position as appropriate.

## Data structure
- Injury data file: Lolium_and_Trifolium_solardomes_Injury_data.csv
- Layout: 24 rows, 7 columns
  - Harvest
  - Species
  - Monoculture or mixture
  - Part of canopy
  - Ozone treatment
  - % leaves that were injured or senesced (determined by biomass)
  - Standard error

## Data management and governance (implications for Data Leaders)
- Emphasis on capturing a coherent data system: linking plant composition, ozone regime, canopy position, and injury/biomass outcomes.
- Clear metadata needs: treatment definitions (monoculture/mixture, canopy layer), measurement methods (porometer, SPAD), and transformation steps (arcsine for injury data).
- Data aggregation step (dome means) critical for reproducibility and traceability of analyses.
- Standardization of units, measurement protocols, and documentation to enable cross-study comparison and integration with broader data ecosystems. 
- Potential for expanding the dataset with raw measurements (per pot, per plant, per leaf) alongside analyzed dome-level summaries to support deeper analyses and meta-analyses.