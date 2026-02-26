# TREE_Northumbria_ICPMS_Vole_FM_Fresh_Mass_Concentration

## Overview
- Data dictionary for a dataset of fresh-mass ICP-MS concentrations in vole tissue from Northumbria.
- Includes sample metadata (species, site, collection date, UKCEH codes) and detailed concentration measurements for multiple elements.
- Documents sample preparation notes and how concentrations are expressed (mg/kg fresh mass).

## Dataset contents

- Taxonomic and sample identifiers
  - Latin_Species_Name
  - Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes
  - Sample_Details
  - CEH_Sample_Description
  - Tissue
  - Fresh_Mass_Ash_Mass_Ratio

- Concentration data (all in mg/kg_FM unless noted)
  - I_mg_kg_FM
  - Li_mg_kg_FM
  - Be_mg_kg_FM (with <Be indicating a censored value)
  - Na_mg_kg_FM
  - Mg_mg_kg_FM
  - Al_mg_kg_FM
  - P_mg_kg_FM
  - K_mg_kg_FM
  - Ca_mg_kg_FM
  - Ti_mg_kg_FM
  - V_mg_kg_FM
  - Cr_mg_kg_FM
  - Mn_mg_kg_FM
  - Fe_mg_kg_FM
  - Co_mg_kg_FM
  - Ni_mg_kg_FM
  - Cu_mg_kg_FM
  - Zn_mg_kg_FM
  - As_mg_kg_FM
  - Se_mg_kg_FM
  - Rb_mg_kg_FM
  - Sr_mg_kg_FM
  - Mo_mg_kg_FM
  - Ag_mg_kg_FM (with <Ag indicating a censored value)
  - Cd_mg_kg_FM
  - Cs_mg_kg_FM
  - Ba_mg_kg_FM
  - Tl_mg_kg_FM
  - Pb_mg_kg_FM
  - U_mg_kg_FM (with <U indicating a censored value)

## Metadata and interpretation notes

- Units
  - All element concentrations: mg/kg fresh mass (FM).
  - Fresh_Mass_Ash_Mass_Ratio is unitless.

- Data interpretation cues
  - Entries prefixed with "<" (e.g., <Be, <Ag, <U) denote “less than” values.
  - Some fields may be marked as n/a (not applicable).

- Sample preparation and tissue information
  - Tissue field includes notes on vole preparation; separate tissues were not prepared.

## Data quality and governance considerations for Data Stewards

- Standardization
  - Ensure consistent field naming and units across datasets (e.g., mg/kg_FM).
  - Preserve explicit handling of censored values (<) and n/a placeholders.

- Metadata completeness
  - Maintain clear linkage between biological samples and UKCEH codes (CEH_Sample_Codes) and descriptions (CEH_Sample_Description).
  - Capture sampling context via Site, Date_Sample_Collected, Sample_Details, and Tissue notes.

- Data provenance and versioning
  - Record sample collection and preparation provenance to support reproducibility.
  - Track any updates to concentration values or metadata and document version history.

- Accessibility and sharing
  - Ensure dataset is discoverable through appropriate portals; provide rich metadata to support reuse by data users.

- Data gaps and limitations
  - Be aware of censored values (<) and potential non-interoperability if units or measurement conventions differ across datasets.
  - Note possible incomplete metadata for dates or site descriptions and address where feasible.