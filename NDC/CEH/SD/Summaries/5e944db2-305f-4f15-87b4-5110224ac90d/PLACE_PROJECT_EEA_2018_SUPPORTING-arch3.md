# Extra cellular enzyme activity from the PLACE project

## Overview
- Dataset of soil extracellular enzyme potential activities measured from PLACE (Phosphorus Limitation And ecosystem responses to Carbon dioxide Enrichment) experiments.
- Autumn 2018 soil samples analyzed in Wageningen University.
- Experimental design uses 35 cm x 35 cm turf mesocosms derived from long-term nutrient manipulation at Wardlow Hay Cop, Peak District, UK.
- Experimental factors include ambient vs elevated CO2 (410 ppm vs 600 ppm) and P-limited grasslands on limestone/calcareous and acidic soils with varying nutrient treatments.

## Data and variables
- LOCATION: Experimental plot ID (string).
- PAIR: Block identifier (numeric).
- CO 2: Level of CO2 fumigation (string: A = ambient; E = 600 ppm).
- GRASS: Grassland ecosystem type (string: acid = acidic; calc = calcareous).
- TREAT: Nutrient treatment (string: P = Phosphorus; 0N = control; LN = Nitrogen at low rate; HN = Nitrogen at high rate).
- DEPTH: Depth of sample from soil profile (string: 0-10; 10-20 cm).
- FL_MATRIX: Fluorescent matrix (string: MUF = 4-Methylumbelliferone; AMC = 7-Amino-4-methylcoumarin).
- ENZYME: Extracellular enzyme measured (string: BG = β-glucosidase; CB = cellobiohydrolase; NAG = N-acetyl-β-D-glucosaminidase; LAP = leucine aminopeptidase; AP = acid phosphatase).
- EEA_FINAL: Rate of enzyme activity (units: nmol g^-1 h^-1).

## Study design and context
- Investigates how soil extracellular enzyme activities respond to long-term nutrient manipulation and simulated atmospheric CO2 enrichment.
- Compares two adjacent P-limited grasslands with different soil types (calcareous vs acidic) under ambient and elevated CO2 conditions.
- Aims to illuminate microbial-mediated nutrient cycling and potential shifts in decomposition processes under environmental change.

## Methods
- Soil samples collected in Autumn 2018 from the mesocosms.
- Enzyme activities analyzed to yield EEA_FINAL (nmol g^-1 h^-1).
- Metadata captures plot, block, CO2 level, grassland type, nutrient treatment, sampling depth, and fluorescence matrix used for enzyme assays.

## Data quality, metadata, and sharing
- Dataset includes structured metadata for each observation (location, treatment, depth, enzyme type, and measurement).
- Metadata completeness is essential for verification and reuse; potential barriers include data sharing requirements and interoperability with other datasets.
- Data provenance from origin (PLACE project) and laboratory analysis to be maintained to support quality assurance and reproducibility.

## Relevance for monitoring frameworks
- Provides a concrete metric (EEA_FINAL) of soil microbial functional potential relevant to nutrient cycling and decomposition under environmental change.
- Useful for monitoring environmental health indicators linked to phosphorus limitation and CO2 enrichment scenarios.
- Can inform policy decisions on soil health, carbon cycling, and nutrient management by illustrating how microbial enzyme activities respond to management practices and climate-like conditions.

## Practical considerations and challenges
- Data standardization across studies and datasets is needed to enable cross-site comparisons.
- Some metadata or sharing constraints may hinder rapid data reuse; ensuring openness and proper data governance is important.
- Transformations or calibrations may be required to integrate enzyme activity data with other environmental indicators.

## Access and governance (implications for monitoring work)
- Clear data provenance (originating project, sampling times, and analytical methods) supports transparent governance.
- Sharing underlying data with appropriate governance and metadata enhances transparency for policy scrutiny and future decision-making.