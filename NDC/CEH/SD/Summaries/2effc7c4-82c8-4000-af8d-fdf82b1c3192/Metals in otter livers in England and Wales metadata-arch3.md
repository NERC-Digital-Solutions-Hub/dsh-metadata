# Otter Liver Tissue Contaminant Dataset Metadata

- This document defines a data dictionary for an otter liver contaminant dataset associated with the Predatory Bird Monitoring Scheme (CEH Ref) and the Cardiff University Otter Project (UWC Ref).
- It captures sample metadata, spatial context, biological characteristics, and a wide panel of liver contaminant concentrations.

## Data sources and identifiers

- CEH Ref: Unique numeric identifier assigned by the Predatory Bird Monitoring Scheme.
- UWC Ref: Unique numeric identifier assigned by the Cardiff University Otter Project.
- Month Found: Month in which the otter body was found.
- Year Found: Year in which the otter body was found.
- County: England or Wales county where the otter body was found.

## Sample and biological metadata

- Sex: Sex class (Female or Male).
- AgeClass: Age class (Juvenile, Sub-adult, or Adult).
- % Dry matter: Dry weight percentage determined by drying a 0.5 g subsample of liver at 70°C for 48 hours.
- Condition coefficient (K): Body condition coefficient calculated per Kruuk & Conroy (1991).

## Spatial data

- X-coordinate: X geographic coordinate.
- Y-coordinate: Y geographic coordinate.

## Contaminant concentrations (liver tissue, dry weight, mg/kg unless stated)

- Al, Mn, Fe, Co, Ni, Cu, Zn, Se, Sr, Mo, Cd, Sb, Pb, Hg, Cr, As, V, Ag: Dry weight concentrations in liver tissue; ND = Non detected; NA = Not analysed.
- Units: mg/kg for metal/metalloid concentrations; % dry matter for the % Dry matter variable.

## Data quality and interpretation notes

- Some concentration fields may be ND (not detected) or NA (not analysed), indicating incomplete data for certain elements.
- Data are organized to support traceability from unique identifiers through to geographic location, biological characteristics, and contaminant measures.
- Metadata completeness and standardization facilitate data governance, sharing, and comparison across studies and monitoring initiatives.

## Implications for monitoring and policy decisions

- Enables assessment of geographic patterns of otter liver contaminant burdens and potential links to exposure sources.
- Supports analyses of how sex, age class, and body condition relate to contaminant loads.
- Provides a structured data foundation for evaluating environmental health policies and informing future monitoring strategies, including data quality improvements and metadata enhancements.