# Photosynthetic pigments in water samples from 20 lochs in Scotland, May-June 2022

## Overview
- Datasets of photosynthetic pigment concentrations (µg L-1) from surface water samples across 20 Scottish lochs collected May–June 2022.
- Purpose: develop a calibration model to resolve pigment concentrations from hyperspectral images taken with a mobile imager.
- Responsibility for accuracy and reliability stated: the first author (corresponding author).

## Data content and structure
- Primary dataset file: pigment_results.csv.
- Key columns in pigment_results.csv:
  - Sampling dates
  - Loch names
  - Sample identification numbers
  - Replicate subsamples (laboratory)
  - Sample volumes for each replicate measured by HPLC and spectrophotometry
- Units: pigment concentrations in micrograms per liter (µg L-1).
- Metadata context: dataset linked to laboratory analyses and sampling events to support traceability.

## Sampling context
- Method: grab sampling from the surface water (pelagial or littoral zones) of lochs listed in Table 1.
- Sample handling: stored at +4 °C and processed within 48 hours; water temperature recorded with a digital handheld thermometer.
- Geographic and temporal coverage: multiple sampling dates (e.g., 04.05.2022 to 09.06.2022) with site-specific coordinates provided in Table 1 (WGS84 coordinates obtained via iPhone).

## Laboratory analyses and data generation
- Chlorophyll and carotenoids (HPLC):
  - Phytoplankton collected on GF/F filters, each with a unique ID linked to field data.
  - Filters flash-frozen in liquid nitrogen and stored at -80 °C; shipped on dry ice to DHI (Denmark) and analyzed within 4–6 months.
  - Analysis: acetone extraction with an internal standard (vitamin E); HPLC system Shimadzu LC-10A; pigments includes a broad list (Chl a, b, c1/c2, pheophytins, various carotenoids, etc.).
- Phycocyanin:
  - Filters stored at -20 °C, shipped and stored at -20 °C; analyzed within 3–6 months.
  - Extraction: prepared buffers (phosphate-based) with careful pH control (6.7–6.8); samples ground, extracted, centrifuged; filtration as needed to prevent clogging.
  - Quantification: absorbance at 615 nm, 652 nm, and 750 nm; concentration Ce calculated via Ce = [(A615−A750) − 0.474×(A652−A750)] / 5.32 (Bennett & Bogorad, 1973).

## Provenance, identifiers, and documentation
- Field-to-lab traceability: sampling date, loch, site, coordinates, and replicate identifiers are recorded to align with pigment measurements.
- Filters and samples assigned unique IDs to match field data with laboratory results.

## Data quality and governance considerations
- Data integrity claim: the first author is responsible for correctness and reliability of the data.
- Comprehensive methodological detail supports reproducibility and auditability (sampling protocol, storage conditions, extraction and analysis procedures, instrument specifics, pigment list).
- Potential data stewardship needs:
  - Clear versioning and metadata to track any future updates or corrections.
  - Documentation of any data exclusions or corrections made during processing.
  - Consistent units and naming conventions across related datasets (e.g., pigment names, abbreviations).

## Data access, sharing, and preservation
- Primary data file identified (pigment_results.csv); context for storage and sharing is described within the document.
- Reuse considerations include the need to follow the described laboratory methods and to reference the original instruments and protocols.
- Data stewardship notes:
  - Ensure long-term preservation of raw and processed results.
  - Consider publishing metadata alongside data to facilitate discovery (sampling dates, locations, IDs, replication, units, and methods).

## Documentation and reproducibility
- Detailed laboratory protocols provided for both chlorophyll/carotenoids (HPLC) and phycocyanin assessments.
- Detailed sampling table (dates, lochs, sites, and coordinates) enables spatial and temporal analyses.
- References: Bennett, A., and L. Bogorad. 1973 (used for phycocyanin calculation).

## Challenges and considerations for data stewards
- Incomplete or variable user needs may affect metadata richness and discoverability; ensure schema supports key fields (dates, locations, IDs, units, methods).
- Handling large, multi-site datasets with many formats and instruments; maintain interoperability between CSV data and lab-derived results.
- Timely data transfer and consistent metadata capture during field collection and lab processing.
- Embargoes or update policies are not specified; define sharing and update workflows if the dataset is to be integrated into larger data portals.

## References
- Bennett, A., and L. Bogorad. 1973. Complementary chromatic adaptation in a filamentous blue-green alga. J. Cell Biol. 58(2): 419-435.