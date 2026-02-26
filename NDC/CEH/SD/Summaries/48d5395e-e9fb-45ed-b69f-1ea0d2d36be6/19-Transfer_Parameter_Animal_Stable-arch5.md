# Supporting documentation for 19-Transfer_Parameter_Animal_Stable.csv

- Purpose and scope
  - Provides a data dictionary for the dataset 19-Transfer_Parameter_Animal_Stable.csv.
  - Defines each field’s meaning, units, and notes, focusing on CR values for stable elements (Cs, Sr, K, Na, Ca, Mg, P, Pb, U, Th) and related metadata.
  - Describes how sample information is recorded, including identifiers, description, collection date, and location.

- Core dataset fields (general metadata)
  - Sample_Code: unique sample identifier.
  - Sample_Type: general description of the sample (e.g., foodstuff group).
  - Location: name of the collection location.
  - Sample_Description: part of the organism analysed (e.g., where whole organism was divided and analysed separately).
  - Collection_Date: date of sample collection; format is dd-mm-yyyy.

- Parameter-specific fields (CR values and quality metadata)
  - For each element (Cs, Sr, K, Na, Ca, Mg, P, Pb, U, Th), the dataset includes:
    - <X>_CR: CR value for stable X (the measured or reported value).
    - Unc_<X>_CR: Uncertainty of the CR value for stable X.
    - Detection_Limit_<X>_CR: Detection limit of the CR value for stable X.
  - Units and notes (per parameter) indicate:
    - Typical units can be unitless or expressed as kg dry matter per L for milk, with some fields indicating per L for milk or unitless, depending on the parameter.
    - Notes state that, where a field is blank, the corresponding result is below the detection limit.
  - The fields are structured consistently across parameters to support quality assurance and comparison.

- Data quality and metadata considerations
  - Completeness: each parameter should have corresponding CR, Unc, and Detection_Limit values; verify any missing fields.
  - Consistency of units: standardize to a uniform unit convention across all parameters (current documentation shows variations such as unitless, kg dry matter per L for milk, or per L for milk); ensure explicit unit specification in a single, consistent schema.
  - Handling below-detection-limit values: document and apply the “blank means below detection limit” rule consistently across all parameter fields.
  - Temporal and spatial metadata: ensure Collection_Date formats are uniform (dd-mm-yyyy) and Location and Sample_Type descriptions are stable and searchable.
  - Data ingestion and sharing: align with portal/catalog requirements and document any data processing performed (quality assurance, cleaning, transformation, updates).

- Practical guidance for data stewardship
  - Validate uniqueness and accuracy of Sample_Code; cross-check with related datasets if applicable.
  - Maintain explicit metadata for each parameter’s CR, Unc, and Detection_Limit to support reuse and interpretation.
  - Normalize units across the dataset and clearly annotate any non-standard or milk-specific units.
  - Capture and document any below-detection-limit cases as blank per the documented convention, and ensure the detection limits are clearly stored.
  - Record any data provenance or processing steps in accompanying documentation to support traceability.

- Potential considerations and recommendations
  - If user needs evolve, consider expanding metadata to include instrument method, detection technique, and calibration details that relate to the CR measurements.
  - Review and resolve any inconsistent or garbled field descriptions (e.g., mixed phrasing around units) to ensure unambiguous interpretation.
  - Maintain a data quality checklist aligned with the dataset’s parameter structure to tractably monitor completeness and accuracy across updates.