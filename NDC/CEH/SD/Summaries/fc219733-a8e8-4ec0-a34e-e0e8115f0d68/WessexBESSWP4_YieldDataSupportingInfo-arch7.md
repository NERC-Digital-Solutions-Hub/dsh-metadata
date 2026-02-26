# Yield of winter-sown oilseed rape plants in relation to insect pollination

## Overview
- Dataset from the Wessex BESS project examining oilseed rape yield in relation to insect pollination and ecosystem services provided by beneficial insects.
- Linked to natural enemy and pollinator datasets within the Wessex BESS program.

## Study design and geography
- Location: 14 farms in southern England; study area bounded by NW corner 51.415482°N, -2.2892761°W and SE corner 51.087135°N, -1.5037537°W.
- Timeframe: 2013–2015.
- Crop: Winter-sown oilseed rape (Brassica napus L.).
- Spatial sampling: In-field transects and points to capture within-field variation.
  - Three 58 m transects per field, perpendicular to field edge.
  - Stratified random transect placement to include hedges/margins.
  - Sampling points along each transect at 8 m, 20.5 m, 32 m, 44.5 m, and 58 m from edge; distance from edge recorded if adjusted for tractor tracks.
- Data structure: Farms (FarmID) may contain multiple fields (FieldID); some fields have multiple transects, and transects contain multiple sampling points (PointID).

## Data collection levels and sampling scheme
- Field-level yield data collected per harvest year (2013–2015): FarmID, FieldID, YearHarv, VarietyCode, HybridConventional, Yield_tHa, SeedTreatment (and ST1–ST3).
- Plant-level and micro-level sampling:
  - Plant data collected at the designated sampling points;Treatment options include open pollinated (A) or bagged/wind-only pollination (B).
  - 2013 and 2015: two plants per sampling point assigned to open pollinated or bagged; 2014: only open pollinated treatment applied.
- Lab analyses:
  - Floral/pollination verification: pollen transfer tests using slides and sticky tape; three treatments (open, bag, pollination bag) evaluated for pollen transfer.
  - Post-flowering field desiccation window used for plant collection and seed analysis.
- Data collection training and protocol: field and lab personnel trained by R. Shaw; standardized data forms; captured in MS Access database.

## Treatments and laboratory measurements
- Treatments per plant:
  - A: Open pollinated
  - B: Bagged (pollination exclusion)
  - Wind-only pollination (context described in dataset)
- Yield and seed measurements:
  - Number of racemes per plant; seeds per plant; seed weight per plant.
  - Pods and seeds assessed across raceme bottoms, middles, and tops; parasitism indicators and pod scars recorded.
  - Pod-level data includes number of ripe pods, split pods, and pods with evidence of parasitism.
  - Pod-level seed weight and seed counts per pod documented; seeds counted and weighed per plant.
- Sampling sizes (plants analyzed):
  - 2013A: 58 plants
  - 2013B: 50 plants
  - 2014A: 180 plants
  - 2015A: 154 plants
  - 2015B: 156 plants

## Data files and linking keys
- Four CSV data files:
  - NERCYieldFieldData.csv
    - Links: FarmID, FieldID, YearHarv
    - Fields include: VarietyCode, HybridConventional, Yield_tHa, SeedTreatment (and ST1–ST3)
  - NERCPlantData.csv
    - Links: FieldID, TransectID, PointCode, PlantID
    - Fields include: Treatment (A/B), NoRacemes, SeedPerPlant, SeedWeight
  - NERCRacemePart.csv
    - Links: PlantID, RacemeID, RacemePosition, RacemePartID
    - Fields include: NoSplitPods, NoPodsExitHoles, TotalRipePods, TotalPodsPerPart
  - NERCSeedsPerPod.csv
    - Links: RacemeID, RacemePartID
    - Fields include: Parasitised, NoSeed, WeightSeedPod
- Meta-data and data quality notes:
  - Missing data: NoRacemes (1 data point in 2013 data); NoSplitPods, NoExitHoles, TotalRipePods have small amounts missing in subset; 23 pods missing seed weight in SeedsPerPod data.
  - Some blank cells in ST1–ST3 denote no seed treatment used rather than missing data.
- Linkability: Datasets are designed to be linked via standardized identifiers (FarmID, FieldID, TransectID, PointCode, PlantID, RacemeID, RacemePartID).

## Data quality, ethics, and provenance
- Data quality: Trained personnel followed a fixed protocol; data entered to prevent duplicates; anomaly checks performed; missing values documented in file metadata.
- Ethics: Approved by CLES Penryn Research Ethics Committee (University of Exeter).

## GIS-relevant implications and potential uses
- Spatial analysis:
  - Map yield_tHa and seed production in relation to spatial features (field edges, hedgerows, margins) and transect locations.
  - Analyze effects of pollination treatment (open vs bagged) across spatial gradients within fields.
- Data integration:
  - Link agronomic yield with pollinator-related and natural-enemy datasets within the Wessex BESS framework for ecosystem service assessments.
  - Combine Field-level, Plant-level, Raceme-level, and Pod-level data for multi-scale GIS analyses (field to pod).
- Data products:
  - Create map-based visualisations of pollination treatment distribution, yields, and productivity hotspots.
  - Develop GIS workflows to incorporate distance-from-edge and transect position to explain yield variation.
- Considerations:
  - Geographic scope limited to southern England; ensure spatial coordinates align with field boundaries and transect lines.
  - Use linking keys to merge with external environmental layers (habitat features, hedges, margins) for richer spatial interpretation.