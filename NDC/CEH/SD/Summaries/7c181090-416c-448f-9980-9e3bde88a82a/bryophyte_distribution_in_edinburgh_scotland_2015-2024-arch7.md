# Bryophytes in an Urban Environment, a case study from Edinburgh

- This dataset, part of the Botanical Society of Scotland's Urban Flora Project (UFP) initiated in 2015, records the distribution of bryophytes (mosses, liverworts, and hornworts) in the City of Edinburgh. It includes presence/absence and habitat information for each species, with some data predating the UFP. The survey aims to understand factors influencing species distribution and richness in an urban setting.

## Spatial coverage and sampling design

- Spatial unit: 138 monads, each 1x1 km, defined by the Ordnance Survey National Grid.
- Study area: Mostly within the A720 Edinburgh city ring road; extends southwest to Water of Leith/Currie and Balerno, north to Cramond Island, and east to Joppa.
- Survey approach: Selected routes within each monad to maximise ecological diversity of public spaces and waste ground; steep ground largely excluded; only a few private gardens surveyed.
- Coverage: All 138 monads surveyed at least once; repeat visits to monads with high species richness.
- Data scope: 272 bryophyte species recorded as present/absent across the 138 monads.
- Temporal note: Some older data included for precipitous locations on unstable crags and steep ground.
- Taxonomy: Species names follow the UK Species Inventory.

## Data collection and data structure

- Data collection goal: Gather data to analyse factors underlying bryophyte distribution and species richness in urban environments.
- Quality control: Experienced bryologists conducted surveys; species identities confirmed with colleagues when needed; species locations checked against maps.

## Files and data structure

- File 1: Species_by_monad.csv
  - Purpose: Records species present or absent in each monad.
  - Key fields (example): Species_name (Latin name), Ordnance_survey_grid_reference (grid reference for the monad), presence/absence indicator (1/0).
  - Monadic coverage: Each row corresponds to a monad-species combination with a 1 (present) or 0 (absent).

- File 2: Species_location_habitat_date.csv
  - Purpose: Expanded, per-observation data linking species to precise location and habitat context.
  - Key fields (examples): Species_name, Taxon_group (Moss, liverwort, or hornwort), Site_name (location identifiers), Original_OS_grid_reference (4–8 figure OS grid), 4_figure_Grid_Ref (1x1 km resolution), Latitude, Longitude, Habitat (coded), Comment/secondary habitat, Date_recorded.

- Habitat coding (Table 3): Detailed codes for Habitat with subcategories to describe the land-use/ground-type context, including:
  - Agricultural, building and walls, crags and quarries, derelict and waste ground, gardens/parks/grounds, heath/moor/grassland, inland water and wetlands, marine/coastal, roads/paths/pavement, woodland/scrub/hedgerow, with extensive subcategories (e.g., A-C, B-Oth roofs, G-Pr private gardens, WA-L lakes/ponds, R-F footpath/cyclepath, WO-C conifer woodland, etc.).

- Miscellaneous: The dataset is cited in a publication "Bryophytes in an Urban Environment, a case study from Edinburgh" (Plant Ecology and Diversity); full reference pending acceptance.

## GIS-ready details and considerations

- Spatial resolution: 1x1 km monads (OS grid), with precise observations also available at finer OS grid references (4-figure to 8-figure) and converted latitude/longitude coordinates.
- Data integration: Can be joined to other spatial layers (e.g., land use, gardens, public spaces, green infrastructure) via monad grid references or precise site coordinates.
- Applications:
  - Map species distribution and calculate monad-level species richness.
  - Analyze associations between bryophyte presence and habitat types or site characteristics.
  - Examine spatial patterns of urban bryophyte diversity in relation to urban features (parks, waste ground, gardens, watercourses).
  - Combine with temporal data (Date_recorded) for historical change analyses if multiple surveys exist.
- Data preparation tips:
  - Use 1x1 km OS grid references for aggregation; utilize 4-figure grid refs for finer localization within monads.
  - Convert Original_OS_grid_reference to consistent coordinates or rely on provided Latitude/Longitude for mapping.
  - Normalize habitat codes using Table 3 to ensure consistent categorization across analyses.
  - Verify presence/absence data alignment between Species_by_monad.csv and Species_location_habitat_date.csv when linking datasets.

## Data quality, provenance, and limitations

- Provenance: Collected by highly experienced bryologists; identities confirmed through collaboration; locations cross-checked on maps.
- Data scope limitations:
  - Coverage focused on accessible urban/public spaces; some private gardens and steeper areas were under-sampled.
  - Data quality and resolution vary, with older data included for challenging terrain.
  - Some data gaps may exist due to accessibility or survey intensity across monads.
- Considerations for use:
  - Acknowledge potential sampling bias toward more accessible or ecologically diverse urban spaces.
  - When combining with other datasets, ensure consistent spatial resolution and habitat coding to avoid misinterpretation.

## Summary of relevance for GIS specialists

- Provides a robust, GIS-ready dataset of urban bryophyte distribution and habitat context across 138 1x1 km units in Edinburgh.
- Enables spatial analysis of species distribution, richness, and habitat associations in an urban environment.
- Supports integration with other GIS layers (green space networks, land-use categories, and environmental variables) to explore drivers of urban bryophyte patterns.
- Includes detailed metadata on data collection, quality control, and habitat coding to facilitate rigorous spatial analyses and reproducibility.