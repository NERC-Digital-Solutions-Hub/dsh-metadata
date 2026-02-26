# TREE_Northumbria_ICPMS_Frog_and_Frogspawn_DM_Concentration

## Overview
- A dataset of ICP-MS concentration measurements in frog tissue or frogspawn from Northumbria, with concentrations expressed on a dry mass basis (mg/kg DM).
- Includes sample metadata to support data provenance and cross-study comparability.

## Data structure and key variables
- Metadata fields: Latin_Species_Name, Common_Species_Name, Site, Date_Sample_Collected, CEH_Sample_Codes, CEH_Sample_Description, Tissue, Fresh_Mass_Dry_Mass_Ratio.
- Concentration data: extensive suite of elements measured (e.g., I, Li, Be, B, Na, Mg, Al, P, S, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U) with values in mg/kg DM.
- Some concentration entries are indicated as “<” values to denote detection limits.
- Units are predominantly mg/kg DM; some fields show non-applicable or placeholder units (n/a).

## Metadata, standards, and quality
- Provides essential sample-level metadata to enable traceability and reuse.
- Presence of detection-limit indicators (<value) requires careful handling in analyses.
- Some fields use “n/a” for units, highlighting potential inconsistencies in metadata standardization.
- UKCEH sample codes and descriptions are included to support cross-referencing with source records.

## Data governance and usability for Data Leaders
- Illustrates the importance of a coherent metadata model for environmental data integration (species, site, date, tissue, sample codes).
- Demonstrates common data-ability challenges: scattered data elements, inconsistent units, and detection-limit notation.
- Suitable for integration into a broader data system with versioning, provenance tracking, and metadata standards to enhance discoverability and reuse.

## Applications and value for environmental monitoring
- Enables assessment of metal accumulation in amphibians as an indicator of ecosystem contamination.
- Supports inter-study comparisons and regional baselines for Northumbria.
- Provides a rich chemical profile across many elements for ecological risk assessment and policy-relevant reporting.

## Gaps, challenges, and recommended next steps
- Standardize units across all concentration fields and ensure consistent naming conventions.
- Harmonize metadata completeness (e.g., include precise site coordinates, sampling methods, and tissue specification details).
- Develop a consistent approach to reporting detection limits (e.g., LOQ/LOD method metadata and uniform formatting for < values).
- Create controlled vocabularies for Site, Tissue, and Species to improve discoverability and interoperability.
- Link metadata to external data (e.g., UKCEH descriptions) and implement data governance practices like versioning and data quality flags.