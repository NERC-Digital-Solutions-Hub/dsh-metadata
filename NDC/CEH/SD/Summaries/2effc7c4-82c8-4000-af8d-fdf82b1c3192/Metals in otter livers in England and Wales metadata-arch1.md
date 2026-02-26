# Dataset Metadata: Otter Liver Tissue Concentrations and Associated Metadata

## Overview
- The dataset contains records of otter bodies found in England or Wales, with a unique identifier for each entry from two reference systems (CEH Ref and UWC Ref).
- For each otter, details include when the body was found (Month Found, Year Found) and where (County; X-coordinate, Y-coordinate).
- Biological and demographic data include Sex and AgeClass (Juvenile, Sub-adult, Adult) and a body condition metric (Condition coefficient, K) calculated according to Kruuk & Conroy (1991).
- The dataset also captures liver tissue analysis, reporting dry matter content and concentrations of numerous elements.

## Key Variables and Measurements
- Identifiers: CEH Ref (Predatory Bird Monitoring Scheme), UWC Ref (Cardiff University Otter Project)
- Temporal and location data: Month Found, Year Found, County, X-coordinate, Y-coordinate
- Demographics and condition: Sex (Female or Male), AgeClass (Juvenile, Sub-adult, Adult), Condition coefficient (K)
- Tissue and composition: % Dry matter (percent of liver mass that is dry matter; determined by drying a 0.5 g subsample of the liver at 70°C for 48 hours)
- Liver metal concentrations (dry weight, mg/kg): Al, Mn, Fe, Co, Ni, Cu, Zn, Se, Sr, Mo, Cd, Sb, Pb, Hg, Cr, As, V, Ag
- Data quality markers: ND = Non detected; NA = Not analysed (for applicable elements)
- Geospatial note: X-coordinate and Y-coordinate are provided but their units or reference system are not specified in the definitions

## Data Quality and Handling
- Some elements may be marked as ND or NA, indicating non-detection or not analysed for certain samples.
- All element concentrations are reported as dry weight concentrations (mg/kg).
- % Dry matter is derived from a standardized drying procedure, ensuring comparability across samples.

## Potential Analyses and Uses
- Descriptive statistics and distribution analyses of heavy metal concentrations across sexes, age classes, counties, and years found.
- Correlations between liver metal concentrations and demographic factors (Sex, AgeClass) or body condition (K).
- Spatial analyses using X/Y coordinates and County to identify geographic patterns of contaminant exposure.
- Temporal analyses to detect trends over time (Month Found, Year Found).
- Data integration with other datasets (e.g., additional environmental or health indicators) to inform risk assessments or ecological studies.

## Data Provenance and Access
- Data originate from the Predatory Bird Monitoring Scheme (CEH) and the Cardiff University Otter Project (UWC Ref).
- The dataset combines field discovery data with lab-derived liver tissue analyses (heavy metal concentrations and % dry matter).
- Metadata provide explicit definitions, units, and coding (e.g., ND/NA) to support reproducible analyses and data sharing.