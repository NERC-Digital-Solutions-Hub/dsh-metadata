# Sunflower seed predation rates in Biodiversity and Ecosystem Function in Tropical Agriculture (BEFTA) plots, Sumatra, Indonesia

## Overview
- Study of granivory (seed predation) on sunflower seeds within BEFTA plots across three estates in Riau Province, Sumatra.
- Data collected from 2014 (mature stands) and 2016–2017 (mature and replanted stands); replanted plots have a separate dataset.
- Data intended for spatial analysis and map-based representation of predation rates across plots, treatments, and sampling times.

## Experimental design and sampling regime
- Location: three Pt Ivo Mas Tunggal estates in Riau: Ujung Tanjung, Kandista, Libo; plots sized 50 x 50 m with internal 50 m spacing from edges and ~1000 m to one track.
- Plot structure: 18 plots established in 2013; each palm numbered with three sampling positions at 45°, 165°, and 285° from compass north.
- Sampling timeline:
  - 2014: granivory measured once in mature oil palm.
  - 2016–2017: measured five times in both mature and replanted stands.
- Field method:
  - Ten shelled sunflower seeds placed on a 15 cm paper disc, covered by a 10 cm high plate to shield from rain.
  - Four treatments using combinations of cage and grease: cage + grease, cage only, grease only, and open.
  - Test apparatus: metal grid boxes (approx. 35 x 20 x 14 cm); exposure ~24 hours per replication.
  - One test per sampling position per plot.

## Data recording and units
- Primary outcome: total seeds remaining (seedsremaining), out of ten (values may be decimals if partial seeds recorded).
- Date/time fields for seed placement and retrieval:
  - Date_set, Time_set (when seeds were placed)
  - Date_coll, Time_coll (when seeds remaining were counted)
- Spatial and experimental identifiers:
  - Estate_abbrev, Plot_no (e.g., C01), Triplet (plot sets of three), Position (bearing from plot center)
  - Period (discrete sampling periods), Treatment (management since Feb 2014)
  - seedstreat (remain_cage, remain_open, remain_cage_grease, remain_open_grease)
  - Dayrain (24 h rainfall at nearest weather station)
  - allnotes (field observations, data entry changes)
  - SAFE_distance (replants only; distance from exclosure center where ant poison was applied; data may indicate not suitable for use)

## Data structure and storage
- Data format: thin format CSV files (one observation per line).
- Files:
  - SunflowerSeedPredationRates_2014.csv (mature stands)
  - SunflowerSeedPredationRates_2016_2017.csv (core mature plots)
  - SunflowerSeedPredationRates_replants.csv (replanted plots)
- Key headers and fields:
  - Estate_abbrev, Plot_no, Triplet, Position
  - Period, Date_set, Time_set, Date_coll, Time_coll
  - seedstreat, seedsremaining, dayrain, allnotes
  - SAFE_distance (replants only)

## Data quality and provenance
- Basic quality checks performed:
  - Checks for impossible values (e.g., more seeds remaining than were placed)
  - 50% of data entry validated against original field sheets; error rate <1%
  - All corrections recorded with an audit trail

## Spatial and GIS relevance
- Plot-level spatial identifiers enable mapping of predation rates by estate, plot, and sampling position.
- Position field provides directional context relative to plot center; allows spatial interpolation and visualization of within-plot variability.
- Coordinate information referenced in Miscellaneous (examples given for mature and replanted plots), facilitating georeferencing and integration with other GIS layers.
- Rainfall (dayrain) and timing information support temporal analyses and correlation with predation rates.

## Scope and accessibility
- Data covers BEFTA core plots (2016–2017) and replanted plots, plus 2014 data for mature stands.
- Metadata includes plot naming conventions (Estate_abbrev, Plot_no), process descriptions, and data lineage (funding reference NE/P00458X/1).

## Notes for GIS analysts
- When integrating into GIS:
  - Use Estate_abbrev and Plot_no to join with plot geometry or shapefiles; utilize Triplet and Position for internal sampling geometry.
  - Use Date_set/Time_set and Date_coll/Time_coll to build temporal layers and time series dashboards of predation.
  - Combine seedsremaining with seedstreat to map treatment effects spatially.
  - Include dayrain as a contextual raster or attribute for rainfall-driven analyses.
  - For replants, consider SAFE_distance as a potential confounder or filter, noting its applicability is limited to replanted data.