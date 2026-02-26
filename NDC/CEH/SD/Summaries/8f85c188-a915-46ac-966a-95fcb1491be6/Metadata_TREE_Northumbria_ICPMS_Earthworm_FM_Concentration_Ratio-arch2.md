# TREE_Northumbria_ICPMS_Earthworm_FM_Concentration_Ratio

## Purpose and scope
- Dataset documenting concentration ratios of a wide range of elements in earthworms (fresh mass, whole body) relative to the dry mass of soil.
- Aimed at monitoring environmental health and informing policy performance with a consistent, auditable format.

## Data content and structure
- Metadata fields:
  - Latin_Species_Name, Common_Species_Name: taxonomic details of the earthworm species sampled.
  - Site: sampling location.
  - Date_Sample_Collected: date of collection.
  - CEH_Sample_Codes and CEH_Sample_Description: internal sample identifiers and preparation notes.
  - Notes: additional sample-related information.
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio: description of the soil sample used for the ratio calculation.
- Concentration ratio variables:
  - I_Concentration_Ratio, Li_Concentration_Ratio, Be_Concentration_Ratio, Na_Concentration_Ratio, Mg_Concentration_Ratio, Al_Concentration_Ratio, P_Concentration_Ratio, K_Concentration_Ratio, Ca_Concentration_Ratio, Ti_Concentration_Ratio, V_Concentration_Ratio, Cr_Concentration_Ratio, Fe_Concentration_Ratio, Co_Concentration_Ratio, Ni_Concentration_Ratio, Cu_Concentration_Ratio, Zn_Concentration_Ratio, As_Concentration_Ratio, Se_Concentration_Ratio, Rb_Concentration_Ratio, Sr_Concentration_Ratio, Mo_Concentration_Ratio, Ag_Concentration_Ratio, Cd_Concentration_Ratio, Cs_Concentration_Ratio, Ba_Concentration_Ratio, Tl_Concentration_Ratio, Pb_Concentration_Ratio, U_Concentration_Ratio.
  - Definition for each: Concentration Ratio = Fresh Mass Earthworm (whole body) divided By Dry Mass Soil.
  - Notes: For Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, there are descriptive notes indicating the ratio calculation reference (often tied to the same fresh/wet vs. dry soil basis).
  - U_Concentration_Ratio has two entries (1 and 2), with the second defined as the U Concentration Ratio (Fresh Mass Earthworm (wholebody) divided By Dry Mass Soil).

## Calculation method
- Concentration ratios are derived by dividing the fresh mass of the earthworm (whole body) by the dry mass of the associated soil for each element listed.
- The dataset links each earthworm sample to a co-located soil sample used in the ratio calculation, ensuring traceability.

## Relevance to environmental monitoring
- Provides a standardised, comparable set of bioavailability metrics across multiple elements.
- Supports assessments of environmental health and the effectiveness of policy/management over time.
- Outputs are suitable for inclusion in reports, maps, and charts to illustrate metal transfer from soil to biota.

## Data management and accessibility
- Emphasises storing and uploading created datasets to appropriate portals.
- Aligns with aiming to enable access to the underlying data used to produce final outputs for transparency and reuse.

## Challenges and opportunities for analysts
- Increasing the value of the datasets by integrating with other relevant environmental data (beyond single-use analyses).
- Improving access to underlying data to support broader scrutiny and secondary analyses.