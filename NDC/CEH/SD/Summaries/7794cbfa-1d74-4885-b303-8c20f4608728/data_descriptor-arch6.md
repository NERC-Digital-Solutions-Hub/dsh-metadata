# Photosynthetic pigments in water samples from 20 lochs in Scotland, May-June 2022

## Overview
- Dataset of photosynthetic pigment concentrations (µg L-1) from surface water samples of 20 Scottish lochs collected May–June 2022.
- Purpose: to develop a calibration model to resolve pigment concentrations from hyperspectral images taken with a mobile imager.
- Data custodianship: first author (corresponding author) responsible for correctness and reliability.
- Stored in pigment_results.csv; aimed at enabling data-driven insight and potential data products for exploration.

## Data content and structure
- Pigment concentrations: measured pigment levels in µg L-1.
- File and key columns (pigment_results.csv):
  - Column 1: sampling dates
  - Column 2: sampled lochs
  - Column 3: sample identification numbers
  - Column 4: replicate subsamples sampled in laboratory
  - Columns 5–6: sample volumes for each replicate measured by HPLC and spectrophotometry
- Measurements and formats support cross-linking with field metadata and lab results.
- Units: pigment concentrations in µg L-1; volumes and replicates recorded for traceability.

## Sampling details
- Method: grab sampling from the surface water layer.
- Storage and handling: samples stored at +4 °C and processed within 48 hours; water temperature recorded with a digital thermometer.
- Temporal and spatial reach: sampling dates and sites listed (Table 1) for 20 lochs, including Loch Leven, Airthrey Loch, Loch Lomond, and others.
- Location data: coordinates provided (WGS84, captured with iPhone) for each sampling point.
- Scope: extensive sampling across multiple lochs and littoral/ pelagic sites, with multiple sampling points per Loch.

## Laboratory protocols

### Chlorophyll and carotenoid assessment
- Sample preparation: phytoplankton collected on GF/F filters; filters labeled to match field data; flash-frozen in liquid nitrogen and stored at -80 °C.
- Shipment and storage: shipped on dry ice to DHI (Denmark); stored at -80 °C; analyzed within 4–6 months.
- Extraction: filters transferred to 6 mL of 95% acetone with an internal standard (vitamin E); vortexed, ice-sonicated, extracted at 4 °C for 20 h; filtered into HPLC vials (0.2 µm filter) with 5:2 buffer/extract ratio.
- Analysis: Shimadzu LC-10A HPLC with LC Solution; pigments analyzed include chlorophylls, carotenoids, and related pigments (e.g., chlorophyll a/b, various xanthophylls, and others listed).

### Phycocyanin assessment
- Sample handling: GF/F filters stored at -20 °C prior to shipping on dry ice; analyzed within 3–6 months.
- Extraction: buffers prepared from phosphate salts; extraction performed by grinding filters to pulp in buffer, with volume 9–18 mL final.
- Processing: samples frozen at -20 °C, thawed, then sonicated on ice; centrifuged at 3500 g for 10 min to clarify.
- Measurement: absorbance at 615, 652, and 750 nm using a Shimadzu UV-1800 spectrophotometer.
- Calculation: phycocyanin concentration Ce calculated using Ce = [(A615 − A750) − 0.474 × (A652 − A750)] / 5.32 (Bennett & Bogorad, 1973).

## Data provenance and quality
- Data provenance: derived from field sampling and standardized lab protocols; first author responsible for accuracy.
- Quality considerations: potential variability from patchy data across lochs and sites; multiple replicates and standardized extraction/instrumentation reduce some uncertainty.
- Formats and accessibility: data organized for self-serve analysis and potential integration with hyperspectral imaging outputs; clear labeling of samples, replicates, and volumes to support traceability.

## Use cases and potential data products
- Calibration and modelling: support development of calibration models linking hyperspectral images to pigment concentrations.
- Dashboards and reports: enable end users to explore pigment distributions across lochs, sites, and dates.
- Data integration: combine with other environmental datasets (temperature, location, sampling time) for broader ecological insights.
- Data sharing and re-use: structured metadata and explicit lab protocols facilitate reuse and reproducibility; potential early prototypes can be refined with user feedback.

## Access and documentation considerations
- Primary data file: pigment_results.csv containing sampling dates, lochs, sample IDs, replicates, and HPLC/spectrophotometry volumes.
- Laboratory methods and pigment scope are documented comprehensively at the lab protocol level within the dataset description, enabling reproducibility and methodological understanding.