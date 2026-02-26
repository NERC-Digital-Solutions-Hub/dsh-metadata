# The dataset:

## Overview
- A dataset of calculated breeding success rates for six seabird species from representative Isle of May colonies (East coast of Scotland).
- Annual breeding success measured as chicks fledged per active nest, for: Atlantic puffin, common guillemot, razorbill, European shag, black-legged kittiwake, and northern fulmar.
- For each year: a single row containing six columns of breeding success rates (each named by common species with a suffix 'BS') and six corresponding columns with the number of active nests used to calculate the rates.
- Dataset is free to use under a UKCEH data licence; users are encouraged to contact UKCEH staff before publication.

## Dataset structure
- Temporal resolution: yearly records from 1982 (for puffin, guillemot, razorbill) and 1987 (for shag, kittiwake, fulmar).
- Columns: six breeding success (BS) columns plus six active nests columns (one pair per species).
- Scope: data originate from Isle of May National Nature Reserve (NNR) and are part of the Isle of May Long-Term Study (IMLOTS) within JNCC’s seabird monitoring program.

## Context and provenance
- Background: Seabird monitoring at Isle of May began in 1973; standardised methods have been used since 1987.
- Fieldwork: conducted by trained staff following defined protocols; data collected in field notebooks and data sheets, then transcribed to spreadsheets.
- Quality control: databases (including Access) with error-checking queries; field checks for inconsistencies; archive of notebooks and field sheets at UKCEH Edinburgh.
- Publication and governance: UKCEH oversight ensures data integrity, reporting alignment with deliverables; staff encouraged to publish non-confidential results with customer approval.

## Data collection, quality, and handling
- Field processes: standardized protocols; double-checking of data; field verification of potential errors.
- Data handling: notebooks and sheets archived; spreadsheets backed up; QA via source-controlled databases.
- Output governance: management vetting and tracking of results and reports; acknowledgement and customer approval for external publication.

## Appendix – methods for seabird productivity monitoring
- The appendix provides detailed, species-specific methods to obtain productivity data, including:
  - Fulmar productivity-monitoring: nest-site mapping, plot selection (3–5 plots), annual plots, photographing plots, marking nest sites, multi-date checks, and calculation of mean fledged per occupied site and colony production.
  - Shag productivity-monitoring: nest-site plots (10–30 nests per plot), 7–10 day visits from mid-April, repeat checks, and colony production calculated as fledged nests per incubating nests.
  - Kittiwake productivity-monitoring: plots of 50–100 nests, photographic documentation, multi-date visits, and recording fledged young per completed nest.
  - Guillemot productivity-monitoring: several plots (randomly selected, at least 50 breeding pairs each), multiple daily visits during incubation, active sites mapping, and fledging estimates based on age thresholds.
  - Razorbill productivity-monitoring: similar plot-based approach to guillemot, with regular visits and active site counts to derive fledging productivity.
  - Puffin productivity-monitoring: burrow checks post-laying, plots of burrows, use of tools to detect incubating birds, re-checks after chick development, and productivity as chicks fledged per refound burrow.
- Key methodological themes:
  - Use of plots to sample larger colonies, with random or dispersal-based plot selection.
  - Repeated annual plots to ensure comparability across years.
  - Photographic overlays to record nest sites and cross-year matching.
  - Ethical, non-disruptive field practices (no flushing birds; careful observation).
  - Productivity definitions generally as fledged chicks per nest or per active/complete nest, depending on species.

## GIS implications and considerations
- Data are primarily annual, with columnar (BS) values by species and corresponding nest counts; spatial granularity at the dataset level is not explicitly provided, but appendices describe plot- and nest-level sampling that can be georeferenced if plot/nest locations are available elsewhere.
- Potential GIS products:
  - Time-series visualization of breeding success (BS) by species across years.
  - Plot-level productivity maps by year (if plot-level data are accessible or linkable).
  - Nest-site density and occupancy maps for each species using plot and nest location data.
  - Change detection of breeding success and nest counts over time to identify trends and hotspots.
- Data integration needs:
  - Link annual row data to plot-level data from appendices or external databases to enable spatial mapping.
  - Ensure consistent units and definitions of productivity across species (per nest vs per active/incubating nest) for cross-species comparisons.
  - Maintain provenance: Isle of May NNR, IMLOTS, JNCC, and UKCEH data licence terms; capture citation requirements.

## Limitations and cautions for GIS users
- The primary dataset is annual and aggregated per year; spatial detail depends on access to the plot/nest data described in the appendices.
- Sampling effort and plot numbers vary by species and year; interpret trends with awareness of changes in sampling design.
- Methodological notes emphasize consistency since 1987, but any linking of year-to-plot data must respect the historical sampling framework and potential changes in plot coverage.

## Recommendations for GIS workflow
- Preserve dataset provenance and licensing terms; document data sources and processing steps for GIS analyses.
- Create a metadata record capturing: species names, BS column definitions, nest-count columns, year range, sampling design, plot counts, and methodologies from appendices.
- If available, integrate plot-level shapefiles or geolocated nest plots to enable spatial analyses and map-based visualizations.
- Use the productivity definitions per species as the basis for cross-species comparisons, ensuring consistent interpretation (e.g., fledged chicks per nest vs per active/incubating nest).

## References
- Walsh, P.M., Halley, D.J., Harris, M.P., del Nevo, A., Sim, I.M.W., & Tasker, M.L. 1995. Seabird monitoring handbook for Britain and Ireland.
- Harris, M.P. 1989a. Development of monitoring of seabird populations and performance: final report to NCC. Nature Conservancy Council.