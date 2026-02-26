# Supporting documentation: Data from the experimental management of arable field options for rare plants (Defra project BD5204)

- Purpose of the document
  - Provides detailed experimental design, data deposition, and data processing information for four main experiments (margin management, herbicide screening, cereal headland, and crop rotation) conducted between 2011 and 2014.
  - Describes quality assurance steps and metadata handling to support data usefulness for monitoring environmental health and informing policy decisions.

- Experimental design overview
  - Margin management experiment
    - Multi-site, randomized complete block split-plot design at three sites (Brecklands, Fivehead, Roundwood).
    - Main-plot factors: cultivation season (spring or autumn) and cultivation method (discing, harrowing, ploughing).
    - Sub-plot factor: herbicide treatment (unsprayed, glyphosate, graminicide, selective broadleaf herbicide plus graminicide).
    - Treatments applied annually from autumn 2010 to spring 2014.
  - Herbicide screening experiment
    - 15 seed strips (1 m width, 110 m length) with 15 rare arable plant species randomized to strips.
    - Perpendicular experimental blocks with 23 herbicide strips; 21 herbicides plus two unsprayed controls.
    - Sowing on 30 April 2012; pre- and post-emergence herbicide applications; plant-condition scoring on 1 August 2012.
  - Cereal headland experiments
    - Two experiments (winter wheat and spring barley) with margin 12 m wide; four replicate blocks.
    - Treatments include varying cereal sowing density and N fertilizer application; central area over-sown with rare arable plant species.
    - Final recordings in July 2014 include species cover, plant numbers, flowers, seed heads, tiller density, height, and bare ground.
  - Crop rotation experiment
    - Split-plot mesocosm design: six crop treatments across two replicate main plots; 144 mesocosms total.
    - Within each main plot, two seed mixes (autumn- vs spring-germinating species).
    - Counts of rare arable plants in March 2014 and June/July 2014; seed production per seed head collected.

- Datasets and their contents
  - Margin management experiment
    - MarginManagementExperiment_01_Design.csv: randomisation of treatments to plots and sub-plots.
    - MarginManagementExperiment_02_VegetationWholeSubplots.csv: annual estimated percent cover by species (2011–2014) in whole sub-plots.
    - MarginManagementExperiment_03_VegetationQuadratAverages.csv: cover estimates from five 1 m2 quadrats per sub-plot (averaged).
    - MarginManagementExperiment_04_RarePlantCounts.csv: twice-annual counts of rare arable plants (early/late census) in 0.3 m quadrats.
    - MarginManagementExperiment_05_FlowersSeedHeads.csv: counts of flowers and seed heads for rare species (2014).
    - MarginManagementExperiment_06_SeedProduction.csv: counts of seeds per seed head (2014).
    - MarginManagementExperiment_07_SoilChemistry.csv: soil chemistry parameters (pH, P, K, Mg, texture, LOI, total N, etc.) at 20 cm depth.
    - MarginManagementExperiment_08_Bryophytes.csv: bryophyte frequencies in 12x0.2 m quadrats (late 2014).
    - MarginManagementExperiment_09_Seedbank.csv: soil seed counts from autumn 2012/2013 sampling; depth-specific pooling; greenhouse germination data.
  - Herbicide screening experiment
    - HerbicideScreeningExperiment_01_Design.csv: randomisation of herbicide treatments and test species within layout.
    - HerbicideScreeningExperiment_02_PlantConditionScores.csv: plant-condition scores on a 6-point scale for treated and unsprayed plots.
  - Cereal headland experiments
    - CerealHeadlandExperiment_01_Design.csv: randomisation of cereal density and N fertilizer within plots/blocks.
    - CerealHeadlandExperiment_02_VegetationCover.csv: species cover across five 0.5 m quadrats per plot.
    - CerealHeadlandExperiment_03_VegetationStructure.csv: cereal cover, tillers (sum across quadrats), height, bare ground.
    - CerealHeadlandExperiment_04_RarePlantDemography.csv: counts of rare arable plants, flowers, seed heads (across five quadrats per plot).
    - CerealHeadlandExperiment_05_SeedProduction.csv: seeds per seed head for rare arable species.
  - Crop rotation experiment
    - CropRotationExperiment_01_Design.csv: randomisation of crop treatments and mesocosm assignments.
    - CropRotationExperiment_02_SecondCount.csv: second count of rare arable plants per mesocosm.
    - CropRotationExperiment_04_SeedProduction.csv: seeds per seed head in mesocosms.

- Data collection and processing details
  - Quality assurance
    - Outlier checks and spot checks of input data.
    - Vegetation data: correction of ID inconsistencies among recorders; formation of species aggregates where necessary.
  - Data processing prior to deposition
    - Aggregation of difficult-to-distinguish taxa into aggregates using established taxonomic references (e.g., Stace 2010).
    - Compilation of background control values using additional sampling within field areas.
  - Data governance considerations
    - Some datasets require sharing underlying data publicly; the project notes potential barriers related to metadata completeness and data sharing policies.
    - Soil analyses performed by an external contractor; documentation of methods and units included.

- Temporal and spatial coverage
  - Timeframe: experimental activities and data collection spanning 2011–2014.
  - Sites: Brecklands, Fivehead, Roundwood (three sites for margin management; related datasets tied to these sites).

- Relevance for monitoring frameworks
  - Provides a comprehensive, multi-layered dataset to monitor environmental health indicators related to arable field management and rare plant populations.
  - Demonstrates rigorous QA practices, metadata handling, and data transformation needs—key considerations for monitoring framework authors.
  - Offers baseline data and treatment-response information to inform policy decisions on crop management, pesticide use, habitat management, and biodiversity conservation.
  - Highlights challenges in data accessibility, standardization, and governance, underscoring the need for clear data-sharing and metadata standards in monitoring frameworks.