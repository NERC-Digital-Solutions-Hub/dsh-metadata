# Dataset Documentation Scottish Pinewoods Survey 1971 (Native Pinewood Survey)

- A detailed ecological survey of Scots pine woodland habitats in Scotland, conducted mainly in 1971 (with 1972 additions), covering 27 major native pinewoods and 16 randomly chosen 200 m2 plots per wood.
- Purpose: define the range of ecological variation in native pinewoods more precisely than earlier work and support the development of an integrated conservation strategy.
- Data emphasis: vegetation (trees, vascular plants, bryophytes), soil horizons and pH, habitat types, slope, and aspect, using standardized field procedures.

## Geographic Coverage
- Scotland, focusing on major native pinewoods (27 sites) across northern Scotland.
- Examples of included woods: Glentanar, Black Wood of Rannoch, Abernethy, Rothiemurchus, Glenmore, Feshie, Mar, Loch Arkaig and Glen Mallie, etc.
- The Dulnan pinewood was surveyed in 1972 (west of Abernethy).

## Overview of Datasets and Data Content
- Vegetation Data: recorded in each 200 m2 plot
  - Trees, saplings & shrubs (by individual trees)
  - Vascular plants (species lists across nested quadrats)
  - Bryophytes (ground bryophytes)
  - Percent cover estimates (by species)
- Soil Data
  - Horizon classification (depths and descriptions)
  - pH measured at top 10 cm
- Habitat Data
  - Habitat categories with multiple classes
  - Slope and aspect measurements
  - Additional site descriptions

## Survey Design and Methods
- Sample Design
  - All major native pinewoods identified in Steven & Carlisle (1959) included; Dulnan added in 1972.
  - 16 randomly assigned 200 m2 plots per wood (1971: 26 woods; 1 extra wood in 1972; Dulnan added in 1972; Abernethy had additional plots up to 50).
- Methods and Standardization
  - Followed Bunce & Shaw (1973) Field Methods; detailed definitions in Shaw & Bunce (1971) National Woodland Classification: Handbook of Field Methods.
  - Vegetation: nested quadrats for vascular plants across increasing quadrat sizes; trees recorded across whole plot; saplings/shrubs recorded in opposing quarters; bryophyte samples collected for identification.
  - Soil: shallow pit and auger samples to classify horizons; top 10 cm sampled for pH.
  - Habitat: predefined categories; slope via clinometer; aspect via bearing toward slope; site-wide descriptions recorded.
- Data Recording
  - Detailed field sheets and data codes; consistent with field handbook guidelines.

## Available Data per Site (Data Tables)
- Scots_Pine_1971_Sites.csv
  - Approximate locations of surveyed Scots Pine woodlands (site IDs 1-27) with names and OS grid coordinates (Easting, Northing).
- SCOTS_PINE_1971_SITE_INFO.csv
  - Descriptions of surveyed sites, plots, habitat and tree data, soil horizons, and data sheet metadata.
  - Includes plot dates, slope, aspect, and data sheet codes.
- SCOTS_PINE_1971_TREE_DATA.csv
  - Tree-level data per plot: DBH (diameter at breast height), height, dead indicators, tree/sapling/shrub classification, etc.
- SCOTS_PINE_1971_GROUND_FLORA.csv
  - Ground flora data per plot: vascular plants and bryophytes; percentage cover per nest; growth form; associated nomenclature and codes.
- SCOTS_PINE_1971_SOIL_DATA.csv
  - Soil data per plot: soil pH, horizon depths, horizon descriptions, litter/organic layers, weathering data, and field sheet references.

## References and Method Documentation
- Shaw, M. W. & Bunce, R. G. H. (1971) National Woodlands Classification 1971: Handbook of Field Methods.
- Bunce R.G.H. & Shaw M.W. (1973) A Standardized Procedure for Ecological Survey.
- Steven, H. M. & Carlisle, A. (1959) The Native Pinewoods of Scotland.
- Stace, C. (1997) New Flora of the British Isles (nomenclature and classification references).

## Acknowledgments
- Survey management: Bob Bunce, Wally Shaw
- Data management and documentation: Claire Wood, Caroline Hallam, Deirdre Caffrey
- Field surveyors: listed personnel for plot and data collection

## Key Notes for Analysts
- Timeframe: primarily 1971, with 1972 additions; comprehensive coverage of 27 major native pinewoods; 16 plots per site (200 m2 each); one site (Abernethy) had extra plots.
- Data linkage: site-level coordinates (OS grid), plot-level metadata (slope, aspect, date), and species-level data for trees, ground flora, and soil horizons.
- Standardization: uses uniform, well-documented field methods and coding schemes, enabling cross-site comparison and potential integration with related datasets (e.g., National Woodland Classification lineage).
- Usability considerations: data delivered as CSV files with explicit field codes and descriptions; includes field sheet references and metadata to support reproducibility and modelling of ecological variation in pinewoods.