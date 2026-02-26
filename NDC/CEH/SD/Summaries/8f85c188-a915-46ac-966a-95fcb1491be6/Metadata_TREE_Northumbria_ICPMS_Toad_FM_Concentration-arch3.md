# TREE_Northumbria_ICPMS_Toad_FM_Concentration

## Overview
- Dataset documenting concentrations of multiple elements in toads from Northumbria, measured by ICP-MS.
- Includes both sample metadata and a comprehensive panel of elemental concentrations expressed as milligrams per kilogram of fresh mass (mg/kg FM).
- Key metadata fields cover species identity, sampling site, collection date, and UKCEH sample coding and description.
- A mass ratio field (Fresh_Mass_Ash_Mass_Ratio) and notes on toad preparation accompany concentration data.

## Data Content and Structure
- Taxonomy and identification
  - Latin_Species_Name
  - Common_Species_Name
- Sampling context
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Code
  - CEH_Sample_Description
- Tissue preparation and mass
  - Fresh_Mass_Ash_Mass_Ratio
  - Notes (toad preparation; indicates whether separate tissues were not prepared)
- Measured concentrations (all in mg/kg FM)
  - I_mg_kg_FM
  - Li_mg_kg_FM
  - Be_mg_kg_FM
  - Na_mg_kg_FM
  - Mg_mg_kg_FM
  - Al_mg_kg_FM
  - P_mg_kg_FM
  - K_mg_kg_FM
  - Ca_mg_kg_FM
  - Ti_mg_kg_FM
  - V_mg_kg_FM
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
  - Ag_mg_kg_FM
  - Cd_mg_kg_FM
  - Cs_mg_kg_FM
  - Ba_mg_kg_FM
  - Tl_mg_kg_FM
  - Pb_mg_kg_FM
  - U_mg_kg_FM
- Notes on data labeling
  - Field naming consistently uses the pattern <Element>_mg_kg_FM with the suffix _FM indicating fresh mass basis.
  - Some descriptions contain inconsistencies (e.g., incorrect element in explanation, trailing underscores, or replicate annotations such as “1”/“2”).

## Metadata and Quality Considerations
- Metadata coverage
  - Comprehensive fields for specimen identity, site, and sample coding, plus explicit notes on preparation.
- Data quality and consistency issues
  - Several field Explanations contain mislabels (e.g., attribution of Cr to Mn or Mn to Cr in several lines).
  - Some field names include minor formatting irregularities (e.g., Fresh_Mass_Ash_Mass_Ratio with space, trailing underscores in Tl_mg_kg_FM_, etc.).
  - Potential replication indicators (e.g., “Pb_mg_kg_FM, 1” and “Pb_mg_kg_FM, 2”) suggesting multiple measurements per sample that should be harmonized.
- Data governance implications
  - Requires quality assurance, cleaning, and potential transformation before analysis.
  - Underlying data should be shared openly where appropriate, with clear governance around sensitive or restricted elements and metadata provenance.
  - Consistency between sample codes (CEH_Sample_Code) and descriptions is essential for traceability.

## Relevance for Monitoring Frameworks
- Purpose alignment
  - Provides a structured dataset to monitor environmental health through amphibian metal burdens, enabling scrutiny of policy implications and informing future decisions.
- Utility for decision-making
  - Enables cross-site comparisons and temporal trends in metal exposure.
  - Supports development of environmental thresholds and risk assessments for amphibians.
  - Facilitates reporting through clear data layers (sample identity, site, date, and metal concentrations) and visualization-ready fields.

## Practical Considerations for Authors of Monitoring Frameworks
- Data collection and harmonization
  - Standardize field explanations to align with actual measurements (correct mislabels and ensure element-specific metadata is accurate).
  - Clarify replication structure (if present) and implement consistent handling of multiple measurements per sample.
- Metadata quality and accessibility
  - Improve metadata completeness and clarity to support data reuse, including explicit units, measurement methods, and QA/QC procedures.
  - Ensure data governance policies for openness, provenance, and versioning are established at the data source.
- Data processing and sharing
  - Implement routines for cleaning, transforming, and validating concentrations (mg/kg FM) prior to publication or dashboarding.
  - Maintain linkage between CEH_Sample_Code, CEH_Sample_Description, site, and date to support traceability and audits.
- Addressing common monitoring challenges
  - Anticipate data gaps and access issues; plan for data acquisition to fill critical gaps.
  - Promote cross-organization data sharing to reduce silos and enhance comparative analyses.
  - Develop clear communication of complex findings for policy audiences.