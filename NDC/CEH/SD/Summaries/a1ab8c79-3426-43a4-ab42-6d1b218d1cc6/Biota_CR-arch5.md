# Supporting documentation for Biota_CR.csv

## Overview
- Defines how concentration ratios (CR) are calculated and stored for Biota_CR.csv: CR = biota stable element concentration / soil stable element concentration.
- Documents data elements, their meanings, units, and how non-detects are represented.
- Uses RAPs (Reference Animals and Plants) per ICRP to classify samples.
- Aims to support reproducibility, data quality, and discoverability for datasets with many elements and samples.

## Key fields and definitions
- Sample_Code
  - Purpose: Unique sample identifier.
  - Notes: Units not applicable.
- RAP
  - Purpose: Sample type classification based on ICRP RAPs.
- Sample_Description
  - Purpose: Additional explanation of the sample where applicable.
- Collection_Date
  - Units: dd month yyyy.
- Soil_used_for_CR_Calculations
  - Purpose: Identifies soil sample(s) used to estimate the CR.
- Element-specific CR and detection-limit fields
  - For each element (e.g., I-127, Li, Be, B, Na, Mg, Al, P, S, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U):
    - [Element]CR (unitless)
      - Purpose: Concentration ratio for the element on a fresh mass basis.
      - Notes: For animals, this is the whole-organism CR. A blank indicates the concentration was below the detection limit (see corresponding Detection_Limit field).
    - Detection_Limit_[Element]
      - Purpose: Estimated likely maximum CR value based on the detection limit quoted for the biota concentration.
      - Units: Unitless.
      - Notes: If blank, the CR value from the previous column is used.
    - Special case patterns
      - Some elements (e.g., Mg, Al, P, S, Cs, Ba, Tl, Pb, U) have fields indicating “value estimated using biota stable element concentration for which the detection limit was quoted” and a corresponding “Detection_Limit_” field that is often presented in the previous column.
      - Cs, Ba, Tl fields show multi-part naming (e.g., Cs, 1; Cs, 2; Cs, 3) to accommodate different presentation aspects.
  - Notes column (per row)
    - Purpose: Notes on analyses or how samples were used to estimate the whole-organism CR, provided where required.

## Data quality, metadata, and interpretation
- Detection limits
  - When CR is blank, the concentration ratio was below the detection limit.
  - Detection_Limit fields provide a likely maximum CR value corresponding to the quoted detection limit for the biota concentration.
- Whole-organism interpretation
  - For animals, the CR values reflect the whole-organism concentration ratio.
- Data provenance
  - Collection dates, sample descriptions, and the soil samples used for CR calculations support traceability.
- RAP-based categorization
  - RAPs align samples with recognized ICRP reference organisms, supporting standardized interpretation across datasets.

## Data governance and stewardship considerations
- Metadata completeness
  - Ensure Sample_Code, RAP, Collection_Date, Soil_used_for_CR_Calculations, and all element-specific CR and Detection_Limit fields are populated where applicable.
- Standardization and interoperability
  - Maintain consistent units (unitless CR) and uniform date formats (dd month yyyy).
  - Preserve the interpretation that CR values can be “below detection limit” with corresponding Detection_Limit fields.
- Data updating and disclosure
  - Document any embargoes, data sharing restrictions, or system-specific limitations that affect updating CR values or metadata.
- Data provenance and lineage
  - Capture how soil concentrations were derived, how RAP classifications were assigned, and how CR values were calculated from raw measurements.
- Usability for discovery and reuse
  - Provide clear definitions for each field, including how to treat non-detects, to facilitate sharing, cataloging, and downstream analyses by data users.

## Practical implications for Data Stewards
- Treat Biota_CR.csv as a richly described, multi-element CR dataset with extensive non-detect handling.
- Enforce metadata completeness for sample identifiers, RAPs, collection dates, and soil sources to enable reliable data discovery and linking.
- Ensure transparent handling of detection limits and whole-organism interpretation to support reproducible analyses.
- Prepare for potential complexity in multi-field element entries (e.g., Cs, Ba, Tl) by documenting the intended presentation and calculations for each sub-field.
- Align dataset publication with governance policies for large, multi-system datasets to facilitate timely sharing while respecting any embargoes or proprietary constraints.