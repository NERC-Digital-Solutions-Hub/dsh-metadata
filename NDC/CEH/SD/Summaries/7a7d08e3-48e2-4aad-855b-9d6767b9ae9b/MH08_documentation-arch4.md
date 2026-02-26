# Vegetation plot data and peat depths from Moor House National Nature Reserve, 2008-09

## Overview
- Dataset of plant species recorded from plots in Moor House National Nature Reserve (NNR) and associated plot information (slope, aspect, peat depth, vegetation height).
- Focus area: Troutbeck catchment of the Moor House-Upper Teesdale NNR; altitude 290–850 m; one of Britain’s largest blanket bog moorlands.
- Time period: surveys conducted June–August 2008 and July–August 2009 (with a few additional plots surveyed in 2012).
- Data collected to support re-surveying a portion of the reserve (previous survey over 50 years earlier).

## Dataset details
- Data categories:
  - Vegetation species
  - Peat depth
  - Plot data
- Sampling design:
  - Grid-based sampling with plots spaced at 200 m intervals (some 100 m), located with GPS.
  - Plot size: 2 × 2 m.
  - General plot information: plot number, location type, slope, aspect, peat depth, vegetation height; year of survey; altitude where available.
  - Vegetation data: presence/absence and percentage cover (to the nearest 5%) for recorded species.
- Survey completeness and accuracy:
  - Full training provided to surveyors; species lists checked for accuracy.
- Data accessibility:
  - Two CSV files provided:
    - MH08_VEGETATION_PLOTS.csv: plot header information and peat depths; coordinates in OSGB36; year of survey; altitude data.
    - Vegetation species information: species codes, scientific names, common names, and total cover per species.

## Data structure and fields
- MH08_VEGETATION_PLOTS.csv
  - REP_ID: plot name
  - SLOPE, ASPECT, VEG_HT_AVE: slope, aspect, average vegetation height (cm)
  - PEAT_DEPTH: peat depth (cm)
  - ALT: altitude (m; 0 if not recorded)
  - LOCATION: location type description
  - X_COORD, Y_COORD: OSGB1936 easting/northing (m)
  - YEAR: year of survey
- Vegetation species information
  - REP_ID: plot name
  - BRC_NUMBER: Biological Record Centre species code
  - BRC_NAMES: scientific name (Stace, 1997)
  - COMMON_NAME: common name (where available)
  - TOTAL_COVER: total cover percentage (to the nearest 1%; recorded as %)

## Origin and key references
- Originators / surveyors: R.J. Rose, C.M. Wood, N. Ostle, C. Turner, M. Whitfield, R.J. Rose, C.M. Wood, B. Driscoll, A. Looker, G. Looker; University of Cumbria; Centre for Ecology and Hydrology, Lancaster.
- Context: Moor House is England’s highest and largest terrestrial NNR; detailed description of habitat and geology provided.
- Related works:
  - Eddy, A., Welch, D. & Rawes, M. (1969) Vegetatio: vegetation of Moor House NNR.
  - Maskell et al. (2008) Vegetation Plots Handbook CS Technical Report No.2/07, CEH Lancaster.
  - Stace, C. (1997) New Flora of the British Isles.

## Relevance for data leadership
- Demonstrates end-to-end data lifecycle considerations:
  - Clear survey design and sampling strategy (grid-based, plot-level measurements, standardized protocols).
  - Structured data capture and metadata (plot headers, coordinates, year, altitude, vegetation height).
  - Data quality and standardization practices (training, accuracy checks; use of established codes and taxonomic references).
  - Data discoverability and reuse potential via explicit data structure and CSV-based formats.
- Opportunities for enhancement and reuse:
  - Integration with other ecological datasets (e.g., long-term vegetation monitoring, peat depth trends, GIS layers).
  - Potential for time-series analysis across years (2008, 2009, and 2012 plots) to study vegetation dynamics and peat depths.
  - Emphasis on metadata completeness (coordinate systems, units, recording standards) to improve discoverability and interoperability.
- Potential challenges to consider in similar initiatives:
  - Time constraints limiting survey extent; grid spacing may affect spatial representativeness.
  - Variability in data granularity (e.g., 0 for unrecorded altitude) and need for clear documentation of missing values.
  - Dependence on taxonomic references and consistent coding (BRC codes) for cross-dataset compatibility.