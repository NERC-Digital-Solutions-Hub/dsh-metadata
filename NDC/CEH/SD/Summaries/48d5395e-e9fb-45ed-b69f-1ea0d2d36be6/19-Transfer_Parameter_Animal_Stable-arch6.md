# Supporting documentation for 19-Transfer_Parameter_Animal_Stable.csv

## Purpose and scope
- Documents the metadata and meaning of columns for the 19-Transfer_Parameter_Animal_Stable.csv dataset.
- Focuses on sample identification, description, collection details, and concentration ratio (CR) values for multiple stable elements in milk, with associated uncertainty and detection information.

## Dataset structure

- Sample metadata
  - Sample_Code: unique sample identifier.
  - Sample_Type: general description of the sample group.
  - Location: name of the collection site.
  - Sample_Description: part of the organism analysed (e.g., specific tissue/organism portion).
  - Collection_Date: date of sample collection (format: dd-mm-yyyy).

- Per-element CR measurements (for each element listed)
  - [Element]_CR: CR value for stable [Element].
  - Unc_[Element]_CR: uncertainty of the CR value.
  - Detection_Limit_[Element]_CR: detection limit for the CR value.
  - Notes: indicates when a field is blank (implies below detection limit in many cases).
  - Units: described per element (e.g., Unitless or kg dry matter per L for milk, or per L for milk).

- Elements covered (examples)
  - Cs_CR, Sr_CR, K_CR, Na_CR, Ca_CR, Mg_CR, P_CR, Pb_CR, U_CR, Th_CR
  - Corresponding Unc_*, Detection_Limit_*, and Notes fields for each element.

## Data quality and interpretation

- Blank fields typically indicate values below the detection limit.
- Unc_* fields provide measurement uncertainty for the CR values.
- Detection_Limit_* fields specify the sensitivity of the measurement for each CR value.
- Units may vary by element and are specified alongside each parameter (often related to milk matrix context).

## How to use

- Use the metadata to correctly interpret CR values, uncertainties, and detection status when analyzing or merging with other datasets.
- Ensure consistent unit handling and account for values reported as below detection via the Notes field.
- Helpful for quality assurance, data cleaning, and constructing data products (dashboards, reports) that allow end-users to self-serve.

## Limitations and notes

- Some descriptions appear garbled or truncated in places, but the overall structure clearly defines CR values, uncertainties, detection limits, and notes for each element.
- Data may be patchy with varying formats across fields; treat missing/blank entries as below detection unless otherwise indicated.