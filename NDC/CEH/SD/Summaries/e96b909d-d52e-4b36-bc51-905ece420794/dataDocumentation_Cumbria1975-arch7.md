# Terrestrial habitat, vegetation and soil data from Cumbria, 1975 Ecological Survey of Cumbria 1975. Dataset Summary

## Overview
- A 1975 survey of terrestrial habitats, soils, and vegetation across Cumbria, England, to inform land-use and nature conservation planning.
- Large-scale stratified sampling aimed to characterize ecological conditions beyond existing designated sites.
- Field methods followed Bunce & Shaw (1973) with standardized procedures and quality control by trained surveyors.
- Site locations are not disclosed to protect landowner privacy.

## Geographic and Temporal Coverage
- Geographic: Cumbria, England (centered on the Lake District region).
- Time period: 1975.
- Plots: nearly 650 plots originally selected; 642 actually surveyed.
- Plot size: 200 m2 nested quadrats per plot; data collected on vegetation, soils, and habitats within and around plots.
- Privacy note: specific site locations withheld.

## Sampling Design and Field Methods
- Design: stratified sampling of Cumbria’s land area into 16 strata based on geographical features; within each stratum, 3 x 1 km2 areas were randomly selected from about 7,100 km2 of land class data.
- Plot selection: within each land class, 16 random points were used to locate 200 m2 plots; some plots inaccessible or in crops reduced total to 642 surveyed.
- Within-plot surveying: nested quadrats (4 m2, 25 m2, 50 m2, 100 m2, 200 m2) to record vegetation; species presence and percentage cover in bands were recorded; full plot includes vascular plants, bryophytes, and macro-lichens.
- Soil data: surface soil examined in a central pit with auger samples for lower horizons; horizon depths and descriptive categories recorded; top 10 cm sampled for pH.
- Habitat data: habitat types recorded both within the 200 m2 plot and within 50 m of the edge; slope and aspect measured; habitat categories defined with field handbook guidance.
- Physiographic features: recorded within 50 m of plot edge (e.g., orientation, landscape features, land use around plot) and integrated into habitat data where applicable.
- Data provenance: field crews included R. Bunce, R. Smith, M. Booy; all data follow standardized methods and were quality checked by supervisors.

## Datasets and Data Structure (CSV Schemas)
- CUMBRIA_1975_VEG.csv
  - Records vascular plants, bryophytes, and macro-lichens by plot.
  - Key fields: STRATUM, SQUARE, PLOT, NEST, COVER (percent cover; 0.5 indicates presence), CODE, SCIENTIFIC_NAME, COMMON_NAME, GROWTH_FORM, FIELD_SHEET.
- CUMBRIA_1975_SOIL.csv
  - Soil horizon descriptions by plot.
  - Key fields: STRATUM, SQUARE, PLOT, CODE, DESCRIPTION, GROUP, FIELD_SHEET.
- CUMBRIA_1975_PLOTS.csv
  - Plot-level physical measurements.
  - Key fields: STRATUM, SQUARE, PLOT, DATE, SLOPE, ASPECT, PH, LITTER_FROM/TO, ORG_FROM/TO, MIXED_FROM/TO, LEACH_FROM/TO, WEATHER_FROM/TO, UNDER_DEPTH.
- CUMBRIA_1975_HABS.csv
  - Habitat data within plots.
  - Key fields: STRATUM, SQUARE, PLOT, CODE, DESCRIPTION, GROUP, SUBGROUP, FIELD_SHEET.
- CUMBRIA_1975_PHYS.csv
  - Physiographic features within 50 m of plot edge.
  - Key fields: STRATUM, SQUARE, PLOT, CODE, DESCRIPTION, GROUP, FIELD_SHEET.
- Full List of Species Recorded
  - Comprehensive species list with scientific and common names; includes growth forms and multiple entries per species as needed by field sheets.

## Data Quality and Access
- Data collected by fully trained surveyors; field methods documented in field handbook; data were quality-checked by supervisors.
- Some plots inaccessible or in fields led to fewer plots surveyed than originally selected.
- Spatial privacy: precise site locations are not provided to protect landowner privacy.
- Related datasets and publications offer additional context (e.g., Land Classification of Cumbria 1975; Bunce & Shaw 1973 procedures).

## How GIS Specialists Can Use This Dataset
- Map and analyze spatial distribution of habitat types, vegetation communities, and soil horizons across Cumbria from 1975.
- Cross-tabulate vegetation types with soil horizon characteristics, pH, slope, and aspect to explore habitat–soil–topography relationships.
- Integrate with other historical or current GIS layers (e.g., 1975 land classification, SSSI data, and modern soil maps) for change detection and historical ecology studies.
- Create map-based data products at plot level (200 m2 scale) and derive landscape-level patterns using stratified strata as analytical units.
- Use nested-plot vegetation data (4, 25, 50, 100, 200 m2) to study species richness, cover distribution, and detection probabilities at varying sampling intensities.
- Leverage the extensive species list for biodiversity inventories and regional flora/habitat modeling, noting that detailed plot coordinates are withheld.

## Related Publications and References
- Bunce, R.G.H. & Shaw, M.W. (1973). A Standardized Procedure for Ecological Survey. Journal of Environmental Management.
- Bunce, R.G.H., Smith, R.S., Hill, M.O. (2015). Land Classification of Cumbria 1975. NERC Environmental Information Data Centre. DOI: https://doi.org/10.5285/0ac6249c-a6f2-4147-8ae9-50d576e85fc5
- Ecological Survey of Cumbria: Handbook of Field Methods (Unpublished, Cumbria County Planning Department / ITE Merlewood).
- Original purpose: inform the Cumbria Structure Plan and nature conservation policies by providing a baseline of wildlife habitats across the county.

## Key Limitations and Considerations for Users
- 1975 vintage data; ecological baselines reflect historical conditions and methods from that era.
- Plot-level data are detailed but may require careful alignment with contemporary GIS standards and coordinate systems.
- Absence of precise site coordinates; spatial analysis relies on plot-level indexing (STRATUM, SQUARE, PLOT, NEST) rather than exact geolocations.
- Some horizon descriptors and habitat classifications are extensive and coded; users should refer to field handbook for exact definitions and code mappings.