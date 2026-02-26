# RIS2017_macromoth_morphometric_data.csv

## Overview
- A dataset of six morphometric traits for 177 macro-moth species from two Rothamsted Insect Survey (RIS) light traps: Bentley Wood and Porton Down III, collected across 33 dates in 2017.
- Measurements derived from images: NHM digitised specimens and, where needed, Skinner (2009) colour plates.
- Aims to characterize body size/shape to support broader ecological analyses, including linking ground-level insect morphology to bioscatterers in weather radar.

## Spatial and Temporal Coverage
- Locations:
  - Bentley Wood (Lat 51.0903, Long -1.6401)
  - Porton Down III (Lat 51.1444, Long -1.6826)
- Timeframe: 33 dates in 2017 (11–14 and 31 May; 1, 14–21, 25–27 June; 1–11, 17–18, 24–26 July)

## Scope and Sampling
- Taxonomic scope: macro-moth species only; micro-moths excluded due to limited representation and NHM digitisation.
- Species included: 177 named macro-moth species.
- Exclusions: three aggregates from RIS counts (Eupithecia spp., Oligia spp., unidentified macro spp.) are not included.
- Sampling approach:
  - NHM-derived measurements: five randomly selected specimens per species; if significant sexual dimorphism, five per sex.
  - NHM limitations: for some species with no NHM-digitised images, measurements from Skinner (2009) plates (five images per species; adjusted for available sexes).
  - For four dimorphic species lacking sex information in NHM records, Skinner data provided five male and five female measurements (or as available).

## Data Collection and Measurement Methods
- Traits measured (all in millimetres):
  - Forewing_length, Body_length, Abdomen_length, Thorax_length, Thorax_width, Abdomen_width
- Measurement procedures:
  - NHM: ImageJ used to measure from digitised images with scale bars for calibration.
  - Skinner (2009): Duratool digital calipers (0.1 mm resolution; ±0.2 mm accuracy) used on to-scale plates.
- Data sources:
  - NHM digitised specimen images
  - Skinner (2009) colour plates
- Handling of specimens:
  - Excluded if missing/damaged or deformed; otherwise measured.
  - Sex recorded where known (M/F).

## Data Structure and Content
- Single CSV: RIS2017_macromoth_morphometric_data.csv
- Columns (12 total):
  1) Family
  2) Binomial
  3) Alternate_biniomial
  4) Sex
  5) Source (NHM Database or Skinner)
  6) Source_ID (permanent URL for NHM or plate/specimen ID for Skinner; NA if missing)
  7) Forewing_length
  8) Body_length
  9) Abdomen_length
  10) Thorax_length
  11) Thorax_width
  12) Abdomen_width

## Provenance and References
- Primary data sources:
  - Natural History Museum (NHM) digitised specimen images
  - Skinner, B. 2009. Colour Identification Guide to Moths of the British Isles, 3rd ed.
- Related references:
  - García-Barros (2015) on body size estimation in Lepidoptera
  - National/ institutional data portals and ImageJ methodology (Schneider et al., 2012)

## Usage Considerations for GIS
- Spatial mapping:
  - Point data can be visualized at trap locations; coordinates included for Bentley Wood and Porton Down III.
- Temporal context:
  - Data restricted to 2017 collection dates; not a longitudinal multi-year dataset.
- Data integration:
  - Can be joined with taxonomic or morphological datasets (by Binomial, Family) and with Source_ID for NHM records.
  - Potential to link morphometric traits to bioscatterer signals in radar-based studies (context of NERC grant NE/S001298/1).
- caveats:
  - Exclusion of micro-moths and three RIS aggregates may affect completeness for some analyses.
  - Some records have missing Source_IDs (NA) due to human error.
  - Variation in measurement source (NHM vs Skinner) and sex coverage for certain species.
  - No dedicated quality control section; users should assess measurement consistency and potential biases when combining NHM and Skinner-derived data.