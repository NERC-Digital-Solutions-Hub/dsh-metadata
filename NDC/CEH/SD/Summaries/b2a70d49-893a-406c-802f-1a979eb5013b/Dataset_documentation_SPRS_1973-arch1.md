# Scottish Pinewood regeneration survey, 1973 Dataset Summary

## Overview
- Follow-up survey to the Scottish Pinewood Survey 1971 assessing regeneration in seven woods.
- 419 x 200 m² plots surveyed across the selected woods.
- Collected data on trees, ground flora, habitat types, regeneration, and soil characteristics using standardized procedures.
- Aimed at understanding regeneration patterns and their relationship to habitat and soil variables.

## Geography and Time
- Geographic coverage: Scotland.
- Sites: Mar, Abernethy, Barisdale, Glen Affric, Shieldaig, Loch Maree, Tyndrum.
- Time period: Fieldwork conducted in 1973 (start dates ranging from July to September 1973); references to methods from the 1971 survey and Bunce & Shaw field protocols.

## Data Categories
- Habitat data: habitat types, slope, aspect; site-level attributes.
- Vegetation data: 
  - Trees, saplings & shrubs (DBH, height, dead indicators, coppice grouping).
  - Vascular plants (species, cover, growth form, codes).
  - Bryophytes (Abernethy site only).
- Regeneration data: heights and counts of regenerating seedlings, ground flora with >5% cover, soil attributes; regeneration quadrats and sampling details.
- Soil data: soil pH measured from top 10 cm in various quadrats (seedling vs non-regeneration plots) and per species.

## Survey Design and Methods
- Sample design: 7 woods selected from the 27 pinewoods in the 1971 survey; 419 plots total; plots 200 m² each.
- Plot layout: nested quadrat system for vegetation; trees recorded throughout the plot; saplings/shrubs recorded in opposing quarters unless >1.3 m tall.
- Regeneration sampling: first 20 seedlings per species marked near plot centre; circular 25 cm diameter quadrats placed over the first five specimens of each species; additional non-seedling quadrats used if fewer seedlings present.
- Measurements included: height of tallest vegetative shoot, seedling height, ground flora species with >5% cover, ground/soil descriptive classes, and soil attributes.
- Habitat and soil data: slope and aspect measured with clinometer and compass; soil pH analyzed from sampled plots.

## Data Files and Key Variables
- SPRS_1973_PLOT_SITE_DESCS.csv
  - Site/plot identifiers, start dates, descriptions, coding groups, sheet references.
- SPRS_1973_PLOTS.csv
  - Site, plot, slope, aspect, and soil pH data (pH values for non-regeneration plots and for plots with different regenerating species: birch, rowan, pine, salix).
- SPRS_1973_GROUND_FLORA.csv
  - Vascular plant species data by plot (species code, common name, growth form), total cover, seedling counts, and presence of bryophytes at Abernethy.
- SPRS_1973_TREE_DATA.csv
  - Trees, saplings, and shrubs: DBH, height, tree category (tree/sapling/shrub), species code, dead indicator, and tree numbering within plots.
- SPRS_1973_REGEN.csv
  - Scots Pine regeneration records by plot: regeneration type, species code/description, seedling height data, and related ground/soil descriptors.

## Data Quality, Access and Documentation
- The dataset provides a comprehensive, standardized set of variables for cross-plot comparisons and regeneration analyses.
- Bryophyte data are site-specific (Abernethy only); regeneration and soil data include detailed quadrat-level measurements.
- Ties to the 1971 Scottish Pinewood Survey methods; data management and field handbook referenced for reproducibility.
- Related dataset: Scottish Pinewood Survey 1971 (habitat, vegetation, tree, soil data) with a DOI link via the NERC Environmental Information Data Centre.

## References
- Shaw, M. W. & Bunce, R. G. H. (1971). National Woodlands Classification 1971: Handbook of Field Methods.
- Stace, C. (1997). New flora of the British Isles.
- Steven, H. M. & Carlisle, A. (1959). The native pinewoods of Scotland.
- Bunce, R.G.H. & Shaw, M.W. (1973). A Standardized Procedure for Ecological Survey.
- Bunce, R.G.H. (Merlewood) and collaborators’ field manuals and methods cited throughout.

## Acknowledgements
- Survey management: R. Bunce
- Laboratory assistance: C. Barr
- Field surveyors: Aberdeen University postgraduate students
- Data management and documentation: C. Wood, B. Dodd, C. Hallam

## Potential Uses for Analysts
- Examine regeneration patterns across habitat types, slopes, aspects, and soil pH gradients.
- Compare 1973 regeneration with 1971 baseline to assess changes over time.
- Model relationships between adult vegetation (trees/saplings) and regeneration success.
- Cross-plot analyses leveraging the nested vegetation data (trees, ground flora, bryophytes) and regeneration metrics.
- Identify data gaps (e.g., bryophytes limited to Abernethy) and plan targeted data collection or harmonization for broader site coverage.