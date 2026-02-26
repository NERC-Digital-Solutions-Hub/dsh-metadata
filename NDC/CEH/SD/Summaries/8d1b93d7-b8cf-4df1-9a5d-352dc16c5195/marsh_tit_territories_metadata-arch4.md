# Metadata for Marsh Tit ( Poecile palustris ) territory surveys in English woods during 2002-2020

## Overview
- Annual surveys counting the number of occupied Marsh Tit territories within individual woods and woodland patches.
- Surveys conducted in early spring (February–April) just before nesting; counts reflect breeding territories.

## Context and Purpose
- Marsh Tits are small, non-migratory woodland birds with large territories; monitoring is important due to significant population declines (about 80% between 1967 and 2018).
- Playback method used to locate territories; some woods also involved colour-ringing in related projects.
- Survey area derived from the Forestry Commission’s National Forest Inventory England 2015; woodland type classified via the Ancient Woodland Inventory (AWI).

## Data Collection and Methods
- Primary method: playback surveys following Broughton et al. 2018; some woods also used colour-ringing data.
- Coverage: 74 woods across 14 English counties (2002–2020); some woods surveyed once, others annually in up to 17 springs.
- Survey extents: most surveys cover the entire wood/patch; a few large woods were partially surveyed.
- Woodland area and classification (ASNW, PAWS, NEW WOODLAND) derived from AWI/NFI data.

## Quality and Limitations
- Territory counts considered very reliable; playback method locates about 96% of birds present.
- Underestimation of counts about 10% for larger woods (>70 ha); no significant difference whether birds were marked or unmarked.

## Data Structure and Variables
- Georeferenced CSV with key fields, including:
  - Wood_id, Wood, County
  - OSGB X and OSGB Y coordinates (British National Grid)
  - Survey year
  - Time Series Analysis flag (1 = used in time series, 0 = not)
  - Wood area (ha)
  - Complete or Partial survey indicator
  - Woodland type (ASNW, PAWS, NEW WOODLAND)
  - Marsh Tit territories (count)
  - Method (Playback or CR for colour-ringing)
- Time Series Analysis flag used to derive mean territory values for a given wood.

## Spatial and Temporal Coverage
- Spatial: 74 woods in 14 English counties; coordinates in OSGB (British National Grid).
- Temporal: 2002–2020, with variation in the number of years surveyed per wood.

## Data Provenance and Access
- Area and classification informed by Forestry Commission National Forest Inventory England (2015) and Natural England Ancient Woodland Inventory (2019).
- Acknowledgements to data collectors and landowners.
- Foundational references include Broughton et al. (2010, 2012, 2014, 2018) and BirdTrends 2018.

## Use and Implications for Analysis
- Suitable for time-series analyses of Marsh Tit territory occupancy and trend assessment across woodlands.
- Rich metadata supports reproducibility and data governance, including method, spatial context, survey completeness, and data quality notes.