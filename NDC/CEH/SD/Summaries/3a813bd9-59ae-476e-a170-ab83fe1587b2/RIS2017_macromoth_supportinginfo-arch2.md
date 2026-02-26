RIS2017_macromoth_morphometric_data.csv

## Overview
- A dataset of six morphometric measurements for 177 macro-moth species from two Rothamsted Insect Survey (RIS) light traps (Bentley Wood and Porton Down III) across 33 dates in 2017.
- Measurements derived from images (NHM digitised specimens) and source plates in Skinner (2009), taken to enable characterisation of body size/shape and potential links to nocturnal bioscatter signals on weather radar.

## Taxonomic scope and exclusions
- Focus is strictly on macro-moth species; micro-moth data were underrepresented and excluded.
- Three aggregates from RIS counts (Eupithecia spp., Oligia spp., and unidentified macro spp.) are not included.
- Analyses concentrated on macro-moth species only.

## Sampling sites and dates
- Sites: Bentley Wood (Lat 51.0903, Long -1.6401) and Porton Down III (Lat 51.1444, Long -1.6826).
- Dates: 11–14 & 31 May; 1, 14–21 & 25–27 June; 1–11, 17–18, 24–26 July 2017.

## Data collection and specimen handling
- Morphometric traits measured from six measurements per specimen; five specimens per species were measured when NHM digitised images were available; if significant sexual dimorphism was present, five specimens per sex were measured.
- Where NHM digitised images were unavailable for a species, measurements were taken from Skinner (2009) colour plates, using five images per species (five per sex where possible).
- For four species with dimorphism but unknown sex information in NHM records, additional measurements were taken from Skinner for five male and five female specimens (or as available).

## Morphometric traits and measurement methods
- Six traits measured in millimetres:
  - Forewing_length
  - Body_length
  - Abdomen_length
  - Thorax_length
  - Thorax_width
  - Abdomen_width
- Measurements follow specific anatomical references (e.g., forewing base to apex; thorax/abdomen landmarks) and were taken using ImageJ or Duratool calipers when applicable.
- Scale calibration: NHM images include scale bars; Skinner measurements used Duratool callipers with resolution 0.1 mm and ±0.2 mm accuracy.

## Data sources and identifiers
- Source: NHM Database (digitised NHM images) or Skinner (2009) plates.
- Source_ID: Permanent URL for NHM records or plate/specimen numbers for Skinner records; ‘NA’ where an identifier is missing due to human error.
- Sex: M or F when known; may be missing for some records.

## Data structure and content
- Single CSV: RIS2017_macromoth_morphometric_data.csv with 12 columns:
  - Family
  - Binomial
  - Alternate_biniomial
  - Sex
  - Source
  - Source_ID
  - Forewing_length
  - Body_length
  - Abdomen_length
  - Thorax_length
  - Thorax_width
  - Abdomen_width

## Quality control and limitations
- Quality control (QA/QC) details are not provided (NA).
- Some records have missing Source_ID (identified as NA).
- Data limited to macro-moths; does not cover micro-moths.

## Context and potential environmental monitoring uses
- Supports standardised, comparable morphometric data across species for environmental health assessments and biodiversity studies.
- Can be integrated with radar-based bioscatterer analyses to explore links between ground-level morphometrics and nocturnal biological signals.
- Aligns with aims to use established data sources, ensure traceability via Source_IDs, and provide outputs suitable for maps and charts in environmental monitoring.

## References
- García-Barros E (2015). Multivariate indices as estimates of dry body weight for comparative study of body size in Lepidoptera. Nota Lepidopterologica.
- Natural History Museum (2014). Dataset: Collection specimens. NHM Data Portal.
- Schneider, C., Rasband, W. & Eliceiri, K. (2012). NIH Image to ImageJ: 25 years of image analysis. Nat Methods.
- Skinner, B. (2009). Colour Identification Guide to the Moths of the British Isles.