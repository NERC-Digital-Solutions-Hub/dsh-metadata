# TREE_Northumbria_ICPMS_Toad_FM_Concentration_Ratio

## Purpose and Context
- Dataset describing concentration ratios of multiple elements in toads, using Fresh Mass Toad (whole body) divided by Dry Mass Soil.
- Data collected from toad samples with co-located soil samples to compute concentration ratios.
- An ICP-MS-based measurement approach underpins the dataset.
- Metadata fields capture species names, site, date, sample codes, descriptions, and notes on preparation.

## Data Structure and Key Variables
- Core identifiers and metadata:
  - Latin_Species_Name
  - Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Code
  - CEH_Sample_Description
  - Notes (preparation details)
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio
- Concentration ratio fields (examples):
  - I_Concentration_Ratio, Li_Concentration_Ratio, Be_Concentration_Ratio, Na_Concentration_Ratio, Mg_Concentration_Ratio, Al_Concentration_Ratio, P_Concentration_Ratio, K_Concentration_Ratio, Ca_Concentration_Ratio, Ti_Concentration_Ratio, V_Concentration_Ratio, Cr_Concentration_Ratio, Mn_Concentration_Ratio, Fe_Concentration_Ratio, Co_Concentration_Ratio, Ni_Concentration_Ratio, Cu_Concentration_Ratio, Zn_Concentration_Ratio, As_Concentration_Ratio, Se_Concentration_Ratio, Rb_Concentration_Ratio, Sr_Concentration_Ratio, Mo_Concentration_Ratio, Ag_Concentration_Ratio, Cd_Concentration_Ratio, Cs_Concentration_Ratio, Ba_Concentration_Ratio, Tl_Concentration_Ratio, Pb_Concentration_Ratio, U_Concentration_Ratio
- Each Concentration_Ratio field is described as the Fresh Mass Toad (whole body) divided by Dry Mass Soil.

## Data Quality and Processing
- Data are intended to be verified, quality assured, cleaned, and transformed as part of standard monitoring data workflows.
- Outputs are prepared in clear formats (e.g., tables) and stored/uploaded to appropriate data portals.

## Usage and Applications
- Enables assessment of environmental health by providing standardized concentration ratios across elements and sites.
- Supports comparisons over time and across locations, aiding policy performance evaluations.
- Facilitates reporting through maps, charts, and summary documents.
- Can be integrated with other environmental datasets to enhance understanding of exposure and risk.

## Accessibility and Sharing
- Includes a field tying each toad sample to a co-located soil sample, supporting traceability.
- Emphasizes accessibility of underlying data used to create final outputs, enabling reuse beyond single analyses.

## Challenges and Considerations for Analysts
- Increasing the value of the dataset by combining with complementary environmental data (e.g., soil chemistry, water quality) to avoid single-use datasets.
- Ensuring broad access to the underlying data used to produce outputs, while maintaining metadata clarity and provenance.