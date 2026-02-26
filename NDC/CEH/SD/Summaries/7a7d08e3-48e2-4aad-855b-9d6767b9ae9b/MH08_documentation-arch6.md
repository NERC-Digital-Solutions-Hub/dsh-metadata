# Vegetation plot data from a survey of Moor House National Nature Reserve, 2008-09

## Overview
- Documents plant species recorded from plots in Moor House NNR and associated plot information (slope, aspect, peat depth, vegetation height, etc.).
- Timeframe: surveys in June–August 2008 and July–August 2009; a few additional plots surveyed in 2012.
- Area: Troutbeck catchment within Moor House-Upper Teesdale NNR; grid-based sampling with plots 2x2 m, spaced 200 m apart (some 100 m).
- Purpose: re-survey part of the reserve due to the previous vegetation data being over 50 years old; focus area dominated by Calluna vulgaris and Eriophorum vaginatum.
- Data collected: presence/abundance of plant species with approximate 5% cover increments and header plot data.

## Data Content
- Data categories:
  - Vegetation species: species codes, scientific names, common names, and total cover percentages.
  - Peat depth.
  - Plot data: plot name, slope, aspect, average vegetation height, altitude, location type, coordinates, and year.
- File structure (two CSV files):
  - MH08_VEGETATION_PLOTS.csv: header/plot data and peat depths with fields such as REP_ID, SLOPE, ASPECT, VEG_HT_AVE, PEAT_DEPTH, ALT, LOCATION, X_COORD, Y_COORD, YEAR.
  - Vegetation species information: BRC_NUMBER, BRC_NAMES (scientific name), COMMON_NAME, TOTAL_COVER; linked to plots by REP_ID.
- Coordinates: OSGB36; units include meters for coordinates and height, centimeters for peat depth.

## Survey Methodology
- Plot design: 2x2 m quadrats; 200 m grid spacing (some plots at 100 m).
- Measurements per plot: altitude, slope, aspect, vegetation height (average of 3 measurements), peat depth; presence and percent cover of species (to nearest 5%).
- Data capture: electronic tablet with software adapted from Countryside Survey 2007; full training provided; species lists checked for accuracy.

## Provenance and Documentation
- Originator/Surveyors: Rose, R.J.; Wood, C.M.; Ostle, N.; Turner, C.; Whitfield, M.; Looker, A.; Looker, G.; University of Cumbria; coordinated by Centre for Ecology and Hydrology, Lancaster.
- Context: Moor House is England’s highest and largest terrestrial NNR with blanket bog habitats; rationale for re-survey in 2008 due to older data (1960s).
- Key documents: Field Survey Handbook (CS Technical Report No. 2/07); related publications Eddy et al. 1969; Stace 1997.

## Temporal and Geographic Coverage
- Time Period: June–August 2008 and July–August 2009; some plots surveyed in 2012.
- Geographic: Troutbeck catchment area of Moor House NNR; location data provided via OSGB36 coordinates.

## Access, Format, and Usage
- Data formats: CSV files as described above.
- Coordinate system and units: OSGB36; coordinates in meters; peat depth and vegetation height in centimeters.
- Potential uses: vegetation and habitat analyses, species distribution, peat depth relationships, and development of self-serve data products or dashboards for conservation planning.

## References
- Eddy, A., Welch, D. & Rawes, M. (1969). The vegetation of Moor House National Nature Reserve in the North Pennines, England. Vegetatio, 16, 239-284.
- Maskell, L. C. et al. (2008). Vegetation Plots Handbook CS Technical Report No.2/07. Centre for Ecology and Hydrology, Lancaster.
- Stace, C. (1997). New flora of the British Isles. Cambridge University Press.