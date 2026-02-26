# Yield of winter-sown oilseed rape plants in relation to insect pollination

- Overview
  - A dataset from the Wessex BESS project linking yield of winter-sown oilseed rape to insect pollination and ecosystem services provided by beneficial insects.
  - Authors and affiliations: Shaw, R.F.; Bullock, J.M.; Osborne, J.L. (University of Exeter and NERC CEH, UK).
  - Data can be linked to natural enemy and pollinator datasets within the Wessex BESS program.
  - Purpose: support monitoring and evaluation of pollination-related environmental health measures for policy and decision-making.

- Study design and data collection
  - Setting: 14 farms in southern England, 2013–2015.
  - Field layout: three 58 m transects per field, stratified sampling at edge features (hedges/margins) where possible.
  - Sampling points: 8 m, 20.5 m, 32 m, 44.5 m, and 58 m from field edge; field- or point-level data recorded.
  - Crop: winter-sown oilseed rape (Brassica napus L.).
  - Experimental treatments: 2013 and 2015 used open pollination vs microperforated pollination bags to exclude insects; 2014 used open pollination only.
  - Pollination efficacy checks: slides with sticky tape to quantify pollen transfer under different pollination treatments.
  - Harvest window: between desiccation (herbicide) and harvest.
  - Data collection includes field-level farmer yield reports and detailed plant- and raceme-level measurements.

- Measurements and laboratory analysis
  - Plant-level data: treatment (A = open pollinated, B = bagged, wind), NoRacemes, SeedPerPlant, SeedWeight.
  - Raceme and pod metrics: raceme IDs, positions (bottom/middle/top), part-level data (pod counts, ripeness, parasitism indicators), and total potential pods per raceme part.
  - Seed-level data: seeds per pod, pod weight, and assessment of parasitism.
  - Laboratory workflow: harvest and seed extraction, raceme/pod sampling across plant sections, seed counting with automated counter.
  - Sample sizes (analysed plants): 2013A = 58; 2013B = 50; 2014A = 180; 2015A = 154; 2015B = 156.
  - Key yield metric: farmer-reported yield in tonnes per hectare (t/ha) at field level.

- Data quality, governance, and ethics
  - Quality assurance: trained personnel, standardized field/lab protocols, data recorded with forms, MS Access database to prevent duplicates, anomaly checks.
  - Data completeness: some missing values due to recorder error; missing data percent documented in file metadata.
  - Ethics: approval from CLES Penryn Research Ethics Committee (University of Exeter).
  - Data sharing considerations: underlying data are intended to be shared, though some barriers may exist (metadata, openness, governance requirements).

- Datasets and metadata
  - Four linked CSV files:
    - NERCYieldFieldData.csv: field-level yields, field IDs, year harvested, seed treatments, and related variables; notes on seed treatment WEIGHT and blanks not indicating missing data when treatments were not used.
    - NERCPlantData.csv: plant- and transect-level data; fields include FieldID, TransectID, PointCode, PlantID, treatment, NoRacemes, SeedPerPlant, SeedWeight, etc.
    - NERCRacemePart.csv: raceme-part level data; includes RacemeID, RacemePosition, RacemePartID, NoSplitPods, NoPodsExitHoles, TotalRipePods, TotalPodsPerPart.
    - NERCSeedsPerPod.csv: seed-level pod data; includes RacemeID, RacemePosition, RacemePartID, Parasitised, NoSeed, WeightSeedPod.
  - Linkages: key identifiers (FarmID, FieldID, TransectID, PointCode, PlantID, RacemeID, RacemePartID) enable cross-dataset integration.
  - Metadata notes: detailed variable descriptions, units, and data quality remarks; explicit mention of how to interpret missing values (e.g., ST1–ST3 due to farmers’ seed-treatment choices).

- Implications for monitoring and policy
  - Provides a structured, linkable data framework to monitor how insect pollination influences yield and related plant metrics.
  - Enables assessment of pollination services’ contribution to crop production and broader ecosystem service outcomes.
  - Supports integration with other biodiversity datasets (pollinators and natural enemies) for holistic environmental health monitoring.
  - Highlights the importance of robust metadata, data sharing practices, and governance to support reproducible policy-relevant analyses.

- Limitations and data gaps to consider for monitoring frameworks
  - Variability in seed treatment applications across farms introduces complexity in isolating pollination effects.
  - Some years/features had open-pollination-only treatments (2014), which limits direct year-to-year comparisons.
  - Missing data due to recording errors; metadata documents the extent of gaps.
  - Data sharing barriers may affect timely availability and reuse by policymakers.