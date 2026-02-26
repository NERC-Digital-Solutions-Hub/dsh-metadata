# Yield of winter-sown oilseed rape plants in relation to insect pollination

## Overview
- Dataset from the Wessex BESS project (NERC) examining yield of winter-sown oilseed rape in relation to insect pollination and ecosystem services provided by beneficial insects.
- Aims to link yield data with pollination context and enable integration with other Wessex BESS datasets (e.g., natural enemies, pollinators).

## Study design and scope
- Location and period:
  - Southern England; 14 farms sampled over three years (2013–2015).
  - Farms coded as FarmID; fields as FieldID (some farms had multiple fields).
- Field sampling:
  - In each field, three 58 m transects perpendicular to field edge.
  - Transects selected to include hedges/margins where possible; edges sampled stratified by edge type.
  - Sampling points per transect: 8 m, 20.5 m, 32 m, 44.5 m, 58 m from edge; distance adjusted to avoid tractor tracks.
- Crop:
  - Winter-sown oilseed rape (Brassica napus L.).

## Treatments and pollination methodology
- Yield assessment in relation to pollination:
  - 2013 and 2015: two plants per sampling point assigned to open pollination or covered with a microperforated pollination bag (to exclude insect pollination).
  - 2014: only open-pollinated treatment applied.
- Pollination bag validation:
  - Effectiveness tested with pollen slides exposed at canopy height (7 days in Apr–May 2014).
  - Slides analyzed for pollen grains under a microscope to compare open pollinated vs bagged conditions.
- Harvest context:
  - Fields often dessicated with herbicide before harvest; plants collected in a two-week window between desiccation and harvest.

## Data collected and structure
- Yield and plant-level metrics:
  - Marked plants for flowering; in lab, racemes and pods counted; seeds per plant and seed weight measured.
  - Laboratory workflow included dissecting racemes into bottom/middle/top sections; assessing ripe pods, dehisced pods, parasitized pods, and flowering scars (total potential pods).
  - From each raceme: two ripe pods from bottom/middle/top thirds were analyzed for seeds per pod and pod weight.
- Pod- and raceme-level data:
  - Pod-level data include number of seeds per pod, weight of seeds per pod, and parasitism indicators.
  - Raceme-level data capture position (bottom, middle, top) and per-part pod counts (including ripened and potentially dehisced pods).
- Farmer-reported field data:
  - Variety (oilseed rape cultivar), seed treatments used (ST1–ST3), and overall field yield (tonnes per hectare).
- Sample sizes (plants analyzed):
  - 2013A: 58 plants; 2013B: 50 plants; 2014A: 180 plants; 2015A: 154 plants; 2015B: 156 plants.
- Files and metadata:
  - 4 files in total:
    - NERCYieldFieldData.csv: field-level yield and treatment information (FieldID, YearHarv, Yield_tHa, SeedTreatment, ST1/ST2/ST3, etc.).
    - NERCPlantData.csv: plant-level data (FieldID, TransectID, PointCode, PlantID, Treatment, NoRacemes, SeedPerPlant, SeedWeight, etc.).
    - NERCRacemePart.csv: raceme-part data (PlantID, RacemeID, RacemePosition, RacemePartID, NoSplitPods, NoPodsExitHoles, TotalRipePods, TotalPodsPerPart, etc.).
    - NERCSeedsPerPod.csv: pod-level data (RacemeID, RacemePosition, RacemePartID, Parasitised, NoSeed, WeightSeedPod, etc.).
  - Metadata notes on missing data and linkage keys (e.g., FieldID, PlantID, RacemeID) to join datasets.
  - Missing data: some fields missing due to recorder error; percentages noted in file metadata; seed treatment columns blank when not used.

## Data quality, governance, and ethics
- Quality assurance:
  - Field/lab staff trained under a standard protocol; data recorded on standardized forms.
  - Data entered into MS Access database to prevent duplicates; routine checks for anomalies.
  - Acknowledgment of missing values due to recorder errors with metadata indicating missingness.
- Ethics:
  - Data collection approved by the CLES Penryn Research Ethics Committee (University of Exeter).

## Reuse and interoperability potential
- Data linkage and standardization:
  - Datasets linked via FarmID, FieldID, PlantID, RacemeID, enabling integrated analyses across field, plant, raceme, and pod levels.
- Ecosystem-service context:
  - Designed to be linked with other Wessex BESS datasets (pollinators, natural enemies) to analyze multiple ecosystem services.
- Accessibility and dissemination:
  - Metadata and structured data formats intended to facilitate upload to data portals and reuse by analysts monitoring environmental health and policy performance over time.
- Value for monitoring:
  - Enables evaluation of the role of insect pollination on crop yield under real-world management, contributing to policy and practice assessments in agricultural ecosystems.