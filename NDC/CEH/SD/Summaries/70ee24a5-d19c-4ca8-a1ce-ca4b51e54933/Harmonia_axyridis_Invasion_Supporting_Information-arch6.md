# Harmonia axyridis invasion: UK distribution data 2004-2016

## Overview
- Dataset of location records for the Harlequin ladybird (Harmonia axyridis) in the UK from 2004–2016 (three records from 2003).
- Majority of records collected online via the Harlequin Ladybird Survey, UK Ladybird Survey, and the iRecord Ladybird app; additional records from coleopterists and a data call for the latest atlas.
- Records include optional abundance, life stage (adult, larva, pupa, and occasionally eggs) and colour form (conspicua, spectabilis, succinea).

## Collection, generation and transformation
- Records consolidated from multiple sources and stored in an Oracle database.
- Records are not altered; standardised exports are provided with documented transformations.
- Abundance and other attributes are included where available; not all fields present for all records.

## Nature and units of recorded values
- Each record represents a sighting of one or more individuals.
- Abundance, life stage, and colour form may be present for some records; abundance can be a single value, a range, or descriptive (e.g., a couple, a few).
- Location provided as grid references (OSGB, OSI, or MGRS) and as latitude/longitude (WGS84). Precision is recorded.
- Grid reference may be derived from postcode/address.
- Recorder identifier refers to a standardized surname + initials; a single ID may map to multiple individuals.

## Recording dates and spatial data details
- STARTDATE and ENDDATE are dates; if only month/year or year is available, the date spans the respective month or year.
- Location data include:
  - GRIDREF with precision and grid-system type (OSGB/OSI/MGRS)
  - LATITUDE/LONGITUDE (center of provided grid)
  - GR_1KM, LATITUDE_1KM, LONGITUDE_1KM (1 km grid)
  - GR_10KM, LATITUDE_10KM, LONGITUDE_10KM (10 km grid)
- Vice County codes (VC) included to link records to British, Channel Islands, and Irish vice counties.
- Data fields enumerated include ABUNDANCE, FORM_ABUNDANCE, FORM, STAGE_ABUNDANCE, STAGE, RECORDER.

## Quality control
- Data validated for plausible locations (land-based grid references) and valid dates (no future or impossible dates).
- Only verified records included; verification performed by Coccinellidae experts via photographs or specimens, or accepted if the recorder is a known expert.

## Data structure (key fields)
- STARTDATE, ENDDATE; GRIDREF; PRECISION; VC; LATITUDE; LONGITUDE
- GR_1KM, LATITUDE_1KM, LONGITUDE_1KM; GR_10KM, LATITUDE_10KM, LONGITUDE_10KM
- ABUNDANCE; FORM_ABUNDANCE; FORM; STAGE_ABUNDANCE; STAGE
- RECORDER (standardized name)

## Recording bias and limitations
- Spatial and temporal bias due to citizen science and online reporting.
- Likely overrepresentation in urban areas and spikes during periods of intensive media activity.