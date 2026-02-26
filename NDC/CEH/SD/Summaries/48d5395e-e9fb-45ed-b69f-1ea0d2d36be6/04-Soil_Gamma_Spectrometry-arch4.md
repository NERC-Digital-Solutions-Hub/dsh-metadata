# Supporting documentation for 04-Soil_Gamma_Spectrometry.csv

- Purpose of the dataset
  - Documentation for soil gamma spectrometry samples, capturing sample identity, context, and measured radionuclide concentrations.

- Core sample metadata
  - Sample_Code: Unique sample identifier
  - Sample_Type: Soil
  - Location: Name of where the sample was collected
  - Sample_Description: Further explication of the sample (e.g., soil collected at depth 0-10 cm)
  - Collection_Date: Date of collection (format dd-mm-yyyy)
  - Sample_size: Amount analyzed in kilograms of dry matter (Kg dry matter)

- Measured radionuclides and associated data
  - Ra-226_Bq/kg_dm: Activity concentration of Ra-226 on a dry mass basis
  - Unc_Ra-226_Bq/kg_dm: Uncertainty of Ra-226 concentration
  - Detection_Limit_Ra-226_Bq/kg_dm: Detection limit for Ra-226 (ISO 11929)
  - Cs-137_Bq/kg_dm: Activity concentration of Cs-137 on a dry mass basis
  - Unc_Cs-137_Bq/kg_dm: Uncertainty of Cs-137 concentration
  - Detection_Limit_Cs-137_Bq/kg_dm: Detection limit for Cs-137 (ISO 11929)
  - Ra-228_Bq/kg_dm: Activity concentration of Ra-228 on a dry mass basis (in equilibrium with Ac-228)
  - Unc_Ra-228_Bq/kg_dm: Uncertainty for Ra-228 concentration (notes indicate equilibrium with Ac-228)
  - Detection_Limit_Ra-228_Bq/kg_dm: Detection limit for Ra-228 (ISO 11929)
  - K-40_Bq/kg_dm: Activity concentration of K-40 on a dry mass basis
  - Unc_K-40_Bq/kg_dm: Uncertainty for K-40 concentration
  - Detection_Limit_K-40_Bq/kg_dm: Detection limit for K-40 (ISO 11929)

- Measurement interpretation notes
  - Where a value is blank for a concentration, it indicates the concentration was below the detection limit.
  - Several fields note equilibrium with progeny isotopes (e.g., Pb-214, Bi-214 for Ra-226; Ac-228 for Ra-228).
  - Some metadata entries include enumerated subfields (e.g., “1 = …, 2 = …, 3 = …”) which suggests formatting inconsistencies in the data dictionary.

- Data quality and standards considerations
  - Detection limits are calculated according to ISO 11929.
  - Consistency in units across all concentration fields: Bq per kg dry matter.
  - Potential data standardization issues (misformatted notes and nested subfields) that may affect integration with other datasets.

- Governance and usage considerations for Data Leaders
  - The dataset supports environmental radiological monitoring and soil contamination assessment, with clear metadata for discoverability and interpretation.
  - Important to maintain provenance, versioning, and consistent unit conventions when integrating with broader data systems.
  - Non-detect handling is explicit (blank ≈ below detection limit), but consistent application across all isotopes is essential for robust analysis.
  - Documentation would benefit from a standardized data dictionary to resolve formatting inconsistencies and clarify multi-field notes.