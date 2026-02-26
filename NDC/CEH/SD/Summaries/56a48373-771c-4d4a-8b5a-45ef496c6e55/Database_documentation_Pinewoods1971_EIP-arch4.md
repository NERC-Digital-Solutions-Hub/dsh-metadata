# Dataset Documentation Scottish Pinewoods Survey 1971 (Native Pinewood Survey)

- A detailed ecological survey of Scots Pine woodland habitats in Scotland (1971–1972) to define ecological variation and support an integrated conservation strategy for remaining native pinewoods.
- 27 major native pinewoods identified; in each wood, 16 randomly selected 200 m² plots were surveyed using standardized procedures (Bunce & Shaw 1973; Bunce & Shaw 1971 field methods).
- Data collected cover vegetation (trees/saplings/shrubs; vascular plants; bryophytes), soil (horizon depths, pH), and habitat characteristics (slope, aspect, habitat types).

## Data Structure and Content

- Datasets and data tables
  - Vegetation Data
    - Trees, saplings & shrubs (by individual stems; DBH; height; dead indicators; coppice status)
    - Vascular plants (species lists by nested quadrats; % cover by plot)
    - Bryophytes (sampled and listed per plot)
  - Soil Data
    - Horizon depths and descriptions; soil pH (top 0–15 cm)
  - Habitat Data
    - Habitat categories and classes; slope and aspect; site descriptions
    - Additional descriptive fields per plot and site
- Data tables (CSV)
  - SCOTS_PINE_1971_Sites.csv
  - SCOTS_PINE_1971_SITE_INFO.csv
  - SCOTS_PINE_1971_TREE_DATA.csv
  - SCOTS_PINE_1971_GROUND_FLORA.csv
  - SCOTS_PINE_1971_SOIL_DATA.csv
- Key fields and data model
  - Site and plot identifiers: SITE_NO, PLOT_NO
  - Tree data: TREE_NO, DBH, TREE_HT, TREE_TYPE, SPECIES, DEAD
  - Ground flora: NEST (plot subunit), COVER (%), SPECIES (Scot. names), GROWTH_FORM
  - Soil: SOIL_PH; horizon-related depth fields
  - Habitat: SLOPE (degrees), ASPECT (degrees magnetic); multiple HABITAT categories/classes
- Sampling design details
  - Nested quadrat system within each 200 m² plot
  - Vegetation inventories at multiple quadrat scales (4 m², 25 m², 50 m², 100 m², 200 m²)
  - Only new species recorded as quadrat size increases; percentage cover recorded by class (including 0.5 for presence)
- Field methods and standards
  - Follow Bunce & Shaw (1973) survey methods; 1971 field handbook for precise classifications
  - Standardized codes and data sheets; field staff entries validated against field handbook
- Geographical coverage
  - 27 woods across Scotland (major native pinewoods); list includes Glentanar, Black Wood of Rannoch, Abernethy, Rothiemurchus, Glenmore, Old Wood of Meggernie, Glen Affric, Loch Maree, Shieldaig, Amat, etc.
  - Dulnan wood (surveyed in 1972) located west of Abernethy (4) and north of Glen Feshie (7)
- Time period
  - Primary fieldwork dates in July–August 1971; additional plots at Abernethy in 1972 (up to 50 plots)

## Survey Design and Methods

- Sample design
  - All major native pinewoods identified by Steven & Carlisle (1959) included; the Dulnan added in 1972
  - 16 randomly assigned 200 m² plots per wood
- Vegetation data collection
  - Nested quadrats within plots; trees recorded across the whole plot; saplings/shrubs recorded in opposing quarters
  - Vascular plants recorded by increasing quadrat sizes; presence and percent cover estimated
  - Bryophytes collected for later identification; plots compiled into a species list
- Soil data collection
  - Central pit dug to examine surface layers; auger samples for lower horizons
  - Horizon descriptions standardized; top 10 cm soil sampled for pH
- Habitat data collection
  - Pre-defined habitat categories with detailed classifications
  - Slope measured with clinometer; aspect measured bearing down slope with Silva compass
- Documentation and references
  - Field methods documented in Shaw & Bunce (1971) and Bunce & Shaw (1973)
  - Taxonomic references include Stace (1997) and earlier pinewood work (Steven & Carlisle, 1959)

## Summary of Available Data per Site

- Data availability indicators (Y/N) for each site across data types (site description, plot descriptions, soil, ground flora, tree data, plot data)
- Approximate start dates for each site (e.g., July 1971 across multiple woods)
- Site-specific details include OS grid references (OSGR), site descriptions, and plot data availability
- Note: Abernethy (Site 4) had additional plots added (up to 50)

## Metadata, Standards, and Reuse

- Data standards and provenance
  - Uses Bunce & Shaw 1971/1973 field methods; standardized data collection and coding
  - Taxonomy aligned with Stace (1997)
- Discoverability and structure
  - Data stored as clearly labeled CSV files with explicit field names and documentation
  - Site-level and plot-level metadata included in SITE_INFO files
  - OS grid references enable geographic integration with other Scottish datasets
- Potential for integration and reuse
  - Comparable with other pinewood surveys (e.g., National Woodland Survey 1971; follow-up surveys 2000–2003)
  - Clear data dictionary and coding schemes support cross-dataset analyses and longitudinal comparisons
- Data governance considerations for Data Leaders
  - Well-documented provenance, methods, and data dictionaries support accountability and reproducibility
  - Historical dataset; consider context and potential gaps when integrating with contemporary data
  - Data quality considerations include older survey context, potential missing plots or measurements, and taxonomic updates

## References and Acknowledgements

- References
  - Shaw, M. W. & Bunce, R. G. H. (1971) National Woodlands Classification 1971: Handbook of Field Methods
  - Bunce, R.G.H. & Shaw, M.W. (1973) A Standardized Procedure for Ecological Survey
  - Steven, H. M. & Carlisle, A. (1959) The Native Pinewoods of Scotland
  - Stace, C. (1997) New Flora of the British Isles
- Acknowledgements
  - Survey management: Bob Bunce, Wally Shaw
  - Data management and documentation: Claire Wood, Caroline Hallam, Deirdre Caffrey
  - Field surveyors: listed individuals