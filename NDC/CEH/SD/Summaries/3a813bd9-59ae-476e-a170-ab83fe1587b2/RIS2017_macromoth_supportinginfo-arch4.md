# RIS2017_macromoth_morphometric_data.csv

## Overview
- Dataset describing six morphometric traits for macro-moth species from two Rothamsted Insect Survey (RIS) light traps in 2017.
- Includes 177 macro-moth species across 33 sampling dates (May–July 2017) at Bentley Wood and Porton Down III.
- Aims to support linking ground-level morphometric diversity to nocturnal bioscatterers on weather radar as part of a NERC project.

## What the data contains
- Six measured morphometric traits (in millimetres): forewing length, body length, thorax length, thorax width, abdomen length, abdomen width.
- Sex of specimens when known (M or F).
- Source of measurements: NHM digitised images or Skinner (2009) colour plates.
- Unique identifiers for data traceability (Source_ID), linking to NHM records or Skinner plates; some records lack Source_ID due to human error.
- Data restricted to macro-moths; micro-moths are excluded due to limited representation and digitisation.

## How data were collected
- Primary data: 177 macro-moth species from RIS light traps; five specimens measured per species when NHM images exist, with five per sex if sexual dimorphism is significant.
- Alternate data: When NHM images were unavailable, measurements from Skinner (2009) colour plates were used, with up to five images per species; where sexual dimorphism was present, measurements for both sexes were taken if possible.
- Handling of missing/damaged specimens: specimens with missing parts or deformation excluded; additional measurements taken from Skinner for certain dimorphic species lacking sex-specific NHM data.
- Instrumentation and calibration: ImageJ software used for measurement; digital callipers used for Skinner data; scale bars in NHM images allowed calibration.

## Data structure and fields
- Single CSV file: RIS2017_macromoth_morphometric_data.csv
- 12 columns:
  1) Family
  2) Binomial
  3) Alternate_biniomial
  4) Sex
  5) Source (NHM Database or Skinner)
  6) Source_ID (URL or plate/specimen number; or NA)
  7) Forewing_length
  8) Body_length
  9) Abdomen_length
  10) Thorax_length
  11) Thorax_width
  12) Abdomen_width

## Measurements and units
- All traits measured in millimetres.
- Forewing_length measured from wing base to apex; body_length from patagium to posterior abdominal segment; thorax_length from patagium to metathorax; abdomen_length from metathorax to final abdominal segment; thorax_width and abdomen_width measured laterally at respective widest/midpoints.
- Specific exclusions: measurements exclude hair fringes and genitals where possible; some measurements could not be taken due to image limitations.

## Provenance and sources
- NHM (Natural History Museum) digitised specimen images underpin most measurements.
- Skinner (2009) Colour Identification Guide to Moths of the British Isles used when NHM data unavailable.
- Image calibration relied on scale bars present in NHM images; Duratool digital calipers used for Skinner-derived measurements.

## Data quality, gaps, and notes
- Quality control section listed as NA.
- Some records lack Source_ID due to human error.
- For four dimorphic species with unknown sex in NHM data, Skinner data provided sex-specific measurements.
- Three aggregates from RIS counts (Eupithecia spp., Oligia spp., unidentified macro spp.) are not included in this dataset.

## Context and purpose
- Part of a project to map standing insect activity and biomass using dual-polarization weather radar.
- Aims to relate ground-level morphometric diversity to radar-detected nocturnal bioscatterers, contributing to broader data-system understanding and cross-domain use.

## References
- García-Barros E (2015). Multivariate indices as estimates of dry body weight for comparative study of body size in Lepidoptera.
- Natural History Museum (2014). Dataset: Collection specimens.
- Schneider, C., Rasband, W., & Eliceiri, K. (2012). NIH Image to ImageJ: 25 years of image analysis.
- Skinner, B. (2009). Colour Identification Guide to the Moths of the British Isles.