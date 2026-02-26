# Extra extracellular enzyme activity from the PLACE project

## Overview
- Dataset of soil extracellular enzyme potential activities measured from PLACE, tied to a phosphorus limitation and CO2 enrichment study.
- Collected in Autumn 2018 and analyzed in a laboratory at Wageningen University.
- Builds on a long-term nutrient manipulation experiment at Wardlow Hay Cop, Peak District, UK, using turf mesocosms subjected to ambient or elevated CO2.

## Study design and setting
- Location: Wardlow Hay Cop, Peak District, UK.
- Experimental setup: 35 cm x 35 cm turf mesocosms from a long-term nutrient manipulation experiment.
- Treatments: Two adjacent P-limited grass lands on different soils (calcareous/limestone and acidic) with nutrient manipulation for over 20 years.
- CO2 exposure: 2018 mesocosms exposed to ambient CO2 (~410 ppm) or 600 ppm CO2.
- Purpose: Investigate how soil extracellular enzyme activities respond to CO2 enrichment, nutrient treatments, and soil/grass types.

## Data collected
- Field-to-lab workflow: Soil samples collected in autumn 2018 and analyzed in the Wageningen University laboratory.
- Data describe the rate of extracellular enzyme activities in soil, expressed as enzyme activity measurements (EEA_FINAL).

## Variables and data structure
- LOCATION: Experimental plot ID (Units: String). Description: Experimental plot identifier.
- PAIR: Block information (Units: Numeric). Description: Pair or block reference within the design.
- CO 2: Level of CO2 fumigation (Units: String). Description: A = ambient; E = 600 ppm.
- GRASS: Grassland ecosystem type (Units: String). Description: acid = acidic soil; calc = calcareous soil.
- TREAT: Nutrient treatment (Units: String). Description: P = Phosphorus addition (3.5 g m^-2 y^-1); 0N = control (deionised water); LN = Nitrogen addition (3.5 g m^-2 y^-1); HN = Nitrogen addition (14 g m^-2 y^-1).
- DEPTH: Depth of soil sample (Units: String). Description: 0-10 cm or 10-20 cm depth.
- FL_MATRIX: Fluorescent matrix used in assays (Units: String). Description: MUF = 4-Methyllumbelliferone; AMC = 7-Amino-4-methylcoumarin.
- ENZYME: Enzyme type measured (Units: String). Description: BG = β-glucosidase; CB = cellobiohydrolase; NAG = N-acetyl-β-D-glucosaminidase; LAP = leucine aminopeptidase; AP = acid phosphatase.
- EEA_FINAL: Rate of enzyme activity (Units: Nmol g^-1 h^-1). Description: Measured extracellular enzyme activity rate.

## Data quality and use considerations
- Data capture a specific snapshot (Autumn 2018) within a controlled experimental framework combining CO2 fumigation, nutrient treatments, soil types, and depths.
- Variables include categorical factors (CO2 level, GRASS type, TREAT) and continuous or semi-continuous measures (EEA_FINAL, DEPTH, PAIR).
- Documentation provides clear units and descriptions for reproducibility and cross-study comparisons.
- Analysts should consider local-scale context, potential interactions between CO2, nutrient treatment, soil type, depth, and enzyme type when modeling enzyme activity.

## Potential uses for data analysts
- Assess how elevated CO2 and nutrient additions modulate soil extracellular enzyme activities across soil types and depths.
- Examine interactions between CO2 levels, phosphorus limitation, and nitrogen fertilization on enzyme activities.
- Develop predictive models linking environmental treatments to enzyme-mediated soil nutrient cycling processes.
- Compare enzyme activity patterns across enzyme types (BG, CB, NAG, LAP, AP) under different experimental conditions.

## Provenance and metadata
- Data originate from a field-based, long-term nutrient manipulation experiment at Wardlow Hay Cop and were analyzed in a laboratory setting at Wageningen University.
- Metadata fields (LOCATION, PAIR, CO2, GRASS, TREAT, DEPTH, FL_MATRIX, ENZYME, EEA_FINAL) capture the experimental design, treatment assignments, sampling depth, assay specifics, and enzyme activity outcomes.