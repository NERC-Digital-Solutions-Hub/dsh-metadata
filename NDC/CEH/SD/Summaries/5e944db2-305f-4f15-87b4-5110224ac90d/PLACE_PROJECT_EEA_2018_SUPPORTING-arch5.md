# Extra cellular enzyme activity from the PLACE project

## Overview
- Dataset of soil extracellular enzyme potential activities measured from the PLACE project.
- Autumn 2018 soil samples analyzed in Wageningen University.
- Experimental design uses 35 cm x 35 cm turf mesocosms from a long-term nutrient manipulation experiment at Wardlow Hay Cop, Peak District, UK.
- Two adjacent P-limited grass lands with calcareous (limestone) and acidic soils; nutrient manipulation for over 20 years; 2018 exposure to ambient CO2 (~410 ppm) or 600 ppm CO2.

## Dataset purpose and scope
- Captures potential extracellular enzyme activities under varying CO2 and nutrient treatments to inform soil biogeochemical responses to nutrient status and elevated CO2.

## Data collection and provenance
- Location: Wardlow Hay Cop experimental plots; data organized by experimental plot ID and block.
- Timeframe: Autumn 2018.
- Analysis performed at Wageningen University; part of the PLACE project.

## Data structure and fields
- Variables and descriptions:
  - LOCATION: Experimental plot ID; Units: String.
  - PAIR: Block; Units: Numeric.
  - CO 2: Level of CO2 fumigation; Units: String (A = ambient; E = 600 ppm).
  - GRASS: Grassland ecosystem type; Units: String (acid = acidic; calc = calcareous).
  - TREAT: Nutrient treatment; Units: String (P = Phosphorus; 0N = control; LN = Nitrogen; HN = Nitrogen high).
  - DEPTH: Depth of sample from soil profile; Units: String (0-10 = 0 to 10 cm; 10-20 = 10 to 20 cm).
  - FL_MATRIX: Fluorescent matrix; Units: String (MUF; AMC).
  - ENZYME: Extracellular enzyme; Units: String (BG, CB, NAG, LAP, AP).
  - EEA_FINAL: Rate of enzyme activity; Units: Nmol g^-1 h^-1.
- All fields include descriptive labels and corresponding units to support interpretation and reuse.

## Metadata and data quality considerations
- Detailed field descriptions and units enable consistent interpretation across datasets.
- Need for consistent coding of CO2, GRASS, and TREAT categories to ensure interoperability.

## Data governance and sharing considerations
- Data tied to a specific long-term experiment; track dataset versioning and provenance.
- Confirm licensing, access conditions, and any embargoes; consider inclusion in appropriate data portals with proper citation.

## Stewardship actions and recommendations
- Validate completeness and consistency of:
  - Location IDs, block IDs (PAIR), CO2 category values, grass types, nutrient treatments.
  - Enzyme codes and associated units; ensure EEA_FINAL values are in the stated nmol g^-1 h^-1.
  - Depth categorizations (0-10, 10-20 cm).
- Document any data processing steps (e.g., conversions from raw fluorescence to enzyme activity) to maintain reproducibility.
- Consider adopting controlled vocabularies or ontologies for stressors, substrates, and enzyme codes to improve interoperability with other datasets.