# Vascular plant and bryophyte survey from a 33-year chronosequence on bare chalk, Dorset, 2019-2020

## Overview
- Investigates primary succession on bare chalk using a 33-year chronosequence across 13 excavated plots at Down Farm, north Dorset.
- Focuses on vascular plants and bryophytes, providing standardized, species-level data and quadrat-level environmental context.
- Data intended to support long-term environmental monitoring and analysis of succession dynamics on chalk grassland.

## Study site and timescale
- Location: Down Farm, Dorset (approximately 50°55'51"N, 002°00'15"W).
- Chronosequence spanning 1986 to 2018 excavation ages, enabling comparison across site age.
- Excavations created a mosaic of bare chalk surfaces that have remained open and unmanaged (no chemical input or biomass removal).

## Methods
- Transects and plots
  - 13 transects established in July 2019, one per excavated block.
  - Blocks dated 1986, 2004–2008, and 2013–2018 (two blocks excavated in 2016).
  - Each transect length: 16 m.
- Sampling design
  - Vascular plants: 50 cm x 50 cm quadrats, surveyed every 1 m along each transect (total of 208 quadrats).
  - Bryophytes: 20 cm x 20 cm quadrats, surveyed February 2020 (two bryophyte plots excluded due to disturbance or time constraints).
- Identification and recording
  - Vascular plants identified to species level (except Taraxacum microspecies).
  - Bryophytes identified to species level (microscopy used as needed); some small/infertile specimens grouped.
  - Data captured as percentage cover per species per quadrat; additional environmental cover (bare chalk, bare soil, stones, flint) and sward height recorded where applicable.
- Quality control
  - Field data collected by experienced ecologists.
  - Paper records digitised into Excel and checked for anomalies.

## Data structure and content
- Vascular plants dataset: Vascular_plant_survey_bare_chalk_Dorset.csv
  - Key fields: Plot_number, Year_exc, Quadrat_number, Unique_ID (Plot_Quadrat), Survey_date.
  - Species columns with percentage cover; Sward_height; Bare_chalk; Bare_soil; Bare_chalk&soil; Total_bare_grd; and other contextual fields.
- Bryophytes dataset: Bryophyte_survey_bare_chalk_Dorset.csv
  - Key fields: Plot_number, Year_exc, Quadrat_number, Unique_ID, Survey_date.
  - Species columns with percentage cover; plus Vegetation and substrate columns (Vas_plant_cov, Bare_chalk, Bare_soil, Stones, Flint, etc.).
- Both datasets include explicit quadrat and plot identifiers, year excavated, survey dates, and a concatenated Unique_ID for cross-referencing.
- Site and method references documented for context and reproducibility.

## Site context and references
- Original work and context:
  - Green, M. (2000) A Landscape Revealed: 10,000 Years on a Chalkland Farm.
  - Preston, C.D. et al. (2009) on bryophyte responses to disturbance in chalk grasslands.
- Related studies:
  - Ridding et al. (under review): Do functional traits influence primary succession patterns for bryophytes and vascular plants? Evidence from a 33-year chronosequence on bare chalk.
  - Hawes et al. (2020): Colonisation of exposed chalk surfaces and the restoration of chalk grassland.

## Data accessibility and reuse
- Data are organized into clearly labeled CSV files with robust metadata in the column headers.
- The standardized data structure supports cross-temporal analyses of species establishment, community composition, and bare-ground dynamics across a chalk chronosequence.
- Potential for integration with additional environmental or management datasets to enhance monitoring and comparative analyses across chalk grassland systems.

## Possible applications for environmental monitoring
- Tracking successional trajectories of vascular plants and bryophytes on bare chalk over multiple decades.
- Assessing how plant communities colonize exposed substrates in the absence of chemical inputs or biomass removal.
- Providing baseline and longitudinal data to evaluate policy outcomes related to chalk grassland restoration and habitat connectivity.
- Enabling data-level integration with other monitoring datasets to improve the value and accessibility of environmental data assets.