# Metadata for Marsh Tit ( Poecile palustris ) territory surveys in English woods during 2002-2020

## Overview
- Annual surveys count the number of occupied Marsh Tit territories in individual woods and woodland patches.
- Surveys occur in early spring (February–April), just before nesting, to reflect breeding territories.
- Marsh Tit populations have declined substantially in recent decades, making consistent monitoring important.
- Primary survey method is playback to locate territories; some woods also used colour-ringing in intensive projects.

## Dataset scope and coverage
- Timeframe: 2002–2020.
- Locations: 74 woods in 14 English counties, with a focus on Cambridgeshire and Oxfordshire.
- Survey frequency: Some woods surveyed once; others annually for up to 17 consecutive springs.
- Geography and classification:
  - Surveyed areas derived from Forestry Commission National Forest Inventory England 2015.
  - Woodland type classified via Ancient Woodland Inventory (AWI): Ancient Semi-Natural Woodland (ASNW), Planted Ancient Woodland Site (PAWS), or NEW WOODLAND.
  - AWI-present woods labeled accordingly; AWI-absent woods categorized as NEW WOODLAND.

## Species context and monitoring importance
- Marsh Tits are small (about 10 g), non-migratory, with large territories (typically 5–6 ha).
- They are specialists of mature deciduous and mixed woodlands.
- Abundance declined ~80% from 1967 to 2018, underscoring the need for robust monitoring.

## Survey methods and data collection
- Primary method: Playback surveys following Broughton et al. (2018) protocol; designed to detect nearly all territories.
- Additional method: Colour-ringing (when part of intensive projects) may be combined with playback.
- Data capture includes notes on method used: Playback or CR (colour-ringing).
- Some woods underwent partial surveys; many covered entire woodland patches.

## Woodland classification and area
- Woodland type indicators:
  - ASNW: Ancient Semi-Natural Woodland (pre-1600)
  - PAWS: Planted Ancient Woodland Site
  - NEW WOODLAND: post-1600 woodland
- Surveyed woodland area (ha) generally corresponds to the entire wood, with exceptions for the largest woods where only a portion was surveyed.

## Data quality and reliability
- Territory counts per wood are considered very reliable.
- Playback method demonstrated to locate an average of 96% of birds present.
- Counting outcomes are robust across marked vs. unmarked birds; however, underestimates of about 10% occur for larger woods (>70 ha).

## Data structure and fields
- Data are georeferenced and stored in a CSV format with the following columns:
  - Wood_id: Unique wood identifier
  - Wood, Description: Wood name
  - County, Description: English county
  - OSGB X, Description: Easting coordinate (British National Grid)
  - OSGB Y, Description: Northing coordinate (British National Grid)
  - Survey year, Description: Year of survey
  - Time Series Analysis, Description: 1 if used in time-series analysis; 0 otherwise
  - Wood area (ha), Description: Surveyed wood area
  - Complete or Partial survey, Description: Indicates full wood or partial survey
  - Woodland type, Description: ASNW, PAWS, or NEW WOODLAND
  - Marsh Tit territories, Description: Estimated number of territories
  - Method, Description: Playback or CR

## Temporal and spatial aspects
- Time-series potential: Many woods have multi-year data (up to 17 consecutive springs), enabling trend analyses of territory occupancy.
- Spatially explicit: Georeferenced records facilitate mapping and integration with habitat and landscape data.

## Outputs, usage and portal considerations
- Outputs are counts of Marsh Tit territories per wood per survey year.
- Data suitable for time-series analyses of environmental health and woodland habitat suitability.
- Metadata and data quality considerations support reproducibility and integration with other environmental datasets.
- As per standard practice for monitoring datasets, dataset storage and uploading to appropriate data portals is anticipated.

## Acknowledgements and references
- Acknowledges survey contributors and landowners for access.
- Key references include methodological papers on playback surveys (Broughton et al. 2018) and related habitat and population studies (multiple works by Broughton et al.; Forestry Commission; Natural England; BirdTrends 2018).