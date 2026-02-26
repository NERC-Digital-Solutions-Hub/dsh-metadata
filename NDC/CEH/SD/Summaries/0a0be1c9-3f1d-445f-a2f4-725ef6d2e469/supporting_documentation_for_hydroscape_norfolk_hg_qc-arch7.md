# Supporting Documentation for QC file uploaded to EIDC

## Overview
- Describes the table headings and results for quality control (QC) measurements of reference sediment LKSD2 and procedural blanks processed alongside core sediments measured by Cold Vapour Atomic Fluorescence Spectroscopy (CV-AFS).
- Associated data file: hydroscape_norfolk_hg_cores_qc.csv.

## Data structure and fields
- Glasow Hg Core Runs, Description: Name of Hg cores run through the CV-AFS machine.
- Tube Code, Description: Tube code (e.g., LKSD2…) linked to each measurement.
- Standard Sediment mass, Description: Mass of reference sediment weighed out (approximately 0.2 g).
- Hg ng/g, Description: Mercury concentration in sediment expressed as ng/g.
- Hg µg/g, Description: Mercury concentration in sediment expressed as µg/g.
- Measured blank (ng/ml), Description: Mercury concentration measured in the procedural blank (ng/ml).

## Measurements and QA metrics
- Reference Sediment: LKSD2 reference sediment measurements used for QC.
- Measured blank values: Used to assess contamination and method cleanliness.
- Units to note: Hg concentrations in ng/g (and µg/g); blanks in ng/ml.

## Reference standards and values
- LKSD2 Reference Sediment Value: 160 ± 19 ng/g.
- Partial Extraction method: Using HNO3.

## Methodology
- Core sediments are measured by CV-AFS; QC uses LKSD2 reference sediment and procedural blanks to validate accuracy and detect contamination.
- Procedural blanks provide baseline for background Hg and help ensure reliability of core sediment measurements.

## References
- Lynch, J. (1990). Provisional Elemental Values for Eight New Geochemical Lake Sediment and Stream Sediment Reference Materials LKSD-1 to LKSD-4 and STSD-1 to STSD-4. Geostandards Newsletter, 14: 153-167. DOI: https://doi.org/10.1111/j.1751-908X.1990.tb00070.x

## GIS relevance and data quality considerations
- This QC documentation supports data reliability for map-based Hg concentration visualizations by validating core sediment measurements against a known reference standard.
- Useful for:
  - Linking Hg concentration data (ng/g) to core location attributes to map spatial distribution.
  - Assessing data quality before layering Hg values on GIS maps (use of LKSD2 and blanks to flag questionable samples).
  - Ensuring consistent data standards and transformation processes when integrating multi-resolution data from core sediments and reference materials.
- Key considerations for GIS workflows:
  - Include QC fields (reference value, blank values) along with core measurements to enable quality filters.
  - Maintain provenance by retaining the CV-AFS methodology and reference standards in metadata.