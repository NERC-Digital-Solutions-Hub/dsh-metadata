# TREE_Northumbria_ICPMS_Bee_FM_Concentration

## Overview
- A dataset of ICPMS-derived elemental concentrations in bees from Northumbria, with fresh mass (FM) units.
- Metadata category includes taxonomic names (Latin and Common), sampling site, date of collection, UKCEH sample codes and descriptions, sample details, and notes.
- Concentrations are provided for a broad panel of elements (I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U) with units of mg/kg FM.
- Some concentration fields use a “<” qualifier to indicate values below a detection threshold.
- Source indicated by CEH/UKCEH sample codes and descriptions.

## Data Model and Key Fields
- Taxonomy and naming
  - Latin_Species_Name
  - Common_Species_Name
- Sampling and context
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes (UKCEH sample codes)
  - CEH_Sample_Description (UKCEH sample description)
  - Sample_Details
  - Notes (bees-specific notes)
- Concentration data (mg/kg_fresh_mass)
  - I_mg_kg_FM, Li_mg_kg_FM, Be_mg_kg_FM, Na_mg_kg_FM, Mg_mg_kg_FM, Al_mg_kg_FM
  - P_mg_kg_FM, K_mg_kg_FM, Ca_mg_kg_FM, Ti_mg_kg_FM, V_mg_kg_FM
  - Cr_mg_kg_FM, Mn_mg_kg_FM, Fe_mg_kg_FM, Co_mg_kg_FM, Ni_mg_kg_FM
  - Cu_mg_kg_FM, Zn_mg_kg_FM, As_mg_kg_FM, Se_mg_kg_FM, Rb_mg_kg_FM
  - Sr_mg_kg_FM, Mo_mg_kg_FM, Ag_mg_kg_FM, Cd_mg_kg_FM, Cs_mg_kg_FM
  - Ba_mg_kg_FM, Tl_mg_kg_FM, Pb_mg_kg_FM, U_mg_kg_FM
  - Note: Some “<” qualifiers appear for Be, Se, U, etc., indicating values below a detection limit.
- Metadata nuance
  - Units and explanations are provided for each concentration column (mg/kg_FM) to support interpretation and reuse.

## Data Quality and Governance Considerations
- Explicit units (mg/kg fresh mass) and coded metadata support consistency and reuse.
- Presence of “<” qualifiers requires special handling in analyses (censored data considerations).
- Some fields show "n/a" in units or explanations, indicating sparsity or gaps in metadata that may need clarification for full interoperability.
- UKCEH/CEH sampling codes and descriptions enable traceability and cross-referencing with related datasets.
- Aligns with data-system concepts: discoverability, provenance, metadata richness, and the potential for data updates and iterative use.

## How Data Leaders Can Use This Dataset
- Part of a holistic data strategy for environmental exposure assessment in pollinators.
- Integrate with other datasets across networks (policy teams, researchers, partners) using shared sampling codes and standardized concentration metrics.
- Assess data completeness and identify gaps by site, species, or element to guide future data collection and prioritization.
- Ensure data assets are well-managed: maintain consistent formats, clear metadata, and up-to-date sample descriptions to support dissemination and policy use.
- Use the concentration data to monitor potential metal exposure in bee populations and inform risk assessments or regulatory discussions.

## Practical Implications and Next Steps
- Validate and harmonize any ambiguous metadata (e.g., ensure consistent interpretation of “n/a” fields and element explanations).
- Establish clear handling rules for censored data (values with “<”) in downstream analyses.
- Maintain linkage between CEH sample codes and broader project or partner datasets to enhance discoverability and cross-use.
- Plan for regular updates and versioning to keep the concentration records current and traceable across projects.