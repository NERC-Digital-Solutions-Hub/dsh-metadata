# CEH Land Cover plus: Fertilisers 2010-2015 (England)

## Overview
- Dataset of predicted average annual application rates for three inorganic fertilisers (nitrogen N, phosphorus P, potassium K) in England from 2010–2015 at 1 km x 1 km resolution.
- Includes uncertainty estimates and is produced to support environmental impact assessments and sustainable agricultural practices.
- Created under the ASSIST project to enable exploration of fertiliser impacts on environment, with potential uses for modelling nutrient fate, greenhouse gas emissions, eutrophication indicators, crop growth links, and policy development.

## Data content and structure
- Two-band raster files (TIFF), 1 km resolution, covering England for each fertiliser:
  - Band 1: Predicted average annual application rate (kg/km^2)
  - Band 2: Uncertainty associated with the predicted rate (percent)
- File naming per fertiliser:
  - fertiliser_n_prediction_uncertainty
  - fertiliser_p_prediction_uncertainty
  - fertiliser_k_prediction_uncertainty
- Data access: Environmental Information Data Centre (EIDC); citation required when used (CEH Land Cover plus: Fertilisers 2010-2015 (England); DOI provided).

## Data collection and provenance
- Raw data from Defra’s British Survey of Fertiliser Practice (BSFP), 2010–2015.
- Each year: voluntary participation by farmers (~3,696 georeferenced farms on average), with geolocation, crop typology (66 classes), soil type, field counts, and unique IDs.
- Zero-value records excluded from analysis due to ambiguity (missing data vs. actual zero application); remaining records assumed spatially predictable where fertiliser was applied.
- Crop typology linked to Lands Cover plus: Crops map (England, averaged 2015–2017) to support aggregation and area-based scaling.

## Analytical methods
- Interpolation approach: Ordinary kriging (OK) chosen for performance, agricultural data familiarity, and ability to produce a variance surface for uncertainty estimation.
- Interpolation implemented in ArcGIS with default parameters aside from a variable search radius (12 input points) to accommodate varying record density by crop.
- Crop-area scaling: Interpolated per-crop fertiliser rates multiplied by crop-typology area (hectares) per 1 km cell to yield total application per crop; then sums across crops to obtain total fertiliser application per 1 km cell (kg/km^2).
- Land Cover plus: Crops data used to provide crop areas per cell; Crops map averaged 2015–2017.

## Uncertainty assessment and quality control
- Kriging variance surfaces produced per crop and fertiliser; aggregated to a single variance surface per fertiliser.
- Uncertainty calculation per cell:
  - U = (2 * sqrt(V)) / P * 100
  - U represents percentage uncertainty; based on doubling the standard deviation to align with 95.5% confidence limits.
- Provides an uncertainty surface (% per cell) alongside the prediction.
- Quality checks performed by overlaying variance with crop-area summary; practical approach for overall uncertainty given methodology.

## Data governance and stewardship considerations
- Provenance and attribution: Dataset produced by CEH with Defra BSFP data; funded under NERC/ASSIST; acknowledgements included.
- Documentation and metadata: Includes data source, interpolation method (OK), crop linkage approach, spatial resolution, coverage, and uncertainty methodology; file formats and naming conventions documented.
- Access and reuse: Clear citation requirement and DOIs; enables traceability for governance, data discovery, and downstream reuse.
- Limitations and caveats for stewarding data:
  - Zeros removed; potential biases where data are missing or represent true zero application.
  - Assumptions of spatial predictability and interpolation-based uncertainty; results are model-derived and should be interpreted with the uncertainty surface.
  - Dependency on ancillary crop-typology data (Land Cover plus: Crops) and its temporal averaging (2015–2017) for 2010–2015 application mapping.
- Maintenance implications: Snapshot for 2010–2015 with potential need for future updates; ensure versioning, clear update cycles, and consistency in crop-typology alignment for new years.