# Woodlands Survey flora data 1971-2001

## Overview
- National dataset of vascular plants, bryophytes, and lichens from 103 broadleaved woodlands across Britain.
- Fieldwork collected at site level and in detail from 16 random plots (200 m2 each) per site.
- Baseline surveys conducted in 1971; re-surveys at 2000, 2002, and 2003 (referred to as 2001) using identical methods.
- Aims to analyse ecological change and identify principal drivers (e.g., atmospheric deposition of sulfur and nitrogen, climate, canopy change, woodland management).
- Related analyses published in Kirby et al. (2005) and Corney et al. (2004); users should consult these for methods and results.

## Data structure and contents
- Site: numeric code (1–103) identifying each woodland site.
- Plot: numeric code (1–16) identifying plots within each site.
- BRC_number: numeric code for species (Biological Record Centre list).
- BRC_names: scientific species name corresponding to BRC_number.
- Amalgams: numeric codes grouping selected species into cross-specific taxa (intra-plot amalgams due to recording inconsistencies).
- Amalgam_names: scientific names for amalgam groupings.
- NEST: numeric flag indicating if an inner 2x2 m plot nest estimate applies (not always filled).
- COV: numeric percentage cover for the whole plot; note 0.5 = <1% cover; -1 indicates certain bare/blank categories; nulls relate to woody species recorded as counts/DBH.
- YR: year of survey (1971, 2000, 2002, 2003).
- Yr_2: year code (1971 or 2000/2002/2003).
- Bryo: text flag (b = bryophyte, l = lichen).
- Woody: text flag (w = woody species).
- Field_sheet: text indicating the original data recording sheet (e.g., 'Ground flora').

- Data caveat: in the 2000s, bare ground, litter, water, rock, and mud have been amalgamated due to inconsistent recording; there may be multiple entries for the same code within a single plot.

## Survey design and methods
- Stratified sampling across the study area.
- Fieldwork followed Bunce & Shaw (1973) standardized survey methods; a field handbook accompanies the dataset.
- Replication: 103 sites with 16 plots each; same methods applied in 1971 and re-surveys in 2000, 2002, and 2003.

## Temporal scope and drivers
- Longitudinal data enabling change detection from 1971 to 2001.
- Explanatory variables assembled from survey data and external sources to estimate drivers of change (e.g., atmospheric deposition of S and N, climate, changes in canopy structure, woodland management).

## Data quality, standards, and integration notes
- Species data use BRC numeric codes linked to species names (requires mapping for GIS labeling).
- Amalgams reflect recording inconsistencies and prior knowledge about difficulty separating certain taxa; may require careful handling in analyses.
- Year coding (YR, Yr_2) differentiates baseline and later surveys; ensure temporal alignment in GIS analyses.
- Absence of explicit coordinate information; spatial use would rely on site polygons or plot centroids and may require georeferencing or external location data.

## GIS applications and considerations
- Suitable for multi-temporal map products:
  - Plot- and site-level distribution maps for species (via BRC names or amalgams).
  - Change-detection maps showing shifts in cover or presence across 1971 and 2000/2002/2003 surveys.
  - Driver-layer overlays (e.g., deposition and climate data) to explore relationships with vegetation changes.
- Spatial data layering:
  - Create site polygons (103) and plot points (16 per site) with attributes from the data structure.
  - Link BRC codes to taxonomic lists for consistent labeling and querying.
- Data preparation steps:
  - Harmonize year fields (YR/Yr_2) to a single temporal dimension per plot.
  - Resolve amalgams by deciding on species-level vs. grouped taxa representations.
  - Handle missing values, especially NEST and COV, and interpret -1 and 0.5 codes correctly.
  - Map to related datasets (e.g., Countryside Survey) for broader basemaps and cross-dataset analyses.
- Documentation needs:
  - Metadata describing coordinate system or geolocation method for site/plot locations.
  - Clear mapping of BRC numbers to taxonomic names and any taxonomic updates since 1971.

## Related datasets and references
- Countryside Survey (related data resource).
- Steele, R.C. (1968); National survey of woodlands.
- Kirby, K.J. et al. (2005); Measuring Long Term Ecological Change in British woodlands (1981-2001) – methodology and change analysis.
- Corney, P.M. et al. (2004); The effect of landscapescale environmental drivers on woodland vegetation.

## Origin and contact
- Originators (1971): R.G.H. Bunce, M.W. Shaw; Woodland Ecology Section, Nature Conservancy Merlewood.
- 2001–2003 contributors: S. Smart, H. Black, K. Kirby, P. Corney (CEH Lancaster; University of Liverpool; English Nature).
- Data handbook and supporting documentation accompany the dataset.