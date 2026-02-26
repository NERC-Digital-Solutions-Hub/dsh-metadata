# TREE_Northumbria_ICPMS_Bee_FM_Concentration_Ratio

## Overview
- Dataset appears to be a data dictionary for a study of ICP-MS concentration ratios between bee samples and nearby soil.
- Primary purpose: capture metadata about bee samples and the calculation of concentration ratios (fresh mass bee concentration divided by dry mass soil) for a range of elements.
- Includes both biological/sample metadata and a comprehensive set of concentration-ratio variables for many elements.

## Key Data Fields

- Metadata (sample and context)
  - Latin_Species_Name: scientific name of bee species
  - Common_Species_Name: common name of species
  - Site: sampling site
  - Date_Sample_Collected: date the sample was collected
  - CEH_Sample_Codes: internal CEH sample codes
  - Sample_Details: sample preparation details
  - CEH_Sample_Description: CEH-defined sample description
  - Notes: notes related to the bee sample

- Calculation context
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio: description of the soil sample used to compute the concentration ratio

- Concentration ratio variables (Bee-to-Soil)
  - I_Concentration_Ratio
  - Li_Concentration_Ratio
  - Be_Concentration_Ratio (and related <Be for less-than values)
  - Na_Concentration_Ratio
  - Mg_Concentration_Ratio
  - Al_Concentration_Ratio
  - P_Concentration_Ratio
  - K_Concentration_Ratio
  - Ca_Concentration_Ratio
  - Ti_Concentration_Ratio
  - V_Concentration_Ratio
  - Cr_Concentration_Ratio (and related <Cr or special formatting)
  - Mn_Concentration_Ratio
  - Fe_Concentration_Ratio
  - Co_Concentration_Ratio
  - Ni_Concentration_Ratio
  - Cu_Concentration_Ratio
  - Zn_Concentration_Ratio
  - As_Concentration_Ratio
  - Se_Concentration_Ratio (and related <Se)
  - Rb_Concentration_Ratio
  - Sr_Concentration_Ratio
  - Mo_Concentration_Ratio
  - Ag_Concentration_Ratio
  - Cd_Concentration_Ratio
  - Cs_Concentration_Ratio
  - Ba_Concentration_Ratio (and possibly a second form)
  - Tl_Concentration_Ratio
  - Pb_Concentration_Ratio
  - U_Concentration_Ratio (and related <U)

- Units and qualifiers
  - Most metadata fields use “n/a” or descriptive text
  - Concentration ratios are presented as dimensionless values
  - Some columns indicate “less than” values (e.g., <Be, <Se, <U) to denote upper limits
  - Some ratio-related columns include numeric suffixes (e.g., 1, 2) for additional annotation or differentiation

## Data Model and Structure

- Combines:
  - Biological/species and site-level metadata
  - Sampling and preparation details
  - The computed concentration ratios for a broad suite of elements
- Designed to enable cross-sample comparisons of bee tissue concentrations relative to soil, facilitating interpretation of metal uptake patterns across species and locations.

## Data Quality, Preparation, and Use

- Data likely require harmonization when combining with other datasets (species naming, site identifiers, date formats).
- The presence of “Notes” and “Sample_Details” supports interpretation and re-use, particularly for understanding preparation methods and context.
- Handling of less-than values and any suffixed annotations should be standardized during analysis.
- The dataset is suitable for self-service exploration (e.g., calculating ratios by species/site, filtering by date or sample details) and for creating data products that reveal uptake patterns or exposure indicators.

## Potential Applications and Outputs

- Comparative analysis of metal uptake across bee species and sites.
- Exploration of relationships between soil metal concentrations and bee tissue ratios.
- Creation of dashboards or reports to communicate bee exposure to metals to stakeholders.
- Data quality checks and feedback loops to refine sample collection and description.

## Notes and Data Provenance

- The document is a detailed data dictionary for a specific dataset focused on bee ICP-MS concentration ratios, with emphasis on the Bee-to-Soil concentration ratio calculation and associated metadata.
- Ensures traceability from sample collection through to the concentration-ratio calculations, supporting reproducibility and transparency in data use.