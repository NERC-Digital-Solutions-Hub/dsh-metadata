# Extra cellular enzyme activity from the PLACE project

## Overview
- Data on soil extracellular enzyme potential activities (EEA_FINAL) from the Phosphorus Limitation And ecosystem responses to Carbon dioxide Enrichment (PLACE) project.
- Collected from Autumn 2018 and analyzed in the laboratory at Wageningen University.
- Measures rate of enzyme activity to assess soil functional responses to environmental conditions.

## Study context and location
- Experimental setup uses 35 cm x 35 cm turf mesocosms from a long-term nutrient manipulation experiment.
- Original site: Wardlow Hay Cop in the Peak District, UK.
- Two adjacent P-limited grass lands on different soil types: limestone/calcareous and acidic soils.
- Long-term nutrient manipulation for more than 20 years.
- CO2 fumigation levels: ambient (~410 ppm) and 600 ppm.

## Experimental design
- Grassland ecosystems categorized by GRASS: acid (acidic) or calcareous (limestone/calcareous).
- Nutrient treatments (TREAT): P (phosphorus 3.5 g m-2 y-1), 0N (control with deionised water), LN (nitrogen 3.5 g m-2 y-1), HN (nitrogen 14 g m-2 y-1).
- Depth of soil samples: 0-10 cm or 10-20 cm (DEPTH).

## Data fields and schema
- LOCATION: Experimental plot ID; Units: String.
- PAIR: Block identifier; Units: Numeric.
- CO2: Level of CO2 fumigation; Units: String (A = ambient; E = 600 ppm).
- GRASS: Grassland ecosystem type; Units: String (acid = acidic; calc = calcareous).
- TREAT: Nutrient treatment; Units: String (P, 0N, LN, HN).
- DEPTH: Depth from soil profile; Units: String (0-10, 10-20).
- FL_MATRIX: Fluorescent matrix; Units: String (MUF, AMC).
- ENZYME: Enzyme type; Units: String (BG, CB, NAG, LAP, AP).
- EEA_FINAL: Rate of enzyme activity; Units: Nmol g-1 h-1.

## Measurements and outputs
- EEA_FINAL represents potential enzymatic activity rates for selected enzymes:
  - BG = β-glucosidase
  - CB = cellobiohydrolase
  - NAG = N-acetyl-β-D-glucosaminidase
  - LAP = leucine aminopeptidase
  - AP = acid phosphatase
- Enzymes measured across different fluorescent matrices (MUF, AMC) to indicate activity under varying conditions.

## Relevance for environmental monitoring
- Provides standardized, comparable data to evaluate soil functional responses to CO2 enrichment and nutrient manipulation.
- Enables cross-site data integration and temporal monitoring of microbial enzyme activity as an indicator of soil health and nutrient cycling.

## Data provenance and access considerations
- Data originate from PLACE project activities (Autumn 2018 sampling; Wageningen University analysis).
- Part of an ongoing effort to store and share environmental monitoring datasets through appropriate portals, aligning with aims to increase data value and accessibility.