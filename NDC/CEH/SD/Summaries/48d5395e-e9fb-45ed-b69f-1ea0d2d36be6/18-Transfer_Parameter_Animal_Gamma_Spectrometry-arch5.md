# Supporting documentation for 18-Transfer_Parameter_Animal_Gamma_Spectrometry.csv

## Overview
- Provides a data dictionary for the 18-Transfer_Parameter_Animal_Gamma_Spectrometry.csv dataset.
- Describes each column’s meaning, units, and notes to support data discovery, interpretation, and reuse.
- Focuses on sample metadata and gamma spectrometry concentration ratio (CR) values for multiple radionuclides, including associated uncertainties and detection limits.

## Core data elements

- Sample metadata
  - Sample_Code: Unique sample identifier.
  - Sample_Type: e.g., Soil.
  - Location: Name of the collection location.
  - Sample_Description: Part of the organism analysed (e.g., which portion was studied).
  - Collection_Date: Date of sample collection (format dd-mm-yyyy).

- Radionuclide concentrations (CR values)
  - Ra-226_CR: CR value for Ra-226.
  - Cs-137_CR: CR value for Cs-137.
  - Ra-228_CR: CR value for Ra-228.
  - K-40_CR: CR value for K-40.
  - Units for CR fields: generally listed as Unitless or kg dry matter per L (milk) depending on context.

- Uncertainties
  - Unc_Ra-226_CR: Uncertainty of Ra-226 CR.
  - Unc_Cs-137_CR: Uncertainty of Cs-137 CR.
  - Unc_Ra-228_CR: Uncertainty of Ra-228 CR.
  - Unc_K-40_CR: Uncertainty of K-40 CR.

- Detection limits and data qualifiers
  - Detection_Limit_Ra-226_CR: Detection limit for Ra-226 CR.
  - Detection_Limit_Cs-137_CR: Detection limit for Cs-137 CR.
  - Detection_Limit_Ra-228_CR: Detection limit for Ra-228 CR.
  - Detection_Limit_K-40_CR: Detection limit for K-40 CR.
  - Notes indicate how non-detections are recorded (e.g., blank or “Not Determined” may indicate values below the detection limit).

## Metadata standards and semantics

- Date format and temporal context
  - Collection_Date uses dd-mm-yyyy format; consider standardizing to ISO 8601 for interoperability.

- Units and consistency
  - CR values have inconsistent unit descriptions (Unitless or kg dry matter per L for milk). This may reflect context-dependent usage; harmonization across records is recommended.
  - Uncertainty fields accompany each CR value, enabling proper propagation of uncertainty in downstream analyses.

- Data quality notes
  - The documentation provides explicit notes for detections and non-detections (e.g., blanks often denote below-detection-limit values).
  - Clear mapping between detected values, their uncertainties, and their detection limits supports transparent quality assessment.

## Data governance considerations

- Discoverability and sharing
  - The documentation supports uploading and cataloguing the dataset in relevant data portals, with metadata about sample origin and measurement parameters.

- Provenance and traceability
  - Sample origin (Sample_Code, Location) and collection date provide traceability back to the original field activities.
  - Documentation of measurement parameters (isotopes, CR values, uncertainties, detection limits) supports auditing and reproducibility.

- Interoperability and standards
  - Use of a shared data dictionary format aids interoperability across related datasets (e.g., other Transfer_Parameter datasets).
  - Potential need to align with controlled vocabularies for Sample_Type and Location.

## Data quality challenges and recommendations for Data Stewards

- Incomplete or inconsistent units
  - Action: Standardize CR units across the dataset or document a matrix-specific unit policy; ensure all CR fields clearly specify a single, consistent unit per matrix context.

- Non-detections handling
  - Action: Establish and document a uniform convention for non-detects (e.g., store detection limits and a flag indicating below detection) to enable consistent filtering and analysis.

- Format and encoding
  - Action: Consider adopting ISO 8601 for Collection_Date and a controlled format for Sample_Type and Location to reduce ambiguity.

- Documentation depth
  - Action: Where possible, add definitions for “CR” (e.g., what it stands for in this context), measurement methods, and any matrix-specific considerations to improve reuse by external data users.

## Next steps for data management

- Validate and harmonize units across all CR-related columns.
- Enforce ISO date formatting for Collection_Date.
- Implement a controlled vocabulary for Sample_Type and Location.
- Capture and store explicit non-detection indicators alongside detection limits.
- Maintain versioning and provenance to track updates to metadata or field interpretations.