# TREE_Northumbria_ICPMS_Woodmice_Whole_Organism_FM_Concentration

## Purpose and scope
- Data dictionary/table for concentrations of a broad suite of elements measured in wood mouse whole-organism tissue (fresh mass, FM) using ICP-MS.
- Includes both measurement fields and accompanying metadata to enable traceability, replication, and comparison across samples.

## Data structure and key fields
- Taxonomy and identification
  - Latin_Species_Name (explanation: Latin name of species)
  - Common_Species_Name (explanation: Common name of species)
- Sampling metadata
  - Site (sampling location)
  - Date_Sample_Collected (date of collection)
  - CEH_Sample_Description (UK CEH sample description)
  - Notes (notes relating to tissues used to calculate wood mice whole-organism concentrations)
- Concentration measurements (units: mg/kg, fresh mass)
  - I_mg_kg_whole_organism_FM (iodine in wood mouse whole-organism FM)
  - Li_mg_kg_whole_organism_FM (lithium)
  - Na_mg_kg_whole_organism_FM (sodium)
  - Mg_mg_kg_whole_organism_FM (magnesium)
  - Al_mg_kg_whole_organism_FM (aluminium)
  - P_mg_kg_whole_organism_FM (phosphorus)
  - K_mg_kg_whole_organism_FM (potassium)
  - Ca_mg_kg_whole_organism_FM (calcium)
  - Ti_mg_kg_whole_organism_FM (titanium)
  - V_mg_kg_whole_organism_FM (vanadium)
  - Cr_mg_kg_whole_organism_FM (chromium)
  - Mn_mg_kg_whole_organism_FM (manganese)
  - Fe_mg_kg_whole_organism_FM (iron)
  - Co_mg_kg_whole_organism_FM (cobalt)
  - Ni_mg_kg_whole_organism_FM (nickel)
  - Cu_mg_kg_whole_organism_FM (copper)
  - Zn_mg_kg_whole_organism_FM (zinc)
  - As_mg_kg_whole_organism_FM (arsenic)
  - Se_mg_kg_whole_organism_FM (selenium)
  - Rb_mg_kg_whole_organism_FM (rubidium)
  - Sr_mg_kg_whole_organism_FM (strontium)
  - Mo_mg_kg_whole_organism_FM (molybdenum)
  - Ag_mg_kg_whole_organism_FM (silver)
  - Cd_mg_kg_whole_organism_FM (cadmium)
  - Cs_mg_kg_whole_organism_FM (cesium)
  - Ba_mg_kg_whole_organism_FM (barium)
  - Tl_mg_kg_whole_organism_FM (thallium)
  - Pb_mg_kg_whole_organism_FM (lead)
  - U_mg_kg_whole_organism_FM (uranium)
- Data qualifiers
  - Some concentration fields may be annotated with a less-than marker (e.g., <I, <Ni, <Ag, <U) indicating detection-limit-based values
- Field-level explanations
  - Each concentration field has a corresponding Explanation describing that it is the concentration of the specific element in wood mouse whole- organism in mg/kg fresh mass
- Notes on tissue and calculation
  - Notes relate to tissues used to calculate the whole-organism concentrations, indicating how the metric was derived

## Data characteristics and integrity considerations
- Units: all concentration fields are mg/kg in fresh mass
- Measurement technique: ICP-MS (as indicated by the document title)
- Data completeness and metadata
  - Several core metadata fields (species name, site, date, sample description) are present to support traceability
  - Some placeholders indicate areas where metadata may need completion or clarification
- Handling of non-detects
  - "<" markers denote concentrations below detection limits for specific elements; these require consistent handling during analysis
- Documentation of data lineage
  - Explanations accompanying each concentration column provide context for interpretation and reproducibility

## Context and intended use for environmental health monitoring
- Designed to support monitoring and assessment of environmental metal and trace element exposure in a sentinel rodent species
- Facilitates cross-sample comparisons and trend analysis by standardizing units, tissue type, and data descriptors
- Provides a structured dataset framework that can be reused or extended for additional sites, dates, or species, aiding decision-making in environmental health risk assessments and policy evaluations