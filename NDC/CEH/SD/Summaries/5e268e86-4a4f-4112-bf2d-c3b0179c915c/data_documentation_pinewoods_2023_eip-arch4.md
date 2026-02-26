<Bunce'> Scottish Pinewood Survey 2018-2022 Habitat, vegetation, tree and soil data from Native Pinewoods in Scotland, 2018-2022

## Scope and purpose
- Detailed ecological survey of Scots Pine woodland habitats across Scotland.
- 27 major native pinewoods identified; within each wood, 16 randomly selected 200 m² plots were surveyed between 2018 and 2022.
- Repeats the 1971 baseline to enable environmental monitoring and assessment of change over time.
- Uses standardized procedures and coding systems (Bunce & Shaw 1973; Smart & Wood 2021) to ensure comparability.

## Geographic coverage and sample design
- Geographic scope: Scotland.
- Coverage includes 27 named pinewoods (e.g., Glentanar, Ballochbuie, Abernethy, Rothiemurchus, Shieldaig, Loch Maree, etc.).
- Sampling design: all major native pinewoods identified in 1971 survey were included; 16 randomly assigned 200 m² plots per wood.
- Original purpose: to define ecological variation in pinewoods and support an integrated conservation strategy; enables monitoring of change since 1971.

## Data collection methods and data categories
- Survey methods: follow Bunce & Shaw (1973) with details in the National Woodland Survey Field Handbook (Smart & Wood 2021).
- Vegetation data per plot (three categories): trees/saplings/shrubs; vascular plants; bryophytes (ground flora).
  - Nested quadrats used for vegetation recording; percent cover estimated in bands; multiple quadrat sizes used for vascular plants.
- Soil data: pH and loss on ignition (LOI) from topsoil (0–15 cm) per plot.
- Habitat data: habitat types classified with predefined categories; slope and aspect measured; additional site descriptions recorded.
- Data capture formats: standardized codes and field sheets; documentation includes field handbook details for classifications and parameters.

## Data formats, schemas, and access points
- Data are provided as five CSV files:
  - SCOTS_PINE_2022_SITES.csv — approximate locations of surveyed woodlands (site IDs, names, grid references, OS grid coordinates).
  - SCOTS_PINE_2022_SITE_INFO.csv — descriptions of surveyed sites and plots, including habitat descriptions, animal signs, and tree data; includes site and plot-level fields.
  - SCOTS_PINE_2022_TREE_DATA.csv — tree-level data per plot (site, plot, tree ID, tree type, species, diameter at breast height, dead indicator, etc.).
  - SCOTS_PINE_2022_GROUND_FLORA.csv — ground flora records per plot (vascular plants and bryophytes), with species codes, cover, growth form, and metadata.
  - SCOTS_PINE_2022_SOIL_DATA.csv — soil data per plot (pH in fresh and air-dried samples, LOI, date of soil sample).
- Data use coordinates: OSGB36 (BNG) coordinates for site locations; data are prepared for analysis with accompanying metadata and data dictionaries.
- Related materials: references to baseline datasets (1971, 1973, 2000-2003, 2020-2022) and the National Woodland Survey Field Handbook (2021) for context and method standardization.
- Access/links: published by UK Centre for Ecology & Hydrology (UKCEH); related DOIs and project documentation available in the references section.

## Data governance, quality, and metadata
- Methodology anchored to standardized, historically consistent procedures (Bunce & Shaw 1973; Shaw & Bunce 1971; Smart & Wood 2021).
- Data dictionaries and field handbooks provide codes, groupings, and descriptions to support data quality, interoperability, and reusability.
- Designed for longitudinal comparison with the 1971 baseline and later repeats; metadata describes site, plot, and measurement details (slope, aspect, habitat types, animal signs, etc.).
- Acknowledges field survey teams, soil analysis collaborators, and permissions, highlighting governance and provenance.

## Data assets, lineage, and related resources
- Originators: S.M. Smart, C.M. Wood (UKCEH, Lancaster) with collaborators; field surveyors listed.
- Related datasets and lineage:
  - Scottish Pinewood Survey 1971 (baseline) and subsequent repeats (1973, 2000-2003, 2020-2022).
  - National Woodland Survey & Native Pine Survey Field Handbook (2021).
  - Foundational methodological works: Bunce & Shaw (1973); Stace (1997); Wood & Bunce (2016).
- Dataset structure enables cross-temporal analysis and integration with broader woodland survey datasets.

## Practical takeaway for data leaders
- A well-documented, standardized, longitudinal ecological data asset for native Scottish pinewoods, enabling trend analysis and conservation planning.
- Five CSV data products with explicit site, plot, vegetation, soil, and habitat data; rich metadata, codes, and field handbook governance support discoverability and reuse.
- Strong data lineage to 1971 baseline, with clearly defined methodologies and update cadence (2018–2022); accessible through UKCEH data publications and linked resources.