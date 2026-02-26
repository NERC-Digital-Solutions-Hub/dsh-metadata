# Description Location of lightning strikes in Nyungwe National Park, Rwanda, with associated strike-level and treelevel attributes and photographs.

- Objective and context
  - Document locations of lightning strikes in Nyungwe National Park with associated strike-level and tree-level attributes and photographs.
  - Assess canopy disturbances as flashover damage and examine whether patterns align with lightning damage; compare 2022 and 2023 survey results; provide a dataset suitable for monitoring and evaluation of disturbance impacts.

- Study design and sampling regime
  - Fieldwork along 23.3 km of trails in Nyungwe National Park (June 2022), covering most trails accessible from Uwinka station.
  - Visual assessment of canopy disturbances to identify probable flashover events; presumptive struck trees identified as canopy trees at the center of disturbance patterns.
  - Tree-level surveys conducted for strikes with diameter at breast height (DBH) > 50 cm within strike areas.
  - Subset of trails resurveyed in October 2023 to revisit existing strike locations and survey new disturbances; photographs captured at a subset of locations, mostly during 2023 resurveys.

- Data collection approach and key variables
  - Strike-level identification and location
    - Each potential strike assigned a unique StrikeID and GPS coordinates recorded (WGS84).
    - Qualitative confidence in lightning attribution recorded (QualitativeAssessment).
    - YearFound (2022 or 2023) and topographic category (TopoCat: ridge, slope, valley).
    - ForestType (open forest or closed canopy).
  - Strike outcomes and canopy impact
    - Damaged_total and Dead_total per strike; records by size class: Damaged/Dead for 1-10 cm, 10-30 cm, 30-50 cm, >50 cm (ov50cm).
    - LaggedDead counts indicate trees that were alive in 2022 but dead by 2023 within each size class.
  - Tree-level surveys within each strike
    - For each TreeID within a StrikeID and YearFound (2022 or 2023): Genus, Species, DBH, TreeHeight.
    - Dieback_initial (initial leaf-volume loss) and CrownForm_initial (initial crown/branch loss index).
    - Dieback_23 and CrownForm_23 (2023 updates).
    - Notes for tree-level observations.
  - Additional contextual data
    - Notes at strike and tree levels; forest type and topography influence on flashover likelihood.
  - Documentation and linking
    - Strike_locations.csv provides strike-level coordinates; Strike_surveys.csv provides strike-level metrics; Tree_surveys.csv provides tree-level metrics.
    - StrikeID serves as the key to join datasets; photographs linked using strike-level identifiers (e.g., T15_1 for strike T15).

- Field instrumentation and measurement methods
  - GPS: Garmin Etrex 22X used to record strike locations.
  - Diameter measurement: 5 m or 10 m diameter tapes.
  - Height: Nikon Forestry Pro II laser range finder.
  - Damage assessment: qualitative confidence based on canopy disturbance patterns compared with reference damage patterns from remote lightning locations in Panama.

- Data quality control and structure
  - Data cross-checked against original field data sheets (quality control).
  - Data structure: 
    - strike_locations.csv (StrikeID, Longitude, Latitude)
    - Strike_surveys.csv (StrikeID, QualitativeAssessment, YearFound, TopoCat, ForestType, Damaged_total, Dead_total, Damaged_1-10cm, Dead_1_10cm, LaggedDead_1_10cm, Damaged_10-30cm, Dead_10-30cm, LaggedDead_10-30cm, Damaged_30-50cm, Dead_30-50cm, LaggedDead_30-50cm, Damaged_ov50cm, Dead_ov50cm, LaggedDead_ov50cm, Notes)
    - Tree_surveys.csv (StrikeID, TreeID, YearFound, Genus, Species, DBH, TreeHeight, Dieback_initial, CrownForm_initial, Dieback_23, CrownForm_23, Notes)
  - Photographs are stored and prefixed with the corresponding strike-level identifier (e.g., T15_1).

- Data applicability and governance considerations
  - Provides a structured, linkable dataset suitable for monitoring frameworks to evaluate lightning-related canopy damage and tree mortality over time.
  - Includes metadata on location, habitat context, and damage metrics to support transparency and reproducibility.
  - Potential limitations include field sampling being limited to accessible trails, reliance on qualitative confidence for strike attribution, and data gaps between years or size classes.