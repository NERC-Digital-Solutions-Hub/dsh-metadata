# TREE_Northumbria_Animal_Tissue_Mass

## Overview
- Dataset detailing tissue masses (fresh and freeze-dried) for animal samples, with species name and associated sample identifiers.
- Fields include tissue type, mass measurements, and descriptive notes.
- Units primarily in kilograms; some fields are not applicable or not available.

## Data fields and definitions
- Latin_Species_Name: Latin name of the species.
- CEH_Sample_Code: CEH sample codes linked to the animal or sample (not applicable for estimates of total muscle and total bone).
- CEH_Sample_Description: Description of the CEH sample.
- Tissue: Type of tissue measured.
- Tissue_Fresh_Mass_kg: Fresh mass of the tissue (kg).
- Tissue_Freeze_Dried_Mass_kg: Mass after freeze-drying (kg).
- Fresh_Mass_Dry_Mass_Ratio: Ratio of fresh mass to freeze-dried mass (dimensionless).
- General_Notes: Additional notes or context.

## Data quality and metadata considerations
- Not available values indicate missing measurements.
- Some fields are not applicable for certain estimates (e.g., total muscle or total bone).
- Metadata clarity is essential to interpret fields (e.g., Latin name, tissue type, sample codes).
- Mass values are provided in kilograms; ensure consistent handling of missing data and ratios.

## Data governance and sharing implications
- Clear documentation of what each field represents supports transparency for monitoring purposes.
- Some data points (sample codes and descriptions) may require careful governance to maintain context and reproducibility.
- When sharing datasets, note which fields are optional, not applicable, or missing to avoid misinterpretation.

## Relevance for environmental health monitoring
- Provides quantitative tissue mass measurements that can inform biomass analyses, tissue-specific health indicators, and comparisons across species.
- The Fresh Mass to Freeze-Dried Mass ratio enables assessments of tissue density or preservation effects.
- Supports reporting and dashboards through clear data definitions and consumable units.

## Challenges and gaps to address in monitoring contexts
- Handling missing data and determining when estimates are feasible.
- Ensuring consistent metadata to verify data suitability for specific monitoring analyses.
- Managing transformations or standardizations required to integrate with other datasets (e.g., aligning tissue nomenclature).

## Practical notes for analysts and managers
- Verify species identification via Latin_Species_Name for accurate cross-dataset analyses.
- Use Tissue and mass fields together to compute tissue mass indices where appropriate.
- Document any data gaps or non-applicable fields when reporting results.