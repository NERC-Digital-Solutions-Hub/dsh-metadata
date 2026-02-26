# Location of lightning strikes in Nyungwe National Park, Rwanda, with associated strike-level and treelevel attributes and photographs.

## Overview
- Dataset documenting locations of lightning strikes in Nyungwe National Park, Rwanda, with associated strike-level and tree-level damage data and photographs.
- Collected through field surveys in 2022 and 2023, with additional resurvey efforts and photography.
- Data are organized to allow linking across strike-level and tree-level observations via unique identifiers.

## Sampling regime and field methods
- 2022: Walked 23.3 km of trails from Uwinka station to survey canopy disturbances and potential flashover damage.
- Identified presumptive directly struck trees as canopy trees at the center of observed damage patterns; included other trees >50 cm DBH within the strike area.
- 2023: Subsets of trails resurveyed to revisit prior strike locations and survey new disturbances; photographs collected on a subset of locations (primarily 2023).
- Qualitative confidence in lightning causation rated based on damage patterns compared to remote lightning location references (Panama data used as a reference).
- Data captured include canopy disturbance patterns, damage counts by size class, forest type (open vs closed canopy), topographic position (ridge, slope, valley), and mortality/damage changes between surveys.

## Data collection and contents
- Strike locations: unique StrikeID with geographic coordinates (Longitude, Latitude) in decimal degrees (WGS84).
- Strike surveys (strike-level data): StrikeID, YearFound (2022 or 2023), QualitativeAssessment, TopoCat (ridge/slope/valley), ForestType (open/closed canopy), Damaged_total, Dead_total, and damage counts by size class (1–10 cm, 10–30 cm, 30–50 cm, >50 cm), including lagged (survival in 2022 vs death by 2023) counts, plus Notes.
- Tree surveys (tree-level data): StrikeID, TreeID, YearFound, Genus, Species, DBH (cm), TreeHeight (m), Dieback_initial, CrownForm_initial, Dieback_23, CrownForm_23, Notes.
- Photography: image files associated with strike locations, named using the strike-level identifier (e.g., T15_1 for strike T15).

## Data structure and compatibility
- Strike_locations.csv provides strike-level coordinates.
- Strike_surveys.csv provides strike-level metrics.
- Tree_surveys.csv provides tree-level measurements within each strike area.
- StrikeID serves as the key to join strike-level and tree-level data; TreeID is unique within each StrikeID.
- Photographs are linked by the StrikeID prefix in file names (e.g., T15_1 corresponds to strike T15).

## Instrumentation and measurement units
- Field instruments:
  - GPS: Garmin Etrex 22X for strike locations.
  - Diameter: 5 m or 10 m diameter tapes for DBH.
  - Height: Laser range finder (Nikon Forestry Pro II) for tree height.
- Units:
  - Coordinates: decimal degrees (WGS84).
  - DBH: centimeters.
  - TreeHeight: meters.
  - Dieback and CrownForm: percentages or index values as defined in field sheets.
  - Damage counts: raw counts per category.
- Data quality control: cross-checked against original field data sheets.

## Data quality, provenance, and governance
- Data validated against field data sheets to ensure accuracy of observations and measurements.
- Clear documentation of data structure, field definitions, and units to support reproducibility and interoperability.
- Metadata describe sampling regime, survey timing (2022 and 2023), and criteria for classifying damage and strike causation.
- File naming and identifiers support traceability and data linking across datasets.

## Usage considerations and limitations
- Coverage limited to surveyed trails near Uwinka station; some areas or events may be underrepresented.
- Qualitative assessments of lightning causation depend on damage patterns and reference data.
- Not all strike locations have photographs; photos exist for a subset (primarily 2023 resurveys).
- Some measurements are estimated (e.g., 2023 size-class estimates for tree metrics) where exact measurements were not possible.

## Access and preservation notes for data stewards
- Primary data files: Strike_locations.csv, Strike_surveys.csv, Tree_surveys.csv; photographs with strike-based prefixes.
- Ensure ongoing data governance by maintaining StrikeID and TreeID consistency across releases.
- Document any updates or reclassifications of damage assessments, and preserve historical versions for audit trails.