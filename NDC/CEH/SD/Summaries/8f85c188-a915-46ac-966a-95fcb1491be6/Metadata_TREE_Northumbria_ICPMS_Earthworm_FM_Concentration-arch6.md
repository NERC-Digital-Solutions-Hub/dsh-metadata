# TREE_Northumbria_ICPMS_Earthworm_FM_Concentration

## What this dataset is
- A measurement dataset of concentrations of multiple elements in earthworms (fresh mass basis, FM) using ICP-MS.
- Contains taxonomic and sampling context fields, including Latin and common species names, sampling site, date collected, and UKCEH sample codes/descriptions.
- Includes a wide panel of element concentrations measured in mg/kg FM across samples.

## Key fields at a glance
- Taxon and sampling context:
  - Latin_Species_Name, Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes, CEH_Sample_Description
  - Notes
- Element concentration variables (mg/kg FM):
  - I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U
- Units indicated as mg/kg_FM (fresh mass)

## Data schema and structure
- Each row represents a single earthworm sample with associated metadata and measured element concentrations.
- Concentration fields are aligned with elemental symbols followed by _mg_kg_FM (e.g., I_mg_kg_FM, Cu_mg_kg_FM).
- Some fields include explanatory notes (Notes) and description fields (CEH_Sample_Description) to provide sampling context.

## Data quality and caveats
- Some field descriptions are misaligned or inconsistent (e.g., multiple "Explanation" entries incorrectly stating "Concentration of Fe" for different elements, and several typos/duplications in the header lines).
- Several fields list Units = n/a, introducing ambiguity about data recording conventions for those fields.
- Occasional formatting issues (e.g., Tl_mg_kg_FM_ line has an extra underscore; some rows show overlapping or merged descriptions like “Concentration of Fe in milligram per kilogram fresh mass” applied to multiple elements).
- Potential missing values or inconsistencies in sample codes and descriptions require cleaning before formal analysis.

## Potential uses
- Assess bioaccumulation patterns of multiple elements in earthworms across sampling sites.
- Compare elemental concentrations across species, sites, or collection dates.
- Integrate with site metadata for environmental monitoring and risk assessment.
- Build self-serve dashboards or pivot-table views to explore relationships between sampling context and metal concentrations.

## Data readiness and recommended preparation
- Clean and validate metadata fields:
  - Correct misaligned Explanations and ensure units are consistently defined (prefer mg/kg Fresh Mass or specify if other mass basis is used).
  - Resolve inconsistencies in sample codes/descriptions and taxon names.
  - Address fields with Units = n/a to confirm recording conventions.
- Normalize units and clarify whether concentrations are on a fresh mass (FM) basis throughout.
- Fix typographical errors and align header definitions with actual data columns.
- Consider adding metadata for detection limits, QA/QC flags, and data provenance.
- Create derived variables as needed (e.g., total metal load per sample, summary statistics by site or species).

## How Data Support can help
- Interpret and document data quality issues, propose a cleaned schema, and produce a cleaned, self-describing data product.
- Develop data dictionaries and accompany the dataset with example queries and visualizations (e.g., site comparisons, time-series across dates).
- Create robust data validation rules to catch mislabeling, unit inconsistencies, and missing values.
- Facilitate metadata harmonization to enable reliable cross-dataset analyses and public sharing.