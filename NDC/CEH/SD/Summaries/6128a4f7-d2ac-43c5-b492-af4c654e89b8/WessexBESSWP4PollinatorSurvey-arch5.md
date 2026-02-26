# Pollinators in oilseed rape fields in relation to local plant diversity and landscape characteristics

## Overview
- A dataset describing pollinator communities in winter-sown oilseed rape (Brassica napus L.) and their relationship to local plant diversity and landscape context.
- Collected as part of the Wessex BESS project, funded by NERC.
- Four data files accompany the study and are designed for integration with other Wessex BESS WP4 datasets.

## Datasets Included
- NERCPollinatorSpeciesList.csv
  - Taxonomic details, functional groups, gender, and how species were recorded.
  - Links to other datasets via SpeciesCode.
- NERCPanTrapData.csv
  - Pan trap counts by species/codes, site, transect, date, and habitat variables (e.g., plant cover, growth stage).
  - Noted missing data due to pan traps being knocked over.
- NERCPollTrans.csv
  - Transect-based observations with counts per species/codes across dates.
- NERCPollLandscapeSurvey.csv
  - Landscape-scale metrics within 0.5–3 km buffers around sampling points (grassland types, semi-natural habitats, oilseed rape area, arable area, hedgerows, margins, and various habitat composition/richness indices).
  - Includes site identifiers (FarmID, FieldID), transect identifiers, and numerous radius-based variables (IG, RES, SppRich, SN, OSR, TotAr, margins, hedges, etc.).

## Study Site, Period, and Design
- Location: Wessex region, southern England (field collection across a broad arable/grassy landscape with remnant calcareous grassland).
- Timeframe: Surveys conducted in 2014 and 2015.
- Field sampling: Twelve fields surveyed each year; three transects per field (58 m long) placed per field with stratified randomization to include hedged and hedgeless edges.
- Landscape context: Used GIS-derived layers (CEH Land Cover Map 2007, Natural England Priority Habitats Inventory, local NVC surveys) to classify grassland types and other semi-natural habitats within buffers from 0.5 to 3 km.

## Data Collection and Methods
- Pollinators
  - Flower visitors recorded along transects ( Bombus spp. and Apis mellifera) and via pan traps (15 cm diameter) placed at 8 m, 32 m, and 58 m into the crop; traps left for 4 days.
  - Observations conducted 10:00–16:00 under suitable weather (temperature > 12°C, wind < 6–8 m/s).
  - Species-level identifications where possible; other visitors identified to family or superfamily as needed.
- Local plant diversity
  - In-field margins and cropped areas surveyed with quadrats (five 1 m² within 20 m of transect start; margins assessed for edge length, hedge proportion, margin width; in-crop diversity recorded per sampling point).
- Landscape metrics
  - Calculated from multiple spatial datasets and field observations within buffers from 0.5–3 km (with 0.5 km increments), including grassland types, semi-natural habitats, oilseed rape area, arable area, and habitat richness indicators.
- Data handling
  - Protocols for field and lab data collection established; data entered into MS Access with QA checks and anomaly detection.
  - Ethics approval obtained: CLES Penryn Research Ethics Committee (2014/622).

## Data Structure and Linkage
- Consistent linking keys across files:
  - FarmID, FieldID, TransectID, PointCode link datasets.
  - SpeciesCode in NERCPanTrapData.csv, NERCPTrans.csv, and NERCPollinatorSpeciesList.csv enables cross-dataset connections.
- Metadata and taxonomic detail
  - NERCPollinatorSpeciesList.csv provides taxonomy, taxonomic level, and functional grouping to enable integration with pollinator efficiency data.
  - Noted limitations in taxonomic resolution for certain groups and gender data limited to Apoidea.

## Data Quality, Documentation, and Ethics
- Quality assurance
  - Standardized field and lab protocols; trained personnel; QA of data entries in MS Access; anomaly checks performed.
- Data limitations
  - Pan traps: some data missing due to traps being knocked over.
  - Taxonomic resolution: some taxa only identified to family/superfamily; gender data limited to Apoidea.
- Ethics
  - Approved by the University of Exeter CLES Penryn Ethics Committee (2014/622).

## Intended Use and Governance
- Primary aim: enable discoverability, reuse, and integration of these datasets by data users, while ensuring appropriate data governance and metadata quality.
- Interoperability
  - Datasets are designed to be used with other Wessex BESS WP4 datasets and potentially with a related Pollinator efficiency data set.
- Data sharing and updates
  - The integration of updates and accuracy of metadata is supported through consistent keys and documented protocols; sharing limitations and embargo considerations should be respected.

## Practical Considerations for Data Stewards
- Ensure ongoing data governance by maintaining consistent identifiers (FarmID, FieldID, TransectID, PointCode, SpeciesCode) across future updates.
- Preserve taxonomic and functional grouping information, while documenting any changes in identifications or methods.
- Provide clear documentation on missing data points and their impact on analyses, especially pan trap gaps.
- Maintain linkage between datasets to support multi-dataset analyses (pollinator abundance, plant diversity, and landscape context).
- Facilitate integration with related WP4 datasets and any downstream pollinator efficiency datasets.