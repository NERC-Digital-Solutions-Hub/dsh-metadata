# Extra cellular enzyme activity from the PLACE project

## Description
- Soil extracellular enzyme potential activities measured from PLACE project samples.
- Samples collected in Autumn 2018; analyzed at Wageningen University.
- Experimental design uses 35 cm x 35 cm turf mesocosms within a long-term nutrient manipulation experiment.
- Location: Wardlow Hay Cop, Peak District, UK; two adjacent P-limited grasslands on limestone/calcareous and acidic soils with >20 years of nutrient manipulation.
- In 2018, mesocosms were exposed to ambient CO2 (~410 ppm) or elevated CO2 (600 ppm).

## Data structure and fields
- LOCATION: Experimental plot ID (string)
- PAIR: Block identifier (numeric)
- CO2: Level of CO2 fumigation (string) — A = ambient; E = 600 ppm
- GRASS: Grassland ecosystem type (string) — acid = acidic; calc = calcareous
- TREAT: Nutrient treatment (string) — P = Phosphorus; 0N = control with deionised water; LN = Nitrogen; HN = Higher Nitrogen
- DEPTH: Depth of sample from soil profile (string) — 0-10 or 10-20
- FL_MATRIX: Fluorescent matrix (string) — MUF = 4-Methyllumbelliferone; AMC = 7-Amino-4-methylcoumarin
- ENZYME: Extracellular enzyme (string) — BG = β-glucosidase; CB = cellobiohydrolase; NAG = N-acetyl β-D-glucosaminidase; LAP = leucine aminopeptidase; AP = acid phosphatase
- EEA_FINAL: Rate of enzyme activity (numeric) — units: Nmol g-1 h-1

## Measurements and units
- EEA_FINAL represents the rate of extracellular enzyme activity per gram of soil per hour (Nmol g-1 h-1).
- Enzyme types correspond to key soil nutrient cycling processes as listed above.

## Temporal and locational context
- Autumn 2018 sampling at Wardlow Hay Cop, Peak District, UK.
- Analyses conducted at Wageningen University.

## Potential uses and analysis
- Assess effects of CO2 elevation on soil enzyme activities across depths, grassland types, and nutrient treatments.
- Explore interactions between nutrient manipulation and CO2 treatment on enzyme production.
- Create dashboards or pivot-table viewpoints to enable self-serve exploration by end users.
- Integrate with broader PLACE datasets to study ecosystem responses to carbon enrichment and nutrient dynamics.

## Data quality and notes
- Maintain consistent coding for categorical fields (CO2, GRASS, TREAT).
- Ensure consistent units across EEA_FINAL (Nmol g-1 h-1).