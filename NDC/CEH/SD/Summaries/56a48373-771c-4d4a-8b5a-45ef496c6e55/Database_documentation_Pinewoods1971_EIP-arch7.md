# Dataset Documentation Scottish Pinewoods Survey 1971 (Native Pinewood Survey)

## Overview
- Detailed ecological survey of native Scots Pine woodlands in Scotland conducted in 1971 (with 1972 follow-up for one additional wood).
- Aimed to define ecological variation and support integrated conservation strategies for remaining native pinewoods.
- Uses standardized field methods and coding systems; data designed for GIS-friendly mapping and analysis.

## Geographic Coverage
- 27 major native pinewoods across Scotland (e.g., Glentanar, Black Wood of Rannoch, Abernethy, Rothiemurchus, Glen Affric, Loch Maree, Shieldaig, etc.).
- Exact site locations provided as OS grid references; some sites include multiple plots within each wood.
- Dulnan (west of Abernethy) surveyed in 1972 as an additional site.

## Datasets and Data Model
- Data organized into five primary CSV tables plus site location data:
  - SCOTS_PINE_1971_Sites.csv: Approximate locations of surveyed woodlands (site IDs, names, OS grid references, easting/northing).
  - SCOTS_PINE_1971_SITE_INFO.csv: Descriptions of each site (wood) and each plot, including plot date, slope, aspect, and data sheet references.
  - SCOTS_PINE_1971_TREE_DATA.csv: Tree-level data per plot (DBH, height, tree type, dead status, etc.) with nested plot/trees identifiers.
  - SCOTS_PINE_1971_GROUND_FLORA.csv: Ground flora and bryophyte data per plot, including percent cover, growth form, and species codes.
  - SCOTS_PINE_1971_SOIL_DATA.csv: Soil horizons, depths, pH, litter/organic layers, and related descriptors per plot.
- Data supports GIS-ready joins by site (wood), plot, and species/habitat attributes.

## Survey Design and Methods
- Sample: 27 major native pinewoods; 16 randomly assigned 200 m2 plots per wood (site 4 Abernethy included up to 50 additional plots; 1972 added Dulnan).
- Nested quadrat approach within each 200 m2 plot:
  - Trees, saplings, shrubs recorded across the plot.
  - Vascular plants recorded with nested quadrats: 4 m2, 25 m2, 50 m2, 100 m2, 200 m2; new species enumerated as quadrat size increases.
  - Bryophytes collected for identification and plotted lists.
- Measurements and classifications:
  - Vegetation: DBH, height, species, cover, and growth form.
  - Soil: horizon descriptions, depths, and top 0-15 cm pH (center pit + auger samples for lower horizons).
  - Habitat: predefined classes for habitat types, slope, aspect; additional site descriptions.
- Documentation and standards:
  - Field methods from Bunce & Shaw (1973); National Woodland Classification 1971: Handbook of Field Methods (Shaw & Bunce, 1971).
  - Vegetation nomenclature aligned with Stace (1997) where applicable.
  - Species coding and data sheets defined in accompanying field sheets.

## Data Tables and Schemas (Key Content)
- Sites: site_no, name, OSGR, approximate location.
- Site Info: per-plot data including plot_date, plot_slope, plot_aspect, data_sheet, code groups, habitat classifications.
- Tree Data: site_no, plot_no, tree_no, nest, tree_type, species, DBH, dead status, tree height.
- Ground Flora: site_no, plot_no, nest, cover%, bryophyte/vascular species, growth_form, common/scientific names.
- Soil Data: site_no, plot_no, horizon depths, horizon descriptions, pH, litter/organic/mixed/under_depth ranges, weathering notes, data_sheet.

## Availability and Access
- Datasets provide site-level and plot-level granularity suitable for map-based visualisations and spatial analyses.
- Geographic coordinates primarily provided in OSGB36 (BNG) with easting/northing values for GIS import.

## Applications for GIS Specialists
- Create choropleth or symbol-based maps of habitat types, vegetation structure, and soil characteristics across pinewoods.
- Join data across tables by site_no and plot_no to build multi-layer GIS datasets (e.g., vegetation cover by plot, soil horizons, and tree composition).
- Assess spatial patterns of biodiversity (vascular plants, bryophytes) and soil properties at 200 m2 resolution within extensive woodland complexes.
- Integrate with other datasets (e.g., National Woodland Classification 1971 methods) for comparative spatial analyses and conservation planning.

## References
- Shaw, M. W. & Bunce, R. G. H. (1971) National Woodlands Classification 1971 Handbook of Field Methods.
- Bunce R.G.H. & Shaw M.W. (1973) A Standardized Procedure for Ecological Survey.
- Steven, H. M. & Carlisle, A. (1959) The native pinewoods of Scotland.
- Stace, C. (1997) New flora of the British Isles.

## Acknowledgements
- Survey management, data management, field surveyors, and supporting staff acknowledged for their contributions.