# TREE_Northumbria_Animal_Tissue_Mass

## Overview
- A data schema for the Northumbria animal tissue mass dataset, detailing how species, samples, tissue types, and mass measurements are represented for map-based data products.
- Supports linking Latin species names, CEH sample codes/descriptions, tissue type, and mass data (fresh and freeze-dried) with general notes for context.

## Data Fields (with purposes and units)
- Latin_Species_Name
  - Units: n/a
  - Explanation: Latin name of species
- CEH_Sample_Code
  - Units: n/a
  - Explanation: CEH sample codes associated with the animal or sample
  - Note: Not applicable for estimates of total muscle and total bone
- CEH_Sample_Description
  - Units: n/a
  - Explanation: CEH sample description
- Tissue
  - Units: n/a
  - Explanation: Tissue type
- Tissue_Fresh_Mass_kg
  - Units: kg
  - Explanation: Tissue fresh mass in kilograms
  - Not available indicates mass was not obtained
- Tissue_Freeze_Dried_Mass_kg
  - Units: kg
  - Explanation: Tissue freeze dried mass in kilograms
  - Not available indicates mass was not obtained
- Fresh_Mass_Dry_Mass_Ratio
  - Units: kg - kilograms
  - Explanation: Fresh mass to freeze dry mass ratio of tissue
  - Not available indicates no ratio can be calculated
- General_Notes
  - Units: n/a
  - Explanation: General notes

## Data Quality and Gaps
- Missing values are indicated as Not available; some fields may be inapplicable (n/a) or not calculable (e.g., ratio for certain samples).
- CEH_Sample_Code has special handling: not applicable for estimates of total muscle and total bone.