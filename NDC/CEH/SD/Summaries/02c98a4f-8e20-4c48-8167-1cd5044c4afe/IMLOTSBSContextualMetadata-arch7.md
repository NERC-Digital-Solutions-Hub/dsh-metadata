# The dataset:

## Overview
- A dataset of calculated breeding success rates for six seabird species from representative Isle of May colonies off Scotland.
- Annual breeding success is measured as the number of chicks fledged per active nest.
- Six species: Atlantic puffin, common guillemot, razorbill, European shag, black-legged kittiwake, northern fulmar.
- For each year, one row with six columns for breeding success ( BS suffix) and six columns for the number of active nests used to calculate the rates.
- Free to use, under a CEH data licence; authors encourage contacting CEH staff before publication.

## Data content and structure
- Temporal coverage varies by species:
  - Puffin, Guillemot, Razorbill: monitoring since 1982.
  - Shag, Kittiwake, Fulmar: monitoring since 1987.
- Data collection and processing:
  - Fieldwork conducted by trained staff using defined protocols.
  - Data recorded in notebooks and field sheets, transcribed to spreadsheets, and backed up.
  - Consistency checks performed (e.g., dates, hatchings, fledgings) with field verification for potential errors.
  - Data quality is controlled at source; Access databases include error-checking queries.
- Output and governance:
  - Results and reports vetted by CEH management.
  - Encourage publication of non-confidential findings with customer approval and acknowledgement.

## Background and methods context
- Seabird monitoring is part of the Isle of May Long-Term Study (IMLOTS) within the UK national seabird monitoring programme.
- Breeding success calculation methods are described in Appendix and have been consistent since 1987.

## Spatial and methodological context (Appendix extracts)
- The document contains detailed, species-specific productivity-monitoring methods, including:
  - Fulmar productivity-monitoring (nest-site mapping; plot selection; yearly plots; photo overlays; coding of nest status; age-based fledge assumptions; calculation as fledged young per occupied site).
  - Shag productivity-monitoring (cliff/rock/boulder sites; regular visits; plot-based sampling; photographing plots; counting nests and incubation/brooding status; colony production as fledged young per incubating nest).
  - Kittiwake productivity-monitoring (50–100 nest plots; photographic and overlay-based recording; repeated checks with age categorisation; final productivity as fledged young per completed nest).
  - Guillemot productivity-monitoring (multiple study plots; incubation-period plots; frequent visits; active sites defined as potential egg/ chick sites; age-based fledge assumptions).
  - Razorbill productivity-monitoring (plot-based sampling; similar approach to Guillemot with emphasis on active sites and chick age assessment).
  - Puffin productivity-monitoring (burrow checks post-peak laying; randomized dispersal of burrow checks; staked burrows; determination of success via presence of chicks; productivity as fledged chicks per burrow where presence/absence determined).
- These methods emphasize plot-based sampling, photographic documentation, repeated visits, and standardized calculations of productivity.

## GIS and data integration considerations
- The dataset provides annual, species-specific breeding success and nest counts that are suitable for GIS-driven time-series analyses.
- Potential GIS products:
  - Spatially explicit layers for study plots and nest sites (where coordinates/locations exist or can be derived from overlays/plots).
  - Temporal maps of breeding success by species and year.
  - Choropleth or dot-density maps of active nests and productivity across plots.
- Recommended data preparation:
  - Link year-by-year breeding success to plot/shapefile polygons or nest-site points.
  - Maintain clear metadata on plot boundaries, nest-site identifiers, and photograph overlays to facilitate georeferencing.
  - Standardize data schemas to enable join operations across species and years.
- Data quality and standards:
  - Preserve provenance from field notebooks to spreadsheets to geospatial layers.
  - Include QA flags or uncertainty indicators where plot sampling varied by year or species.
  - Note any years with incomplete plot coverage or changes in sampling effort.

## Licensing and usage notes
- Data is free to use under CEH licensing.
- For publications, contact CEH staff prior to use to obtain acknowledgement and permissions.

## Appendices and methodological details (summarised)
- The document provides detailed, species-specific productivity-monitoring methods used to obtain the dataset:
  - Fulmar, Shag, Kittiwake, Guillemot, Razorbill, Puffin productivity protocols.
  - Common themes: plot-based sampling, photographic overlays, repeated checks through the breeding season, careful handling to avoid disturbance, age/flight status assessments, and standardized productivity calculations (typically fledged chicks divided by suitable denominators such as occupied or incubating nests).
- These methods underpin the interpretation of the breeding success rates and nest counts in the dataset.

## References
- Walsh, P.M., et al. 1995. Seabird monitoring handbook for Britain and Ireland.
- Harris, M.P. 1989a. Development of monitoring of seabird populations and performance. CSD Report No. 941.