# Vegetation plot data from a survey of Moor House National Nature Reserve, 2008-09

## Overview
- A vegetation survey of plots within Moor House National Nature Reserve (Troutbeck catchment), focusing on plant species presence/abundance, peat depth, and plot metadata.
- Re-survey conducted in 2008 (June–August) and 2009 (July–August); a few additional plots surveyed in 2012.
- Data designed for GIS use to map spatial patterns of vegetation and associated environmental variables.

## Spatial and temporal coverage
- Geographic area: Moor House National Nature Reserve, England; Troutbeck catchment within the reserve.
- Time period: June–August 2008 and July–August 2009 (some plots in 2012).
- Altitude range: 290–850 m; georeferenced plots using OSGB1936 coordinates (easting/northing).

## Data collection and methods
- Survey design: grid-based sampling with plots spaced at 200 m intervals (some at 100 m); GPS-located plots.
- Plot size: 2 x 2 meters.
- Data collected per plot:
  - Header information: plot number/name, location type, slope, aspect, vegetation height, peat depth, altitude.
  - Vegetation data: species presence/absence and percent cover (to the nearest 5%), vegetation height measurements (average of three measurements).
- Peat depth measured with an extendable pole.
- Data capture: electronic tablet with customized software (adapted from Countryside Survey 2007); plots trained and checked for accuracy.
- Data structure: two CSV files (see below).

## Data structure and contents
- MH08_VEGETATION_PLOTS.csv
  - Plot information and peat depths: REP_ID (plot name), SLOPE, ASPECT, VEG_HT_AVE (average vegetation height in cm), PEAT_DEPTH (cm), ALT (altitude in m, 0 if not recorded), LOCATION (location type), X_COORD (OSGB1936 eastings, m), Y_COORD (OSGB1936 northings, m), YEAR (survey year)
- Vegetation species information
  - REP_ID (plot name), BRC_NUMBER (species code), BRC_NAMES (scientific name, per Stace 1997), COMMON_NAME (common name, where available), TOTAL_COVER (percent cover, to nearest 5%)
- Data completeness: year included to reflect multiple survey periods; species lists checked for accuracy.

## Data quality, provenance, and references
- Originators and survey team: Rose, Wood, Ostle, Turner, Whitfield, Looker, Driscoll, and colleagues; led by University of Cumbria; coordination by Centre for Ecology and Hydrology, Lancaster.
- Context: Moor House is England’s highest and largest terrestrial NNR, with blanket bog and peat depths of 2–3 m; survey re-visits a 50-year gap since the 1969 baseline (Eddy et al., 1969).
- Key documents and publications:
  - Field survey handbook
  - Maskell et al. (2008) Vegetation Plots Handbook (CS Technical Report No. 2/07)
  - Stace (1997) New Flora of the British Isles
- Quality assurance: full training for surveyors; species lists cross-checked for accuracy.