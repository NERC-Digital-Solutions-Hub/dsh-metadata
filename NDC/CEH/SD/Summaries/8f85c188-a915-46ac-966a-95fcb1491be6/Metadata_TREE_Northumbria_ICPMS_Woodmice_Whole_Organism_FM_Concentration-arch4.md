# TREE_Northumbria_ICPMS_Woodmice_Whole_Organism_FM_Concentration

## Overview
- Dataset of element concentrations in wood mouse whole-organism tissue (fresh mass) from Northumbria, described as part of a UKCEH/ICP-MS dataset.
- Includes taxonomic identifiers, sampling metadata, and a comprehensive panel of elemental concentrations measured in mg/kg fresh mass.
- Notation indicates when a value is below detection (e.g., < marker).

## Data Model and Key Fields
- Taxonomy and identifiers
  - Latin_Species_Name
  - Common_Species_Name
- Sampling and context
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Description
  - Notes (tissues used to calculate whole-organism concentrations)
- Concentration measurements (columns for each element)
  - I_mg_kg_whole-organism_FM, Li_mg_kg_whole-organism_FM, Na_mg_kg_whole-organism_FM, Mg_mg_kg_whole-organism_FM, Al_mg_kg_whole-organism_FM, P_mg_kg_whole-organism_FM, K_mg_kg_whole-organism_FM, Ca_mg_kg_whole-organism_FM, Ti_mg_kg_whole-organism_FM, V_mg_kg_whole-organism_FM, Cr_mg_kg_whole-organism_FM, Mn_mg_kg_whole-organism_FM, Fe_mg_kg_whole-organism_FM, Co_mg_kg_whole-organism_FM, Ni_mg_kg_whole-organism_FM, Cu_mg_kg_whole-organism_FM, Zn_mg_kg_whole-organism_FM, As_mg_kg_whole-organism_FM, Se_mg_kg_whole-organism_FM, Rb_mg_kg_whole-organism_FM, Sr_mg_kg_whole-organism_FM, Mo_mg_kg_whole-organism_FM, Ag_mg_kg_whole-organism_FM, Cd_mg_kg_whole-organism_FM, Cs_mg_kg_whole-organism_FM, Ba_mg_kg_whole-organism_FM, Tl_mg_kg_whole-organism_FM, Pb_mg_kg_whole-organism_FM, U_mg_kg_whole-organism_FM
- Data conventions
  - "<" markers denote concentrations below detection/thresholds
  - Units specified as mg/kg (fresh mass) for most elements
- Data quality considerations (implied)
  - Presence of notes on tissues used and potential measurement caveats
  - Variable formatting in column headers; consistent units and definitions are implied but should be validated in a data dictionary

## Data Quality and Access Considerations
- Concentrations are reported with explicit metadata on sampling and tissue calculation; some values may be censored with "<".
- The dataset relies on consistent naming and units to enable comparability across samples and studies.
- For data owners, ensuring a standardized data dictionary and validation rules will improve interoperability and reuse, particularly across networks and partners.

## Relevance for Data Leaders
- Data governance
  - Clearly defined fields for taxonomy, location, timing, and sample description support traceability and reuse.
  - Comprehensive elemental panels enable cross-study comparisons and multi-parameter analyses.
- Metadata and discoverability
  - Rich metadata around sample description and tissue calculation enhances user understanding and correct interpretation.
  - Standardized units (mg/kg fresh mass) and explicit censoring markers improve data quality assessment.
- Data strategy and prioritization
  - Assess data coverage across species, sites, and elements to identify gaps and inform data collection plans.
  - Address potential barriers to access by ensuring metadata clarity, documentation, and alignment with shared data standards.
- Collaboration and community
  - The dataset sits within a broader environmental data ecosystem; coordinating metadata standards and data sharing with partner networks will reduce duplication and improve utility.

## Practical Recommendations
- Develop and publish a concise data dictionary detailing column names, units, detection limits, and censoring conventions.
- Normalize header naming to reduce formatting inconsistencies (e.g., unify "m g_kg_whole-organism_FM" formatting).
- Implement data quality checks for detection-limit handling and consistent unit reporting.
- Facilitate discoverability by indexing the dataset with clear keywords (e.g., ICPMS, wood mouse, whole-organism, fresh mass, mg/kg).
- Encourage cross-network collaboration to harmonize metadata and enable broader data integration.