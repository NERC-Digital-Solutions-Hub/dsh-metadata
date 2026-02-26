# Dataset Documentation Scottish Pinewoods Survey 1971 (Native Pinewood Survey)

- Comprehensive ecological survey of Scots Pine woodland habitats across Scotland, focusing on native pinewoods and providing standardized, comparable data for environmental health and conservation analysis.

## Geographic Coverage
- Major native Scots Pine woodlands identified in Scotland; 27 woods included.
- Sites span from Glentanar, Black Wood of Rannoch, Abernethy, Rothiemurchus, and notable Glens (Affric, Cannich, Strathfarrar, Moriston, etc.).
- 26 woods surveyed in 1971; 1 extra wood (Dulnan) surveyed in 1972.
- Precise site locations provided (OS grid references) for site plotting.

## Overview of Datasets
- Scottish Pinewood Survey 1971: Detailed ecological survey of native pinewoods with standardized field methods.
- Vegetation Data: Vascular plants, bryophytes, and trees/saplings/shrubs.
- Soil Data: Horizon depths, horizon descriptions, and soil pH.
- Habitat Data: Habitat categories, slope, and aspect; additional site descriptions.
- Sample Design: 16 randomly assigned 200 m2 plots per wood (except Abernethy, with additional plots up to 50 in some cases).

## Survey Design & Methods
- Time period: 1971–1972 (Dulnan wood added in 1972).
- Field Methods: Bunce & Shaw standardized procedures (field methods handbook; 1971).
- Plot Design: 200 m2 plots, with nested quadrats for vegetation recording:
  - Trees, saplings & shrubs: recorded per individual within plot.
  - Vascular plants: lists recorded in nested quadrats of 4 m2, 25 m2, 50 m2, 100 m2, and 200 m2; new species recorded as quadrat size increases.
  - Bryophytes: collected for identification; species lists compiled.
- Soil Sampling: Central plot pit for horizon examination; auger samples for lower horizons; top 10 cm sampled for pH.
- Habitat Data: Pre-defined categories with multiple classes; slope measured with clinometer; aspect measured with compass.
- Data Coding: Detailed field handbook definitions and codes; standardized data capture on data sheets.

## Data per Site (Summary)
- For each site, data include plot-level and site-level descriptions, with soil, vegetation, and habitat information.
- Original dataset notes indicate: approximate start dates per site, plot counts, and data availability (e.g., site descriptions, plot data, soil data, and vegetation data presence).

## Data Tables and Descriptions (Files Included)
- Scots_Pine_1971_Sites.csv
  - Approximate locations of surveyed Scots Pine woodlands (27 sites).
  - Fields: ID, NAME, OSGR, POINT_X, POINT_Y, etc.
- SCOTS_PINE_1971_SITE_INFO.csv
  - Descriptions of surveyed sites (whole woodland) and plots (individual), including habitat descriptions, animal descriptions, tree descriptions, soil horizon categories, site names, slope, and date of plot surveys.
  - Key fields: SITE_NO, PLOT_NO, PLOT_DATE, PLOT_SLOPE, PLOT_ASPECT, DATA_SHEET, CODE_GROUP, DESCRIPTION.
- SCOTS_PINE_1971_TREE_DATA.csv
  - Tree-level data per plot: species, DBH, height, dead indicators, tree type (tree/sapling/shrub), and plot associations.
  - Key fields: SITE_NO, PLOT_NO, TREE_NO, SPECIES, DBH, TREE_HT, DEAD, NEST.
- SCOTS_PINE_1971_GROUND_FLORA.csv
  - Ground flora records for each plot: vascular plants and bryophytes, cover estimates, and growth forms.
  - Key fields: SITE_NO, PLOT_NO, NEST, COVER, BRC_NUMBER, COMMON_NAME, GROWTH_FORM.
- SCOTS_PINE_1971_SOIL_DATA.csv
  - Soil data per plot: pH, horizon depths and descriptions, litter and organic layers, weathering depth, and data sheet references.
  - Key fields: SITE_NO, PLOT_NO, SOIL_PH, LITTER_FROM/TO, ORGANIC_FROM/TO, HORIZON_DEPTHS, DATA_SHEET.

## Data Content Highlights
- Vegetation Data
  - Trees, saplings & shrubs tracked by individual stems; height, diameter at breast height (DBH), and dead indicators recorded.
  - Vascular plants and bryophytes recorded with % cover and presence across nested quadrats.
- Soil Data
  - Horizon depth descriptions and horizon classifications; pH measured at 0–15 cm.
  - Central pit methodology for horizon development; auger sampling for deeper horizons.
- Habitat Data
  - Pre-defined habitat categories with sub-classes; slope (degrees) and aspect (magnetic bearing) recorded.
  - Additional site-level habitat descriptions and land-use indicators (e.g., human habitats, rock outcrops, open habitats, etc.).

## Temporal Scope
- Primary data collected in 1971 (most woods); 1972 additional data for the Dulnan site.
- Follow-up and related datasets exist within the cited references and subsequent surveys (e.g., National Woodland Survey 1971, follow-ups 2000–2003).

## Data Quality, Standardization, and Access
- Data collected using standardized field methods and coding systems (field handbook and Bunce & Shaw references).
- Outputs are organized into distinct CSVs with clear site/plot associations to enable integration with other environmental datasets.
- Designed to support cross-site comparisons and long-term monitoring of ecological variation and pinewood conservation status.
- Emphasis on enabling reuse and combination with other datasets (as per the monitoring archetype’s aims) and providing underlying data to end-users through structured datasets.

## References
- Shaw, M. W. & Bunce, R. G. H. (1971) National Woodlands Classification 1971: Handbook of Field Methods.
- Stace, C. (1997) New Flora of the British Isles.
- Steven, H. M. & Carlisle, A. (1959) The Native Pinewoods of Scotland.
- Bunce R.G.H. & Shaw M.W. (1973) A Standardized Procedure for Ecological Survey.
- Related publications detailing pinewood ecology and methods.

## Acknowledgements
- Survey management: Bob Bunce, Wally Shaw
- Data management and documentation: Claire Wood, Caroline Hallam, Deirdre Caffrey
- Field surveyors: list of contributors (e.g., C. Eccles, D.J. Taylor, P. Bassett, etc.)