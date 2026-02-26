# About the UK Butterfly Monitoring Scheme

## Overview
- A national butterfly monitoring program organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology (CEH), the British Trust for Ornithology, and the Joint Nature Conservation Committee.
- Relies on volunteers to collect annual population data to understand biodiversity status and trends in the UK since 1976.
- Large spatial coverage with over 3,000 active sites annually; data from all sampling methods are analyzed together.
- Data support policy questions and biodiversity assessments.

## Nature of data collected and sampling framework
- Three main components:
  - Standard butterfly transects (Pollard walks): fixed routes (2–4 km), 5 m wide belt, weekly counts (up to 26 per year), site-selected by recorders; 45 minutes to 2 hours per walk.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel 1-km transects, 2–3 visits per year.
  - Targeted surveys: single-species transects or alternative methods (timed counts, egg/larval web counts).
- Sampling includes both high-frequency, site-level transects and broader-scale 1 km square surveys, enabling multi-resolution coverage (site-level and landscape-scale).

## Nature of data and trend analysis
- Outputs are abundance indices (relative measures) rather than absolute population counts.
- Indices reflect a constant proportion of butterflies present, with species-dependent detectability.
- Overall species indices are produced with the Generalised Abundance Index (GAI) method (2016), weighted by the proportion of the flight period surveyed at each site/year.
- The season’s counts across all methods inform the seasonal pattern and extrapolate gaps in data, giving more weight to observed data over extrapolated data.

## Quality control
- Field data recorded on standard forms and entered online or via Transect Walker.
- Automated checks flag unusual values and records outside flight periods; regional transect coordinators validate data.
- Additional automated and manual validation checks screen for out-of-range distributions, unusual timings, first-time site records, and extreme values.
- Data corrections are implemented through queries and coordination with recorders/coordinators as needed.

## Details of this data download (format and schema)
- Provides long- and short-term trends for species with sufficient data; available as a CSV (.csv) file.
- Time span: long-term trends from 1976 to 2023 (start year may vary by species due to data availability).
- Key columns include:
  - COMMON_NAME, SCI_NAME
  - NYEARS (years in series)
  - F_LIN_B, F_LIN_SE, F_LIN_P, F_TRENDDETAIL, F_FULL_R
  - T20_LIN_B, T20_LIN_SE, T20_LIN_P, T20_TRENDDETAIL, T20_20_R
  - T10_LIN_B, T10_LIN_SE, T10_LIN_P, T10_TRENDDETAIL, T10_10_R
- Trend descriptions classify direction and significance (rapid decline/increase or stable) based on p-values.
- Data fields follow standard taxonomic references for common and scientific names and use established checklists for consistency.

## Licence and attribution
- Data are provided under the Open Government Licence (OGL), enabling free use and reuse with few conditions.
- Attribution must include the citation details and DOI as specified in the metadata.
- Required attribution statement: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, and JNCC.

## Collaboration and contact details
- UKBMS partners offer guidance on dataset details and interpretation of outputs.
- Opportunities for co-authorship and intellectual input in publications, conferences, or posters resulting from UKBMS data.
- Contact:
  - UK Centre for Ecology & Hydrology: Marc Botham, ukbms@ceh.ac.uk
  - Butterfly Conservation: Transect co-ordinator, transect@butterfly-conservation.org

## GIS considerations and how to use this data
- Spatially explicit: data cover fixed transects and 1 km squares, suitable for map-based analyses of spatial and temporal trends.
- Enables mapping of species-specific trends across the UK, integrating with habitat, land-use, and climate layers.
- Data can be joined to site polygons or square grids, supporting policy briefing, conservation planning, and public-facing visualizations.
- Important to note that indices are relative, not absolute, and detection probabilities vary by species; account for these when interpreting maps and trends.