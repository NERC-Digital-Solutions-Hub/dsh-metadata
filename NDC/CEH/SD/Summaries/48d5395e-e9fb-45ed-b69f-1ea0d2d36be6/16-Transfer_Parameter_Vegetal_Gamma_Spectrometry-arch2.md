# Supporting documentation for 16-Transfer_Parameter_Vegetal_Gamma_Spectrometry.csv

- Purpose and scope
  - Provides metadata and explanations for the 16-Transfer_Parameter_Vegetal_Gamma_Spectrometry.csv dataset.
  - Documents transfer parameters (Fv) for vegetally-derived gamma spectrometry, focusing on radionuclide transfer factors in plant-related matrices (olive oil and wine) and soil context.
  - Supports standardized data verification, quality assurance, and eventual publication/archiving within environmental monitoring programs.

- Data structure and key fields
  - Sample_Code: Unique sample identifier.
  - Sample_Type: Indicates the sample is soil.
  - Location: Name of the collection site.
  - Sample_Description: Part of the plant analysed (e.g., portion of the plant used).
  - Collection_Date: Date of sample collection (format dd-mm-yyyy).
  - File focuses on transfer parameter values (Fv) for several radionuclides and their uncertainties/detection limits:
    - Ra-226_Fv: Transfer value for Ra-226.
    - Unc_Ra-226_Fv: Uncertainty of Ra-226 Fv.
    - Detection_Limit_Ra-226_Fv: Detection limit for Ra-226 Fv.
    - Cs-137_Fv: Transfer value for Cs-137.
    - Unc_Cs-137_Fv: Uncertainty of Cs-137 Fv.
    - Detection_Limit_Cs-137_Fv: Detection limit for Cs-137 Fv.
    - Ra-228_Fv: Transfer value for Ra-228.
    - Unc_Ra-228_Fv: Uncertainty of Ra-228 Fv.
    - Detection_Limit_Ra-228_Fv: Detection limit for Ra-228 Fv.
    - K-40_Fv: Transfer value for K-40.
    - Unc_K-40_Fv: Uncertainty of K-40 Fv.
    - Detection_Limit_K-40_Fv: Detection limit for K-40 Fv.
  - For each radionuclide, the dataset notes that blanks indicate the value was below the detection limit, or within detection limits as appropriate.

- Measurement details and units
  - Fv values are described as unitless or expressed as kg dry matter per L for olive oil and wine, depending on the nuclide.
  - K-40_Fv similarly described with units ranging from unitless to kg dry matter per L for olive oil (with references to olive oil and wine in related fields).

- Metadata and data quality considerations
  - Explanations accompany each field to clarify meaning and usage.
  - Uncertainty fields (Unc_*) provide the precision context for each Fv value.
  - Detection limit fields (Detection_Limit_*) indicate when a value is considered non-detect versus detected.
  - Where a Fv value is blank, the accompanying notes indicate this corresponds to non-detect situations or limit-based reporting.

- Data management and accessibility
  - Aligns with the aim of storing, standardizing, and facilitating access to environmental monitoring datasets.
  - Supports uploading to appropriate data portals and downstream analyses, enabling consistency across monitoring outputs (reports, maps, charts).

- Practical implications for environmental monitoring
  - Enables consistent reporting of plant-to-environment transfer factors for key radionuclides in edible/industrial plant matrices.
  - Facilitates quality-controlled comparisons over time and across sites by standardizing sample-type, collection date, location, and plant-portion metadata.
  - Encourages transparent handling of non-detects through explicit detection limits and uncertainty fields.