# Yield of winter-sown oilseed rape plants in relation to insect pollination

## Overview
- Dataset from the Wessex BESS project (NERC) aims to collect yield data on winter-sown oilseed rape in relation to insect pollination and ecosystem services provided by beneficial insects.
- Data can be linked to natural enemy and pollinator datasets within Wessex BESS.

## Study design and scope
- Location and duration: 14 farms in southern England, 2013–2015.
- Field structure: Some farms contained multiple fields (FieldID); within fields, three 58 m transects (TransectID) perpendicular to field edges; transects selected to include hedged/margined edges where possible.
- Sampling points: 5 points per transect at 8 m, 20.5 m, 32 m, 44.5 m, and 58 m from the field edge; distance from edge recorded if adjusted to avoid tracks.
- Crop: Winter-sown oilseed rape (Brassica napus L.).
- Data files: Four linked datasets (see Metadata section) enabling field, plant, raceme part, and seed-level analyses.

## Treatments and experimental design
- Pollination treatments (yield relation to pollination assessed in 2013 and 2015): two plants per sampling point were randomly allocated to open pollination or protected with a microperforated pollination bag.
- 2014: open pollination applied to all plants; no bagged treatment.
- Pollination bag effectiveness: tested with pollen slides at canopy height under three conditions (open pollinated, bagged with plant, bagged without plant); pollen grains counted to compare pollen transfer across treatments.
- Pollen counts (lab): open pollinated mean 462.4 ± 753.9 SD (n=9); microperforated bag with plant mean 389.2 ± 353.9 SD (n=9); microperforated bag without plant mean 291.9 ± 355.04 SD (n=8).

## Data collection and variables
- Yield data (field level): Year harvested, farm, field, variety, hybrid/conventional, seed treatment status, total yield (tonnes per hectare), and seed treatment details (ST1–ST3).
- Plant-level data: FieldID, TransectID, PointCode, PlantID, Treatment (A=open pollinated, B=bagged, wind only pollinated), NoRacemes, SeedPerPlant, SeedWeight.
- Raceme-level data: RacemeID, RacemePosition (bottom/middle/top of plant), RacemePartID, RacemePart (bottom/middle/top), NoSplitPods, NoPodsExitHoles, TotalRipePods, TotalPodsPerPart.
- Pod/seed data: Seeds per pod, weight of seeds per pod, Parasitised status, NoSeed per pod, WeightSeedPod. Each raceme provides multiple parts and seeds; 18 pods analyzed per plant when possible.
- Metadata linking: Fields marked with * (e.g., FieldID, PlantID, RacemeID) enable linking across datasets to build plant- and field-level analyses.

## Data quality assurance and ethics
- Protocols and training: Field and laboratory staff trained by R. Shaw; standardized data collection forms; data entered into MS Access to prevent duplicates.
- Data checks: Anomalies checked; missing values present due to recorder error; percentages noted in file metadata.
- Ethics: Study approved by the CLES Penryn Research Ethics Committee (University of Exeter).

## Files and metadata (datasets)
- NERCYieldFieldData.csv
  - Contains field-level/yield data: FarmID, FieldID, YearHarv, VarietyCode, HybridConventional, Yield_tHa, SeedTreatment, ST1/ST2/ST3.
  - Note: Blank ST1/ST2/ST3 indicate no seed treatment used; numbers vary by farmer.
- NERCPlantData.csv
  - Plant-level data: FieldID, TransectID, PointCode, PlantID, Treatment, NoRacemes, SeedPerPlant, SeedWeight, etc.
  - Data note: NoRacemes has one missing data point (0.17%).
- NERCRacemePart.csv
  - Raceme-part data: PlantID, RacemeID, RacemePosition, RacemePartID, RacemePart, NoSplitPods, NoPodsExitHoles, TotalRipePods, TotalPodsPerPart.
  - Missing data: NoSplitPods (12/5828), NoExitHoles (13/5828), TotalRipePods (17/5828).
- NERCSeedsPerPod.csv
  - Pod-level seed data: RacemeID, RacemePosition, RacemePartID, RacemePart, Parasitised, NoSeed, WeightSeedPod.
  - Missing data: 23 pods missing seed weight data.

## How to use and link the datasets
- Core identifiers to unite datasets: FarmID, FieldID, TransectID, PointCode, PlantID, RacemeID, RacemePartID.
- Cross-dataset analyses possible: yields by field/variety and seed treatments; plant-level to pod-level relationships; pollination treatment effects on seed production and pod characteristics.
- Data can support analyses of pollination effects on yield, accounting for spatial variation (edges, hedges), farm-level practices (seed treatments), and raceme/ pod-level outcomes.

## Summary of practical considerations for analysts
- Scale and scope: 14 farms over 3 years with field- and plant-level detail enables robust multilevel analyses of pollination effects on yield.
- Data richness vs. gaps: rich dataset with comprehensive QA, but some missing values due to recorder error; detailed metadata facilitates data cleaning.
- Scale-specific challenges for analysts: aligning field-level yield with plant- and pod-level variables; ensuring correct linking across four datasets; handling optional seed treatments that vary by farmer.
- Ethical and provenance notes: ethically approved; data collected with standardized protocols and training; datasets are clearly documented for reproducibility.