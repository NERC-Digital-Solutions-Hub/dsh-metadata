# Data from the experimental management of arable field options for rare plants (Defra project BD5204)

## Overview
- Describes four main experiments conducted between 2011 and 2014 as part of a Defra project BD5204: Margin management, Herbicide screening, Cereal headland, and Crop rotation.
- Provides details on experimental design, data collection, processing, and quality assurance (QA) prior to data deposition.
- Aims to support modelling and analysis of rare arable plant dynamics under different management and crop scenarios.

## Experimental design (high-level)
- Margin management experiment
  - Multi-site, randomized complete block split-plot design at Brecklands, Fivehead, and Roundwood.
  - Main plots: cultivation season (spring/autumn) and cultivation method (discing, harrowing, ploughing).
  - Sub-plots: herbicide treatments (unsprayed, glyphosate, graminicide, selective broadleaf plus graminicide).
  - Treatments applied annually (2010–2014).
- Herbicide screening experiment
  - Seed strips for 15 rare arable plant species; 23 herbicide strips per block.
  - 21 herbicides randomly assigned to strips; 2 unsprayed controls.
  - Sowing on 30 April 2012; pre- and post-emergence herbicides applied; plant-condition scoring on 1 August 2012.
- Crop embedding (density and fertilizer) experiments
  - Two separate randomized block experiments (winter wheat and spring barley) to test standard vs reduced cereal sowing density and N fertilizer application.
  - 5 treatments including controls, low/high density, and with/without N.
  - Central 5 m × 5 m area over-sown with rare arable species; final measurements in July 2014.
  - Data collected: percent cover, numbers of rare plants, flowers, seed heads, vegetation structure, and seed production in recorded quadrats.
- Cereal headland experiments
  - Separate WW and SB experiments testing cereal density and N fertilizer within headland contexts.
  - Data include treatment randomisation, plot-level cover, tiller density, height, bare ground, and seed production per head.
- Crop rotation experiment
  - Split-plot mesocosm design: six crop treatments across two blocks; 144 mesocosms total.
  - Each main plot contains two seed mixes (autumn- vs spring-germinating species) with random inoculation of soil seed mix.
  - Counts of established rare arable plants in March 2014; final counts in June/July 2014; seed production per seed head collected.

## Datasets and data types
- MarginManagementExperiment_01_Design.csv: randomisation and layout of main plots and sub-plots.
- MarginManagementExperiment_02_VegetationWholeSubplots.csv: year-specific estimated percent cover per sub-plot; single-plot, whole-subplot surveys.
- MarginManagementExperiment_03_VegetationQuadratsAverages.csv: averaged percent cover across five 1 m quadrats per sub-plot.
- MarginManagementExperiment_04_RarePlantCounts.csv: twice-annual counts of rare arable plants per sub-plot.
- MarginManagementExperiment_05_FlowersSeedHeads.csv: counts of flowers and seed heads in 2014; per sub-plot.
- MarginManagementExperiment_06_SeedProduction.csv: seed counts per sampled seed head.
- MarginManagementExperiment_07_SoilChemistry.csv: soil chemical parameters (pH, available P/K/Mg, texture fractions, LOI, total N and C) at main-plot level (2014).
- MarginManagementExperiment_08_Bryophytes.csv: bryophyte frequencies in 0.2 m quadrats (2014).
- MarginManagementExperiment_09_Seedbank.csv: seed counts from soil cores (depth 0–5 cm and 5–20 cm) with greenhouse germination.
- HerbicideScreeningExperiment_01_Design.csv: randomisation of herbicide strips and test species; timing pre/post-emergence.
- HerbicideScreeningExperiment_02_PlantConditionScores.csv: plant-condition scores on a 0–5 scale for treated and control plots.
- CerealHeadlandExperiment_01_Design.csv: randomisation for WW/SB experiments; cereal density and N fertilizer per plot.
- CerealHeadlandExperiment_02_VegetationCover.csv: species cover (5 quadrats per plot) in headland experiments.
- CerealHeadlandExperiment_03_VegetationStructure.csv: cereal cover, tillers, height, bare ground per plot (aggregated across quadrats).
- CerealHeadlandExperiment_04_RarePlantDemography.csv: counts of rare arable plants, flowers, seed heads (per plot).
- CerealHeadlandExperiment_05_SeedProduction.csv: seeds per seed head (head-level data).
- CropRotationExperiment_01_Design.csv: mesocosm layout and seed mix for crop rotation experiment.
- CropRotationExperiment_02_SecondCount.csv: second count of rare arable plants per mesocosm.
- CropRotationExperiment_04_SeedProduction.csv: seeds per seed head in crop rotation mesocosms.

## Data quality and processing
- QA procedures performed on deposition data:
  - Outlier checks and spot checks of input data.
  - Vegetation data: correction of ID inconsistencies among recorders; creation of species aggregates where necessary.
- Data processing prior to deposition includes normalizing species names (e.g., aggregations like Agrostis stolonifera agg.) and ensuring consistent metadata across datasets.
- Datasets are designed to be linked via common identifiers (site, year, plot/sub-plot, mesocosm) to enable cross-dataset analyses.

## Data structure and governance considerations
- Datasets use consistent descriptive fields (Site, Description, Year, Plot, Sub-plot, Species, etc.) to support integration and re-use.
- Species identifiers are standardized to published taxonomies (Stace, 2010) with defined aggregates for difficult-to-distinguish taxa.
- Metadata captures experimental design details (block structure, treatment levels, timing) to enable reproducibility and proper analysis.
- Timeframe and scope: experiments conducted 2011–2014; data deposited to support modelling of rare arable plant dynamics under various management and rotation scenarios.

## Implications for data leaders
- Demonstrates how a multi-experiment data architecture can support a broad data strategy:
  - Comprehensive design documentation paired with rich observational datasets facilitates end-to-end data lifecycle management.
  - Emphasizes data discoverability through standardized schemas and consistent identifiers across experiments.
  - Highlights the importance of QA, metadata, and species standardization for cross-study comparability.
- Provides a model for capturing multi-site, multi-method data with clear pathways for integration, reuse, and potential cross-linkage with partner datasets.

## Potential uses and value
- Modelling population dynamics of rare arable plants under different crop management, herbicide regimes, and rotation schemes.
- Comparative analyses across experiments to identify robust management practices affecting rare species presence, abundance, and reproduction.
- Longitudinal assessment of soil chemistry, bryophyte presence, seed banks, and seed production in relation to management variables.
- Data governance blueprint for multi-study data deposition, enabling future reuse by policy colleagues, researchers, and data networks.