# Experimental design / sampling regime

## Overview
- Study location: three oil palm estates in Riau Province, Sumatra, Indonesia, owned by Pt Ivo Mas Tunggal (Ujung Tanjung, Kandista, Libo).
- Timeframe and scope: part of the BEFTA project; plots established in 2013 to study vegetation management; mature stands (Ujung Tanjung and Kandista) and replanted stands (Libo).

## Location and plots
- Estate details: estates planted 1987–1995 on mineral soils; plots arranged within each estate.
- Experimental layout: 18 plots in total, each 50 x 50 meters; 50 m from access tracks on three sides, ~1000 m from the fourth side.
- Sampling design within plots: each palm has a number; three sampling positions marked on the plot edge at 45°, 165°, and 285° from compass north.
- Plot categorisation: mature stands (Ujung Tanjung and Kandista) vs replanted stands (Libo, replanted 2014).

## Experimental design specifics
- Predation measurements: conducted in 2014 (mature) and 2016–2017 (mature and replanted).
- predation unit and method: six freshly-killed mealworms glued to trimmed palm frond segments; exposed for ~24 hours.
- Treatments: factorial combination of canopy vs ground and caged vs uncaged (vertebrate exclusion achieved with rat-trap cages).
- Vertical testing: one exclosure palm in the crown and one at the edge of the harvesting circle per palm.
- Randomisation: three sets of treatment combinations per plot chosen by random-number generator.
- Basic response: number of mealworms remaining (out of six) after exposure.

## Data collected and variables
- Core response variable: worms_remaining (0–6).
- Treatment descriptor: wormtreat (e.g., Remain_top_nocage, Remain_top_cage, Remain_base_nocage, Remain_base_cage).
- Spatial and temporal identifiers: Estate_abbrev, Plot_no, Palm, Period, Date_set, Time_set, Date_coll, Time_coll.
- Additional contextual fields: Ants characteristic (if applicable), Ants Quantity (approximate), dayrain (24-hour rainfall at nearest station), distance (applicable to replants; distance to palm center from an ant-exclosure experiment; exclusion radius details).
- Data quality notes: All_notes includes observations and data-check notes; fields indicate whether data were checked against original field sheets and any changes.

## Data quality and management
- Quality control: basic checks for impossible values, date ranges, and correct formatting; 50% data-entry checks against original field sheets with an error rate <1%; changes recorded with provenance.

## Data formats and storage
- Files (three CSVs in thin format; one observation per line):
  - MealwormPredationRates_2013_2014.csv (mature stands, BEFTA core plots)
  - MealwormPredationRates_2016_2017.csv (mature stands, BEFTA core plots, funded by NERC)
  - MealwormPredationRates_replants.csv (replanted stands, Libo estate; NERC-funded)
- Key fields (illustrative): Estate_abbrev, Plot_no, Treatment, Palm, Period, Date_set, Time_set, Date_coll, Time_coll, wormtreat, worms_remaining, Ants characteristic, Ants Quantity, All_notes, dayrain, distance.
- Data structure: “thin format” with one record per observation; plot metadata (Plot_no, Triplet, etc.) supports linking observations to specific plots and palms.

## Geographic context and GIS readiness
- Geographic scope: three estates with defined boundaries in Sumatra; plot locations and sampling positions enable spatial analysis.
- Plot-level georeferencing: coordinates and plot mappings are provided to support geospatial visualization and analyses (mature vs replanted plots, canopy/ground strata, and exclosure proximity).
- Temporal context: discrete sampling periods across 2013–2014, 2016–2017, enabling time-series map-based visualizations.
- GIS opportunities: map predation rates by estate, plot, palm, and treatment; incorporate rain data and proximity to ant-exclosures; compare mature vs replanted stands; integrate with other spatial datasets for biodiversity and ecosystem-function analyses.

## Provenance and funding
- Funding reference: NE/P00458X/1.
- Data provenance: BEFTA core plots (KNDE and UTNE) 2013–2014; BEFTA core plots 2016–2017; replanted plots (LIBE) 2016–2017; all under NERC funding for later datasets.