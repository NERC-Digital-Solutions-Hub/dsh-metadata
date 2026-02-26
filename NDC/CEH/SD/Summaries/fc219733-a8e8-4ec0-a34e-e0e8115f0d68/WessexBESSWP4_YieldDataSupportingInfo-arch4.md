# Yield of winter-sown oilseed rape plants in relation to insect pollination

## Purpose and Scope
- A dataset from the Wessex BESS project aiming to collect yield data on winter-sown oilseed rape in relation to insect pollination and ecosystem services from beneficial insects.
- Data can be linked to the natural enemy and pollinator datasets from the same project.

## Study Design and Data Collection
- Location and period: 14 farms in southern England, 2013–2015.
- Field setup: some farms with multiple fields; three 58 m transects per field, positioned to include hedges/margins where possible.
- Sampling points: five points per transect at 8 m, 20.5 m, 32 m, 44.5 m, and 58 m from field edge; distances recorded if adjusted to avoid tracks.
- Treatments: 2013 and 2015 included open-pollinated vs pollination bagging on two plants per sampling point; 2014 used only open pollination.
- Pollination validation: effectiveness of bags tested using pollen slides at canopy height, with counts of pollen grains across treatments.

## Measurements and Analyses
- Yield data (field level): farmer-reported yield (tonnes per hectare) and seed treatment details (ST1–ST3) per field; cultivar information and seed treatment use recorded.
- Plant-level data: for 2013 and 2015, selected plants were either left open-pollinated or bagged; flowering monitored; plants harvested after desiccation; racemes, pods, seeds, and parasitism indicators recorded.
- Lab analyses: raceme and pod traits measured by parts (bottom/middle/top) of racemes; metrics include number of ripe pods, split pods, parasitized pods, flowering scars, seeds per pod, seed weight, and total seeds per plant.
- Sampling details: up to 18 pods analyzed per plant (or all available if fewer); seed and pod data collected from multiple racemes/parts to capture yield components.

## Datasets and File Structure
- Four linked files:
  - NERCYieldFieldData.csv: field-level yield data, farm/field IDs, YearHarv, variety, hybrid/conventional status, seed treatments.
  - NERCPlantData.csv: plant-level data, transects/points, treatments, raceme counts, seeds per plant, seed weight.
  - NERCRacemePart.csv: raceme-part level data, positions within plant, pod counts, split pods, parasitism indicators, total ripe pods, and total potential pods per part.
  - NERCSeedsPerPod.csv: pod-level seed data, including parasitism status, number of seeds per pod, and weight of seeds per pod.
- Key linking fields indicated (e.g., FarmID, FieldID, PlantID, RacemeID) to enable integrated analyses.

## Data Quality, Governance, and Ethics
- Data quality: trained personnel followed a standardized protocol; data entered into MS Access; anomaly checks performed; some missing values recorded in metadata.
- Missing data notes:
  - NoRacemes: 0.17% missing
  - NoSplitPods: 0.2% missing
  - NoExitHoles: 0.2% missing
  - SeedsPerPod: 23 pods missing seed weight
- Ethics: approved by the CLES Penryn Research Ethics Committee (University of Exeter).

## Metadata and Linking
- Datasets are designed for integration across the four files via key fields (e.g., FarmID, FieldID, PlantID, RacemeID, RacemePartID).
- Metadata highlights variable descriptions, units, and data provenance to support discoverability and reuse.

## Potential Uses and Implications for Data Leaders
- Enables system-wide analysis of how insect pollination influences yield and component traits (pod formation, seed weight/number).
- Supports assessment of ecosystem services from beneficial insects and links to related datasets on pollinators and natural enemies.
- Demonstrates a multi-tier data collection approach (field, plant, raceme part, and seed-level data) suitable for governance, data quality practices, and cross-domain collaboration.
- Highlights importance of thorough metadata, data linkage keys, and clear documentation to facilitate data discoverability, reuse, and co-ownership across user communities.