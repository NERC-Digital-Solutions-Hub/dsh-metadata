# TREE_Northumbria_ICPMS_Deer_Whole_Organism_FM_Concentration

## Overview
- Dataset describing ICP-MS measured concentrations of multiple elements in deer whole-organism samples, reported as mg/kg fresh mass (FM).
- Includes metadata on species, sampling location, collection date, and sample identifiers.
- Covers a wide suite of elements (I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U) with most as single concentration columns; some elements have duplicate/paired columns (e.g., Ba 1 and Ba 2, Tl 1 and Tl 2, Pb 1 and Pb 2, U 1 and U 2).
- Some values are reported as “less than” ( < ) for certain entries.
- Notes field records tissue types used to calculate whole-organism concentrations; CEH sample codes and descriptions provide provenance.

## Key variables and structure
- Taxonomy and common name: Latin_Species_Name, Common_Species_Name
- Sampling and provenance: Site, Date_Sample_Collected, CEH_Sample_Codes, CEH_Sample_Description, Notes
- Concentrations (mg/kg FM): I_mg_kg_whole-organism_FM, Li_mg_kg_whole-organism_FM, Be_mg_kg_whole-organism_FM (with < handling), Na_mg_kg_whole-organism_FM, Mg_mg_kg_whole-organism_FM, Al_mg_kg_whole-organism_FM (with <), P_mg_kg_whole-organism_FM, K_mg_kg_whole-organism_FM, Ca_mg_kg_whole-organism_FM, Ti_mg_kg_whole-organism_FM, V_mg_kg_whole-organism_FM, Cr_mg_kg_whole-organism_FM, Mn_mg_kg_whole-organism_FM, Fe_mg_kg_whole-organism_FM, Co_mg_kg_whole-organism_FM, Ni_mg_kg_whole-organism_FM (with <), Cu_mg_kg_whole-organism_FM, Zn_mg_kg_whole-organism_FM, As_mg_kg_whole-organism_FM, Se_mg_kg_whole-organism_FM, Rb_mg_kg_whole-organism_FM, Sr_mg_kg_whole-organism_FM, Mo_mg_kg_whole-organism_FM (with <), Ag_mg_kg_whole-organism_FM (with <), Cd_mg_kg_whole-organism_FM, Cs_mg_kg_whole-organism_FM, Ba_mg_kg_whole-organism_FM (two columns: 1 and 2), Tl_mg_kg_whole-organism_FM (two columns: 1 and 2), Pb_mg_kg_whole-organism_FM (two columns: 1 and 2), U_mg_kg_whole-organism_FM (two columns: 1 and 2)
- Data nuances: "<" indicates a concentration below the reporting threshold; duplicated columns likely reflect replicates or alternative measurement methods.

## Data quality, standards and gaps
- Metadata richness supports traceability (species, site, date, CEH codes, tissue notes).
- Some inconsistencies in column naming and formatting (e.g., occasional spacing and hyphenation issues) require standardization for interoperability.
- Presence of “<” values and duplicate measurement columns necessitates clear handling rules in analyses (detection limits, imputation or censoring strategies).
- Important missing context for governance and reuse (sampling methodology, QA/QC procedures, detection limits, sample sizes, geographic coordinates, age/sex of deer).
- Metadata describes tissues used for whole-organism calculations but may need a formal data dictionary to ensure consistent interpretation across users.

## How this supports data leadership aims
- System-wide view: Provides a comprehensive chemical profiling dataset for deer, useful for contaminant surveillance, environmental exposure assessment, and cross-site comparisons.
- User needs and co-ownership: Metadata fields (Notes, CEH_Sample_Description) aid understanding for policy colleagues and researchers; potential to evolve into a shared data product with stakeholder feedback.
- Data discovery and quality: Rich provenance and descriptor fields improve discoverability and governability; awareness of data gaps (e.g., replication, low-concentration measurements) supports prioritization.
- Data management practices: Encourages proper handling of units, metadata, and updates; highlights need for consistent naming conventions and documented QA/QC processes.
- Community and collaboration: Aligns with wider data networks by using standardized sample coding (CEH codes) and sharing structure that could be harmonized with other environmental contaminant datasets.

## Practical considerations and recommended next steps
- Standardize variable names and formatting across the dataset to enable seamless integration with other data sources.
- Develop a formal data dictionary detailing units, detection limits, handling of "<" values, and meanings of duplicate columns (1 vs 2).
- Capture and integrate missing governance data: sampling methodology, QA/QC procedures, sample sizes, and metadata on deer demographics when available.
- Establish data stewardship processes for updates, versioning, and metadata refresh to maintain discoverability and trust.
- Create data products or dashboards that leverage the full element suite for policy, research, and cross-network comparisons, with clear documentation for end users and feedback mechanisms.