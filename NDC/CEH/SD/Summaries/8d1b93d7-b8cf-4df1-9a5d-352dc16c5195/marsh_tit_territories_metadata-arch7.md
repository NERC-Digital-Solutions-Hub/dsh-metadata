# Metadata for Marsh Tit ( Poecile palustris ) territory surveys in English woods during 2002-2020

## Overview
- Annual, georeferenced surveys of the number of occupied Marsh Tit breeding territories within individual woods and woodland patches.
- Surveys conducted in early spring (February–April) prior to nesting to reflect breeding territories.
- Playback method used to locate territories; some woods also involved colour-ringing during intensive projects.
- Study area: 74 woods across 14 English counties (predominantly Cambridgeshire and Oxfordshire) from 2002–2020; some woods surveyed only in a single spring, others annually for up to 17 consecutive springs.

## Spatial data and geospatial context
- Data are georeferenced and stored in a CSV with British National Grid (OSGB) coordinates: OSGB X (easting) and OSGB Y (northing).
- Surveyed area for each wood derived from the Forestry Commission’s National Forest Inventory England 2015.
- Woodland type classification from the Ancient Woodland Inventory (AWI) for England:
  - ASNW: Ancient Semi-Natural Woodland (continuous woodland since 1600)
  - PAWS: Planted Ancient Woodland Site
  - NEW WOODLAND: woodland not in AWI, dating from after 1600

## Data contents and structure
- Core fields (example): Wood_id, Wood, County, OSGB X, OSGB Y, Survey year, Time Series Analysis, Wood area (ha), Completion status (Complete/Partial), Woodland type, Marsh Tit territories, Method.
- Time Series Analysis flag indicates whether a wood is used in time-series analyses to derive mean territory values (1 = yes, 0 = no).
- Provides the number of Marsh Tit territories estimated per wood per survey.

## Methodology
- Primary survey method: Playback following Broughton et al. (2018) protocol.
- Additional data: Some woods surveyed with colour-ringing (CR) in conjunction with playback in detailed population projects.
- Completeness: Most surveys cover the entire defined wood/patch; a few Woods were partially surveyed (Partial).

## Quality and reliability
- Territory counts are considered highly reliable.
- Playback method detects about 96% of birds present; no significant difference in territory estimates between marked and unmarked birds.
- Potential underestimation of ~10% in larger woods (>70 ha).

## Temporal coverage
- Years encompassed: 2002–2020.
- Some woods have single-year data; others have multi-year time series (up to 17 consecutive springs).

## Usage notes and considerations for GIS work
- Ensure OSGB coordinates are used with British National Grid for spatial analyses and mapping.
- Consider separately analyzing complete versus partial surveys to avoid bias in area-derived metrics.
- When integrating with AWI classifications, maintain clear distinctions between ASNW, PAWS, and NEW WOODLAND categories.
- Use the Time Series Analysis field to identify woods included in longitudinal analyses for trend assessment.

## Acknowledgements
- Contributors to data collection: Paul Bellamy, Jane Carpenter, Colin Everett, Jonathan Groom, Alex Inzani, Ash Murray, Simon Tucker.
- Landowners acknowledged for access to private woods.

## References
- Broughton et al. (various years) on playback methodology and habitat occupation.
- Forestry Commission (2019) National Forest Inventory Woodland England 2015.
- Natural England (2019) Ancient Woodland (England).
- BirdTrends 2018: trends in numbers, breeding success and survival for UK breeding birds.