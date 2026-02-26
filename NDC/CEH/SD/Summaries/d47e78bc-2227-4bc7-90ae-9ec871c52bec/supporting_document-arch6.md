# Description

- Purpose: Document the location and characteristics of lightning strikes in Nyungwe National Park, Rwanda, including strike-level and tree-level attributes and accompanying photographs.

- Sampling regime:
  - Fieldwork spanned 23.3 km of trails in June 2022, focusing on trails accessible from Uwinka station to assess canopy disturbances and potential flashover damage.
  - Suspected directly struck trees identified as canopy trees at centers of observed damage patterns; tree-level surveys conducted for trees with DBH > 50 cm within strike areas.
  - A subset of trails re-surveyed in October 2023 (existing strike locations and new disturbances); photographs collected at selected locations, mainly during 2023 resurveys.

- Data collection methods:
  - Each potential strike assigned a unique StrikeID; GPS coordinates recorded for strike locations.
  - Qualitative confidence in lightning origin assessed based on canopy damage patterns, using remote lightning location patterns from Panama as a reference.
  - Metrics recorded: number of damaged and dead trees by size classes (<10 cm, 10–30 cm, 30–50 cm, >50 cm); forest type (open vs. closed canopy); topographic position (ridge, slope, valley).
  - Tree-level surveys included crown dieback (percent leaf volume lost), crown loss (percent branch volume lost), tree height, and DBH; 2023 surveys estimated size class instead of precise DBH.

- Fieldwork instrumentation:
  - Strike locations recorded with Garmin Etrex 22X GPS.
  - DBH measured with 5 m or 10 m diameter tapes; tree height measured with Nikon Forestry Pro II laser range finder.

- Nature and units of recorded values:
  - Strike_locations.csv: StrikeID, Longitude (WGS84), Latitude (WGS84).
  - Strike_surveys.csv: StrikeID, QualitativeAssessment, YearFound (2022/2023), TopoCat (ridge/slope/valley), ForestType (open/closed), Damaged_total, Dead_total, Damaged_1-10cm, Dead_1_10cm, LaggedDead_1_10cm, Damaged_10-30cm, Dead_10-30cm, LaggedDead_10-30cm, Damaged_30-50cm, Dead_30-50cm, LaggedDead_30-50cm, Damaged_ov50cm, Dead_ov50cm, LaggedDead_ov50cm, Notes.
  - Tree_surveys.csv: StrikeID, TreeID, YearFound, Genus, Species, DBH (cm), TreeHeight (m), Dieback_initial, CrownForm_initial, Dieback_23, CrownForm_23, Notes.

- Data structure and linkage:
  - Strike locations are in strike_locations.csv; strike-level metrics in Strike_surveys.csv; tree-level metrics in Tree_surveys.csv.
  - StrikeID serves as the key to join strike-level and tree-level data.
  - Photographs are linked by strike-level identifiers (e.g., T15_1 for strike T15).

- Quality control:
  - Data input checked against original field data sheets to ensure accuracy.

- Accessibility and usage notes:
  - Data are organized to enable analysis of patterns across strikes, forest types, topography, and tree size classes, with year-over-year comparisons (2022 vs. 2023).
  - Photos accompany strike records and are named with the corresponding StrikeID prefix for traceability.
  - Some limitations include reliance on qualitative confidence for strike identification, partial resurvey in 2023, and size class estimates in 2023 instead of exact measurements.