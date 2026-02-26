# TREE_Northumbria_ICPMS_Toad_AM_Concentration

## Overview
- Dataset of elemental concentrations in toad ash samples, measured by ICP-MS.
- Provides a comprehensive ash-mass–based chemical profile (mg/kg ash mass) across numerous elements.
- Includes sample identifiers, taxonomic information, sampling details, and preparation notes to support environmental health monitoring and policy evaluation.

## Data fields and structure

### Taxonomy and sampling identifiers
- Latin_Species_Name
- Common_Species_Name

### Sampling and sample metadata
- Site
- Date_Sample_Collected
- CEH_Sample_Code (UKCEH sample codes)
- CEH_Sample_Description (UKCEH sample description)
- Fresh_Mass_Ash_Mass_Ratio (ratio of whole-organism mass to ash mass)
- Notes (notes related to toad preparation)

### Analyte concentrations (mg/kg ash mass)
- I_mg_kg_AM
- Li_mg_kg_AM
- Be_mg_kg_AM
- Na_mg_kg_AM
- Mg_mg_kg_AM
- Al_mg_kg_AM
- P_mg_kg_AM
- K_mg_kg_AM
- Ca_mg_kg_AM
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
- Ag_mg_kg_AM
- Cd_mg_kg_AM
- Cs_mg_kg_AM
- Ba_mg_kg_AM
- Tl_mg_kg_AM
- Pb_mg_kg_AM
- U_mg_kg_AM

## Units and normalization
- All elemental concentrations are expressed as milligrams per kilogram ash mass (mg/kg AM).

## Data quality and use considerations
- The dataset includes explicit notes on toad preparation and a mass-ratio field to enable normalization to ash mass.
- Metadata inconsistencies are visible in field naming (e.g., minor typos in some entries), which may require cleaning prior integration.
- The ash-mass basis (via Fresh_Mass_Ash_Mass_Ratio) supports standardized comparisons across samples and environments.
- Contains UKCEH sample codes and descriptions to support traceability and data provenance.