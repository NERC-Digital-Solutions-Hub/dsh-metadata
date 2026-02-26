# Bryophytes in an Urban Environment, a case study from Edinburgh

- Scope and purpose
  - Dataset from the Botanical Society of Scotland's Urban Flora Project (UFP) initiated in 2015.
  - Documents distribution of bryophytes (mosses, liverworts, hornworts) in the City of Edinburgh.
  - Records species presence/absence and habitat associations to understand factors driving urban species distribution and richness.
  - Includes some data predating the UFP.

- Spatial coverage
  - 138 monads (1 x 1 km squares) defined by the Ordnance Survey National Grid.
  - Geographic span: mostly inside the A720 Edinburgh city ring road; extends SW along the Water of Leith to Currie and Balerno; north to Cramond Island; east to Joppa.

- Experimental design and data collection
  - A route through each monad selected to maximize ecological diversity in public spaces and waste ground.
  - Excluded steep ground; only a few private gardens surveyed.
  - Each monad surveyed at least once; repeat visits to particularly species-rich monads.
  - 272 bryophyte species recorded as present/absent across 138 monads.
  - Some older data included for precipitous locations on unstable crags/steep ground.
  - Species names follow the UK Species Inventory taxonomy.

- Data files and structure
  - Species_by_monad.csv: species presence (1) or absence (0) in each monad; includes Ordnance Survey grid references for each monad.
  - Species_location_habitat_date.csv: expanded dataset with location and habitat details.
  - Habitat codes (Table 3) used to classify habitats; codes expanded in accompanying tables.
  - Key fields (from Table 2 and Table 3)
    - Species_name (Latin name)
    - Taxon_group (Moss, liverwort, hornwort)
    - Site_name (location description)
    - Original_OS_grid_reference and 4_figure_Grid_Ref (resolution from 1 x 1 km to finer)
    - Latitude and Longitude
    - Habitat (coded)
    - Comment / secondary habitat
    - Date_recorded (DD/MM/YYYY)

- Habitat coding
  - Broad categories with subcategories, including:
    - agricultural, building and walls, crags and quarries, derelict and waste ground, gardens/parks/grounds, heath/moor/grassland, inland water and wetlands, marine and coastal, roads/paths/pavement, woodland/scrub/hedgerow
  - Each category contains subcategories (e.g., grassland types, wall types, quarry types, etc.).

- Quality control and data provenance
  - All recorders were experienced bryologists; confirmations sought from others when needed.
  - Species locations validated against maps.
  - Data collected to high standards to support reliable presence/absence and habitat associations.

- Temporal and usage notes
  - Some older records included for certain locations.
  - Data intended to illuminate factors influencing urban bryophyte distribution and richness; suitable for correlation analyses and habitat association studies.
  - Cited in a peer-reviewed article: Chamberlain, D.F., and Wilson, J. Bryophytes in an Urban Environment, a case study from Edinburgh (Plant Ecology and Diversity); full reference pending acceptance.

- Accessibility and references
  - Data described via two CSV files with clearly defined fields and metadata.
  - Habitat coding and grid references enable spatial analyses and potential GIS integration.