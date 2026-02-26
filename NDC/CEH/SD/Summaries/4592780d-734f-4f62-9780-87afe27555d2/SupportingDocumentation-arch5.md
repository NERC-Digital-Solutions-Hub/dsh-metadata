# Supporting documentation: Data from the experimental management of arable field options for rare plants (Defra project BD5204)

## Overview
- Sets out data and quality assurance for four main experiments (2011–2014) on rare arable plants: margin management, herbicide screening, cereal headland, and crop rotation.
- Documents experimental design, data collection, and data processing prior to deposition.
- Quality assurance processes included outlier checks, spot data checks, correction of ID inconsistencies, and creation of species aggregates where needed.

## Experimental design (summary)
- Margin management experiment
  - Multi-site, randomized complete block split-plot design at Brecklands, Fivehead, Roundwood.
  - Main plots: cultivated season (spring/autumn) and cultivation method (discing, harrowing, ploughing).
  - Sub-plots: four herbicide treatments (unsprayed, glyphosate, graminicide, selective broadleaf herbicide plus graminicide).
  - Treatments applied annually 2010–2014.
- Herbicide screening experiment
  - Seed strips (1 m width, 110 m length) with 15 rare arable species; 3 blocks with 23 herbicide strips.
  - 21 herbicides randomly assigned to strips; 2 unsprayed controls.
  - Sowing 30 Apr 2012; pre-emergence and post-emergence herbicides applied; scoring on 1 Aug 2012 for plots with sufficient establishment.
- Crop rotation experiment
  - Baseline data to model rare arable species under crop rotations using a split-plot mesocosm design.
  - Six crop treatments randomly assigned in two replicate blocks; within each main plot, twelve mesocosms with two seed mixes (autumn- vs spring-germinating species).
  - Counts of rare arable plants and seed production collected across counts in 2014.
- Cereal headland experiments
  - WW (winter wheat) and SB (spring barley) experiments with multiple plots and treatments.
  - Data capture includes sowing density (cereal), N fertilizer levels, and subsequent vegetation measurements.

## Datasets (by experiment)

- MarginManagementExperiment
  - MarginManagementExperiment_01_Design.csv: randomisation of treatments to main plots and sub-plots (sites, blocks, plots, sub-plots; main-plot and sub-plot treatments).
  - MarginManagementExperiment_02_VegetationWholeSubplots.csv: annual estimated percent cover by species (2011–2014) per sub-plot; edge-buffer avoidance noted; species aggregates formed for difficult-to-distinguish taxa.
  - MarginManagementExperiment_03_VegetationQuadratAverages.csv: yearly average percent cover per species from five 1 m quadrats per sub-plot.
  - MarginManagementExperiment_04_RarePlantCounts.csv: twice-annual counts of rare arable plants (0.3 m quadrats) per sub-plot.
  - MarginManagementExperiment_05_FlowersSeedHeads.csv: counts of flowers and seed heads for rare species (2014).
  - MarginManagementExperiment_06_SeedProduction.csv: seeds per seed head for rare species.
  - MarginManagementExperiment_07_SoilChemistry.csv: soil chemistry parameters (pH, P, K, Mg, texture, LOI, Total N, etc.) at main-plot level, Sept–Oct 2014.
  - MarginManagementExperiment_08_Bryophytes.csv: bryophyte frequencies in unsprayed sub-plots (Nov–Dec 2014).
  - MarginManagementExperiment_09_Seedbank.csv: seed counts from soil cores (autumn 2012–2013) at two depths; greenhouse germination method; species aggregates.
  - MarginManagementExperiment_10? (not listed)

- HerbicideScreeningExperiment
  - HerbicideScreeningExperiment_01_Design.csv: randomisation of herbicide treatments and test species within layout (blocks, herbicide strips, timing: pre/post).
  - HerbicideScreeningExperiment_02_PlantConditionScores.csv: plant condition scores (0–5) by strip, treatment, and species.

- CropRotationExperiment
  - CropRotationExperiment_01_Design.csv: randomisation of six crop treatments across two blocks; mesocosm IDs; seed mix (autumn vs spring).
  - CropRotationExperiment_02_SecondCount.csv: counts of all rare arable species in mesocosms (second count, June/July 2014).
  - CropRotationExperiment_04_SeedProduction.csv: seeds per seed head in crop rotation mesocosms.

- CerealHeadlandExperiment
  - CerealHeadlandExperiment_01_Design.csv: design for cereal headland experiments (WW and SB); block and plot identifiers; cereal density and N fertilizer levels.
  - CerealHeadlandExperiment_02_VegetationCover.csv: percent cover per species in five 0.5 m quadrats per plot (averaged across quadrats).
  - CerealHeadlandExperiment_03_VegetationStructure.csv: cereal cover, tiller density, height, and bare ground (averaged across quadrats or summed as noted).
  - CerealHeadlandExperiment_04_RarePlantDemography.csv: counts of rare arable plants, flowers, and seed heads (per plot).
  - CerealHeadlandExperiment_05_SeedProduction.csv: seeds per seed head (per plot).

## Quality assurance, data processing, and provenance
- QA steps included outlier detection, spot checks of input data, alignment of recorder IDs, and creation of species aggregates to handle identification challenges.
- Data have been processed prior to deposition (e.g., aggregation of species, standardized taxonomic references).
- Taxonomy references used for species aggregates and identification: Stace (2010) and Smith et al. for bryophytes.
- Data are organized with consistent keys and descriptors (Site, Sub-plot, Plot/Mesocosm, Species) to enable traceability from design to results.
- Temporal coverage spans 2011–2014 with vegetation surveys typically in July, soil sampling in Sept–Oct 2014, and seed-related data collected mid-year.

## Governance, interoperability, and reuse
- Data are stored as CSV files with explicit column descriptions; metadata embedded in headers and dataset documentation.
- Common identifiers across datasets (Site, Sub-plot, Plot, Mesocosm, Species) enable integrative analysis across experiments.
- Clear separation of design data from outcome data to support data lineage and reproducibility.
- Potential reuse considerations include units, taxonomic harmonization, and handling of aggregates for difficult-to-identify taxa.

## Access and stewardship implications
- For data stewards, the collection demonstrates comprehensive QA, standardized metadata, and explicit data provenance across multiple interrelated experiments.
- Requires ongoing governance to maintain consistency across datasets, manage updates, and document any methodological changes or clarifications.