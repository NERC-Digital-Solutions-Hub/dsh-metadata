# hydroscape_lakedistrict_hg _cores_qc.csv

- Overview
  - Describes the table headings for results of mercury measurements in reference sediment LKSD2 and procedural blanks, processed with core sediments measured by Cold Vapour Atomic Fluorescence Spectroscopy (CV-AFS) after reduction with SnCl2.
  - Mercury concentrations were measured at UCL Geography using freeze-dried core samples digested in aqua regia (100°C for 2 hours) in acid-leached tubes.
  - Uses LKSD2 reference sediment with a certified Hg value (160 ± 19 ng/g) as a standard.

- Data collection and preparation
  - Samples: LKSD2 reference sediment and aqua regia sample blanks run alongside core sediments.
  - Digestion: aqua regia digestion at 100°C for 2 hours in 50 mL tubes.
  - Measurement: CV-AFS for Hg, with routine quality control.

- Data structure and fields
  - Lake_District_Hg_Core_Runs: Name of each Hg core run through the CV-AFS instrument.
  - Tube_Code: Identifier for each run (e.g., LKSD2…).
  - Reference_Sediment_mass_g: Mass of reference sediment weighed out (approximately 0.2 g).
  - Hg_ng_g: Mercury concentration in sediment expressed in ng/g.
  - Hg_µg_g: Mercury concentration in sediment expressed in µg/g.
  - Measured_blank_ng_ml: Mercury concentration measured in the procedural blank (ng/mL).
  - Description: Additional notes, including the specific Hg cores run.

- Standards and quality control
  - Standard reference material LKSD2 used as a reference sediment; certified Hg value and provenance cited.
  - Laboratory standard solutions and QC blanks measured every five samples to monitor instrument stability and data quality.

- Provenance and references
  - LKSD2 reference values and methodology reference Lynch (1990), Geostandards Newsletter, for contextual calibration and standardization.

- Implications for data strategy and governance (Data Leaders perspective)
  - Data quality and reliability: explicit QC measures (standards and blanks) enhance trust and reproducibility across laboratories.
  - Metadata clarity: well-defined column headers and units support discoverability and downstream reuse.
  - Provenance: linkage to LKSD2 as a certified reference material provides traceability and comparability with other studies.
  - Data utilization: suitable for assessing Hg levels in lake sediments and for cross-study comparisons, provided consistent digestion and measurement protocols are maintained.
  - Potential improvements: include explicit measurement dates, instrument IDs, and method version to strengthen data lineage and reproducibility.