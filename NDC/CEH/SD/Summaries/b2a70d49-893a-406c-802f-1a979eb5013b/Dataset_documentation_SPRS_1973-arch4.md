# Scottish Pinewood regeneration survey, 1973 Dataset Summary

## Overview
- A follow-up regeneration survey of 7 woods from the Scottish Pinewood Survey 1971.
- 419 × 200 m2 plots surveyed across the selected woods; more plots per wood than in 1971.
- Data collected include detailed information on trees, ground flora, habitat types, and regeneration using standardized procedures.

## Data scope and content
- Geographic/time coverage: 7 pinewoods in Scotland; approximate survey start dates in 1973 (July–September).
- Data categories:
  - Habitat data: habitat types, slope, aspect; some site-wide attributes.
  - Vegetation data: vegetation presence and cover using a nested quadrat system; trees, saplings, shrubs; vascular plants; bryophytes (Abernethy only).
  - Regeneration data: heights and counts of regenerating seedlings; ground flora with >5% cover; soil attributes; regeneration-specific sampling.
  - Soil data: soil pH from the top 10 cm for seedling and non-seedling plots.
- Site information: seven woods with plot-level data and coordinates (OSGR references) including Mar, Abernethy, Barisdale, Glen Affric, Shieldaig, Loch Maree, and Tyndrum.

## Methods and sampling design
- Design: follow-up to the 1971 survey; 7 woods selected from 27 based on grouping (Eastern, South Western, Central, North Western, etc.). 419 plots in total.
- Survey methods: Bunce & Shaw (1973) standardized procedures; field handbook provides classifications and definitions.
- Habitat data collection: predefined habitat categories; plot slope and aspect measured with clinometer and compass.
- Vegetation data collection: nested quadrats within each 200 m2 plot; trees/saplings/shrubs counted with DBH and height; percent cover for vascular plants; bryophytes recorded where applicable.
- Regeneration data collection: first 20 seedlings per species (up to 1.3 m) marked; regeneration quadrats used to record seedling height, ground flora, and soil attributes; soil samples taken from top 10 cm for each seedling type and non-regenerating plots.

## Data files and structure
- SPRS_1973_PLOT_SITE_DESCS.csv
  - Plot and site descriptions; site number, site name, start date, plot numbers, codes, and sheet references.
- SPRS_1973_PLOTS.csv
  - Plot-level descriptors: site, plot number, survey date; plot slope and aspect; soil pH values for non-regenerating and regenerating seedling plots by seedling type.
- SPRS_1973_GROUND_FLORA.csv
  - Ground flora data: site/plot, nest (sub-plot) within plot; species code, scientific name, common name, growth form, total cover; seedling counts where applicable.
- SPRS_1973_TREE_DATA.csv
  - Trees, saplings and shrubs: site/plot/nest; tree number and category (tree, sapling, shrub); species; DBH; dead indicator; height of widest tree.
- SPRS_1973_REGEN.csv
  - Scots Pine regeneration data: site/plot/sheet; nest; regeneration type (species or none); measurements for regenerating seedlings (heights, seedling height); ground flora and soil descriptors; categorical and numeric fields.

## Sites and sampling details
- Woods involved: Mar, Abernethy, Barisdale, Glen Affric, Shieldaig, Loch Maree, Tyndrum.
- Site coordinates (OSGR) and site descriptions were recorded; approximate start dates for each site are provided in the dataset summary.
- Data collection adhered to standardized field methods (Bunce & Shaw, 1971; Bunce & Shaw, 1973).

## Related work and references
- Bunce R.G.H. & Shaw M.W. (1971). National Woodland Classification 1971: Handbook of Field Methods.
- Bunce R.G.H. & Shaw M.W. (1973). A Standardized Procedure for Ecological Survey. Journal of Environmental Management.
- Shaw, M. W. & Bunce, R. G. H. (1971). National Woodlands Classification 1971 Handbook of Field Methods.
- Stace, C. (1997). New flora of the British Isles.
- The dataset is a follow-up to the Scottish Pinewood Survey 1971; related 1971 dataset is available via the NERC Environmental Information Data Centre DOI listed in the documentation.

## Access, provenance and acknowledgements
- Origin: Follow-up to the 1971 Scottish Pinewood Survey; data collected using Bunce & Shaw’s standardized survey methods (1973).
- Related dataset: Scottish Pinewood Survey 1971 data (with a provided DOI link in the documentation).
- Acknowledgements: project management, laboratory assistance, field surveyors, data management and documentation teams.