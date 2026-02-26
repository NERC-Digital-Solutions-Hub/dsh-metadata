# Metadata for Marsh Tit ( Poecile palustris ) territory surveys in English woods during 2002-2020

## Overview
- Annual surveys count occupied Marsh Tit territories in individual woods and woodland patches.
- Surveys occur in early spring (February–April) before nesting, reflecting the number of breeding territories.
- Marsh Tit background: small, non-migratory woodland specialist with large territories (5–6 ha); populations have declined significantly (around 80% 1967–2018), increasing monitoring importance.
- Primary method: playback surveys to locate territories; some woods also used color-ringing in intensive projects; combined methods noted where applicable.
- Survey coverage: 74 woods across 14 English counties (2002–2020), with some woods surveyed in a single spring and others for up to 17 consecutive springs.

## Context and provenance
- Survey area derived from Forestry Commission's National Forest Inventory England 2015.
- Woodland type classified via Ancient Woodland Inventory (AWI): Ancient Semi-Natural Woodland (ASNW), Planted Ancient Woodland Site (PAWS), or NEW WOODLAND (post-1600).
- Some woods existed in AWI; others did not; classifications reflect pre- or post-1600 woodland status.

## Data structure and contents
- Data are georeferenced and stored in a CSV format with these columns:
  - Wood_id, Wood, County
  - OSGB X, OSGB Y (British National Grid coordinates)
  - Survey year
  - Time Series Analysis (1 = used in time series; 0 = not used)
  - Wood area (ha)
  - Complete or Partial survey
  - Woodland type (ASNW, PAWS, NEW WOODLAND)
  - Marsh Tit territories
  - Method (Playback; CR for color-ringing)
- Notes:
  - Some woods were partially surveyed; others covered entire patches.
  - Playback method details aligned with Broughton et al. (2018); color-ringing details referenced to related studies.

## Quality control and reliability
- Territory counts are considered very reliable.
- Playback method tested to locate a mean 96% of birds present.
- No significant difference in territory estimates whether birds were marked or unmarked; underestimation of about 10% for larger woods (>70 ha).

## Usage and interpretation
- Time Series Analysis flag indicates inclusion in time-series derivations to compute mean territory values per wood.
- Data suitable for longitudinal analyses of territory occupancy across multiple springs and woods.
- Some data may be linked with additional marking/resighting studies (colour-ringing) when present.

## Provenance, acknowledgments, and references
- Acknowledgements: list of contributors and landowners who permitted access to private woods.
- Key references and data sources:
  - Broughton et al. (2010, 2012a, 2012b, 2014, 2018) on habitat occupation, nest placement, and survey methods.
  - Forestry Commission (2019) National Forest Inventory England 2015.
  - Natural England (2019) Ancient Woodland (England).
  - Woodward et al. (2018) BirdTrends 2018.
- Links to data portals referenced for underlying inventories and datasets.

## Data governance and stewardship considerations
- The dataset is georeferenced and structured for interoperability in CSV format; suitable for integration into catalogues and portals.
- Metadata includes methodology, area classifications, and data quality notes to support reproducibility and proper use.
- Potential stewardship actions:
  - Maintain clear provenance and versioning for time-series data (time-series flag and year of survey).
  - Ensure consistent use of OSGB coordinates and woodland type classifications.
  - Document any partial surveys and their implications for aggregations or analyses.
  - Provide licensing and access details alongside data portal references where applicable.