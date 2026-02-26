# Bryophytes in an Urban Environment, a case study from Edinburgh

- Overview
  - Dataset from the Botanical Society of Scotland's Urban Flora Project (UFP), initiated in 2015.
  - Documents distribution of bryophytes (mosses, liverworts, hornworts) in the City of Edinburgh.
  - Records species presence/absence and habitat per monad; some data predates UFP.
  - Purpose: understand factors underlying species distribution and species richness in the urban environment.

- Spatial Coverage
  - 138 monads (1x1 km squares) defined by the Ordnance Survey National Grid.
  - Area mostly within the A720 Edinburgh ring road; extends southwest along the Water of Leith to Currie and Balerno; north to Cramond Island; east to Joppa.

- Experimental Design / Data Collection
  - Routes chosen to maximize ecological diversity in public spaces and waste ground; steep ground excluded; few private gardens surveyed.
  - Each monad surveyed at least once; repeat visits to species-rich monads.
  - 272 bryophyte species recorded across 138 monads.
  - Some older data included for precipitous locations on unstable crags/steep ground.
  - Species nomenclature aligned with the UK Species Inventory.

- Data Files and Structure
  - Species_by_monad.csv: records presence (1) or absence (0) of species in each monad; includes Latin species name, short abbreviation, and OS grid reference for each monad.
  - Species_location_habitat_date.csv: expanded dataset with species name, taxon_group (Moss/Liverwort/Hornwort), site name, original OS grid reference (4–8 figure), 4_figure_Grid_Ref (1x1 km), latitude, longitude, habitat code, secondary habitat description, and date recorded.
  - Habitat codes (Table 3): coded habitat taxonomy with broad categories and numerous subcategories (e.g., agricultural, building/walls, crags, derelict/waste ground, gardens/parks, heath/moor, inland water, coastal/marine, roads/paths, woodland/hedgerow).
  - Data quality: all recorders were experienced bryologists; species identity confirmation sought as needed; locations checked by map.

- Data Quality and Provenance
  - Provenance tied to a bryophyte-focused urban ecological study; data quality control protocols described.
  - Some data referenced in a scholarly article: Bryophytes in an Urban Environment, a case study from Edinburgh (Plant Ecology and Diversity); full reference pending publication.

- Use and Reuse Considerations
  - Structured, georeferenced presence/absence data across a urban gradient, suitable for analyses of species distributions and richness relative to habitat types.
  - Metadata-rich, with standardized habitat codes and multiple coordinate representations (OS grid, latitude/longitude) to support integration with other data sources.
  - Taxonomic alignment to UK Species Inventory facilitates cross-study comparisons.
  - Documentation supports reproducibility and potential linkage to other urban flora/fauna datasets and urban planning analyses.

- Related Context
  - The dataset is part of a broader urban biodiversity initiative and contributes to understanding bryophyte distribution in urban environments.
  - The work is cited in related publications and provides a data resource for urban ecological research and data governance practices.