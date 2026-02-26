# Impacts of Argentine ant ( Linepithema humile ) on seed dispersal services in Jonkershoek, Cape Floristic Region.

## Overview
- Dataset describing seed dispersal processes under invaded (presence of Linepithema humile) and non-invaded (absence of L. humile) ant communities.
- Focused on ant-mediated seed dispersal in Jonkershoek Nature Reserve, South Africa.
- Collected during the southern hemisphere summers of 2014, 2015, and 2017 (Nov–Dec 2014; Jan–Feb 2015; Jan–Feb 2017).
- Built from three independent experiments to compare dispersal ability of dominant seed-dispersing ants in invaded vs non-invaded communities.

## Location and spatial coverage
- Study site: Jonkershoek Nature Reserve, Western Cape, South Africa.
- Coordinates provided for the study area: 33°55'51"S, 18°51'16"E.
- Data likely organized around spatial plots or locations where ants and seeds were tested (specific site-level details available in the supporting documentation).

## Data collection and experiments
- Experiment 1: Determine ant community structure using pitfall and baiting traps (invaded vs non-invaded sites).
- Experiment 2: Cafeteria-style seed presentation (seeds from twelve plant species); measure seed removal rate over three hours.
- Experiment 3: Seeds presented to nests of invasive L. humile and six native ant species; after 24 hours nests were cast with dental plaster, excavated, and seeds retrieved with burial depths recorded.
- Data were collected systematically across the three experiments to test hypotheses about dispersal ability and how invasion status affects seed dispersal.

## Variables and data structure (data components)
- Ant community data (Experiment 1): invaded vs non-invaded conditions; presence/absence or abundance of ant species from pitfall and baiting traps.
- Seed removal data (Experiment 2): seed removal rate for twelve plant species over a three-hour window; potentially per site and per ant community status.
- Seed burial data (Experiment 3): seeds retrieved from nests after 24 hours; burial depth measurements; associated with nest type (invasive vs native species).
- Metadata: site details, dates (year/month), methods, and experimental setup per experiment.
- Plant species identity (twelve species) and the identity/status of ant communities.

## Temporal scope
- Data collected across three separate summers:
  - 2014: November–December
  - 2015: January–February
  - 2017: January–February

## Provenance, quality, and documentation
- Data collected to assess impacts of L. humile on ant community structure and seed dispersal services.
- Methodologies described as three independent experiments; detailed procedures available in supporting documentation and in the Bristol thesis repository.
- Funding support: NERC-Case studentship (NE/K007076/1) and Varley-Gradwell Travelling Fellowship.
- Data quality and provenance documented; full experimental details accessible via the Bristol thesis repository and associated documentation.

## GIS-ready considerations and potential uses
- GIS-ready potential:
  - Create layers for invaded vs non-invaded plots, trap locations, seed dispersal events, and nest sites.
  - Map spatial patterns of seed removal rates and burial depths across the landscape.
  - Combine with land-cover data to assess habitat factors influencing dispersal under invasion.
- Suggested data preparation:
  - Confirm and document coordinate reference system and exact plot coordinates for spatial joins.
  - Harmonize temporal fields (year, month) and units across experiments.
  - Standardize species names and status (invaded vs non-invaded) for consistent mapping.
- Potential analyses:
  - Compare spatial distributions of seed removal rates between invaded and non-invaded areas.
  - Analyze spatial clustering of burial depths around invasive nests.
  - Integrate with environmental layers (vegetation type, soil, elevation) to explore drivers of dispersal differences.

## Access and supporting information
- Methodological details and experimental design available in the Bristol thesis repository: https://researchinformation.bristol.ac.uk
- Full provenance and data collection description referenced in the dataset documentation.