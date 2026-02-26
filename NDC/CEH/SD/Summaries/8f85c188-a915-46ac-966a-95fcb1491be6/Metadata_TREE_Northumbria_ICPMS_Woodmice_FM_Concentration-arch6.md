# TREE_Northumbria_ICPMS_Woodmice_FM_Concentration

## Overview
- Metadata-driven dataset detailing concentrations of multiple elements in wood mice tissues, using ICP-MS, from Northumbria.
- Includes both sample metadata and a wide range of element concentration measurements in mg/kg fresh mass (FM).

## Data Structure and Key Variables
- Sample and species identifiers
  - Latin_Species_Name and Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes and CEH_Sample_Description
  - Tissue (name of the sampled wood mouse tissue)
  - Fresh_Mass_Dry_Mass_Ratio (FM/ratio)
- Data coding notes
  - Several columns use suffixes like _FM to denote concentrations in mg/kg fresh mass
  - Some columns indicate special coding (e.g., “1 = mg/kg. 2 = fresh mass”) to describe measurement context
  - < marker is used to identify concentrations reported as “less than” a value
- Concentration measurements (selected examples)
  - I_mg_kg_FM, Li_mg_kg_FM, Na_mg_kg_FM, Mg_mg_kg_FM, Al_mg_kg_FM, P_mg_kg_FM, K_mg_kg_FM, Ca_mg_kg_FM, Ti_mg_kg_FM, V_mg_kg_FM, Cr_mg_kg_FM, Mn_mg_kg_FM, Fe_mg_kg_FM, Co_mg_kg_FM, Ni_mg_kg_FM, Cu_mg_kg_FM, Zn_mg_kg_FM, As_mg_kg_FM, Se_mg_kg_FM, Rb_mg_kg_FM, Sr_mg_kg_FM, Mo_mg_kg_FM, Ag_mg_kg_FM, Cd_mg_kg_FM, Cs_mg_kg_FM, Ba_mg_kg_FM, Tl_mg_kg_FM, Pb_mg_kg_FM, U_mg_kg_FM
- Data gaps and tissue-specific notes
  - No data for Hind Leg Bone and woodmouse 8 liver
  - No data for tissue containing thyroid for certain elements (e.g., several entries for P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, etc.)
  - “<” values indicate detection limits lower than stated
- Data quality indicators
  - The dataset combines both sample metadata and element concentration data; careful alignment is needed between sample records and measurements

## Data Quality, Gaps, and Format Considerations
- Missing records
  - Hind Leg Bone and woodmouse 8 liver lack data
- Tissue-specific limitations
  - Some elements report no data when analyzing tissue containing thyroid
- Handling censored data
  - Values with “<” require censored-data methods or reporting as below detection limits
- Potential data cleaning needs
  - Inconsistent or garbled field descriptions (e.g., formatting around units and suffixes) may require standardization
  - Verify cross-references between CEH_Sample_Codes and external sample metadata

## Data Preparation and Product Ideas (Data Support)
- Create a clean, analysis-ready dataset
  - Standardize column names and units (preferably mg/kg FM)
  - Consolidate tissue-specific concentration fields and clearly document any exclusions (e.g., thyroid-containing tissues)
- Metadata documentation
  - Develop a comprehensive data dictionary describing each field, coding, and units
- Data products for end users
  - Self-serve dashboards or pivot-table-ready datasets by site, date, species, tissue, and element
  - Summary tables and visuals showing concentration patterns across tissues and sites
- Data quality checks
  - Validate sample codes against CEH_Sample_Codes
  - Flag missing data and censored values; document handling rules
- Analysis-ready guidance
  - Provide templates for common analyses (e.g., concentration by tissue and site, comparisons across elements, detection-limit handling)

## Usage and Limitations for End Users
- Suitable for exploring element distribution across wood mouse tissues and sites
- Be mindful of:
  - Missing data in specific tissues (e.g., hind leg bone, woodmouse 8 liver)
  - Tissue-containing thyroid data gaps
  - censored (<) values requiring appropriate statistical treatment
  - Inconsistencies in data formatting that may require preprocessing before analysis