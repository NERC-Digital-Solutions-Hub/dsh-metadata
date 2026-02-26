# Supporting documentation for 18-Transfer_Parameter_Animal_Gamma_Spectrometry.csv

- Purpose of the document
  - Provides metadata and explanations for the 18-Transfer_Parameter_Animal_Gamma_Spectrometry.csv dataset.
  - Defines what each field represents to support data provenance, quality, and reuse in environmental health monitoring.

- Dataset scope and key variables
  - Sample_Code: Unique sample identifier.
  - Sample_Type: Example value "Soil".
  - Location: Name of the sampling site.
  - Sample_Description: Part of the organism analysed (e.g. where the whole organism was divided and analysed separately).
  - Collection_Date: Date of sample collection (format dd-mm-yyyy).
  - Radionuclide transfer parameters (CR values) and related fields:
    - Ra-226_CR, Unc_Ra-226_CR, Detection_Limit_Ra-226_CR
    - Cs-137_CR, Unc_Cs-137_CR, Detection_Limit_Cs-137_CR
    - Ra-228_CR, Unc_Ra-228_CR, Detection_Limit_Ra-228_CR
    - K-40_CR, Unc_K-40_CR, Detection_Limit_K-40_CR
  - CR values: described as either unitless or kg dry matter per liter for milk.
  - Unc_..._CR: uncertainty corresponding to each CR value.
  - Detection_Limit_..._CR: detection limit corresponding to each CR value.
  - Notes: Indicates if a CR value is blank or "Not Determined" to denote values below the detection limit.

- Data interpretation rules
  - If CR value is blank or marked Not Determined, the value is below the detection limit.
  - Units for CR values may be unitless or kg dry matter per liter (milk).

- Data quality and governance implications
  - Metadata quality is essential to verify data applicability and comparability across samples and radionuclides.
  - Presence of uncertainty and detection-limit fields supports robust interpretation and uncertainty propagation in monitoring analyses.
  - Standardized date formats and explicit sample descriptions aid traceability and reproducibility.
  - Clear documentation of data fields facilitates data sharing and governance aligned with monitoring frameworks.