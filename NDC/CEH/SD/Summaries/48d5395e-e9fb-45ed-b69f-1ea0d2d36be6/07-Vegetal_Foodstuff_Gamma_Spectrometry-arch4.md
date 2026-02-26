# Supporting documentation for 07-Vegetal_Foodstuff_Spectrometry.csv

## Scope and purpose
- Provides the metadata and field explanations for the Vegetal Foodstuff Spectrometry dataset.
- Documents sample metadata (ID, type, location, description, collection date, size) and radiometric measurements (Ra-226, Ra-228, Cs-137, K-40) with uncertainties and detection limits.
- Notes sample-specific unit conventions (dry mass basis; olive oil and wine may use Bq/L) and in-equilibrium relationships between isotopes.

## Data structure and key fields
- Sample_Code: unique sample identifier.
- Sample_Type: general description of sample group.
- Location: collection site name.
- Sample_Description: part of the plant analysed (sub-sample description).
- Collection_Date: date of sample collection (dd-mm-yyyy).
- Sample_size: amount analyzed (e.g., kg fresh matter or L for olive oil and wine).
- Ra-226_Bq/kg_dm: Ra-226 activity on a dry mass basis.
- Unc_Ra-226_Bq/kg_dm: uncertainty of Ra-226 on a dry mass basis.
- Detection_Limit_Ra-226_Bq/kg_dm: ISO 11929-based detection limit for Ra-226.
- Cs-137_Bq/kg_dm: Cs-137 activity on a dry mass basis.
- Unc_Cs-137_Bq/kg_dm: uncertainty of Cs-137 on a dry mass basis.
- Detection_Limit_Cs-137_Bq/kg_dm: detection limit for Cs-137.
- Ra-228_Bq/kg_dm: Ra-228 activity on a dry mass basis.
- Unc_Ra-228_Bq/kg_dm: uncertainty of Ra-228.
- Detection_Limit_Ra-228_Bq/kg_dm: detection limit for Ra-228 (ISO 11929).
- K-40_Bq/kg_dm: K-40 activity on a dry mass basis.
- Unc_K-40_Bq/kg_dm: uncertainty of K-40.
- Detection_Limit_K-40_Bq/kg_dm: detection limit for K-40 (ISO 11929).

## Measurement details and conventions
- Units: primary units are Bq/kg_dm; for olive oil and wine, Bq/L may apply.
- Detection limits: determined according to ISO 11929.
- Equilibrium notes: Ra-226 in equilibrium with Pb-214 and Bi-214; Ra-228 in equilibrium with Ac-228.
- Missing values (blanks) indicate concentrations below detection limits or unspecified data.

## Data quality, gaps and challenges
- Detection-limit information is essential for interpreting non-detects.
- Some fields may be sample-type dependent (unit differences).
- Metadata completeness and standardization are crucial for cross-study comparability.

## Metadata, standards, and discoverability
- Provides explicit explanations for each field to support data understanding and reuse.
- Adheres to ISO 11929 for detection limits; notes on isotope equilibrium inform data interpretation.
- Clear structure supports data discovery, provenance tracing, and potential integration with other datasets.

## Data governance, accessibility, and usage
- Data can support risk assessment, regulatory compliance, and research on radionuclide content in vegetal foods.
- Requires consistent governance: unit standardization, clear handling of below-detection-limit values, and updated documentation.
- Potential for integration into a broader data catalog with standardized vocabularies and cross-dataset links.

## Recommendations for data leaders
- Standardize units across all samples; clearly flag per-sample unit usage (Bq/kg_dm vs Bq/L).
- Implement a consistent “below detection limit” indicator to accompany blank values.
- Enforce controlled vocabularies for Sample_Type and ensure consistent sample descriptions.
- Document data provenance: collection methods, instrumentation, QA/QC procedures, and any data transformations.
- Align metadata with established data standards (ISO 11929 for detection limits) and maintain a detailed data dictionary.
- Enhance discoverability: assign persistent identifiers, publish in a data catalog, and provide API access or downloadable formats.
- Identify and address data gaps (granularity, missing isotopes) through planned sampling or data augmentation.
- Clearly articulate data lineage and relationships between isotopes (e.g., equilibrium context) to aid interpretability in analyses and dashboards.