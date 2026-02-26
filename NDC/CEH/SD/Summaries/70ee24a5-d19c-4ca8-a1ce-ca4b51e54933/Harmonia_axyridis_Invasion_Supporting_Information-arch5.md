# Harmonia axyridis invasion: UK distribution data 2004-2016

## Overview
- Dataset of Harlequin ladybird (Harmonia axyridis) UK distribution records from 2004–2016 (three records in 2003).
- Collected from multiple sources, with the majority via online recording portals.
- Includes abundance, life stage (adult, larva, pupa; eggs in a few cases) and colour form (conspicua, spectabilis, succinea) where available.
- Records are collated and stored in an Oracle database; standardised exports may include changes documented in the dataset notes.
- Records have undergone quality control but are not altered beyond standardisation for export.

## Collection and sources
- Primary data sources:
  - Harlequin Ladybird Survey website
  - UK Ladybird Survey website
  - iRecord Ladybird app
- Additional records from coleopterists and a data call for the most recent ladybird atlas (local record centres, natural history societies, county Coleoptera recorders).
- Data integration aimed at standardising formats while retaining original observations; stored in an Oracle database.
- Export to standardised formats involves documented changes to ensure consistency across records.

## Nature and units of recorded values
- Each record represents a sighting of one or more individuals.
- Fields may include:
  - Abundance (numeric, range, or qualitative terms like a couple, a few, approximately fifty)
  - Life stage (larva, pupa, adult) and associated abundance
  - Colour form (conspicua, spectabilis, succinea)
- Location data provided as:
  - Grid references (OSGB for Britain, OSI for Ireland, or truncated MGRS for Channel Islands)
  - Lat/Lon (WGS84) for the centroid of the supplied grid reference
  - Grid precision (in metres)
  - 1 km and 10 km grid references with corresponding latitudes and longitudes
- Records include the recorder identifier (RECORDER), which is standardized to surname followed by initials; a single recorder ID may refer to multiple individuals.
- Date information:
  - STARTDATE and ENDDATE (dates or ranges) with full dates when available; otherwise months/years spanning larger periods.
- Data structure fields include:
  - STARTDATE, ENDDATE, GRIDREF, PRECISION, VC (Watsonian vice county), LATITUDE, LONGITUDE
  - GR_1KM, LATITUDE_1KM, LONGITUDE_1KM, GR_10KM, LATITUDE_10KM, LONGITUDE_10KM
  - ABUNDANCE, FORM_ABUNDANCE, FORM, STAGE_ABUNDANCE, STAGE
  - RECORDER

## Quality control
- Data subjected to validation checks:
  - Grid references are checked to ensure a terrestrial location
  - Dates are validated (e.g., not impossible dates or future dates)
- Records are verified by a team of Coccinellidae experts, using photographs or specimens; or deemed correct if the recorder is a known expert.
- Dataset includes only verified records; some exports may alter formatting but not the underlying observations.

## Data structure
- Detailed metadata and field descriptors accompany the dataset, including:
  - STARTDATE and ENDDATE (type Date)
  - GRIDREF (text) and precision (integer)
  - VC (integer)
  - LATITUDE/LONGITUDE and their 1km and 10km counterparts
  - ABUNDANCE and STAGE-related fields as text
  - FORM (colour form) and related abundance fields
  - RECORDER (numeric ID corresponding to standardized recorder name)

## Recording bias
- Potential spatial bias toward urban areas due to citizen-science data collection.
- Temporal spikes may align with periods of intensive media activity around the Ladybird Survey, affecting submission rates.

## Data governance and stewardship considerations
- Provenance and transparency:
  - Data come from multiple public sources and are stored in an Oracle database; export standardisations should be well-documented to preserve provenance.
- Standards and interoperability:
  - Spatial data use multiple grid schemes (OSGB, OSI, MGRS) and include both grid-based and lat/long coordinates; ensure consistent transformation and metadata to enable cross-dataset interoperability.
- Completeness and quality:
  - Not all records include abundance, life stage, or colour form; stewardship should track missingness and document data coverage by year, location, and source.
  - Verification status is essential; maintain records of expert verification or known expert authorship.
- Updating and versioning:
  - As new records are added or exports are restandardised, maintain versioned datasets with clear changelogs.
- Data access and use:
  - Clearly document licensing, access rights, and any restrictions arising from data provenance (e.g., from citizen science sources) to guide sharing and reuse.
- Handling of recorder identifiers:
  - RECORDER IDs may map to multiple individuals; ensure ongoing governance of recorder identity resolution and metadata describing recording context.