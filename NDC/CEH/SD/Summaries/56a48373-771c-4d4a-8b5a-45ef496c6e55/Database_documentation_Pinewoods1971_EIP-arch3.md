# Dataset Documentation Scottish Pinewoods Survey 1971 (Native Pinewood Survey)

- Detailed ecological survey of Scots Pine woodland habitats in Scotland
- 27 major native pinewoods identified; 16 randomly selected 200 m² plots per wood
- Data types: vegetation (trees, vascular plants, bryophytes), soil (horizon descriptions, pH), habitat characteristics (slope, aspect, habitat categories)
- Timeframe: 1971 (1972 for Dulnan subset); methods extended to 1971-72
- Purpose: define ecological variation range in pinewoods and support integrated conservation planning

## Geographical Coverage
- 27 woods across Scotland (locations listed by site names and OS grid references)
- Sites include Glentanar, Ballochbuie, Mar, Abernethy, Rothiemurchus, Glenmore, Feshie, Black Wood of Rannoch, and others
- Dulnan surveyed in 1972; notes on western Abernethy site

## Overview of Datasets
- Vegetation Data: Trees, saplings & shrubs; vascular plants; bryophytes
- Soil Data: Horizon depths/descriptions; soil pH
- Habitat Data: Habitat types classified with multiple classes; slope and aspect measurements; site-level habitat descriptions
- Data Tables Provided (CSV):
  - SCOTS_PINE_1971_Sites.csv — approximate locations and site identifiers
  - SCOTS_PINE_1971_SITE_INFO.csv — descriptions of whole woodlands, plots, habitats, and soil horizons
  - SCOTS_PINE_1971_TREE_DATA.csv — tree and DBH data by plot
  - SCOTS_PINE_1971_GROUND_FLORA.csv — vascular plants and bryophytes by plot, with cover and growth form
  - SCOTS_PINE_1971_SOIL_DATA.csv — soil pH and horizon-depth data by plot
- Each dataset uses standardized field codes and references to a field handbook for definitions

## Survey Design & Methods
- Original Purpose: Define ecological variation range to inform conservation strategy for remaining native pinewoods
- Sample Design: All major native pinewoods from Steven & Carlisle (1959); 16 randomly assigned 200 m² plots per wood (site 4 Abernethy had up to 50 plots)
- Survey Methods: Bunce & Shaw (1973) procedures; detailed in the 1971 National Woodlands Classification field handbook (Shaw & Bunce, 1971)
- Vegetation Data Collection:
  - Nested quadrat system within each 200 m² plot
  - Trees recorded throughout plot; saplings/shrubs recorded in opposing quarters
  - Vascular plants recorded by quadrat sizes (4 m², 25 m², 50 m², 100 m², 200 m²) with increasing discovery lists
  - Bryophytes collected for later identification
  - Percentage cover estimated by bands; presence of litter, wood, rock, bare ground, water, bryophytes also recorded
- Soil Data Collection:
  - Horizon classification using standard categories; shallow pit in plot center; auger samples for deeper horizons
  - Top 10 cm soil pH analyzed
- Habitat Data Collection:
  - Habitat categories recorded with multiple class possibilities
  - Slope measured with clinometer; aspect measured bearing down slope with compass
  - Additional site descriptions captured
- Data Documentation: Field sheets, coding schemes, and a field handbook ensure consistency and reproducibility

## Summary of Available Data per Site
- Start dates range July–August 1971 (with Dulnan in 1972)
- Data coverage per site includes: site description, plot descriptions, soil data, ground flora, and tree data (where available)
- Abernethy (Site 4) has additional plots noted
- The per-site summary indicates which data components exist for each wood; overall, comprehensive data across vegetation, soil, and habitat variables are available for many sites

## Data Tables and Descriptions (Field Details)
- Site-level and plot-level descriptors:
  - SITE_NO, PLOT_NO; PLOT_DATE; PLOT_SLOPE; PLOT_ASPECT; DATA_SHEET
  - CODE_GROUP and CODE_GROUP_DESCRIPTION describe classification schemes
- Tree Data:
  - TREE_NO; DBH (diameter at breast height); TREE_HT; DEAD status; NEST (quadrant-specific stem data); TREE_TYPE and SPECIES
- Ground Flora Data:
  - NEST; COVER (%); BRC_NUMBER/BRC_NAME; COMMON_NAME; GROWTH_FORM
- Soil Data:
  - SOIL_PH; horizon depth ranges (LITTER_FROM/TO, ORGANIC_FROM/TO, etc.); WEATHER and UNDER_DEPTH
- Data standards:
  - Uses Stace (1997) nomenclature for vascular plants; standardized growth forms and species coding
- Additional metadata:
  - FLORA_RECORDER initials; DATA_SHEET references field sheets and codes

## Original Purpose and Monitoring Implications
- Provides a robust baseline of ecological variation in native Scottish pinewoods for monitoring and conservation planning
- Standardized methodology enables comparability across woods and over time, supporting policy evaluation and future decisions
- Extensive data dictionaries and field handbooks facilitate data reuse, quality checks, and transparent governance

## Data Quality, Metadata, and Governance Considerations
- Metadata is documented through multiple CSVs and comprehensive field descriptions
- Standardized data collection methods and coding schemes support reproducibility and comparability
- Data management and documentation performed by dedicated staff; clear acknowledgments and references provided
- Potential barriers for monitoring (historical context):
  - Complexity of coding schemes and need for field handbook to interpret
  - Some sites have partial data (not all data types available for every site)
  - Publication-ready data require careful interpretation of codes and units across tables

## References and Acknowledgements
- Shaw, M. W. & Bunce, R. G. H. (1971) National Woodlands Classification 1971 Handbook of Field Methods
- Bunce, R.G.H. & Shaw, M.W. (1973) A Standardized Procedure for Ecological Survey
- Steven, H. M. & Carlisle, A. (1959) The Native Pinewoods of Scotland
- Acknowledgements to survey management, data management, field surveyors, and contributors to the dataset and documentation