# Harmonia axyridis invasion: UK distribution data 2004-2016

## Overview
- Dataset of location records for the Harlequin ladybird (Harmonia axyridis) in the UK, spanning 2004–2016 (three records from 2003).
- Collected from multiple sources, mainly online recording via the Harlequin Ladybird Survey, UK Ladybird Survey, and the iRecord Ladybird app; also from coleopterists and a data call for the most recent ladybird atlas.
- Records include abundance, life stage (adult, larva, pupa, and occasionally eggs), and colour form (conspicua, spectabilis, succinea) where available.
- Data stored in an Oracle database; records are not altered, with some standardized exports for analysis.

## Data collection and sources
- Major sources: Harlequin Ladybird Survey website, UK Ladybird Survey website, iRecord Ladybird app.
- Additional records from local record centres, natural history societies, and county Coleoptera recorders.
- Records compiled and quality-checked before inclusion.

## Data content and units
- Each record represents a sighting of one or more individuals.
- Abundance, life stage, and colour form may be provided for some records.
- Location data: grid references (OSGB, OSI, or MGRS) and latitude/longitude (WGS84), at full precision, plus 1km and 10km grid-level summaries.
- Start and end dates typically the same; where only month/year or year is provided, dates span the relevant period.
- Recorder identifiers refer to standardized surnames and initials; a single recorder ID may correspond to multiple individuals.
- Grid reference precision and associated metadata (precision, vice county code, etc.) are included.

## Nature and units of recorded values (detailed)
- STARTDATE and ENDDATE: record date range (DD/MM/YYYY).
- GRIDREF: location of observation; formats vary by region (OSGB, OSI, MGRS).
- PRECISION: grid reference precision in metres.
- VC: Watsonian vice county code.
- LATITUDE/LONGITUDE: coordinates for the supplied grid reference centroid.
- GR_1KM / LATITUDE_1KM / LONGITUDE_1KM: centroid of the 1 km grid square (if precision allows).
- GR_10KM / LATITUDE_10KM / LONGITUDE_10KM: centroid of the 10 km grid square.
- ABUNDANCE: text field with quantity (may be a single figure, a range, or qualitative terms).
- FORM_ABUNDANCE: abundance information by colour form, if available.
- FORM: colour form (conspicua, spectabilis, succinea) when available.
- STAGE_ABUNDANCE / STAGE: abundance by life stage and life stage type (larva, pupa, adult).
- RECORDER: standardized recorder ID (surname + initials).

## Quality control
- Validation checks include ensuring grid references refer to locations on land and dates are valid (not in the future or impossible dates).
- Only verified records are included; verification is performed by Coccinellidae experts via photographs or specimens, or accepted if the recorder is a known expert.

## Data structure (fields)
- STARTDATE, ENDDATE, GRIDREF, PRECISION, VC, LATITUDE, LONGITUDE
- GR_1KM, LATITUDE_1KM, LONGITUDE_1KM
- GR_10KM, LATITUDE_10KM, LONGITUDE_10KM
- ABUNDANCE, FORM_ABUNDANCE, FORM
- STAGE_ABUNDANCE, STAGE
- RECORDER

## Geographic scope and precision
- Coordinates provided at multiple scales (full precision, 1 km, and 10 km) to support analyses at various spatial resolutions.
- Grid reference systems used include OSGB (Great Britain), OSI (Ireland), and MGRS (Channel Islands) with explicit conventions.

## Recording bias and limitations
- Data likely biased spatially toward urban areas due to citizen-science participation.
- Temporal spikes may align with periods of intensive media coverage or public interest in the Ladybird Survey.
- As with citizen-science datasets, recognition of potential biases is important for robust interpretation and modeling.

## Usage considerations for analysts
- Suitable for distribution mapping, detection of spread patterns, and analyses by life stage or colour form where data exist.
- Abundance data are heterogeneous (may be single values, ranges, or qualitative descriptors), requiring careful harmonization for quantitative analyses.
- Knowledge of recording biases is essential when inferring trends or making predictions about invasion dynamics.