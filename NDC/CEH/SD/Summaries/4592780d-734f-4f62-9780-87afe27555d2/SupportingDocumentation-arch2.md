# Data from the experimental management of arable field options for rare plants (Defra project BD5204)

## Overview
- Timeframe: 2011–2014
- Four main experiments:
  - Margin management experiment
  - Herbicide screening experiment
  - Cereal headland experiment
  - Crop rotation experiment
- Purpose: document and standardise environmental monitoring data on rare arable plants, enabling assessment of environmental health and policy-relevant outcomes over time.
- Data handling: quality assurance includes outlier checks, spot checks of input data, correction of ID inconsistencies, and aggregation of taxa as needed.
- Outputs: datasets describing experimental design, vegetation metrics, rare plant counts, seed production, soil chemistry, bryophytes, seedbank, and more, collected across multiple sites and years.
- Reuse potential: designed for cross-site comparisons, aggregation with other data sources, and modelling of population dynamics and environmental responses under different management scenarios.

## Experimental designs (summary)

- Margin management experiment
  - Multi-site (Brecklands, Fivehead, Roundwood) set up in autumn 2010
  - Randomised complete block split-plot design
  - Three sites with 3–4 replicate blocks; main plots 12 m x 60 m
  - Factors:
    - Cultivation season: spring or autumn
    - Cultivation method: discing, harrowing, ploughing
  - Sub-plots: four 12 m x 15 m plots per main plot, assigned to herbicide treatments
  - Herbicide treatments: unsprayed, glyphosate, graminicide, selective broadleaf herbicide plus graminicide
  - Treatments applied annually (2010–2014)

- Herbicide screening experiment
  - 15 seed strips (1 m width x 110 m length) with 15 rare arable species
  - Perpendicular experimental blocks with 23 herbicide strips
  - 21 different herbicides randomly assigned; 2 unsprayed controls
  - Sowing: 30 April 2012
  - Pre-emergence and post-emergence herbicide applications in 2012
  - Plant condition scored on 1 August 2012 in plots meeting establishment criteria (minimum 10 plants)
  - Design dataset: 01_Design
  - Plant condition scores dataset: 02_PlantConditionScores

- Cereal headland experiment
  - Two separate experiments within margin: winter wheat (WW) and spring barley (SB)
  - Margin 12 m wide; four replicate blocks
  - Five treatments within each block (varying cereal density and fertilizer):
    - Control (no cereal, no fertilizer)
    - Low density
    - Low density + N fertilizer
    - High density
    - High density + N fertilizer
  - Plot lengths differ by fertilizer regime
  - Sowing dates: WW on 27 Sept 2013; SB on 14 Mar 2014
  - Central 5 m x 5 m area over-sown with a rare arable seed mix
  - Fertilizer: N and S applied only where designated
  - Final counts (late July 2014) in five 0.5 m x 0.5 m quadrats per plot; counts of rare species, flowers, seed heads; seed head collection for seed production

- Crop rotation experiment
  - Baseline mesocosm experiment to model population dynamics under rotation
  - Split-plot design: six crop treatments in two replicate main plots
  - Mesocosms: 12 per main plot (total 144)
  - Seed mixes: two seed mixtures (predominantly autumn-germinating vs predominantly spring-germinating species)
  - Inoculation: 18 Sept 2013
  - Sowing: winter crops on 19 Sept 2013; spring crops on 20 Mar 2014
  - Counts of established rare arable plants (first count: 19 Mar 2014; second count: 2 Jun 2014 or 7 Jul 2014 depending on crop)
  - Seed head collection for seed production analyses

## Datasets (content and purpose)

- Margin management experiment
  - MarginManagementExperiment_01_Design.csv
    - Randomisation and treatment mapping for main plots/sub-plots
  - MarginManagementExperiment_02_VegetationWholeSubplots.csv
    - Estimated percentage cover for all species per sub-plot per year (2011–2014)
  - MarginManagementExperiment_03_VegetationQuadratAverages.csv
    - Average cover from three 1 m quadrats per sub-plot (2011–2014)
  - MarginManagementExperiment_04_RarePlantCounts.csv
    - Twice-annual counts of rare arable species per sub-plot (2011–2014)
  - MarginManagementExperiment_05_FlowersSeedHeads.csv
    - Counts of flowers and seed heads for rare arable species (2014)
  - MarginManagementExperiment_06_SeedProduction.csv
    - Seed counts per seed head for rare arable species (2014)
  - MarginManagementExperiment_07_SoilChemistry.csv
    - Soil chemical parameters (pH, available P/K/Mg, texture, LOI, total N, etc.) by main plot (2014)
  - MarginManagementExperiment_08_Bryophytes.csv
    - Bryophyte frequencies in unsprayed sub-plots (late 2014)
  - MarginManagementExperiment_09_Seedbank.csv
    - Seed counts from soil cores by depth and census (2011–2014)

- Herbicide screening experiment
  - HerbicideScreeningExperiment_01_Design.csv
    - Randomisation of herbicide treatments and test species within layout
  - HerbicideScreeningExperiment_02_PlantConditionScores.csv
    - Plant condition scores (0–5) for sprayed and unsprayed plots across species

- Cereal headland experiment
  - CerealHeadlandExperiment_01_Design.csv
    - Design data: experiment (SB vs WW), blocks, plots, cereal density, N fertilizer
  - CerealHeadlandExperiment_02_VegetationCover.csv
    - Species cover by plot from five 0.5 m quadrats
  - CerealHeadlandExperiment_03_VegetationStructure.csv
    - Cereal cover, tiller density, height, bare ground (and related structure metrics)
  - CerealHeadlandExperiment_04_RarePlantDemography.csv
    - Counts of rare arable plants, flowers, seed heads within five quadrats per plot
  - CerealHeadlandExperiment_05_SeedProduction.csv
    - Seed head counts of rare arable species; seeds per head

- Crop rotation experiment
  - CropRotationExperiment_01_Design.csv
    - Design: block, main plot, crop, mesocosm, seed mix
  - CropRotationExperiment_02_SecondCount.csv
    - Count data for all rare arable species in each mesocosm (second count)
  - CropRotationExperiment_04_SeedProduction.csv
    - Seed head counts and seed counts per seed head by mesocosm and species

## Data quality and processing notes
- Quality assurance performed prior to deposition:
  - Outlier checks
  - Spot checks of input data
  - Verification and correction of ID inconsistencies among recorders
  - Formation of species aggregates for difficult-to-distinguish taxa (e.g., Agrostis stolonifera agg., Veronica persica agg., etc.)
- Datasets use standard taxonomic references (Stace, 2010) and consistent site labels:
  - Sites: Brecklands, Fivehead, Roundwood
  - Years: 2011–2014 (varies by dataset)
  - Units and descriptive fields provided within each dataset

## Data access, storage, and standardisation
- Data designed for deposition in appropriate data portals; datasets follow standard naming conventions and field structures.
- Descriptors and measurement protocols are documented within the dataset descriptions, enabling reproducibility and cross-study synthesis.
- Aggregation and standardisation (e.g., taxon groups, summary statistics) support comparability across experiments and over time.

## Relevance for environmental monitoring and policy assessment
- Provides longitudinal, multi-site data on management impacts to rare arable flora and associated environmental parameters (soil chemistry, bryophyte communities, seedbank).
- Enables evaluation of habitat quality and species responses to agricultural practices (margin management, herbicide use, cereal density, nutrient application, and crop rotation).
- Supports ecological modelling and scenario analysis for policy-relevant questions about conservation of rare arable plants under different management regimes.
- Offers a rich, standardised data backbone for monitoring environmental health, with potential for data integration and broader environmental health reporting.