# Supporting documentation for 11-Feedstuff_Gamma_Spectrometry.csv

## Purpose and scope
- Provides metadata and field definitions for a dataset of gamma spectrometry results on feedstuff.
- Establishes how sample information and radionuclide activity concentrations are recorded, interpreted, and linked to measurement metadata.

## Data fields and metadata

- Sample_Code: Unique sample identifier (no units; notes column present).
- Sample_Type: General description of the sample (no units; notes column present).
- Location: Location where the sample was collected (no units; notes column present).
- Sample_Description: Part of the organism analyzed (e.g., tissue or section) (no units; notes column present).
- Collection_Date: Date of sample collection (units: dd-mm-yyyy).
- Sample_size: Amount of sample analyzed (units: kg fresh mass).

## Radionuclide measurements and related fields

- Ra-226_Bq/kg_dm: Activity concentration of Ra-226 on a dry mass basis (units: Bq/kg dry mass). Notes specify equilibrium with Pb-214 and Bi-214; blanks indicate concentrations below detection limit.
- Unc_Ra-226_Bq/kg_dm: Uncertainty of Ra-226 activity concentration (units: Bq/kg dry mass); linked to the same equilibrium context.
- Detection_Limit_Ra-226_Bq/kg_dm: Detection limit for Ra-226 (units: Bq/kg dry mass); calculated according to ISO 11929; context notes about equilibrium.
- Cs-137_Bq/kg_dm, Unc_Cs-137_Bq/kg_dm, Detection_Limit_Cs-137_Bq/kg_dm: Analogous fields for Cs-137 on a dry mass basis; blanks denote non-detects.
- Ra-228_Bq/kg_dm, Unc_Ra-228_Bq/kg_dm, Detection_Limit_Ra-228_Bq/kg_dm: Ra-228 measurements; notes specify equilibrium with Ac-228; some fields include multiple labeled components (e.g., 1, 2, 3) within Unc_ and Detection_Limit_.
- K-40_Bq/kg_dm, Unc_K-40_Bq/kg_dm, Detection_Limit_K-40_Bq/kg_dm: K-40 measurements on a dry mass basis with corresponding uncertainties and detection limits; blanks indicate non-detects.

## Interpretation and data conventions

- Non-detects are represented by blank fields; detection limits indicate the threshold at which a value would be reported as detectable (per ISO 11929).
- Equilibrium assumptions are explicitly stated for Ra-226 (with Pb-214 and Bi-214) and Ra-228 (with Ac-228), affecting interpretation of activity concentrations.
- Data are standardized to a dry mass basis for radionuclide concentrations; collection date uses a consistent dd-mm-yyyy format.

## Data quality and standards

- Detection limits are calculated using an ISO standard (ISO 11929).
- Metadata explicitly describes the sample context, measurement basis (dry mass), and equilibrium conditions to support comparability and auditability across monitoring efforts.

## Data governance and practical implications for monitoring frameworks

- The dataset exemplifies the need for clear, machine-actionable metadata to support reproducibility, quality assurance, and data sharing in monitoring programs.
- Includes explicit definitions for each field, units, and interpretation rules (e.g., handling of non-detects and equilibrium conditions), which are essential for cross-program data integration and reporting.
- Highlights potential challenges for framework authors: ensuring completeness of metadata, consistent notation (especially for multi-component uncertainty/detection-limit fields), and alignment with methodological standards (ISO 11929) and mass basis conventions.