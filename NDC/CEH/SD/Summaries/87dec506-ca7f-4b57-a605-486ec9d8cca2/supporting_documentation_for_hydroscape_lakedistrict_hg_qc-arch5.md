# Associated file: hydroscape_lakedistrict_hg _cores_qc.csv

## Overview
- Describes table headings and results for measurements of reference sediment LKSD2 and procedural blanks, processed alongside core sediments using Cold Vapour Atomic Fluorescence Spectroscopy (CV-AFS) after reduction with SnCl2.
- Mercury concentrations were measured at UCL Geography. Samples were prepared by digesting freeze-dried cores in aqua regia at 100°C for 2 hours in rigorously acid-leached 50 mL tubes.
- LKSD2 reference sediment has a certified Hg value of 160 ± 19 ng g^-1, with the method referenced to partial extraction elements using concentrated HNO3 and HCl.
- QC approach included running LKSD2 and blanks as samples, plus laboratory standards and blanks every five samples to monitor instrument stability.

## Data structure and variables
- Table columns:
  - Lake_District_Hg_Core_Runs
  - Tube_Code
  - Reference_Sediment_mass_g
  - Hg_ng_g
  - Hg_µg_g
  - Measured_blank_ng_ml
  - Description
- Field meanings:
  - Tube_Code: identifier for each run (e.g., LKSD2…)
  - Reference_Sediment_mass_g: mass of reference sediment weighed (~0.2 g)
  - Hg_ng_g: mercury concentration in sediment (ng/g)
  - Hg_µg_g: mercury concentration in sediment (µg/g)
  - Measured_blank_ng_ml: mercury concentration measured in procedural blanks (ng/mL)
  - Description: name of Hg cores run through the CV-AFS machine

## Methodology and QA
- Procedure:
  - Core sediments are measured by CV-AFS after reduction with SnCl2.
  - Samples and LKSD2 reference sediment digested in aqua regia at 100°C for 2 hours.
- Quality control:
  - Laboratory standard solutions and QC blanks measured every five samples to monitor instrument stability.
  - Procedural blanks tracked alongside sample measurements.

## Reference materials and provenance
- LKSD2 reference sediment used with a certified Hg value: 160 ± 19 ng g^-1.
- Reference material described by Lynch (1990): Provisional Elemental Values for LKSD-1, LKSD-2, LKSD-3, LKSD-4, STSD-1, STSD-2, STSD-3, STSD-4. Geostandards Newsletter, 14: 153-167. DOI provided.

## Data governance and provenance considerations
- Data are linked to a specific reference material (LKSD2) and include detailed metadata on sample mass, measurement units, and blanks to support traceability and reproducibility.
- Documentation should ensure consistent unit usage (ng/g, µg/g, ng/mL) and clear linkage between core runs and their corresponding tube codes.
- The dataset is suitable for reuse in similar sediment-mercury assessments, with explicit QA steps and reference material provenance.

## Practical notes for data stewards
- Ensure all entries maintain the same column order and units for interoperability with other CV-AFS Hg datasets.
- Preserve the relationship between Tube_Code, Reference_Sediment_mass_g, Hg_ng_g, Hg_µg_g, and Measured_blank_ng_ml for traceability.
- Include the Lynch 1990 reference in metadata to support future validation and cross-dataset comparisons.