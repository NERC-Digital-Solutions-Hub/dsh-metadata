# Macroinvertebrates of the Conwy catchment

## Overview
- Dataset describing macroinvertebrate communities from the Conwy catchment, Wales, UK, collected over three years (2008–2010).
- Includes species-level data plus supporting habitat and geographical information.
- Files:
  - Macroinvertebrates of the Conwy catchment - taxon data.csv
  - Macroinvertebrates of the Conwy catchment - environmental variables.csv
  - Macroinvertebrates of the Conwy catchment - supporting information.csv
- Contributors span sample collection, laboratory analysis, supporting information, and project management.
- Map variables derived for sample locations using Intelligent River Network; taxon codes based on Davies and Edwards (2011).

## Data collection and processing
- Study design: tributary streams of the Conwy, sampling conducted in November 2008, 2009, and 2010.
- Field method: macroinvertebrates sampled with a 1 mm kick net following RIvPACS protocol; site variables recorded (depth, width, velocity, substrate cover, macrophyte cover).
- Sample handling: collected samples preserved in 4% formaldehyde in the field, later washed through a 500 μm sieve; macroinvertebrates identified to the lowest possible taxonomic level (usually species).
- Taxonomic coding: valid names and unique taxon codes provided in Davies, C. & Edwards, F.K. (2011).
- Data quality: data entry validated by crosschecking against laboratory sheets.
- Geospatial data: site coordinates and map-derived variables prepared via Intelligent River Network (IRN) version 17; references include Dawson et al. (2002).

## Data structure and contents

- Taxon dataset (taxon data.csv)
  - Columns: 
    - A: Site code
    - B: Year
    - C: Sample date
    - D: Taxon code (per Davies & Edwards 2011)
    - E: Taxon name (per Davies & Edwards 2011)
    - F: Life stage (L, larva/nymph; P, pupa; A, adult; U, life stage not relevant)
    - G: Abundance in sample

- Environmental variables dataset (environmental variables.csv)
  - Columns include:
    - Site code, Year
    - Wetted width (m)
    - Water depth (cm)
    - Velocity (m/s)
    - % cover of rock pavement
    - % cover of boulders/cobbles, pebble/gravel, sand and silt/clay (percentages that sum to 100%)
    - % cover by macrophytes

- Supporting information dataset (supporting information.csv)
  - Columns include:
    - Site code, Site name
    - Easting, Northing, OS grid reference
    - Distance from source (km)
    - Altitude (m)
    - Slope (m/km)
    - Stream Strahler order
    - Upstream catchment area

- Sample identifiers: each sample defined by a unique combination of site code and project year; a key to site codes is provided in the supporting information.

- Taxon coding: taxon names and codes aligned with Davies & Edwards (2011) list; life stage codes documented as above.

## Data quality and provenance
- Data validation performed by crosschecking data printouts with laboratory sheets.
- Clear attribution of responsibilities:
  - Sample collection: Gearóid Webb, Peter Scarlett, John Davy-Bowker
  - Laboratory analysis: Gearóid Webb, Helen Vincent, François Edwards
  - Supporting information: Peter Scarlett, Gearóid Webb, François Edwards
  - Planning and management: François Edwards, David Cooper

## Access, reuse, and context
- Primary outputs are three CSV data files accompanying the project; suitable for ingestion into dashboards, self-service analyses, or reports.
- Outputs support broader data use, including potential policy and environmental assessments, by enabling integration of biological data with habitat and geographical context.
- Foundational references:
  - RIvPACS field protocol (Murray-Bligh et al., 1997)
  - Code list for recording freshwater macroinvertebrates (Davies & Edwards, 2011)
  - Mapping variable methodology (Dawson, Hornby, & Hilton, 2002)
- Versioning: Version 1.0, dated 28/06/2016; authored by F. Edwards.