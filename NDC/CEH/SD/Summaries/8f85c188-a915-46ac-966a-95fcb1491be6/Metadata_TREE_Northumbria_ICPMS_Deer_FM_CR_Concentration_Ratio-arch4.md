# TREE_Northumbria_ICPMS_Woodmice_FM_Concentration_Ratio

## Overview
- Metadata-driven data table capturing ICP-MS–based concentration ratios for Woodmice (whole body) relative to surrounding soil (dry mass).
- Key contextual fields include Latin and common species names, sampling site, date of collection, CEH sample description, notes, and the co-located soil sample used to calculate concentration ratios.
- Concentration ratio variables are defined for a wide range of elements (e.g., I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U). Most are described as “Concentration Ratio (Fresh Mass Woodmice (wholebody) divided By Dry Mass Soil).”
- Some ratio fields are paired (e.g., a second variant) and may include less-than indicators (shown as “<” in the value) or placeholders (1 = n/a) depending on the column.

## Data Content and Schema
- Core identifiers and context:
  - Latin_Species_Name
  - Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Description
  - Notes
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio
- Concentration Ratio variables (examples of structure):
  - I_Concentration_Ratio
  - Li_Concentration_Ratio
  - Be_Concentration_Ratio
  - Na_Concentration_Ratio
  - Mg_Concentration_Ratio
  - Al_Concentration_Ratio
  - P_Concentration_Ratio
  - K_Concentration_Ratio
  - Ca_Concentration_Ratio
  - Ti_Concentration_Ratio
  - V_Concentration_Ratio (and variants)
  - Cr_Concentration_Ratio (and variants)
  - Mn_Concentration_Ratio (and variants)
  - Fe_Concentration_Ratio (and variants)
  - Co_Concentration_Ratio (and variants)
  - Ni_Concentration_Ratio (and variants)
  - Cu_Concentration_Ratio (and variants)
  - Zn_Concentration_Ratio (and variants)
  - As_Concentration_Ratio (and variants)
  - Se_Concentration_Ratio (and variants)
  - Rb_Concentration_Ratio (and variants)
  - Sr_Concentration_Ratio (and variants)
  - Mo_Concentration_Ratio (and variants)
  - Ag_Concentration_Ratio (and variants)
  - Cd_Concentration_Ratio (and variants)
  - Cs_Concentration_Ratio (and variants)
  - Ba_Concentration_Ratio (and variants)
  - Tl_Concentration_Ratio (and variants)
  - Pb_Concentration_Ratio (and variants)
  - U_Concentration_Ratio (and variants)
- Notable formatting/interpretation cues:
  - Units are listed as n/a for these fields.
  - Some values indicate less-than bounds using a “<” marker.
  - Some entries show placeholders (e.g., “1 = n/a” for certain variant fields).

## Metadata, Provenance, and Interpretation
- Each column includes an Explanation field clarifying meaning (e.g., species names, site, sample date, co-located soil context, and the ratio calculation).
- The dataset explicitly ties Woodmice tissue measurements to soil mass for concentration ratio calculations.
- The schema suggests potential duplication or variant handling in columns (e.g., 1 vs 2 variants) that may require normalization for consistent downstream use.

## Data Quality, Gaps, and Handling
- Data quality considerations:
  - Presence of not-applicable (n/a) and less-than markers indicates partial or bounded data, requiring careful interpretation.
  - Inconsistencies in column naming or variant handling (e.g., some fields showing two variants with “1” and “2”) may necessitate normalization.
  - Absence of unit specifications (n/a) could challenge cross-study comparability without explicit unit conventions or downstream normalization.
- Data gaps:
  - Potential missing values in many concentration ratio fields and contextual metadata (as suggested by n/a and placeholder indicators).
  - Co-located soil sample context may vary between records, impacting reproducibility of ratio calculations.

## Access, Use, and Governance
- Rich accompanying explanations support data discoverability and interpretability, aligning with data-leader aims for reusable data products.
- To maximize utility for data strategy, ensure:
  - Consistent metadata formatting and column naming across the dataset (normalize variants, clarify 1 vs 2 fields).
  - Clear handling rules for less-than values and missing data.
  - Documentation of data provenance, collection methods, and any transformations applied to ratio calculations.
  - Mechanisms for updating and versioning the dataset to maintain discoverability and trust.

## Practical Takeaways for Data Leaders
- Leverage the detailed metadata to ensure clear understanding of each field and the calculation basis for concentration ratios.
- Prioritize standardization and normalization of the concentration ratio columns to improve interoperability and governance.
- Implement data quality checks around less-than markers, n/a values, and variant fields to support reliable analytics and reporting.
- Facilitate broader data sharing and community engagement by maintaining comprehensive documentation of sampling context and calculation methodologies.