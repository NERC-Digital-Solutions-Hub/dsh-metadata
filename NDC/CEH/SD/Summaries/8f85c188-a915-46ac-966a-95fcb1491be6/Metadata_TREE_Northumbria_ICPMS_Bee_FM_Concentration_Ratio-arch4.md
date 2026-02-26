# TREE_Northumbria_ICPMS_Bee_FM_Concentration_Ratio

## Overview
- A dataset header describing ICP-MS measured concentrations in bee samples used to calculate concentration ratios with co-located dry soil.
- Focuses on Fresh Mass Bee (whole-body) concentrations divided by Dry Mass Soil concentrations across multiple elements.
- Includes detailed sample metadata, specimen names, sampling context, and descriptive notes.

## Dataset Structure and Key Fields
- Taxonomic and common names:
  - Latin_Species_Name
  - Common_Species_Name
- Sampling and site details:
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes
  - Sample_Details
  - CEH_Sample_Description
  - Notes
- Provenance and context:
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio
  - I_Concentration_Ratio (general indicator)
- Concentration ratio measurements (Bee concentration divided by Dry Soil concentration), for numerous elements:
  - Be_Concentration_Ratio, Li_Concentration_Ratio, Na_Concentration_Ratio, Mg_Concentration_Ratio, Al_Concentration_Ratio, P_Concentration_Ratio, K_Concentration_Ratio, Ca_Concentration_Ratio, Ti_Concentration_Ratio, V_Concentration_Ratio, Cr_Concentration_Ratio, Mn_Concentration_Ratio, Fe_Concentration_Ratio, Co_Concentration_Ratio, Ni_Concentration_Ratio, Cu_Concentration_Ratio, Zn_Concentration_Ratio, As_Concentration_Ratio, Se_Concentration_Ratio, Rb_Concentration_Ratio, Sr_Concentration_Ratio, Mo_Concentration_Ratio, Ag_Concentration_Ratio, Cd_Concentration_Ratio, Cs_Concentration_Ratio, Ba_Concentration_Ratio (with possible two variants 1 and 2), Tl_Concentration_Ratio, Pb_Concentration_Ratio, U_Concentration_Ratio
- Special indicators:
  - Some elements have a less-than marker (e.g., <Be_Concentration_Ratio, <Se_Concentration_Ratio, <U_Concentration_Ratio) to denote concentration ratios below a threshold.
  - Ba_Concentration_Ratio_1 and Ba_Concentration_Ratio_2 (multiple representations for certain elements)
- Data formatting notes:
  - Units field often marked as n/a
  - Some lines show garbled or partially missing descriptions in the header (interpretation required for data integration)

## Calculation Details
- Primary calculation:
  - Concentration Ratio = Fresh Mass Bee (wholebody) concentration divided by Dry Mass Soil concentration
- Columns reflect element-specific concentration ratios for a broad suite of elements, with some entries indicating less-than values rather than exact figures.

## Metadata, Provenance, and Documentation
- Links to sampling events and codes via CEH_Sample_Codes and CEH_Sample_Description
- Co-located soil sample context used to derive ratios
- Sample preparation details and notes provide contextual metadata for reproducibility and assessment of data quality

## Data Quality, Standards, and Limitations
- Metadata completeness varies; many fields show Units = n/a, indicating missing unit metadata
- Some header descriptions are inconsistent or partially garbled, which may affect data integration across datasets
- Presence of less-than indicators requires clear handling during analysis to avoid misinterpretation
- Cross-referencing between bee and soil samples depends on the Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio field

## Implications for Data Leadership and Use
- Supports environmental monitoring and assessment of bee exposure to soil-derived elements through bioaccumulation indicators
- Highlights need for data governance practices:
  - Standardize units and metadata across related datasets
  - Ensure consistent naming and versioning for concentration-ratio fields (e.g., Ba_Concentration_Ratio_1/2)
  - Improve data discoverability by harmonizing field definitions and providing complete provenance
- Encourages data system thinking and cross-domain collaboration (bee data linked to soil context) to strengthen analytical capabilities and co-ownership of data products
- Useful for risk assessment, policy support, and networked data sharing across partners if standardized and integrated with other datasets (e.g., soil chemistry, bee health metrics)