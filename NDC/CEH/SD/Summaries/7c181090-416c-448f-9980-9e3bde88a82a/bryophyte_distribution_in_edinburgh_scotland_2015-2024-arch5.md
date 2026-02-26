# Bryophytes in an Urban Environment, a case study from Edinburgh

## Overview
- Part of the Botanical Society of Scotland's Urban Flora Project (UFP), started in 2015.
- Dataset covers distribution of bryophytes (mosses, liverworts, hornworts) in the City of Edinburgh.
- Records species presence/absence and associated habitat for each urban monad; aims to understand factors underlying species distribution and species richness in an urban environment.
- Some data predates the UFP; data quality is maintained through expert identification and verification.

## Spatial Coverage
- 138 monads (1x1 km squares) defined by the Ordnance Survey National Grid.
- Geographic extent: predominantly within the A720 Edinburgh city ring road, with extensions south-west along the Water of Leith to Currie and Balerno; north to Cramond Island; east to Joppa.

## Experimental Design / Data Collection
- A route through each monad selected to maximize ecological diversity of public spaces and waste ground.
- Avoided overly steep ground; few private gardens surveyed.
- Each monad surveyed at least once; repeat visits to particularly species-rich monads.
- 272 bryophyte species recorded as present or absent across 138 monads.
- Some older data incorporated for precipitous locations on unstable crags and steep ground.
- Species names follow the UK Species Inventory.

## Data Files and Structure
- File (i): Species_by_monad.csv
  - Records species present/absent in each monad.
  - Includes Ordnance Survey grid reference for each monad and species abbreviations.
- File (ii): Species_location_habitat_date.csv
  - Expanded data with site name, original OS grid reference, 4-figure grid reference, latitude, longitude.
  - Taxon_group (Moss, liverwort, or hornwort); habitat code; comment/secondary habitat; date recorded.
- Habitat codes (Table 3) provide detailed subcategories across:
  - Agricultural, buildings, crags, derelict/waste ground, gardens/parks, heath/moor, inland water, marine/coastal, roads/paths, and woodland/hedgerow.
- Data quality control
  - Recorders were highly experienced bryologists; species identifications confirmed with others as needed.
  - Species locations checked against maps.

## Data Quality and Standards
- Taxonomy aligned with UK Species Inventory.
- Location data includes high-precision coordinates (latitude/longitude) derived from original grid references.
- Presence/absence encoded as binary values (1 = present, 0 = absent).

## Provenance and Citation
- Cited in "Bryophytes in an Urban Environment, a case study from Edinburgh" (Plant Ecology and Diversity); full reference pending acceptance.

## Governance, Access, and Stewardship Considerations for Data Stewards
- Metadata and structure support discoverability, interoperability, and reuse (two well-documented CSV files; explicit fields for species, location, habitat, and date).
- Clear documentation of sampling design, quality controls, and taxonomic standardization aids data governance and reproducibility.
- Data predates or predates full UFP integration in parts; clarify update and versioning policy if new data are added.
- Sharing and licensing details are not specified; ensure future data stewardship includes licensing, access rights, and any embargo or reuse restrictions.
- For interoperability, the dataset uses standardized habitat codes and OS grid references; ensure future updates maintain coding schemes and coordinate reference systems.