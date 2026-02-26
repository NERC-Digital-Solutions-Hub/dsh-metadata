# Supporting documentation for 18-Transfer_Parameter_Animal_Gamma_Spectrometry.csv

- Aim of the document
  - Provides explanations, units, and notes for each field in the 18-Transfer_Parameter_Animal_Gamma_Spectrometry.csv dataset to support correct interpretation and use in data products.

- Data structure overview
  - Core identifiers:
    - Sample_Code: Unique sample identifier (no units).
    - Location: Name of the collection site.
    - Sample_Type: Indicates the sample type (example given: Soil).
    - Sample_Description: Specifies the part of the organism analysed (e.g., where whole organism was divided and analysed separately).
    - Collection_Date: Date of sample collection (format: dd-mm-yyyy).
  - Radionuclide transfer parameters (per radionuclide): Ra-226, Cs-137, Ra-228, K-40
    - For each radionuclide, fields include:
      - <Radionuclide>_CR: Transfer ratio/critical value (CR) for that radionuclide.
      - Unc_<Radionuclide>_CR: Uncertainty associated with the CR value.
      - Detection_Limit_<Radionuclide>_CR: Detection limit for the CR value.
    - Units noted across CR fields: Unitless or kg dry matter per L for milk (same units repeated for equivalent fields).
    - Notes for CR fields: If a CR value is blank or Not Determined, it indicates the value was below the detection limit.
    - Notes for Unc_<Radionuclide>_CR: If blank, the CR value was below the detection limit.
    - Notes for Detection_Limit_<Radionuclide>_CR: If blank, the CR value was above the detection limit.
  - Example radionuclides included: Ra-226, Cs-137, Ra-228, K-40
    - Detection limit fields present for each radionuclide (with the same format and notes as above).

- Data quality and interpretation considerations
  - Inconsistencies to watch for:
    - Sample_Type is listed as Soil, while Sample_Description refers to parts of an organism analyzed, suggesting potential mismatch between sample type and analysis description.
    - Units for CR fields are stated as Unitless or kg dry matter per L for milk, which may be context-dependent and should be validated against the actual sample type and matrix.
  - Handling below-detection data:
    - CR values that are blank or Not Determined should be treated as below the detection limit.
    - Uncertainty fields may be blank when the corresponding CR is below the detection limit.
  - Data completeness:
    - Detection limit fields may be blank if the value is above the detection limit; this requires careful treatment in GIS analyses (e.g., censoring or flagging).
  - Temporal and spatial mapping:
    - Collection_Date enables time-series visualization if locations have multiple samples.
    - Location enables spatial mapping of CR values across sites; ensure consistent geospatial labeling if integrating with GIS layers.

- How this supports GIS-based data products
  - Attribute mapping:
    - Use CR, Unc_CR, and Detection_Limit_CR attributes to symbolize and filter by radionuclide transfer levels, including uncertainty and detection-limit status.
  - Spatial-temporal analysis:
    - Combine Location and Collection_Date to create maps showing spatial distribution over time for each radionuclide.
  - Data quality labeling:
    - Flag records with below-detection values or missing uncertainty/detection-limit data to inform reliability and decision-making.
  - Data integration guidance:
    - Prior to GIS ingestion, validate unit consistency, resolve any sample_type vs. sample_description discrepancies, and standardize date formats to dd-mm-yyyy or ISO equivalents.