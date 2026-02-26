# TREE_Northumbria_ICPMS_Vole_FM_Concentration_Ratio

## Overview
- Defines the data schema for a dataset of ICP-MS concentration ratios in vole tissue relative to associated soil samples.
- Supports environmental monitoring by standardising data capture, provenance, and interpretation of metal/element ratios in small mammals.
- Emphasises data quality, reproducibility, and traceability to sampling and soil context.

## Data Model (Key Columns)
- Species and identifiers
  - Latin_Species_Name
  - Common_Species_Name
- Spatial and temporal context
  - Site
  - Date_Sample_Collected
- Sample identifiers and descriptions
  - CEH_Sample_Code
  - CEH_Sample_Description
  - Notes
- Provenance and linkage
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio
- Concentration ratio calculations
  - I_Concentration_Ratio: Fresh Mass Vole (wholebody) divided By Dry Mass Soil
  - Ba_Concentration_Ratio (and Ba_Concentration_Ratio_1, Ba_Concentration_Ratio_2)
  - For each element: Be, Li, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Tl, U
  - Each element has a corresponding _Concentration_Ratio (Fresh Mass Vole divided By Dry Mass Soil)
  - Special markers
    - <Be, <Ni, <Ag, <U: indicate the concentration ratio is a “less-than” (detection-limit) value
- Units
  - All concentration ratio fields listed as n/a units (ratios without units in this schema)

## Concentration Ratio Calculations
- Concentration ratios are defined as the ratio of vole whole-body fresh mass to the associated dry mass of soil, enabling normalization across samples.
- Some elements include two related fields (e.g., Ba_Concentration_Ratio_1 and Ba_Concentration_Ratio_2), suggesting multiple ratio measurements or formats per element.
- Detection-limit values are represented with less-than markers (e.g., <Be, <Ni).

## Data Provenance and Quality
- Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio provides linkage between vole samples and the soil samples used for ratio computation.
- CEH_Sample_Code and CEH_Sample_Description capture standardized sample identifiers and context.
- Notes field allows recording of sample-specific information that may affect interpretation.
- The schema standardizes data capture to support verification and reproducibility across monitoring programmes.

## Outputs and Use by Analysts
- Enables consistent reporting formats (tables, maps, charts) for environmental health assessments and policy performance over time.
- Supports archival storage and portal uploads of standardized datasets.
- Facilitates cross-site comparisons of metal concentrations in small mammals relative to soil, informing contamination assessments and risk analyses.

## Challenges and Opportunities
- Increasing the value of datasets by integrating these concentration-ratio data with other environmental datasets (e.g., climate, land use, pollution sources) to support broader analyses.
- Ensuring broad access to underlying data used to generate final concentration-ratio outputs to enable secondary analyses and transparency.

## Data Storage and Access
- Emphasizes proper storage of the created datasets and uploading to appropriate portals, ensuring long-term accessibility and interoperability.

## Additional Notes
- The dataset uses a comprehensive, explicit field-level description to minimize ambiguity and support consistent data interpretation across monitoring programs.