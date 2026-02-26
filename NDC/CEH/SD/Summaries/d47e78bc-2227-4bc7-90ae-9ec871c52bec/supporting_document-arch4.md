# Description Location of lightning strikes in Nyungwe National Park, Rwanda, with associated strike-level and treelevel attributes and photographs.

## Study design and scope
- Location and objective: documenting lightning strike locations in Nyungwe National Park, Rwanda, with associated strike-level and tree-level attributes and photographs.
- Sampling regime: walked 23.3 km of trails in June 2022 (majority of trails from Uwinka station) to detect canopy disturbances indicating flashover damage; identified presumptive strikes by canopy damage patterns; targeted tree-level surveys for center canopy trees and other trees >50 cm DBH within strike areas.
- Follow-up: subset of trails resurveyed in October 2023, revisiting existing strike locations and surveying new disturbances; photographs collected primarily during 2023 resurveys.
- Damage assessment approach: qualitative confidence in lightning-based canopy disturbance using damage-pattern references from a remote lightning location system in Panama.

## Data collection and variables
- Identification and location: each potential strike has a unique StrikeID and GPS coordinates (longitude, latitude).
- Confidence and timing: QualitativeAssessment (yes/maybe) indicating confidence that a disturbance is a strike; YearFound (2022 or 2023).
- Environmental context: TopoCat (ridge, slope, valley); ForestType (open forest or closed canopy).
- Struck trees metrics (strike-level): Damaged_total, Dead_total; Damaged and Dead counts by size classes (<10 cm, 10-30 cm, 30-50 cm, >50 cm); LaggedDead counts by size class (survivor in 2022 but dead by 2023).
- Survey coverage: notes per strike; disturbance patterns used to infer strike plausibility.
- Tree-level metrics (per struck tree): Genus, Species; DBH (cm); TreeHeight (m); Dieback_initial (percent leaf volume lost); CrownForm_initial (branch-volume loss index); Dieback_23 and CrownForm_23 (2023 estimates); Tree-level notes.
- Context and selection criteria: focus on directly struck canopy trees and other trees >50 cm DBH within strike areas; crown dieback and damage patterns recorded to assess consistency with lightning.

## Fieldwork instrumentation
- Strike location recording: Garmin Etrex 22X handheld GPS.
- Tree diameter: 5 m or 10 m diameter tapes.
- Tree height: Nikon Forestry Pro II laser range finder.

## Data structure and metadata
- Strike_locations.csv: StrikeID, Longitude (WGS84), Latitude (WGS84).
- Strike_surveys.csv: StrikeID, QualitativeAssessment, YearFound, TopoCat, ForestType, Damaged_total, Dead_total, Damaged_1-10cm, Dead_1-10cm, LaggedDead_1-10cm, Damaged_10-30cm, Dead_10-30cm, LaggedDead_10-30cm, Damaged_30-50cm, Dead_30-50cm, LaggedDead_30-50cm, Damaged_ov50cm, Dead_ov50cm, LaggedDead_ov50cm, Notes.
- Tree_surveys.csv: StrikeID, TreeID, YearFound, Genus, Species, DBH, TreeHeight, Dieback_initial, CrownForm_initial, Dieback_23, CrownForm_23, Notes.
- Data linkage: StrikeID serves as the linking key across Strike_locations, Strike_surveys, and Tree_surveys; Tree_surveys are organized by StrikeID and TreeID.
- Photographs: image files prefixed with the strike-level identifier (e.g., T15_1 corresponds to strike T15).

## Units and definitions
- Strike_locations: Longitude and Latitude in decimal degrees (WGS84).
- Strike_surveys and Tree_surveys: field values include counts, percentages, and categorical indices defined in the header; specific size-class counts correspond to the same size cutoffs across records.
- DBH: diameter at breast height (cm).
- TreeHeight: height (m).
- Dieback_initial and Dieback_23: percentage of leaf volume lost.
- CrownForm_initial and CrownForm_23: index of branch volume remaining (5 = nearly intact to 0 = all branches lost).

## Data quality and provenance
- Quality control: data were cross-checked against original field data sheets to ensure accuracy and consistency.

## Temporal coverage
- Surveys conducted in 2022 and 2023, with 2023 data including updated measurements and new strike observations.

## Taxonomic resolution
- Tree identification to genus and, where possible, species; some entries may be indeterminate (indet) if identification was not achieved.

## Practical relevance for data leaders
- Clear, linked data model with three CSV files and a unique StrikeID to enable integrated analyses across strike- and tree-level observations.
- Explicit metadata on scope, methods, confidence, and context to support data governance, discoverability, and reuse.
- Structured, size-class based damage and mortality data enabling temporal analyses of canopy disturbance and tree mortality related to lightning events.
- Photographic records linked to strike records to provide qualitative context for field observations.