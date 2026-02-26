# Metadata for Marsh Tit ( Poecile palustris ) territory surveys in English woods during 2002-2020

## Overview
- Annual surveys count the number of occupied Marsh Tit territories in individual woods and woodland patches.
- Surveys occur in early spring (February–April), just before nesting, serving as an index of breeding territories in each wood.
- Marsh Tits are a small, non-migratory species living year-round in mature deciduous/mixed woodlands; their populations have declined substantially (about 80% from 1967 to 2018), making monitoring important.
- A playback method (recorded song/calls) is used to locate territories; some woods were also surveyed with colour-ringing in dedicated projects.

## Dataset scope and purpose
- Location: 74 woods in 14 English counties, primarily Cambridgeshire and Oxfordshire.
- Time period: 2002–2020, with some woods surveyed only once and others annually for up to 17 springs.
- Purpose: provide a reliable record of Marsh Tit territory occupancy over time to support population monitoring and trend analysis.
- Additional context: surveyed area derived from the National Forest Inventory England 2015; woodland types categorized by Ancient Woodland Inventory (AWI).

## Methods and survey protocol
- Primary method: playback surveys following the protocol of Broughton et al. 2018.
- Supplemental method: colour-ringing (in some woods) during intensive projects; may be combined with playback.
- Survey coverage: most surveys encompassed the entire woodland patch; a few large woods were only partially surveyed.
- Reliability: playback method locates a mean of 96% of birds present; territory estimates are robust whether birds are marked or unmarked, with minor underestimations (~10%) in larger woods (>70 ha).

## Quality, uncertainty, and validation
- Territory counts are considered very reliable.
- Validation shows no significant difference in estimates based on marking status; potential undercounting in large woods (~10%).
- Metadata and provenance are documented to support verification and reuse.

## Data structure and metadata
- File format: CSV with georeferenced data.
- Key columns (examples):
  - Wood_id, Wood, County
  - OSGB X, OSGB Y (British National Grid coordinates)
  - Survey year
  - Time Series Analysis (1 = used in time series; 0 = not used)
  - Wood area (ha)
  - Complete or Partial survey
  - Woodland type (ASNW, PAWS, NEW WOODLAND)
  - Marsh Tit territories (count)
  - Method (Playback or CR)
- Data are linked to the wood’s location and descriptive metadata to enable spatial and temporal analyses.

## Spatial and temporal coverage
- Spatial: 74 woods across 14 English counties; coordinates provided for precise mapping.
- Temporal: annual surveys across 2002–2020, with varying frequency per wood (some years missing, some woods surveyed every year).

## Data governance, accessibility, and implications for Monitoring Frameworks
- Data provenance and methodological transparency are explicit (playback methodology, references, and classifications).
- Metadata completeness supports data verification and reuse; structure facilitates integration into time-series analyses.
- Potential barriers discussed in monitoring frameworks (data access, metadata quality, data transformations) are addressed through explicit fields (e.g., complete/partial surveys, time-series usage) and standardized woodland classifications.
- Public sharing of underlying data is contextualized via acknowledgements and data provenance, highlighting the importance of data governance and openness for monitoring frameworks.

## Acknowledgements and references
- Acknowledges contributors and landowners for access and data collection.
- References include key methodological and ecological sources detailing the survey approach, habitat mapping, and Marsh Tit ecology.