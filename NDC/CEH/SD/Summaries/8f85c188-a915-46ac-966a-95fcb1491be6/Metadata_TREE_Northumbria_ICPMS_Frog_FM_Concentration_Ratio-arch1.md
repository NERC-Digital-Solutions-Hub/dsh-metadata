# TREE_Northumbria_ICPMS_Bee_FM_Concentration_Ratio

## Overview
- Data dictionary for a dataset that records concentration ratios of multiple elements in bees relative to soil, based on ICP-MS analyses conducted by Northumbria (CEH context).
- Focuses on bee samples (whole body fresh mass) and their associated soil samples (dry mass) used to compute concentration ratios.
- Includes both biological sample metadata and a wide set of element-specific concentration ratio fields, enabling exposure and environmental transfer analyses at local scales.

## Key Data Fields
- Biological and sampling metadata
  - Latin_Species_Name
  - Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes
  - Sample_Details
  - CEH_Sample_Description
  - Notes
- Soil-bee linkage
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio
  - (Description of soil sample used to calculate the concentration ratio)
- Concentration ratio fields
  - I_Concentration_Ratio
  - Li_Concentration_Ratio
  - Be_Concentration_Ratio
  - Na_Concentration_Ratio
  - Mg_Concentration_Ratio
  - Al_Concentration_Ratio
  - P_Concentration_Ratio
  - K_Concentration_Ratio
  - Ca_Concentration_Ratio
  - Ti_Concentration_Ratio
  - V_Concentration_Ratio
  - Cr_Concentration_Ratio
  - Mn_Concentration_Ratio
  - Fe_Concentration_Ratio
  - Co_Concentration_Ratio
  - Ni_Concentration_Ratio
  - Cu_Concentration_Ratio
  - Zn_Concentration_Ratio
  - As_Concentration_Ratio
  - Se_Concentration_Ratio
  - Rb_Concentration_Ratio
  - Sr_Concentration_Ratio
  - Mo_Concentration_Ratio
  - Ag_Concentration_Ratio
  - Cd_Concentration_Ratio
  - Cs_Concentration_Ratio
  - Ba_Concentration_Ratio
  - Tl_Concentration_Ratio
  - Pb_Concentration_Ratio
  - U_Concentration_Ratio
- Data note indicators
  - Entries such as <Be, <Se, <U to flag concentration ratios that are less-than values

## Concentration Ratio Definition
- Each element-specific concentration ratio is defined as:
  - Fresh Mass Bee (wholebody) concentration divided by Dry Mass Soil
- For each element, there is a corresponding Concentration_Ratio field (e.g., Be_Concentration_Ratio, Na_Concentration_Ratio, etc.)
- Some ratio fields may contain less-than values (e.g., <Be, <Se, <U) to indicate censored or detection-limit-related values.

## Metadata and Sample Details
- Sampling and identification details are captured to enable traceability and reproducibility:
  - Species information (Latin and common names)
  - Sampling site and collection date
  - CEH sample codes and descriptions
  - Sample preparation details and general notes
  - Linked soil sample details used in concentration ratio calculations

## Data Quality and Access Considerations
- Many fields are listed with Units = n/a, indicating no standard unit specification within this header.
- Potential data quality issues relevant to analysts:
  - Local-scale data availability and linkage between bee and soil samples
  - Handling of censored data (less-than concentration ratios)
  - Consistency of sample identifiers and soil-bee pairing
- The dataset emphasizes clear provenance (CEH Northumbria context) and traceable sample metadata to support rigorous analyses.

## Potential Analytical Uses
- Investigate correlations between soil metal concentrations and bee body concentrations across sites and dates.
- Compare concentration ratios across species, sites, or time periods to assess exposure pathways.
- Identify which elements show stronger transfer from soil to bees in a local ecological context.
- Support risk assessments and environmental monitoring by linking bee exposure data to soil contamination metrics.

## Practical Considerations for Analysts
- Ensure proper alignment of bee samples with their co-located soil samples when computing or interpreting concentration ratios.
- Pay attention to less-than values as they may require censoring methods or substitution with detection-limit approaches.
- Leverage the metadata fields (species, site, date, sample codes) to stratify analyses and enhance interpretability of results.