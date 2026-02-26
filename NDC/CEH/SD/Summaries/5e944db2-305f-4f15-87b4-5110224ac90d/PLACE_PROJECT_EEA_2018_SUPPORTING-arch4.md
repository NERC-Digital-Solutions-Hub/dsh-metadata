# Extra extracellular enzyme activity from the PLACE project

## Overview
- Soil extracellular enzyme potential activities measured from the PLACE project.
- Collected in Autumn 2018; analysed in the laboratory at Wageningen University.
- Experimental design uses 35 cm x 35 cm turf mesocosms from a long-term nutrient manipulation experiment.
- Original experiment based at Wardlow Hay Cop, Peak District, UK; two adjacent P-limited grass lands on limestone/calcareous soil and an acidic soil with >20 years of nutrient manipulation.
- In 2018, mesocosms were exposed to ambient CO2 (~410 ppm) or 600 ppm CO2.

## Data structure and fields
- LOCATION, Description: Experimental plot ID; Units: String.
- PAIR, Description: Block; Units: Numeric.
- CO 2, Description: Level of CO2 fumigation; Units: String (A = ambient; E = 600 ppm).
- GRASS, Description: Grassland ecosystem type; Units: String (acid = acidic; calc = calcareous).
- TREAT, Description: Nutrient treatment; Units: String (P = Phosphorus; 0N = control; LN = Nitrogen; HN = Nitrogen).
- DEPTH, Description: Depth of sample from soil profile; Units: String (0-10 = 0 to 10 cm; 10-20 = 10 to 20 cm).
- FL_MATRIX, Description: Fluorescent matrix; Units: String (MUF = 4-Methyllumbelliferone; AMC = 7-Amino-4-methylcoumarin).
- ENZYME, Description: Extracellular enzyme; Units: String (BG = β-glucosidase; CB = cellobiohydrolase; NAG = N-acetyl-β-D-glucosaminidase; LAP = leucine aminopeptidase; AP = acid phosphatase).
- EEA_FINAL, Description: Rate of enzyme activity; Units: Nm ol g⁻¹ h⁻¹.

## Experimental context
- Samples are soil-derived, with enzyme activity assessed as extracellular potential activity.
- Linkage between CO2 fumigation, nutrient treatments, grassland type, and soil depth to enzyme activity is explored.

## Data quality, provenance, and metadata
- Data are tied to a clearly described experimental design and measurement lab (Wageningen University).
- Metadata fields explicitly define variable names, descriptions, and units, supporting reproducibility and interpretability.
- Although not stated, potential enhancements include timestamps, sampling IDs, method specifics, and quality flags to improve data quality assessment and cross-study comparability.

## Relevance for data strategies (Data Leaders)
- Demonstrates end-to-end data lifecycle: from field sampling design to lab analysis and clear metadata.
- Highlights the importance of standardized data dictionaries, consistent units, and clear variable definitions for discoverability and reuse.
- Illustrates managing complex, multi-factor experimental data (CO2 level, nutrient treatments, soil types, depths) within a single dataset.
- Suggests need for robust metadata, data provenance, and potential for cross-study integration across sites and projects.

## Practical considerations and next steps for data stewardship
- Ensure comprehensive metadata coverage (sampling dates, methods, QC, sample IDs).
- Maintain clear data dictionary and consistent coding for categorical fields (e.g., CO2, GRASS, TREAT).
- Promote data discoverability and sharing within the broader PLACE project and related data networks.
- Consider data quality flags and documentation of any data gaps or anomalies.
- Plan for updates or extensions to include additional sites, depths, or enzyme measurements to support broader analyses.