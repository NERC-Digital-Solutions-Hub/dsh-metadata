# TREE_Northumbria_Animal_Tissue_Mass

## What this dataset captures
- Records tissue mass measurements for animal samples, linking species, sample identifiers, and tissue type to mass metrics.
- Aims to support analysis and self-serve exploration of tissue mass data across different tissues and samples.

## Data fields and definitions
- Latin_Species_Name: Latin name of the species (no units).
- CEH_Sample_Code: CEH sample codes associated with the animal or sample (no units); not applicable for estimates of total muscle and total bone.
- CEH_Sample_Description: Description of the CEH sample.
- Tissue: Tissue type (no units).
- Tissue_Fresh_Mass_kg: Tissue fresh mass in kilograms (kg). Mass not obtained is marked as Not available.
- Tissue_Freeze_Dried_Mass_kg: Tissue freeze-dried mass in kilograms (kg). Mass not obtained is marked as Not available.
- Fresh_Mass_Dry_Mass_Ratio: Ratio of fresh mass to freeze-dried mass (dimensionless but expressed in kg units here). Not available when the ratio cannot be calculated.
- General_Notes: Additional notes (no units).

## Data quality and gaps
- Some mass values may be missing (Not available) for both fresh and freeze-dried masses.
- Notable potential formatting irregularity in field name (e.g., "Tissue_Freeze_Dried _Mass_kg"), which may affect data parsing.
- Variation in how data are recorded across samples and systems; requires careful data cleaning and harmonisation.
- Explanations indicate partial applicability (e.g., CEH sample codes not used for certain estimates).

## Potential data products and analyses
- Dashboards or pivot tables by species, tissue type, and mass metrics (fresh vs. freeze-dried) to support quick comparisons.
- Self-serve exploration of mass distributions and mass ratios across tissues.
- Data provenance and notes field integration to track observations and data quality issues.

## Data integration and access considerations
- Link Latin_Species_Name with taxonomic references for consistent species identifiers.
- Integrate CEH_Sample_Code with broader sample inventories to ensure traceability.
- Maintain unit consistency (kg) and clearly handle missing values (Not available).

## Challenges and recommended actions for Data Support
- Spend time understanding the data ask to determine the best extraction and integration approach.
- Implement data quality checks for missing values, inconsistent field naming, and unit consistency.
- Develop a clear data dictionary and provenance log to aid reproducibility and reuse.
- Promote outputs and gather user feedback; share early prototypes to increase adoption and re-use.