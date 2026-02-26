# Scottish Pinewood regeneration survey, 1973 Dataset Summary

## Overview
- A follow-up regeneration survey in seven Scottish native pinewoods from the 1971 Scottish Pinewood Survey.
- Large sampling: 419 plots of 200 m2 across the seven woods.
- Collected data on vegetation (trees, saplings, ground flora, bryophytes in Abernethy), habitat and soil characteristics, and detailed regeneration metrics using standardized procedures.
- Aims to illuminate regeneration patterns by comparing regenerating vs. non-regenerating areas within plots.

## Scope and Coverage
- Geographic area: Scotland.
- Time period: 1973 (following up the 1971 survey).
- Woods/sites included: Mar (Abernethy), Abernethy, Barisdale, Glen Affric, Shieldaig, Loch Maree, Tyndrum.
- Start dates per site range from late July to late August 1973.
- Data categories: Vegetation, Regeneration, Habitat, Soil; with specific subdata for plot/site descriptions and regeneration measurements.

## Data Categories and Key Variables
- Habitat Data
  - Habitat types per plot, plot slope, plot aspect; site-wide attributes for selected sites.
- Vegetation Data
  - Trees, saplings and shrubs (DBH, height, dead indicator, coppice grouping).
  - Vascular plants (species, coverage by nested quadrats; growth forms).
  - Bryophytes (ground flora data; Abernethy only).
- Regeneration Data
  - Seedling measurements: heights, counts, tallest shoot height; regeneration quadrats with seedling and non-seedling sampling surrounding the seedling center.
  - Ground flora and soil attributes within regeneration quadrats.
  - Soil samples from top 10 cm for seedlings and non-seedling quadrats.
- Soil Data
  - Soil pH measurements by seedling type and by plot (with 0 indicating no sample for that category).
- Data Structure
  - Plot/site level metadata and descriptive fields (start date, site name, plot descriptions).
  - Data captured in CSV files for cross-site and cross-plot analyses.

## Methods and Standardization
- Survey design follows Bunce & Shaw (1973) standardized ecological survey procedures; detailed field methods documented in the field handbook (Bunce & Shaw 1971, 1973).
- Plot design: 419 plots of 200 m2 across 7 woodlands; nested quadrat system for vegetation (4 m2, 25 m2, 50 m2, 100 m2, 200 m2) with expanding species lists and % cover estimates.
- Habitat categories and descriptive classes with explicit definitions; slope measured with clinometer; aspect measured bearing down the slope.
- Regeneration methodology:
  - Marking first 20 seedlings per species up to 1.3 m; specific height criteria per species.
  - Central 25 cm diameter circular quadrats to record regeneration parameters for the first five seedlings per species, plus mirrored non-seedling quadrats for comparison.
  - Recorded metrics per quadrat: tallest shoot height, seedling height, ground flora >5% cover, ground/soil descriptive classes, soil attributes.
- Soil sampling: top 10 cm soil collected for pH analysis from seedling and non-seedling quadrats.

## Data Organization and Access
- Data files (CSV) available:
  - SPRS_1973_PLOT_SITE_DESCS.csv: Plot and site descriptions, habitat information, start dates, and sheet references.
  - SPRS_1973_PLOTS.csv: Plot slope, aspect, and pH data by seedling type and plot.
  - SPRS_1973_GROUND_FLORA.csv: Vascular plants and Bryophytes (Abernethy) by plot and nest, with species codes, covers, counts.
  - SPRS_1973_TREE_DATA.csv: Trees, saplings, and shrubs data including DBH and height.
  - SPRS_1973_REGEN.csv: Scots Pine regeneration data by plot and regeneration type, with measurements and soil descriptions.
- Data are linked across files using identifiers such as SITE_NO, PLOT_NO, NEST, and REGEN_TYPE, enabling multi-facet analysis (habitat, vegetation, and regeneration in context).

## Provenance, References, and Acknowledgements
- Originators: R.G.H. Bunce, C.M. Wood, and colleagues (Nature Conservancy Merlewood; Aberdeen University field team).
- Related publications and foundational methodologies:
  - Bunce & Shaw (1971) National Woodland Classification: Handbook of Field Methods.
  - Bunce & Shaw (1973) A Standardized Procedure for Ecological Survey.
  - Steven & Carlisle (1959) The Native Pinewoods of Scotland.
  - Stace (1997) New Flora of the British Isles.
- Acknowledgements include survey management (R. Bunce), lab assistance, field surveyors, and data management personnel.