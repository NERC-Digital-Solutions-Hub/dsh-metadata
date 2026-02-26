# TREE_Northumbria_ICPMS_Woodmice_DM_Concentration

## Overview
- Metadata and data table for ICP-MS measured concentrations of multiple elements in wood mice tissues from Northumbria, with UKCEH sampling provenance.
- Captures sample identifiers, species names (Latin and common), site, collection date, sample codes and descriptions, tissue type, mass ratio (fresh/dry), and element concentrations.

## Data Structure
- Core identifiers: Latin_Species_Name, Common_Species_Name, Site, Date_Sample_Collected, CEH_Sample_Codes, CEH_Sample_Description.
- Biological context: Tissue, Fresh_Mass_Dry_Mass_Ratio (ratio of fresh to dry mass).
- Concentration columns: I_mg_kg_DM, Li_mg_kg_DM, Na_mg_kg_DM, Mg_mg_kg_DM, Al_mg_kg_DM, P_mg_kg_DM, K_mg_kg_DM, Ca_mg_kg_DM, Ti_mg_kg_DM, V_mg_kg_DM, Cr_mg_kg_DM, Mn_mg_kg_DM, Fe_mg_kg_DM, Co_mg_kg_DM, Ni_mg_kg_DM, Cu_mg_kg_DM, Zn_mg_kg_DM, As_mg_kg_DM, Se_mg_kg_DM, Rb_mg_kg_DM, Sr_mg_kg_DM, Mo_mg_kg_DM, Ag_mg_kg_DM, Cd_mg_kg_DM, Cs_mg_kg_DM, Ba_mg_kg_DM, Tl_mg_kg_DM, Pb_mg_kg_DM, U_mg_kg_DM.
- Data flags: Some concentrations are denoted as “<” values indicating censored/upper-bound measurements.
- Notes on data gaps: No data for Hind Leg Bone and woodmouse 8 liver.
- Data naming: Column names and explanations accompany each variable; some formatting irregularities present in the provided text.

## Key Variables and Units
- Primary concentration unit: mg/kg dry mass (DM).
- Elements included: I, Li, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U.
- Tissue- and body-location notes: Some entries indicate measurements in tissues other than thyroid-containing tissue; mass ratio and tissue description are recorded.

## Data Quality, Gaps, and Notes
- Presence of less-than markers (<I, <Al, <V, etc.) to indicate upper-bound measurements.
- Some data fields indicate no data for specific tissues or samples.
- Formatting inconsistencies and typographical issues in column names (e.g., spacing in "Fresh_Mass_Dry_Mass_Ratio") may affect programmatic parsing.
- Gaps identified: Hind Leg Bone data missing; data for woodmouse 8 liver missing.

## Provenance and Metadata
- Source: UK Centre for Ecology & Hydrology (UKCEH) sample codes and descriptions.
- Temporal and spatial context: Sampling site and date collected are recorded, enabling cross-site comparisons.
- Taxonomic context: Both Latin and common species names provided.

## Implications for Data Leaders
- The dataset supports end-to-end data governance needs: data discovery, provenance, metadata completeness, and quality checks for complex environmental contaminant data.
- Highlights importance of standardized units, clear tissue identifiers, and consistent handling of censored data to enable reuse across teams and partner networks.

## Recommendations and Next Steps
- Standardize column naming, units, and metadata to align with established data standards for contaminant/ICP-MS datasets.
- Improve metadata clarity for tissue types, sample provenance, and mass ratio definitions.
- Implement data validation to properly handle < values and identify missing data areas (e.g., Hind Leg Bone, woodmouse 8 liver).
- Enhance data discoverability: provide a formal data dictionary, data lineage, and versioning; consider publishing schema for broader data-community use.
- Plan for coordination with wider data networks to reduce duplication and strengthen communities of practice around similar datasets.