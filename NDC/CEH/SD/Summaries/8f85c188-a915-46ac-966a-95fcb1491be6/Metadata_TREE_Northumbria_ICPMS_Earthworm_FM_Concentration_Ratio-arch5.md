# TREE_Northumbria_ICPMS_Earthworm_FM_Concentration_Ratio

## Overview
- Dataset records concentration ratios of various elements in earthworms (fresh mass, whole body) divided by the dry mass of soil.
- Associated with Northumbria/ICPMS analysis and includes sample metadata and context about the co-located soil samples used for ratio calculations.

## Key Variables and Metadata
- Species and site identifiers:
  - Latin_Species_Name, Common_Species_Name
  - Site
  - Date_Sample_Collected
- Sample identifiers and descriptions:
  - CEH_Sample_Codes
  - CEH_Sample_Description
  - Notes
- Soil context:
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio
- Concentration ratio variables (element-specific):
  - I_Concentration_Ratio, Li_Concentration_Ratio, Be_Concentration_Ratio, Na_Concentration_Ratio, Mg_Concentration_Ratio, Al_Concentration_Ratio, P_Concentration_Ratio, K_Concentration_Ratio, Ca_Concentration_Ratio, Ti_Concentration_Ratio, V_Concentration_Ratio, Cr_Concentration_Ratio, Fe_Concentration_Ratio, Co_Concentration_Ratio, Ni_Concentration_Ratio, Cu_Concentration_Ratio, Zn_Concentration_Ratio, As_Concentration_Ratio, Se_Concentration_Ratio, Rb_Concentration_Ratio, Sr_Concentration_Ratio, Mo_Concentration_Ratio, Ag_Concentration_Ratio, Cd_Concentration_Ratio, Cs_Concentration_Ratio, Ba_Concentration_Ratio, Tl_Concentration_Ratio, Pb_Concentration_Ratio
- Uranium (special case):
  - U_Concentration_Ratio_1 (listed as 1 = not applicable in some entries)
  - U_Concentration_Ratio_2 (defined as U Concentration Ratio: Fresh Mass Earthworm divided By Dry Mass Soil)

## Data Collection and Provenance
- Samples collected from specific sites with earthworm tissue analyzed by ICP-MS.
- Concentration ratios calculated using fresh earthworm mass divided by dry soil mass.
- Sample preparation and descriptive notes captured in CEH_Sample_Description and Notes.

## Data Quality, Standards, and Anomalies
- Units field often shows n/a; standardization of units is needed.
- Some metadata entries show inconsistencies or typographical issues (e.g., Fe_Concentration_Ratio description referencing MnConcentration Ratio; Tl_Concentration_Ratio_ trailing underscore).
- U_Concentration_Ratio includes multiple fields with ambiguous labeling (1 and 2 variants) requiring clarification.
- Overall data governance should ensure consistent field names, complete metadata, and harmonized units.

## Provenance and Documentation Needs
- Document the link between the soil sample used and the specific concentration ratio calculation (co-located soil context).
- Maintain clear meaning for CEH_Sample_Codes and CEH_Sample_Description to support reproducibility.

## Access, Use, and Maintenance
- Data are intended for inclusion in portals/catalogues of dataset holdings; suitable for cross-dataset analyses of uptake and environmental exposure.
- Regular updates should align with data creators to maintain current and historical comparisons.

## Challenges and Recommendations for Data Stewards
- Incomplete user needs: clearly define expected outputs and data formats for end users.
- Timely data delivery: establish processes to chase and receive data promptly from creators.
- Standards adherence: implement a controlled vocabulary for Site, Species, and sample descriptions; enforce consistent units across all concentration ratio fields.
- Interoperability: align column naming and data types to common schemas to facilitate cross-dataset merging.
- Handling large/complex data: plan for efficient storage, transfer, and retrieval of multi-element ratio data.