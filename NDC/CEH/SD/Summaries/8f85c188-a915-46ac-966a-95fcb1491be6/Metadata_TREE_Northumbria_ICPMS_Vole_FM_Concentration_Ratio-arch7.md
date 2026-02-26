# TREE_Northumbria_ICPMS_Vole_FM_Concentration_Ratio

## Purpose and scope
- Data dictionary for a dataset of ICP-MS concentration ratios in voles, comparing vole tissue mass to soil mass.
- Enables map-based visualization and spatial analysis of metal/element transfer from soil to vole tissue.
- Supports GIS-driven exploration of how concentrations vary by site and over time.

## Core fields and meaning
- Species and identification:
  - Latin_Species_Name, Common_Species_Name: scientific and common names of vole species.
- Sampling and location:
  - Site: sampling location identifier.
  - Date_Sample_Collected: date of sampling.
  - CEH_Sample_Code, CEH_Sample_Description: laboratory sample code and description.
  - Notes: ancillary information about the vole sample.
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio: soil sample linked to the vole for ratio calculation.
- Concentration ratios (ratio = Fresh Mass Vole (wholebody) divided By Dry Mass Soil):
  - I_Concentration_Ratio, Li_Concentration_Ratio, Be_Concentration_Ratio, Na_Concentration_Ratio, Mg_Concentration_Ratio, Al_Concentration_Ratio, P_Concentration_Ratio, K_Concentration_Ratio, Ca_Concentration_Ratio, Ti_Concentration_Ratio, V_Concentration_Ratio, Cr_Concentration_Ratio, Mn_Concentration_Ratio, Fe_Concentration_Ratio, Co_Concentration_Ratio, Ni_Concentration_Ratio, Cu_Concentration_Ratio, Zn_Concentration_Ratio, As_Concentration_Ratio, Se_Concentration_Ratio, Rb_Concentration_Ratio, Sr_Concentration_Ratio, Mo_Concentration_Ratio, Ag_Concentration_Ratio, Cd_Concentration_Ratio, Cs_Concentration_Ratio, Ba_Concentration_Ratio, Tl_Concentration_Ratio, Pb_Concentration_Ratio, U_Concentration_Ratio.
- Notation and data nuances:
  - Some elements include special markers (e.g., “<Be”, “<Ni”, “<Ag”, “<U”) indicating values below detection or a threshold.
  - For certain elements, multiple ratio fields exist (e.g., Ba_Concentration_Ratio_1 and Ba_Concentration_Ratio_2; Tl_Concentration_Ratio_1 and Tl_Concentration_Ratio_2, etc.).
  - Units are listed as n/a; the ratios are dimensionless.

## Spatial and temporal context
- Data ties each ratio to a specific sampling site and date, enabling temporal trend analysis and spatial mapping of element transfer patterns.
- Co-located soil samples provide the basis for calculating each vole-to-soil concentration ratio, linking biological and soil geochemical contexts.

## Data quality and structure considerations
- Consistent naming and fields needed for cross-dataset joins (e.g., Site, Date_Sample_Collected, CEH_Sample_Code).
- Some fields contain multiple values or less-than indicators; handling these requires careful parsing and explicit treatment of non-detects.
- Data may include missing or variant fields for certain elements (hence multiple ratio columns for some elements).

## How GIS specialists can use this data
- Map concentration ratios by site to identify spatial patterns of metal uptake in voles.
- Join with site coordinates to create point or area-based maps showing element-specific ratios.
- Compare temporal snapshots using Date_Sample_Collected to visualize changes over time.
- Link with soil data (via Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio) to analyze soil-to-biota transfer in space.
- Use less-than markers to map detection limits and uncertainty in contaminant measurements.
- Combine with species name fields to explore species-specific accumulation patterns.