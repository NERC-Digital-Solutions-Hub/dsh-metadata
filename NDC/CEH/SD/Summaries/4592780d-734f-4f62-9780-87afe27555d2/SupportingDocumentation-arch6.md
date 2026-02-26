# Supporting documentation: Data from the experimental management of arable field options for rare plants (Defra project BD5204)

## Overview
- A collection of data from four interlinked experiments (2011–2014) on rare arable plants, designed to model and understand plant responses to management and crop practices.
- Provides multi-site experimental designs, detailed data collection protocols, and a range of data types including vegetation cover, species counts, seed production, and soil properties.
- Quality assurance includes outlier checks, spot checks of input data, correction of recorder ID inconsistencies, and formation of species aggregates where needed.

## Experimental designs

- Margin management experiment
  - Multi-site, autumn 2010 setup with randomised complete block split-plot design across Brecklands, Fivehead, and Roundwood.
  - Main plots: six 12m x 60m plots per block; two factors for cultivation season (spring/autumn) and cultivation method (discing, harrowing, ploughing).
  - Sub-plots: four 12m x 15m sub-plots per main plot, each assigned to one of four herbicide treatments (Unsprayed, Glyphosate, Graminicide, Graminicide + selective broadleaf herbicide).
  - Treatments applied annually (2010–2014).

- Herbicide screening experiment
  - Set up April 2012 with 15 seed strips (1 m wide, 110 m long) for 15 rare arable plant species.
  - Perpendicular to seed strips, three blocks containing 23 herbicide strips; 21 herbicides randomly assigned to herbicide strips; two unsprayed controls.
  - Sowing: 30 April 2012; pre- and post-emergence herbicides applied; plant-condition scoring on 1 August 2012 using a 6-point scale.
  - Outcome focused on establishment and condition of sown species.

- Cereal headland experiments
  - Two separate experiments for winter wheat and spring barley.
  - Design uses margin 12 m wide with four replicate blocks; central area over-sown with a seed mix for the respective crop type.
  - Treatments include cereal density (sowing rate) and nitrogen fertilizer application, with plots measured in late July 2014.
  - Central 5 m x 5 m area used for detailed vegetation assessments, including sown vs unsown arable species, and seed production.

- Crop rotation experiment
  - Split-plot mesocosm design to model population dynamics under crop rotation.
  - Two main plots with six crop treatments each; within each main plot, twelve mesocosms assigned to two seed mixes (autumn- vs spring-germinating species).
  - Inoculation of soil with seed mix (Sept 18–19, 2013); sowing of crops (Sept 19, 2013 for winter crops; spring crops sown March 2014).
  - Counts of rare arable plants at two time points (March 2014 and June/July 2014) and final seed production data collected.

## Datasets deposited (by experiment)

- Margin management experiment
  - MarginManagementExperiment_01_Design.csv: randomisation of main plots and sub-plots; treatments by site, block, main plot, sub-plot.
  - MarginManagementExperiment_02_VegetationWholeSubplots.csv: estimated annual percent cover by species per sub-plot (2011–2014).
  - MarginManagementExperiment_03_VegetationQuadratAverages.csv: average percent cover from five 1 m quadrats per sub-plot.
  - MarginManagementExperiment_04_RarePlantCounts.csv: twice-annual counts of rare arable species across sub-plots.
  - MarginManagementExperiment_05_FlowersSeedHeads.csv: counts of flowers and seed heads for rare species in 2014.
  - MarginManagementExperiment_06_SeedProduction.csv: seed counts within sampled seed heads (2014).
  - MarginManagementExperiment_07_SoilChemistry.csv: soil chemical parameters (pH, available P/K/Mg, texture, LOI, N) from 20 cm depth in 2014.
  - MarginManagementExperiment_08_Bryophytes.csv: bryophyte frequencies in unsprayed sub-plots (late 2014).
  - MarginManagementExperiment_09_Seedbank.csv: soil seed counts from autumn 2012–2013, using seed germination method.

- Herbicide screening experiment
  - HerbicideScreeningExperiment_01_Design.csv: randomisation of herbicide treatments and test species within layout.
  - HerbicideScreeningExperiment_02_PlantConditionScores.csv: plant condition scores (0–5) by herbicide strip, treatment, and species.

- Cereal headland experiments
  - CerealHeadlandExperiment_01_Design.csv: randomisation of cereal density and nitrogen fertilizer within WW and SB experiments.
  - CerealHeadlandExperiment_02_VegetationCover.csv: species percent cover across five quadrats per plot.
  - CerealHeadlandExperiment_03_VegetationStructure.csv: cereal cover, tillers, height, bare ground (averaged or summed as indicated).
  - CerealHeadlandExperiment_04_RarePlantDemography.csv: counts of rare arable plants, flowers, and seed heads (across five quadrats per plot).
  - CerealHeadlandExperiment_05_SeedProduction.csv: seeds per seed head for rare arable species.

- Crop rotation experiment
  - CropRotationExperiment_01_Design.csv: randomisation of six crops, mesocosm IDs and seed mix (autumn- vs spring-germinating).
  - CropRotationExperiment_02_SecondCount.csv: second count data for all rare arable species in mesocosms.
  - CropRotationExperiment_04_SeedProduction.csv: seed head counts and seed totals per mesocosm and species.

## Data integrity and processing

- Quality assurance involved outlier checks, spot data verification, and correction of ID inconsistencies among recorders for vegetation data.
- Species aggregates were created for difficult-to-distinguish taxa (e.g., Agrostis stolonifera agg., Veronica persica agg.).
- Data are organized with consistent key fields: Site, Year, Sub-plot/Mesocosm, Species, and measurement variables (cover, counts, scores, chemistry, seed production).

## Key notes for users

- Data spans 2011–2014 across three sites and multiple experimental setups, with rich longitudinal vegetation and rare arable plant data.
- Datasets enable analysis of management effects (cultivation, herbicides, sowing density, fertilizer, crop rotation) on rare arable flora and associated vegetation structure.
- Metadata includes detailed experimental designs, treatment layouts, and sampling protocols, facilitating self-serve data exploration and product development.