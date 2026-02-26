# Supporting documentation: Data from the experimental management of arable field options for rare plants (Defra project BD5204)

## Overview
- Four main experiments conducted between 2011 and 2014 to study rare arable plants under different management and cropping scenarios.
- Data types include vegetation cover, species counts, seed production, bryophyte frequencies, soil chemistry, seedbanks, and demography of rare arable plants.
- Datasets are organized by site (Brecklands, Fivehead, Roundwood), plot-level and mesocosm-level identifiers, years, and treatment factors.
- Quality assurance involved outlier checks, spot checks of input data, correction of recorder ID inconsistencies, and creation of species aggregates where needed.
- Data are deposited as multiple CSV files describing experimental design, treatments, and ecological measurements prior to deposition.

## Experimental design (four main experiments)

- Margin management experiment
  - Multi-site setup at Brecklands, Fivehead, and Roundwood (autumn 2010 start).
  - Randomised complete block split-plot design with three sites (Brecklands has four blocks; others have three).
  - Main plots: six 12 m x 60 m plots with two cultivation seasons (spring/autumn) and three cultivation methods (discing, harrowing, ploughing).
  - Sub-plots: four 12 m x 15 m sub-plots per main plot with four herbicide treatments (unsprayed, glyphosate, graminicide, and selective broadleaf herbicide plus graminicide).
  - Treatments applied annually (2010–2014).
  - Additional cereal-density and nitrogen-fertilizer experiments within the margin framework using winter wheat and spring barley to assess effects on sown rare arable species and spontaneous weed flora; involved multiple density and N-fertilizer combinations with counts and measurements taken in mid- to late 2014.

- Herbicide screening experiment
  - 15 seed strips dedicated to rare arable plant species, crossed by 23 herbicide strips in three experimental blocks.
  - 21 herbicides randomly assigned to strips, with two unsprayed controls.
  - Sowing on 30 Apr 2012; pre- and post-emergence herbicides applied.
  - Plant-condition assessments (6-point scale) conducted on 1 Aug 2012 in 1 m x 1.5 m plots, requiring at least 10 established plants per plot.

- Cereal headland experiments
  - Two experiments: winter-wheat (WW) and spring-barley (SB).
  - Randomised block design with four replicates; plots labeled SB01–SB20 and WW01–WW20.
  - Cereal densities and N fertilizer levels varied across plots.
  - Central 5 m x 5 m area over-sown with a mix of rare arable species.
  - Sowing dates: WW on 27 Sep 2013; SB on 14 Mar 2014; N and S fertilization applied as specified.
  - Final and mid-season measurements in 2014 included percent cover, tiller density, height, bare ground, and seed-head sampling for rare species.

- Crop rotation experiment
  - Split-plot mesocosm design in two main plots, each with six crop treatments.
  - 12 mesocosms per main plot (total 144 mesocosms); two seed-mix types per main plot (A: autumn-germinating; S: spring-germinating).
  - Inoculation of top 5 cm of soil with seed mixes on 18 Sep 2013; sowing of winter crops on 19 Sep 2013 and spring crops on 20 Mar 2014.
  - Early count of established rare arable plants before sowing spring crops; final count in Jun–Jul 2014 with seed-head and seed production sampling.

## Datasets (by experiment)

- Margin management experiment
  - MarginManagementExperiment_01_Design.csv: randomisation of main plots, sub-plots, and treatments.
  - MarginManagementExperiment_02_VegetationWholeSubplots.csv: estimated percent cover by species per sub-plot (2011–2014), with species aggregates for difficult-to-distinguish taxa.
  - MarginManagementExperiment_03_VegetationQuadratAverages.csv: average percent cover from three 1 m quadrats per sub-plot (2011–2014), with species aggregates.
  - MarginManagementExperiment_04_RarePlantCounts.csv: twice-annual counts of rare arable plants per sub-plot (2011–2014).
  - MarginManagementExperiment_05_FlowersSeedHeads.csv: counts of flowers and seed heads for rare species (2014).
  - MarginManagementExperiment_06_SeedProduction.csv: counts of seeds per seed head (2014).
  - MarginManagementExperiment_07_SoilChemistry.csv: soil chemical parameters at main-plot level (pH, available P/K/Mg, texture fractions, loss-on-ignition, total N and C) measured in 2014.
  - MarginManagementExperiment_08_Bryophytes.csv: bryophyte frequencies in unsprayed sub-plots (late 2014).
  - MarginManagementExperiment_09_Seedbank.csv: seed counts from soil samples (autumn 2012 and 2013) with depth stratification and greenhouse recording.

  - Experimental design (within margin): not a separate file here beyond MarginManagementExperiment_01_Design.csv; descriptions include a couple of cereal-density and N-fertilizer experiments integrated into the margin framework.

- Herbicide screening experiment
  - HerbicideScreeningExperiment_01_Design.csv: randomisation of herbicide treatments and test species within layout (blocks, herbicide strips, timing: pre/post-emergence).
  - HerbicideScreeningExperiment_02_PlantConditionScores.csv: plant condition scores (0–5 scale) by herbicide strip, treatment, and species.

- Cereal headland experiments
  - CerealHeadlandExperiment_01_Design.csv: randomisation info for WW and SB experiments (experiment type, block, plot, cereal density, N fertilizer).
  - CerealHeadlandExperiment_02_VegetationCover.csv: species cover percentages per plot (SB01–SB20, WW01–WW20), averaged across five quadrats.
  - CerealHeadlandExperiment_03_VegetationStructure.csv: additional metrics per plot (cereal cover, tillers per 1.25 m^2, height, bare ground), averaged or summed as specified.
  - CerealHeadlandExperiment_04_RarePlantDemography.csv: counts of rare arable plants, flowers, and seed heads per plot across five quadrats.
  - CerealHeadlandExperiment_05_SeedProduction.csv: seeds per seed head by plot and species.

- Crop rotation experiment
  - CropRotationExperiment_01_Design.csv: randomisation of blocks, main plots, crop treatments, mesocosm IDs, and seed mix (A or S).
  - CropRotationExperiment_01_Counts.csv: first count of rare arable plants by mesocosm and species (March 2014).
  - CropRotationExperiment_02_SecondCount.csv: second count by mesocosm and species (June/July 2014) including seed heads.
  - CropRotationExperiment_04_SeedProduction.csv: seeds per seed head by mesocosm and species.

## Data quality and deposition

- QA procedures performed across datasets:
  - Outlier checks and spot checks of input data.
  - Verification and correction of recorder IDs for vegetation data.
  - Creation of species aggregates for difficult-to-distinguish taxa.

- Data processing and preparation:
  - Data were cleaned and transformed prior to deposition.
  - Aggregations were applied where species were hard to distinguish (e.g., certain grass and plant groups).

## GIS-ready potential and interpretation notes

- Spatial structure
  - Data are organized by site (Brecklands, Fivehead, Roundwood) and nested within main plots, sub-plots, and mesocosms, enabling hierarchical spatial analysis and potential mapping of treatments and responses when plot boundaries are available.
- Temporal coverage
  - Multiple measurements across 2011–2014, including annual treatment applications and seasonal field surveys.
- Measurement types
  - Vegetation cover (whole subplots and per-plot quadrats), rare arable plant counts, flower/seed-head counts, seed production, soil chemistry, bryophyte frequencies, and seedbank data.
- Applications for GIS
  - Create map layers showing treatment allocations and changes in vegetation composition over time.
  - Overlay soil chemistry or bryophyte/seedbank indicators with plot boundaries for spatial modelling.
  - Use counts and seed production data to model patch-level responses to management regimes and crop rotations.

## End notes

- The collection provides a comprehensive, multi-faceted dataset across four experimental themes (margin management, herbicide screening, cereal headlands, and crop rotation) with rich spatial and temporal resolution suitable for GIS-driven analyses and map-based data products.