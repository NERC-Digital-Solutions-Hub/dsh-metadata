# Associated file: hydroscape_glasgow_hg _cores_qc.csv

## Overview
- Describes the table headings for results of measurements of reference sediment LKSD2 and procedural blanks processed with core sediments measured by Cold Vapour Atomic Fluorescence Spectroscopy (CV-AFS).
- Focuses on Glasgow Hg Core Runs as the basis for reporting Hg concentrations in core sediments.

## Data fields and descriptions
- Glasgow Hg Core Runs, Description: Name of Hg cores run through the CV-AFS machine.
- Tube Code, Description: Tube code (e.g., LKSD2…).
- Standard Sediment Mass, Description: Mass of reference sediment weighed out (approximately 0.2 g).
- Hg ng/g, Description: Hg concentration in sediment expressed as nanograms per gram.
- Hg µg/g, Description: Hg concentration in sediment expressed as micrograms per gram.
- Measured blank (ng/ml), Description: Concentration of Hg measured in procedural blanks (ng/ml).
- LKSD2 Reference Sediment Value: 160 ± 19 ng/g; Partial extraction using HNO3.

## Data provenance and methods
- Measurements performed on core sediments using CV-AFS.
- LKSD2 reference sediment value established as 160 ± 19 ng/g, with partial extraction using HNO3 referenced.

## References and standards
- Lynch, J. (1990). Provisional Elemental Values for LKSD-1, LKSD-2, LKSD-3, LKSD-4 and STSD reference materials. Geostandards Newsletter, 14: 153-167. (DOI provided in reference text)

## GIS relevance and usage notes
- The dataset is tabular with Hg concentration measurements and related QA metrics, suitable for joining with spatial core data to produce map-based visualizations of Hg distribution across Glasgow cores.
- To use in GIS, data should be linked to core locations and metadata; units include Hg ng/g, Hg µg/g, and blank measurements (ng/ml).
- The presence of procedural blanks aids in QA assessment for spatially referenced Hg concentration maps.

## Quality considerations and caveats
- Standard sediment mass is small (~0.2 g), which may influence detection limits and comparability across cores.
- Measurements include blanks to account for contamination; ensure proper handling when integrating with GIS-derived analyses.
- LKSD2 reference sediment value is a fixed standard (160 ± 19 ng/g) and may be used for normalization or QA across samples.