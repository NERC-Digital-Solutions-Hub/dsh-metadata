# Metadata for Marsh Tit ( Poecile palustris ) territory surveys in English woods during 2002-2020

## Overview
- Annual surveys of occupied Marsh Tit territories in individual woods and woodland patches, conducted in early spring to reflect breeding territories.
- Timeframe: 2002–2020; spatial scope: 74 woods across 14 English counties, with a focus on Cambridgeshire and Oxfordshire.
- Purpose: monitor a declining species (80% decline 1967–2018) and support population trend analyses and habitat associations.

## Data scope and structure
- Georeferenced dataset stored as CSV with the following columns: Wood_id, Wood, County, OSGB X, OSGB Y, Survey year, Time Series Analysis, Wood area (ha), Complete or Partial survey, Woodland type (ASNW, PAWS, NEW WOODLAND), Marsh Tit territories, Method (Playback or CR).
- Spatial reference: OSGB (British National Grid) coordinates.
- Time-series flag indicates if a wood is used in time-series analysis to derive mean territory values.

## Data collection and methods
- Primary method: Playback surveys (recorded song/calls to locate territories); detailed protocol described in Broughton et al. (2018).
- Supplementary: Colour-ringing (CR) conducted in some woods during intensive projects; may be combined with playback.
- Coverage: 74 woods in 14 counties; some woods surveyed in a single spring, others annually for up to 17 consecutive springs.
- Survey area defined using Forestry Commission National Forest Inventory England 2015; woodland type categorized by Ancient Woodland Inventory (AWI).
- Woodland classifications:
  - ASNW: Ancient Semi-Natural Woodland (pre-1600)
  - PAWS: Planted Ancient Woodland Site
  - NEW WOODLAND: post-1600 woodlands

## Data quality and reliability
- Territory counts are regarded as very reliable.
- Playback method validated to locate a mean 96% of birds present.
- No significant difference in territory estimates for marked vs unmarked birds; potential underestimation of ~10% in larger woods (>70 ha).

## Data contents and interpretation notes
- Marsh Tit territories: number of breeding territories estimated from surveys.
- Complete vs partial surveys indicate whether whole wood/patch were assessed or only a portion.
- Time-series analysis flag (1 = used, 0 = not used) facilitates aggregation of mean territory values across woods.

## Potential uses (Data Support perspective)
- Build trend analyses of Marsh Tit occupancy over time and space.
- Create dashboards or reports to explore territory dynamics by wood type (ASNW/PAWS/NEW), size, and location.
- Integrate with woodland inventories (AWI, NFI data) to examine habitat associations and conservation implications.
- Compare with other monitoring datasets (e.g., BirdTrends) to contextualize population changes.

## Provenance and references
- Acknowledgements to data collectors and landowners.
- Core methodological references: Broughton et al. (2010, 2012a, 2012b, 2014, 2018); Forestry Commission (2019); Natural England (2019); BirdTrends 2018.
- Data sources for inventory classifications: Forestry Commission National Forest Inventory England 2015; Ancient Woodland Inventory (England).