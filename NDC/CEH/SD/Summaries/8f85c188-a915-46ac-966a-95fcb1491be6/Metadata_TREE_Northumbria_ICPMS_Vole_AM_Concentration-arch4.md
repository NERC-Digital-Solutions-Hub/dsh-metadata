# TREE_Northumbria_ICPMS_Vole_AM_Concentration

## Overview
- Data schema for ICP-MS concentration measurements in vole ash (AM) from Northumbria, UKCEH-related sampling.
- Captures both specimen metadata and multi-element concentration data at the sample level.
- Aims to support analysis of elemental concentrations in vole ash with traceability to species, site, and collection details.

## Key data fields

- Identification and taxonomy
  - Latin_Species_Name
  - Common_Species_Name

- Sampling and provenance
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes
  - Sample_Details
  - CEH_Sample_Description
  - Notes (including preparation notes, e.g., whether separate tissues were prepared)

- Mass and preparation
  - Fresh_Mass_Ash_Mass_Ratio (ratio of whole-organism fresh mass to ash mass)

- Concentration measurements (mg/kg, AM)
  - I_mg_kg_AM, Li_mg_kg_AM
  - Be_mg_kg_AM (with "<" value support)
  - Na_mg_kg_AM
  - Mg_mg_kg_AM
  - Al_mg_kg_AM
  - P_mg_kg_AM
  - K_mg_kg_AM
  - Ti_mg_kg_AM
  - V_mg_kg_AM
  - Cr_mg_kg_AM
  - Mn_mg_kg_AM
  - Fe_mg_kg_AM
  - Co_mg_kg_AM
  - Ni_mg_kg_AM
  - Cu_mg_kg_AM
  - Zn_mg_kg_AM
  - As_mg_kg_AM
  - Se_mg_kg_AM
  - Rb_mg_kg_AM
  - Sr_mg_kg_AM
  - Mo_mg_kg_AM
  - Ag_mg_kg_AM (with "<" value support)
  - Cd_mg_kg_AM
  - Cs_mg_kg_AM
  - Ba_mg_kg_AM
  - Tl_mg_kg_AM
  - Pb_mg_kg_AM
  - U_mg_kg_AM

- Data conventions
  - Some concentration entries use a “less than” (<) marker to denote sub-threshold values.
  - Units for all listed concentrations are mg/kg (ash mass basis).

## Data quality and metadata considerations

- Inconsistencies and potential metadata quality issues
  - Some column explanations appear misaligned (e.g., Ti_mg_kg_AM explanation refers to Ca; several element explanations show similar mismatches), indicating possible documentation glitches.
  - Formatting irregularities (e.g., mixed column labels and explanations) suggest the need for data validation and metadata cleaning.

- Handling of censored data
  - Presence of “<” values for certain elements (Be, Ag, etc.) requires clear handling in analyses (treatment as censored or substituted values).

- Data discoverability and provenance
  - Includes explicit sample codes, site, date, and notes on preparation, aiding traceability and reproducibility.
  - Rich metadata supports filtering by species, site, date, and preparation details.

## Implications for data governance (Data Leaders)

- Data quality controls
  - Validate alignment between column names and explanations.
  - Establish consistent handling of < values and any other censored measurements.
  - Verify unit consistency and address any mislabeling in metadata.

- Metadata completeness and consistency
  - Harmonize descriptions across element fields to avoid misinterpretation.
  - Ensure Notes and Sample_Details capture all relevant preparation steps for reproducibility.

- Data discovery and stewardship
  - Maintain clear linkage between sample codes, sites, dates, and concentration results to support longitudinal and spatial analyses.
  - Implement updates and versioning to reflect corrections in metadata or data values.

- Data usage and integration
  - The dataset enables cross-sample comparisons by species, site, and collection date, with potential integration into broader environmental or ecological data networks.
  - Clear documentation of data conventions will facilitate sharing with policy colleagues and wider data communities.

## Practical takeaways for action

- Prioritize metadata validation to correct misaligned explanations and ensure accurate interpretation of each concentration column.
- Establish a consistent policy for handling < values in analyses and reporting.
- Maintain and communicate clear data provenance (sample codes, preparation details, notes) to support reuse across partners and projects.
- Leverage the structured fields to enable user-focused reporting and dissemination, aligning with data governance goals for discoverability and quality.