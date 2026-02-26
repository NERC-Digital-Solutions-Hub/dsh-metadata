# Bunce' Scottish Pinewood Survey 2018-2022

## Overview
- Detailed ecological survey of native Scots Pine woodlands in Scotland.
- 27 woods identified; within each wood, 16 randomly selected 200 m2 plots surveyed between 2018 and 2022.
- Repeats the 1971 baseline survey to enable monitoring and assessment of change over time.
- Standardized procedures and coding systems used for data collection.

## Geographic Coverage
- Scotland (27 native pinewood sites across northern Scotland).
- Site examples include Glentanar, Ballochbuie, Mar Lodge, Abernethy, Rothiemurchus, Glenmore, Black Wood of Rannoch, Shieldaig, Loch Maree, and others.
- Note: The Dulnan area has little Scots pine remaining.

## Survey Design & Methods
- Based on Bunce & Shaw (1973) standardized procedures; field handbook Smart & Wood (2021) provides details.
- Sample design: 16 randomly assigned 200 m2 quadrats per major native pinewood.
- Vegetation data collected in three categories per plot:
  - Trees, saplings & shrubs
  - Vascular plants
  - Bryophytes
- Nested quadrat system for vascular plants (2 m2 to 200 m2) with % cover estimates by size band.
- Soil analyses for pH and loss on ignition (LOI) from topsoil (0–15 cm) per plot.
- Habitat data: classification into predefined habitat categories, plus slope and aspect measurements.
- Site-level and plot-level descriptions capture additional context (e.g., signs of damage, disease, etc.).

## Data Types and Variables
- Vegetation Data
  - Trees, saplings & shrubs (by individual tree; dead indicators; coppice/stem grouping)
  - Vascular plants (species lists; % cover across nested quadrats; growth form)
  - Bryophytes (ground flora bryophyte data)
  - Additional cover/abundance metrics (litter, wood, rock, bare ground, water, bryophytes)
- Soil Data
  - Soil pH (fresh and air-dried), LOI (%)
  - Soil date of sampling
- Habitat Data
  - Habitat types (predefined categories and classes)
  - Slope (degrees) and aspect (bearing)
  - Site-wide notes and plot-specific descriptions
- Data Coding
  - Standard codes and descriptions defined in the field handbook (Smart & Wood, 2021)
  - Species nomenclature follows Stace (1997)

## Data Availability and Structure
- SCOTS_PINE_2022_SITES.csv: Approximate locations of surveyed woodlands (site IDs 1–27) with site names and coordinates.
- SCOTS_PINE_2022_SITE_INFO.csv: Descriptions of surveyed sites and plots, including habitat descriptions, slopes, aspects, and survey dates.
- SCOTS_PINE_2022_TREE_DATA.csv: Tree-level data for each plot (SITE_NO, PLOT_NO, TREE_ID, TREE_TYPE, SPECIES, DBH, DEAD).
- SCOTS_PINE_2022_GROUND_FLORA.csv: Ground flora records per plot (species, growth form, cover, etc.).
- SCOTS_PINE_2022_SOIL_DATA.csv: Plot soil data (PH_FRESH, PH_AIRDRY, LOI_PERCENT, SOIL_DATE).
- Number of plots per site: 16 per wood (site 4 includes ancillary plots up to 50).
- Data span: 2018–2022, with a connection to the 1971 baseline for long-term monitoring.

## Temporal Coverage & Lineage
- Time period: 2018–2022.
- Purpose: provide a repeatable, standardized ecological snapshot to compare with the 1971 baseline and assess changes over time.

## References and Documentation
- Field methodologies and classification schemes: Bunce & Shaw (1973); Smart & Wood (2021) National Woodland Survey Field Handbook; Stace (1997) for plant nomenclature.
- Previous and related surveys: Scotish Pinewood Survey 1971; Bunce National Woodland Survey 1971; related editions and follow-ups.

## GIS and Analytical Considerations
- Rich, multi-resolution data suitable for map-based visualization of spatial patterns across woodlands and plots.
- Enables analysis of changes over time when linked to the 1971 baseline data.
- Requires respect for standardized codes and field Handbook definitions for consistent interpretation of habitat classes, species, and plot-level attributes.
- Potential integration with additional pinewood datasets and environmental layers to contextualize vegetation, soil, and habitat patterns.