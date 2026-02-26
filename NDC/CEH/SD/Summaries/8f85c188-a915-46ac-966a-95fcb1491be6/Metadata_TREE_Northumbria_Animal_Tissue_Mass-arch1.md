# TREE_Northumbria_Animal_Tissue_Mass

## Data overview
- A dataset describing tissue measurements from animal samples, including species, sample identifiers, tissue type, and mass metrics in kilograms.
- Includes both fresh tissue mass and mass after freeze-drying, plus a ratio between fresh and dry mass.
- Some fields are not applicable for certain estimates (e.g., total muscle and total bone estimates).

## Fields and definitions
- Latin_Species_Name: Latin name of the species.
- CEH_Sample_Code: CEH sample codes associated with the animal or sample. Not applicable for estimates of total muscle and total bone.
- CEH_Sample_Description: Description of the CEH sample.
- Tissue: Type of tissue.
- Tissue_Fresh_Mass_kg: Fresh mass of the tissue in kilograms. Not available where mass was not obtained.
- Tissue_Freeze_Dried _Mass_kg: Mass of the tissue after freeze-drying in kilograms. Not available where mass was not obtained.
- Fresh_Mass_Dry _Mass_Ratio: Ratio of fresh mass to freeze-dried mass for the tissue. Not available when the ratio cannot be calculated.
- General_Notes: General notes related to the sample or measurements.

## Data quality and handling considerations
- Not available indicates missing data.
- Some calculations (e.g., totals for muscle or bone) may not be applicable to this dataset.
- Inconsistent field formatting (e.g., spacing in field names like "Tissue_Freeze_Dried _Mass_kg") may require standardisation during data preparation.

## Analytical opportunities for analysts
- Compare tissue masses across species and tissue types to identify patterns.
- Use Fresh_Mass_Dry _Mass_Ratio to infer tissue composition (water content) where appropriate.
- Link masses to CEH sample codes to trace provenance and ensure reproducibility.
- Assess data completeness by field and species, and plan imputation or careful interpretation where data are missing.