# Harmonia axyridis invasion: UK distribution data 2004-2016

## Overview
- Compilation of location records for the Harlequin ladybird (Harmonia axyridis) in the UK from 2004–2016 (three records from 2003).
- Predominantly sourced from online recording platforms (Harlequin Ladybird Survey, UK Ladybird Survey, iRecord Ladybird app) plus contributions from coleopterists, local record centres, natural history societies, and county recorders.
- Records include optional data on abundance, life stage, and colour form where available.

## Data collection and sources
- Major sources: online recording surveys; additional data from expert networks and a recent ladybird atlas data call.
- Records stored in an Oracle database; not altered except for standardized export for this dataset.
- Quality checks applied to ensure location validity (land-based grid references) and date validity.

## Nature and units of recorded values
- Each record represents a sighting (one or more individuals).
- Attributes available (when present): abundance, life stage (adult, larva, pupa, eggs in some cases), colour form (conspicua, spectabilis, succinea).
- Abundance may be a single value, a range, or qualitative (e.g., a couple, a few).
- Location data provided as:
  - Grid references (OSGB for Britain, OSI for Ireland, truncated MGRS for Channel Islands) with precision in metres.
  - Latitude/Longitude (WGS84) for centre of grid reference.
  - Also provided at 1km and 10km grid scales when available (GR_1KM, LATITUDE_1KM, LONGITUDE_1KM; GR_10KM, LATITUDE_10KM, LONGITUDE_10KM).
- Recorder identifier refers to standardized surname + initials; a single ID may represent multiple individuals.

## Data structure and fields (highlights)
- STARTDATE, ENDDATE: Start and end dates for the record (DD/MM/YYYY; could span a month/year if only partial date provided).
- GRIDREF: Location reference (OSGB/OSI/MGRS) with corresponding PRECISION (metres).
- VC: Watsonian vice county code.
- LATITUDE, LONGITUDE: Coordinates for the centroid of the supplied grid reference.
- GR_1KM, LATITUDE_1KM, LONGITUDE_1KM: 1km grid reference and centroid coordinates.
- GR_10KM, LATITUDE_10KM, LONGITUDE_10KM: 10km grid reference and centroid coordinates.
- ABUNDANCE: Text field for overall abundance.
- FORM_ABUNDANCE: Abundance information by colour form, if available.
- FORM: Colour form (conspicua, spectabilis, succinea), if available.
- STAGE_ABUNDANCE: Abundance information by life stage, if available.
- STAGE: Life stage (larva, pupa, adult).
- RECORDER: Recorder ID (non-unique per person; standardized naming).

## Quality control and provenance
- Validation checks include: grid reference lies on land; dates are valid (no future dates, no impossible dates).
- Only verified records included; verification via photographs, specimens, or trusted expert evaluation.
- Records are not altered beyond standardized export adjustments for this dataset.

## Spatial and temporal coverage
- Temporal range: 2004–2016 (three records from 2003).
- Spatial scope: UK and Channel Islands (data include Britain, Ireland, and Channel Islands with corresponding grid systems).

## Recording bias and limitations
- Potential spatial bias: data likely skewed toward urban areas due to citizen-science collection methods.
- Temporal bias: surges in records during periods of intensive media coverage of the Ladybird Survey.
- Overall, data quality relies on multiple sources with varying resolutions and verification levels.

## GIS-focused considerations and potential uses
- Suitable for map-based distribution visuals, hotspot mapping, and regional occupancy analyses.
- Can support multi-resolution analyses by integrating OSGB/OSI/MGRS references with 1km and 10km grid aggregations.
- Useful for linking abundance and life-stage data to spatial units (vice counties, grid cells).
- Important to account for potential recording bias during analysis; consider bias-aware modelling or weighting by data density.

## Practical notes for processing
- When exporting or integrating: preserve original grid references and their precision; use 1km/10km grid fields for scalable mapping.
- Validate dates and ensure correct interpretation of ranges or qualitative abundance.
- Separate records by life stage and colour form where possible to enable nuanced mapping.