# TREE_Northumbria_ICPMS_Deer_DM_Concentration

## Overview
- Structured dataset header for ICP-MS measured elemental concentrations in deer tissue.
- Fields cover species info, sampling details, tissue type, mass ratio, and concentrations for multiple elements (I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U).
- Primary unit indicated: mg/kg dry mass (DM). Some values are flagged as "<" (less than) or "No data" for Roe deer 4 thyroid.

## Data Schema and Metadata
- Key identifiers: Latin_Species_Name, Common_Species_Name, Site, Date_Sample_Collected, CEH_Sample_Codes, CEH_Sample_Description, Tissue, Fresh_Mass_Dry_Mass_Ratio.
- Element concentrations are represented by columns such as I_mg_kg_DM, Li_mg_kg_DM, Be_mg_kg_DM, etc., each with accompanying explanations and units.
- Qualifiers noted: "<" markers for detection limits and occasional "No data" statements (e.g., Roe deer 4 thyroid).

## Data Quality and Gaps
- Notable gap: No data for Roe deer 4 thyroid across several elements.
- Presence of detection-limit qualifiers without accompanying limit details in this excerpt.
- Metadata is extensive but may lack full provenance (sampling methods, QA/QC, instrument details).

## Implications for Data Strategy
- Demonstrates a multi-attribute wildlife contaminant dataset suitable for integration into a broader data system.
- Highlights need for standardized units, clear handling of detection limits, and complete provenance to ensure cross-study comparability and reusability.

## Actions for Data Leaders
- Improve discoverability and cataloging with clear metadata on units, qualifiers, and provenance.
- Standardize handling of "<" values and missing data; document detection limits and QA/QC procedures.
- Align with wider data networks (e.g., partners like UKCEH) and implement data governance, versioning, and update workflows.
- Develop and enforce data standards for wildlife tissue contaminant concentrations to facilitate integration and reuse.