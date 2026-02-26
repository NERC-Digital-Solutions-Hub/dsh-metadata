# Harmonia axyridis invasion: UK distribution data 2004-2016

## Overview
- Dataset of location records for the Harlequin ladybird (Harmonia axyridis) in the UK, spanning 2004–2016 (three records from 2003).
- Records sourced mainly from online recording via the Harlequin Ladybird Survey, UK Ladybird Survey, and the iRecord Ladybird app; plus contributions from coleopterists and a data call for a recent ladybird atlas.
- Records include abundance, life stage (adult, larva, pupa, and occasionally eggs) and colour form (conspicua, spectabilis, succinea) where available.
- Data collated and stored in an Oracle database; strict quality control applied; some data exports are standardized for consistency.

## Data collection and generation
- Data compiled from multiple sources and consolidated in a single database.
- Records are not altered post-collection; standardization adjustments are applied during export to provide consistent data outputs.
- Quality checks implemented as part of data processing (see Quality control).

## Nature and units of recorded values
- Each record is a sighting of one or more individuals.
- Abundance, life stage, and colour form available for some records; abundance may be a single figure, a range, or qualitative (e.g., a couple, a few).
- Location provided as:
  - Grid references (OSGB for Britain, OSI for Ireland, or MGRS for Channel Islands) and corresponding latitude/longitude (WGS84).
  - Data supplied at full precision, and also represented for 1km and 10km grid scales when available.
  - Grid reference precision (in metres) and vice-county codes included.
- Start and end dates reflect the level of date precision available (full date if provided; otherwise month/year or year, spanning the appropriate interval).
- Recorder identifiers are standardized by surname followed by initials; a single ID may refer to multiple individuals.

## Data structure (key fields)
- STARTDATE and ENDDATE: date of record.
- GRIDREF: location reference (OSGB, OSI, or MGRS).
- PRECISION: grid reference precision (metres).
- VC: Watsonian vice county code.
- LATITUDE/LONGITUDE: coordinates for centre of the referenced location.
- GR_1KM / LATITUDE_1KM / LONGITUDE_1KM: 1 km grid square location details.
- GR_10KM / LATITUDE_10KM / LONGITUDE_10KM: 10 km grid square location details.
- ABUNDANCE: textual abundance information.
- FORM_ABUNDANCE: abundance information by colour form, if available.
- FORM: colour form (conspicua, spectabilis, succinea), if available.
- STAGE_ABUNDANCE / STAGE: abundance by life stage and life stage type (larva, pupa, adult), if available.
- RECORDER: standardized recorder ID (surname + initials).

## Quality control
- Validation checks for grid references (ensuring terrestrial locations) and date validity (e.g., no impossible dates).
- Only verified records included; verification carried out by Coccinellidae experts via photographs or specimens, or deemed correct if the recorder is a known expert.

## Recording bias and limitations
- Spatial bias likely due to citizen-science nature, with records skewed toward urban areas.
- Temporal bias possible during periods of intensive media activity related to the Ladybird Survey, causing surges in online submissions.

## Relevance for monitoring and use
- Provides a standardized, verifiable record of UK distribution over time to support monitoring of environmental health and policy performance.
- Facilitates trend analysis, species distribution assessment, and integration with other monitoring datasets through consistent data structure and quality controls.
- Clear documentation of data provenance, collection methods, and limitations enhances transparency and reproducibility for environmental analytics.