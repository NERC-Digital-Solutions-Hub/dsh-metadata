# Vascular plant and bryophyte survey from a 33-year chronosequence on bare chalk, Dorset, 2019-2020

- Purpose and scope
  - investigates primary succession on bare chalk using a 33-year chronosequence across a mosaic of exposed surfaces at Down Farm, north Dorset.
  - Targets two taxa: vascular plants and bryophytes.
  - Provides a time-structured, site-based dataset suitable for map-based analyses and spatial visualization of colonisation patterns over time.

- Study site and chronology
  - Location: Down Farm, Dorset (approx. 50°55'51"N, 002°00'15"W).
  - Chronosequence created by archaeological excavations (1986 onward), generating a mosaic of bare chalk surfaces with no chemical input or biomass removal.
  - 13 transects established across excavated blocks dated 1986, 2004–2008, 2013–2018 (two blocks in 2016).

- Survey design and field methods
  - Vascular plants
    - 13 transects; each transect 16 meters long.
    - Sampling: 50 cm x 50 cm quadrats along each meter (1 m) of the transect, totaling 208 quadrats.
    - Survey timing: July 2019.
    - Identification: vascular plants to species level (except Taraxacum microspecies).
  - Bryophytes
    - 20 cm x 20 cm quadrats; same transect layout as vascular plants.
    - Survey timing: February 2020.
    - Identification: bryophytes to species level (with microscopy as needed); most specimens identified to species, with some grouped where necessary.
  - Exclusions and constraints
    - Two bryophyte plots not recorded (excavated 2006 with rubble, and 2016 due to time constraints).
  - Quality control
    - Data collected by experienced field ecologists; paper forms digitised to Excel and checked for anomalies.

- Data structure and content
  - Vascular plant dataset: Vascular_plant_survey_bare_chalk_Dorset.csv
    - Core fields: Plot_number (1-13), Year_exc (1986–2018), Quadrat_number (0–15), Unique_ID (PlotQuadrat), Survey_date, Sward_height (cm).
    - Species columns: full scientific names with associated percent cover per quadrat.
    - Additional fields: Bare_chalk, Bare_soil, Bare_chalk&soil (percent cover within quadrat).
  - Bryophyte dataset: Bryophyte_survey_bare_chalk_Dorset.csv
    - Core fields: Plot_number, Year_exc, Quadrat_number, Unique_ID, Survey_date.
    - Species columns: full bryophyte names with percent cover per quadrat.
    - Additional fields: Vas_plant_cov, Bare_chalk, Bare_soil, Stones, Flint, Total_bare_grd (percent cover sums).
  - Data granularity: quadrat-level coverage data across 13 plots and multiple excavation years, enabling spatially-explicit analyses of plant and bryophyte distributions over time.

- Spatial and temporal coverage
  - Temporal range: excavation years from 1986 to 2018; surveys conducted in 2019 (vascular) and 2020 (bryophytes).
  - Spatial layout: 13 transects across a mosaic of bare chalk plots at Down Farm; transects provide a structured grid of quadrats for mapping cover across time.
  - Exact site coordinates provided for the study location; transect-level plot and quadrat indexing facilitate spatial mapping, replication, and integration with GIS layers.

- Using the data for GIS and map-based products
  - Suitable for creating map layers of species composition and percent cover across quadrats, plots, and years.
  - Can be combined with spatial basemaps of the bare chalk chronosequence to visualize colonisation dynamics and succession patterns.
  - Enables temporal analysis by linking quadrat data to excavation year (Year_exc) and plotting changes in cover and bare ground components over time.
  - Potential to generate productivity or habitat suitability maps by plotting sward height, bare ground, and stone/flake cover alongside species distributions.

- Limitations and considerations
  - Bryophyte data had two plots excluded; interpret results with awareness of incomplete bryophyte coverage for those ages.
  - Some bryophyte identifications limited to groups due to small or infertile specimens.
  - Taxonomic note: Taraxacum microspecies among vascular plants may have unresolved taxonomy in some records.
  - Data are provided in tabular format with per-quadrat species percent covers, requiring spatial reconstruction to create polygon or gridded GIS layers (e.g., by plotting quadrats along transects).

- References and related work
  - Related publications and data context cited (Ridding et al. under review; Hawes et al. 2020) for survey approach and context on chalk surface colonisation and disturbance effects.
  - Primary data files: Vascular_plant_survey_bare_chalk_Dorset.csv and Bryophyte_survey_bare_chalk_Dorset.csv.