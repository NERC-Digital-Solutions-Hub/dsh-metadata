# TREE_Northumbria_Animal_Tissue_Mass

## Purpose and Scope
- Defines a structured data schema for recording animal tissue mass measurements associated with Northumbria CEH sampling.
- Captures species identification, sample coding, tissue type, and mass data (fresh and freeze-dried) along with a derived ratio and general notes.
- Supports consistent data collection to enable environmental health monitoring and temporal comparisons.

## Data Fields and Definitions
- Latin_Species_Name: Latin name of the species.
- CEH_Sample_Code: CEH sample codes tied to the animal or sample; not applicable for estimates of total muscle and total bone.
- CEH_Sample_Description: Description of the CEH sample.
- Tissue: Type of tissue.
- Tissue_Fresh_Mass_kg: Fresh tissue mass in kilograms; “Not available” when mass was not obtained.
- Tissue_Freeze_Dried _Mass_kg: Freeze-dried tissue mass in kilograms; “Not available” when mass was not obtained.
- Fresh_Mass_Dry _Mass_Ratio: Ratio of fresh mass to freeze-dried mass; “Not available” when the ratio cannot be calculated.
- General_Notes: Additional general notes.