# TREE_Northumbria_ICPMS_Bee_DM_Concentration

## Overview
- Dataset detailing concentrations of multiple elements in bee dry matter using ICP-MS.
- Includes both metadata about samples and quantitative measurements for numerous elements.

## Metadata and Structure
- Metadata fields:
  - Latin_Species_Name, Common_Species_Name
  - Site, Date_Samples_Collected
  - CEH_Sample_Codes, CEH_Sample_Description
  - Sample_Details
- Measurement data:
  - Elements measured (I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U)
  - Units for most concentrations: mg/kg_DM (milligram per kilogram dry mass)
  - Some fields use “<” to denote below-detection values (e.g., <Be, <Se, <U)
  - A few field descriptions contain typographical inconsistencies (e.g., “A Concentration of l” for Al)

## Data Format and Scope
- Wide-format dataset with one row per sample.
- Columns blend descriptive metadata with elemental concentration measurements.
- Some fields note n/a (not applicable) for units or explanations.

## Data Quality and Cleaning Considerations
- Presence of below-detection-limit values requiring special handling (censoring).
- Inconsistent or erroneous description text (minor data quality issues to address during ingestion).
- Linkage between CEH_Sample_Codes and CEH_Sample_Description important for traceability.

## Potential Uses and Outputs
- Build dashboards or pivot-table style reports to explore element concentrations by:
  - Species (Latin/Common names)
  - Site
  - Date of sampling
- Compare concentration patterns across elements and samples
- Facilitate data self-service for researchers or policy teams investigating bee exposure to trace metals

## Practical Data Support Considerations
- Ensure data provenance is clear by maintaining links between sample codes, descriptions, and details.
- Standardize unit representations and resolve minor text inconsistencies to improve usability.
- Plan handling strategies for < value entries and any missing data during analysis and visualization.