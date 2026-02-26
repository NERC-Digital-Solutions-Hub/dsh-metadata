# Experimental design/sampling regime

- Overview
  - Bird species and abundance were recorded in 10 parks within Sheffield City Region across three survey occasions in June–July 2018.
  - Part of the NERC IWUN Project (Improving well-being through urban nature); aims to correlate biodiversity exposure with emotions/mental well-being via a mobile app.
  - Data collected by Ms Riley; interpretation by Drs Cameron and Brindley alongside other datasets for later correlations.
  - Total observations: 2775. No data were excluded.

- Study design and field methods
  - 10 green spaces surveyed: Bolehills Park, Botanical Gardens, Crookes Valley Park, Devonshire Green, Endcliffe Park, Graves Park, Peace Gardens, Ponderosa, South Street Park, Weston Park.
  - Each site surveyed on 3 occasions (rep 1: 6–22 Jun 2018; rep 2: 27 Jun–10 Jul 2018; rep 3: 11–18 Jul 2018).
  - Surveys conducted in the early morning (05:30–09:30).
  - Transects: 6 pre-designated line transects per site, each 60 m long; transects did not overlap and provided stratified habitat coverage.
  - Observations recorded along lines using binoculars to verify distant sightings.
  - Birds noted within distance bands: 0–25 m, 26–50 m, 51–100 m; individuals counted and identified by common name and BTO code.
  - A single experienced ecologist conducted all surveys for consistency.

- Data collection details and purpose
  - Data recorded: date, time, site, transect, observation details, and counts of birds.
  - Primary objective: relate bird diversity and abundance to participants’ emotions about the places, to assess well-being impacts of urban nature.

- Data records and structure
  - Dataset name: BirdsSheffAllReps2018.csv
  - Spatial/time coverage: 10 sites in Sheffield with three replicate surveys per site in June–July 2018; early morning sampling.
  - Observational data: 2775 total bird observations across 3 replicates and multiple transects.

- Quality control and limitations
  - Data sheet checked by Ross Cameron for logical consistency.
  - No guarantee birds were not counted twice; however, methodology was systematic and assumed consistent error across the dataset.
  - Potential data limitations include overlapping distance bands and single-observer design, which may affect duplication risk and consistency of counts.

- Data structure and metadata
  - The CSV contains 11 columns:
    - VisitNo: visit number (1, 2, or 3)
    - BTOCode: British Trust for Ornithology code
    - BirdName: common name
    - ActivityCode: code for activity observed (C: calling, F: in flight, P: present, S: singing)
    - Activity: activity observed
    - Site: site name
    - Transect: transect number (1–6)
    - Date: date of observation (DD/MM/YYYY)
    - No.Birds: number of birds observed
    - DistanceBand: observation distance band (0–25 m, 26–50 m, 51–100 m)
    - Time: observation time band (HH:MM – HH:MM)
  - The dataset includes coordinates for each site and a structured approach to species identification and observation context.