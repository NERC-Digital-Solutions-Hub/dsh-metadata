# Supporting documentation for bird ringing data

## Overview
- Dataset from Wytham Woods, Oxfordshire, UK, collected in 2020–2021 as part of long-term population monitoring of breeding biology and behaviour.
- Methods include trapping unringed breeding pairs at nests (Apr–Jun), fitting BTO metal rings; great tits and blue tits also fitted with plastic RFID (PIT) tags; nestlings tagged at 2 weeks.
- Additional autumn/winter ringing across the woodland; mistnetting used for capture; biometrics recorded (mass, wing length, tarsus length, fats score, bill length).
- Immigrants tagged; birds released after processing.
- Data entered into EBMP (Edward Grey Institute Bird Data Management Project) and quality checked (e.g., detecting erroneous nestbox identities).
- Primary data entry and QA by Keith McMahon and Sam Crofts, with some assistance from field staff.

## Data collection and scope
- Species focus includes blue tits and great tits; tagging also applied to other birds where captured.
- Sampling window spans trapping at nests (breeding season) and supplementary autumn/winter ringing.
- Location identified by nestbox codes within Wytham Woods; captures include both adults and nestlings (with associated biometrics).
- Each record can reflect a physical hold or diurnal identification without capture; various retrap statuses.

## Data structure and fields
- Single CSV file: Ringing_data (23 columns).
- Key field groups:
  - Identification and capture status: Record.type, Retrap, Location, Date.time.
  - Tag/identity: Bto.ring (BTO ring number), Pit.tag (PIT tag code or blank), Pit.tag.state (0–6 with defined meanings).
  - Species and age/sex: Bto.species.code, Age, Sex, Sexing method.
  - Measurements: Wing.length, Weight, Bill.length (method and value), Bill.depth (method and value), Tarsus.length (method and value).
  - Health and condition: Pox, Leg.condition.description, Tick.description.
  - Miscellaneous: Comments; references to species and age code definitions via linked resources.
- Coding and references:
  - Bto.species.code uses BTO abbreviations (with external PDF link provided).
  - Age and other codes reference BTO resources (agecodes.pdf, etc.).
  - Pit.tag.state encodes tag presence, scanning status, and tag integrity (0–6).

## Data quality and provenance
- Data quality checks performed in EBMP, including validation of nestbox identities and other entries.
- Primary data collection and entry performed by named field staff (notably McMahon and Crofts).
- Data may contain missing values (e.g., Pit.tag could be blank; Pit.tag.state indicates tag status), requiring careful interpretation during GIS integration.

## GIS considerations and usage
- Spatial dimension is anchored to nestbox locations within Wytham Woods; exact coordinates are not provided in the CSV, so GIS use may require:
  - Geocoding nestbox codes to spatial coordinates using a separate spatial reference dataset.
  - Treating each record as a point event with time stamps and rich attribute data.
- Useful attributes for mapping and analysis:
  - Species, age, sex, and corresponding biometrics for demographic and phenotypic mapping.
  - Tag status (BTO vs PIT) and scans, enabling studies of tagging prevalence and data quality.
  - Health indicators (Pox, ticks, leg injuries) as potential risk or habitat association indicators.
  - Location codes enabling spatial aggregation by nestbox or habitat units within Wytham Woods.
- Limitations:
  - Origin limited to a single woodland site and short timeframe (2020–2021) relative to long-term studies.
  - Location is coded rather than georeferenced in the CSV, requiring external lookup for full GIS integration.
  - Some fields rely on external code lists (species, age), so reproducible mapping requires those code lists.

## Access and preparation notes
- Data is provided as a single CSV (Ringing_data) with 23 columns; users should consult linked BTO resources for code interpretation (species, age).
- Prior to GIS use, prepare: geocode nestbox locations, harmonize units, handle missing PIT-tag data, and validate tag states.
- Consider coupling with EBMP metadata or related documentation to ensure consistent interpretation of codes and measurement methods.