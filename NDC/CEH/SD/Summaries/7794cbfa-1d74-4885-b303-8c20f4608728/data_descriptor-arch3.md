# Photosynthetic pigments in water samples from 20 lochs in Scotland, May-June 2022

## Overview
- Dataset of photosynthetic pigment concentrations (µg L-1) from water samples of 20 Scottish lochs collected May–June 2022.
- Purpose: develop a calibration model to estimate pigment concentrations from hyperspectral images taken with a mobile imager.
- First author (corresponding author) responsible for data correctness and reliability.

## Data file and structure
- Data stored in pigment_results.csv.
- Core columns:
  - Sampling dates (column 1)
  - Loch names (column 2)
  - Sample identification numbers (column 3)
  - Replicate subsamples (column 4)
  - Sample volumes for each replicate HPLC and spectrophotometry assessment (columns 5 and 6)

## Sampling methodology
- Grab sampling from surface water layers at listed lochs/sites (as per Table 1 in the document).
- Samples stored at +4 °C and processed in the laboratory within 48 hours.
- Water temperature measured with a digital handheld thermometer.
- Sampling dates/sites include multiple lochs (e.g., Loch Leven, Airthrey Loch, Loch Lomond, etc.) with various littoral, pelagial, harbour, and other sites.

## Laboratory analysis

### Chlorophyll and carotenoids (HPLC)
- Phytoplankton collected on GF/F filters (Whatman or Fisherbrand MF300); filters uniquely identified to match field data.
- Filters flash-frozen in liquid nitrogen, stored at -80 °C, then shipped on dry ice to DHI (Denmark) and stored at -80 °C.
- Analysis: acetone extraction with an internal standard (vitamin E), 4 °C extraction for 20 h, filtration, and HPLC analysis (Shimadzu LC-10A with LC Solution).
- Pigments analyzed: a broad suite including chlorophylls a, b, c1, c2; chlorophyllide a; pheophorbide a; various carotenoids (e.g., peridinin, fucoxanthin, neoxanthin, zeaxanthin, lutein, β-carotene, α-carotene, etc.); plus related pigments such as diadinoxanthin, diatoxanthin, canthaxanthin, antheraxanthin, violaxanthin, astaxanthin, alloxanthin, myxoxanthophyll, etc.

### Phycocyanin
- Filters GF/F stored at -20 °C prior to shipping on dry ice to the analysis lab; stored at -20 °C there and analyzed within 3–6 months.
- Extraction: fresh buffer prepared daily (composition includes NaH2PO4·2H2O and Na2HPO4·7H2O to achieve pH 6.7–6.8); samples ground to pulp, extraction volume 9–18 mL after rinsing.
- Processing: freeze-thaw cycles, sonication on ice, centrifugation (3500 g, 10 min); supernatant filtered (0.2 µm) and injected into spectrophotometer.
- Measurement: absorbance at 615 nm, 652 nm, and 750 nm (against buffer) using Shimadzu UV-1800.
- Calculation: phycocyanin concentration Ce = [(A615 − A750) − 0.474 × (A652 − A750)] / 5.32 (Bennett and Bogorad, 1973).

## Data provenance and handling
- Filters and samples tracked with unique identifiers to align field data with laboratory results.
- Data and protocols indicate careful chain-of-custody: cold storage, dry-ice shipping, and documented extraction/instrumentation procedures.
- The record explicitly notes the first author’s responsibility for correctness and reliability of the data.

## Relevance for monitoring frameworks
- Provides a comprehensive set of pigment measurements across multiple lochs, enabling calibration of remote sensing (hyperspectral imaging) against ground-truth pigment concentrations.
- Data structure supports traceability: dates, locations, sample IDs, replicates, and processing volumes are explicitly recorded.
- Detailed laboratory protocols support reproducibility and comparability, including strict temperature controls, internal standards, and standardized extraction and analysis workflows.
- List of measured pigments enables assessment of phytoplankton community structure (various photosynthetic pigments and carotenoids) alongside total pigment concentrations.
- Metadata transparency (sampling sites, coordinates, dates, replication) facilitates governance, quality assurance, and data sharing within monitoring programs.