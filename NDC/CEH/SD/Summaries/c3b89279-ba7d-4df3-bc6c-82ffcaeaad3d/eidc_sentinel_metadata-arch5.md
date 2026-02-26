# Sentinel project bat and bird survey data, 20202023

## Overview
- Part of the Sentinel project on Social and Environmental Trade-Offs in African Agriculture, funded by UKRI GCRF.
- Aim: assess ecological impacts of agricultural expansion in Ghana and Zambia; analyze community structure across land-use gradients; identify bat and bird species and investigate dietary habits to infer ecosystem service implications.
- Data package includes two dataframes within Sentinel_survey_data.zip: bird point counts and bat/bird mistnetting records.

## Survey scope and design
- Timeframe: December 2020 – March 2023.
- Study regions: Ghana (3 localities) and Zambia (5 localities).
- Site characteristics: Ghana in Upper Guinean wet evergreen forests near cacao/rubber; Zambia in subtropical climates with dry miombo woodlands and evergreen Cryptocephalum forests, surrounded by maize and cassava cultivation.
- Site selection: mixture of recently expanding agricultural areas and baseline references with more intact primary vegetation.
- Sampling design: two-tier stratified random; 1 km x 1 km grid over each locality; sites categorized as:
  - Not Applicable (NA)
  - Agriculture Only
  - Forest edge
  - Forest
- Within each site, survey points chosen along transects at intervals of ≥200 meters.
- Accessibility: some sites were later inaccessible, prompting sampling plan adjustments.

## Data collection methods

### Birds
- Survey method: standardized point counts conducted at dawn, lasting ~3 hours per sampling point.
- 10-minute counts within a 50-meter radius; individuals counted or estimated; seen/heard records; additional observations beyond 50 meters recorded separately.
- At each point: record prevailing weather and vegetation data.
- Mist netting: conducted at a subset of sites to sample understory birds; at least 180 meters of net lanes with specified net types and mesh; netting timed 5:30–10:00; avoid nets near sunrise/sunset to minimize impact on bats; birds netted, identified to species, sexed/aged where possible, weighed, held briefly (≤30 minutes) before release.
  
### Bats
- Survey method: night-time sampling at the same sites using a combination of mist nets and harp traps; sampling conducted on separate nights.
- Trapping: nets and harp traps deployed with checks every 15–30 minutes; typical night duration ≥4 hours.
- Equipment: harp traps, single-storey mist nets, high-volume net systems; identification guided by regional references.

## Data management and quality assurance
- Multiple data inputters entered field data; dataset consolidated, error-checked, and validated.
- Data package Sentinel_survey_data.zip includes:
  - Sentinel_Pointcount_data.csv: bird point-count observations with fields on location, timing, observer, species (common and scientific), counts, observation type, and environmental metadata.
  - Sentinel_Mistnetting_data.csv: bat and bird mistnetting observations with fields on location, site type, collection date, specimen number, taxonomic class, and species names.
- Missing data are designated as NA.

## Data structure and key fields

### Bird point counts (Sentinel_Pointcount_data.csv)
- Location identifiers: Country, Locality, Grid, Transect, Point, Site; coordinates (Latitude, Longitude).
- Temporal: Collection.date, Time.Started.
- Observer: Observer.Initials.
- Species data: Common.name, Species.name; Observation.Type (e.g., heard, seen, both).
- Counts: Perch.Under.50m, Flyover.Under.50m, Total.Under.50m, Over.50m, Total.
- Environmental context: Temp, Cloud.Cover, Wind, Rain; Land.Grid, Land.Point, Land.Site; MaxCan, MinCan, MeanCan; MaxVis, MeanVis; TreeS, TreeM, TreeL, TreeTotal.
- Spatial and sampling structure: Country, Locality, Grid, Transect, Point, Site; coordinates; collection date; etc.

### Mistnetting (Sentinel_Mistnetting_data.csv)
- Location identifiers: Country, Locality, Site; Site.type (Forest, Forest edge, Agriculture, Riverine, etc.).
- Coordinates: Latitude, Longitude.
- Temporal: Collection.date; Specimen.number.
- Taxonomy: Class; Scientific.name; Common.name.

## Access, sharing, and governance considerations
- Data described as two primary dataframes with standardized variable names and definitions; designed for discovery and reuse.
- Taxonomic references used include eBird and regional guides; clear fields for harmonization with metadata standards.
- Data sharing and updates should account for:
  - Plan changes due to site accessibility (documenting sampling adjustments and any gaps).
  - Ongoing updates or corrections to metadata, coordinates, and species identifications.
  - Clear documentation of data provenance, field protocols, and QA steps to support interoperability with other datasets.

## Limitations and considerations for reuse
- Incomplete site coverage due to accessibility issues; presence of NA and potential sampling gaps across land-use categories.
- Data formats are CSVs within a ZIP; ensure downstream interoperability by aligning with internal metadata schema.
- Some fields rely on observer judgment (e.g., counts at varying distances, weather estimates) and may introduce variability; appropriate uncertainty notes should accompany analyses.
- Metadata and provenance are essential for correct interpretation of bird counts, mistnet captures, and the relationship between point counts and mistnetting records.

## References and methodological context
- Methodological references for bird survey techniques, bat guides, and regional fauna guides are cited to support species identifications and field procedures.