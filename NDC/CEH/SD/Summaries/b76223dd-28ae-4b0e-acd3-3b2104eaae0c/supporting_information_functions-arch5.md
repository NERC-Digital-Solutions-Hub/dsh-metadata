# The response of plants, carabid beetles and birds to 30 years of native reforestation in the Scottish Highlands

## Overview
- Examines ecosystem function responses to native reforestation in the central Scottish Highlands, comparing reforestation plots to unforested (grazed and ungrazed) and to mature Caledonian pinewood.
- Data collected from 14 fenced reforestation sites established between 1990 and 2012, with grazing exclusion to assess restoration outcomes.
- Fieldwork conducted in summer 2018 to evaluate aboveground carbon, soil carbon and nitrogen, decomposition, soil invertebrate feeding, tree regeneration, ground-layer vegetation, moss and shrub layers, and seedling dynamics.
- Sites are in Glen Affric and Glen Moriston with heterogeneous tree cover and varied drainage/topography. Mature forest plots included at a subset of sites for comparison.

## Study design and site context
- Hierarchical sampling: 14 reforestation sites plus associated unforested (grazed and ungrazed) areas, and 5 mature forest plots (grazed and ungrazed) at three sites.
- Treatments represented in all combinations except reforestation × grazed (deer grazing pressure prevents this pairing in the landscape).
- Plot layout: 10 × 10 m plots across treatments; plots spaced 30–400 m apart within sites.
- Reforestation plots were selected to represent best-case forest establishment; ungrazed plots matched to grazed/unforested references on topography, aspect, and elevation.
- Site details include year of establishment, planting method, species mix, and whether mature forest was present at each site.

## Data collected and variables (structure)
- Data files and key contents:
  - plot_locations.csv: plot IDs, site IDs, plot type (reforestation ungrazed; unforested grazed; unforested ungrazed; mature forest grazed; mature forest ungrazed), forest and grazing status, year established, grid references.
  - aboveground_carbon.csv: total aboveground tree carbon per plot (kg/m2).
  - topsoil_C_N.csv: topsoil (0–10 cm) carbon and nitrogen (%), bulk density (g/cm3 or g/ha in header), and derived carbon/nitrogen stocks (kg/m2).
  - decomposition_rate.csv: Tea Bag Index-derived decomposition rate constant k for each plot and teabag type.
  - soil_invert_feeding.csv: soil invertebrate feeding activity from bait lamina sticks; per-bait perforation feeding (1/0), proportion fed, and overall eaten indicator.
  - seedling_regeneration.csv: seedling counts by species and height category per plot.
  - shrub_height.csv: mean shrub layer height per plot.
  - moss_height.csv: mean moss layer depth per plot.
- Plot and measurement specifics:
  - Sampling included 10 × 10 m plots across treatments; some mature forest plots included with five grazed/ungrazed pairs.
  - Aboveground carbon: derived from DBH measurements using species- and region-appropriate allometric equations; carbon concentration assumed 49% for broadleaf and 50% for conifers.
  - Topsoil carbon/nitrogen: ISO-based analysis with bulk density and carbon/nitrogen percentages to estimate stocks.
  - Decomposition: Tea Bag Index with six pairs per plot buried at 8 cm depth for about 55–67 days.
  - Soil invertebrate feeding: bait lamina strips deployed in each plot, monitored over 30 days.
  - Seedling regeneration: counts of young trees with DBH < 2.5 cm across height classes.
  - Ground-layer and moss: measurements of shrub layer height and moss depth via multiple quadrats per plot.
- Data collection protocols are adapted from Warner et al. (2021) and include standardized methods for comparability.

## Data structure and documentation
- Data files are provided as CSVs with clearly defined columns and units:
  - plot_locations.csv includes plot-level metadata: site, plot type, forest and grazing status, year, grid reference.
  - aboveground_carbon.csv records plot-level carbon (kg/m2).
  - topsoil_C_N.csv includes bulk density, %C, %N, and derived carbon/nitrogen stocks (kg/m2).
  - decomposition_rate.csv contains k-values for each teabag sample by plot and teabag.
  - soil_invert_feeding.csv contains per-bait perforation feeding data and overall indices.
  - seedling_regeneration.csv lists seedling frequencies by species and height category.
  - shrub_height.csv and moss_height.csv capture mean shrub height and moss depth per plot.
- File-level notes and data dictionaries describe each variable, site associations, plot classifications, and measurement dates.

## Methods and data processing notes
- Allometric equations for biomass conversion are chosen from UK/European sources with high R2 values, and used to convert DBH to aboveground biomass, then to carbon.
- Topsoil carbon and nitrogen stocks derived from measured percentages and bulk density; carbon concentrations applied (49% for broadleaf, 50% for conifers).
- Decomposition uses Tea Bag Index protocol (fast and slow tea bags) with standardized burial duration.
- Soil invertebrate feeding uses bait lamina methodology with a fixed substrate and exposure times.
- Seedling regeneration, ground-layer, and moss data collected via defined plots and height categories, enabling cross-treatment comparisons.
- Data reflect a 2018 snapshot, with historical site establishment dates and planting methods documented.

## Data quality, scope, and limitations
- Sample design robust across treatments, but some limitations:
  - Two sites could not extract soil cores for carbon and nitrogen, reducing soil sample sizes to 12 in those categories.
  - Mature forest data are limited to five plots per two to three sites due to availability of mature forest remnants.
  - Some datasets rely on allometric equations from regional sources; species identification sometimes at genus level (e.g., Betula and Salix) when species-level equations are unavailable.
  - The study reflects a cross-sectional assessment at a single time point (summer 2018) across long-standing restoration sites.
- Documentation includes an appendix listing author roles and experimental design responsibilities, supporting data provenance and accountability.

## Governance, access, and reuse considerations for Data Stewards
- The dataset is composed of multiple interconnected CSV files with consistent ID references (plot, site) to support integrative analyses across ecosystem functions.
- Documentation provides a clear metadata scaffold, including treatment categories, sampling dates, measurement protocols, and units, facilitating discoverability and reuse.
- Versioning: data are tied to the 2018 sampling event; future updates would require consistent metadata and version control to maintain data integrity.
- Potential uses: assessing impacts of deer grazing and reforestation on ecosystem functions (carbon storage, soil nutrients, decomposition, soil fauna, regeneration, and understory structure); cross-variable analyses enabled by unified plot IDs.
- Recommended data governance practices: maintain standardized naming conventions, preserve measurement protocols and equations, ensure transparent data lineage, and provide data citations with all tables, including references to underpinning methods (e.g., Warner et al. 2021; ISO standards).

## Appendix and authors’ roles
- Appendix 1 outlines roles: experimental design (Emily Warner, Andy Hector, Owen Lewis, Nick Brown); fieldwork support (Doug Gilbert, Alan McDonnell); data collection (Emily Warner, Rowan Green).
- This attribution supports data stewardship by clarifying responsibilities for data provenance and methodological decisions.