# Spatial masks for calcareous, coastal, upland and lowland heath habitats [Key Habitats 1992-93] (2017)

- Purpose and scope
  - National habitat-focused data product derived from Countryside Surveys (ITE/CEH) to identify existing and potential areas for four key habitats: calcareous grassland, coastal landscapes, upland landscapes, and lowland heath in England.
  - Enables stratified sampling and location of survey points at 1 km resolution; supports habitat reporting and analysis across a broad range of topics.
  - Supplemented by Countryside Survey 1990 data for some lowland reporting; masks define populations for selecting 1 km sampling sites.

- Geographic and temporal coverage
  - England, 1992–1993 (with supplementary data from 1990 for lowland contexts).

- Data design and methodology
  - Vector dataset consisting of 1 km grid squares; each square can be annotated with one or more habitat masks.
  - Masks were GIS-based products combining multiple data layers and transformation steps.
  - Masks were validated against other information sources; overall fit deemed acceptable, with some mismatches acknowledged.

- Mask definitions and criteria
  - Calcareous grassland mask
    - Based on 1 km squares containing existing or potential calcareous grassland.
    - Derived by integrating geology and drift deposits; focused on areas suitable for calcareous grassland, including potential future expansion.
    - Excludes areas with more than 75% urban land.
    - Coverage: 26,555 1 km squares.
  - Coastal mask
    - Defined as 500 m inland from the high water mark plus contiguous coastal features (saltmarsh, dunes, coastal bare land).
    - High water mark (HWM) derived from Land Cover Map 1990; coastline delineation used Landsat-based classifications and GIS processing.
    - Final dataset covers 8,870 km squares; after exclusions (urban >75% and predominantly sea), 7,341 squares remain.
  - Lowland heath mask
    - Based on soils and landscape potential for heath; uses Soil Survey and Land Research Centre soil types indicative of heath vegetation.
    - Differentiation from upland heath considered using ITE Land Classification 1990; coastal heathlands reported separately due to methodological constraints.
    - Coverage: 8,538 1 km squares in lowland England.
  - Upland mask
    - Derived from ITE Land Classification 1990, grouping 1 km squares into predominantly upland ( Classes 17–24, 27–32; excluding some zones not present in England).
    - Excludes predominantly urban squares (>75% urban).
    - Coverage: 15,616 1 km squares.

- Dataset structure and fields
  - Format: vector dataset; each 1 km square polygon includes indicators for habitat presence.
  - Columns and descriptions:
    - DOMGEOL, Type = Number; Description = calcareous mask detail (e.g., 2 = Oolitic limestone, 7 = Chalk, 8 = Massive limestone, 0 = Other for Calc = 1).
    - COAST, Type = Number; Description = coastal mask indicator.
    - CALC, Type = Number; Description = calcareous mask indicator.
    - LOHEATH, Type = Number; Description = lowland heath mask indicator.
    - UPHEATH, Type = Number; Description = upland mask indicator.
    - STRATA, Type = Text; Description = coastal mask subtype (H = hard coast, S = soft coast, E = estuarine).
  - Note: Masks can overlap; coastal heathlands are reported separately in related work.

- Provenance and validation
  - Masks built from established datasets and classifications:
    - Geology and drift data (for calcareous mask).
    - Land Cover Map 1990 (for coastal delineation and HWM approximation).
    - ITE Land Classification 1990 (for upland vs. lowland delimitation).
    - Soil data (for lowland heath potential).
  - Validation involved comparisons with additional information; overall fit considered acceptable for project purposes, with acknowledged mismatches.

- Uses and implications
  - Supports targeted habitat mapping, landscape-scale analyses, and planning for habitat restoration or conservation.
  - Facilitates objective, reproducible selection of 1 km sampling units and templates for self-serve exploration of habitat masks.
  - Useful for policy work, environmental reporting, and integration with related datasets (e.g., Countryside Survey outputs).

- Related publications and access
  - Barr, C.J.; Bunce, R.G.H.; Cummins, R.P.; Hallam, C.J.; Hornung, M.; Wood, C.M. (2017). Habitat and vegetation data from an ecological survey of terrestrial key habitats in England, 1992-1993. NERC Environmental Information Data Centre. DOI: 10.5285/7aefe6aa-0760-4b6d-9473-fad8b960abd4
  - Supporting field handbooks and reports (1990–1997) detailing methodology and applications.
  - Data management: Institute of Terrestrial Ecology / Centre for Ecology & Hydrology; publicly referenced via NERC Environmental Information Data Centre.