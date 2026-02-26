# TREE_Northumbria_ICPMS_Woodmice_DM_Concentration

## Overview
- Dataset of inductively coupled plasma mass spectrometry (ICPMS) concentrations for wood mice tissues.
- Concentrations expressed on a dry mass basis (mg/kg_DM).
- Includes both biological metadata (species, tissue) and sampling metadata (site, date, UKCEH sample codes/description).
- Intended to support analysis of trace element exposure and correlations with tissue type, site, and collection date.

## Data structure and contents
- Primary identifiers and metadata
  - Latin_Species_Name, Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes, CEH_Sample_Description
  - Tissue, Fresh_Mass_Dry_Mass_Ratio
- Element concentration variables (all in mg/kg_DM)
  - I_mg_kg_DM, Li_mg_kg_DM, Na_mg_kg_DM, Mg_mg_kg_DM, Al_mg_kg_DM, P_mg_kg_DM, K_mg_kg_DM, Ca_mg_kg_DM, Ti_mg_kg_DM, V_mg_kg_DM
  - Cr_mg_kg_DM, Mn_mg_kg_DM, Fe_mg_kg_DM, Co_mg_kg_DM, Ni_mg_kg_DM, Cu_mg_kg_DM, Zn_mg_kg_DM, As_mg_kg_DM, Se_mg_kg_DM
  - Rb_mg_kg_DM, Sr_mg_kg_DM, Mo_mg_kg_DM, Ag_mg_kg_DM, Cd_mg_kg_DM, Cs_mg_kg_DM, Ba_mg_kg_DM, Tl_mg_kg_DM, Pb_mg_kg_DM, U_mg_kg_DM
- Data conventions and qualifiers
  - Some concentrations are flagged with “<” (less-than) indicators (e.g., <I, <Al) to denote nondetects or below-reporting-limit values.
  - Some samples include tissue-specific notes such as “Tissue containing thyroid.”
  - Notable data gaps: Hind Leg Bone and woodmouse 8 liver have no data; various tissues may lack data for specific elements.
  - Inconsistent or garbled column notes indicating complexities in data capture (e.g., 1/2 indicators for Sr_mg_kg_DM; multiple tissue-designation columns).

## Data quality, gaps, and considerations
- Many missing values across elements and tissues; data are not uniformly complete.
- Nondetects and < values require careful handling (imputation, censoring, or dedicated statistical methods).
- Tissue type and thyroid-related designations affect comparability across samples; standardization of tissue categories advisable.
- Some samples have restricted or unclear metadata (garbled field descriptions); ensure provenance via CEH_Sample_Codes/Descriptions when joining datasets.
- Scale and locality: designed for local/regional (Northumbria) context; caution when extrapolating beyond sampled sites or times.

## Provenance and metadata
- UK Centre for Ecology & Hydrology (CEH) sample codes and descriptions referenced.
- Sampling context includes date, site, and tissue type details to enable ecological or toxicological interpretation.
- Fresh_Mass_Dry_Mass_Ratio provided to support conversion to dry mass when needed.

## Usage guidance and analyst considerations
- Ensure consistent units and tissue definitions before cross-sample comparisons (dry mass basis, tissue category alignment).
- Develop a strategy for nondetects (<) and for samples with missing tissue data.
- Leverage sample codes and descriptions to trace samples to original collection events and laboratories.
- When modeling, consider stratifying by tissue type and site; account for limited data density per element/tissue combination.
- Document any data cleaning steps to maintain reproducibility given the dataset’s signaling nuances and gaps.