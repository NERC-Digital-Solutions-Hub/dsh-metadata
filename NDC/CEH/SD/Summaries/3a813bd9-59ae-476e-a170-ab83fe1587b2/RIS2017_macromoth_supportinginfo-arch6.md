# Brief description of the data

- A morphometric trait dataset for macro-moth species collected from two Rothamsted Insect Survey (RIS) light traps (Bentley Wood and Porton Down III) in 2017 across 33 dates.
- Measurements focus on six body morphometrics (in millimetres): forewing length, body length, thorax length, abdomen length, thorax width, and abdomen width.
- Data sources include digitised NHM specimen images and to-scale Skinner (2009) colour plates, with five specimens measured per species (five per sex when sexual dimorphism is present).
- Aims linked to mapping ground-level morphometric diversity to bioscatterer signals on weather radar as part of a NERC grant.

## Scope and organisms

- Analyzed group: macro-moth species only; micro-moth data were underrepresented and excluded.
- Final dataset excludes three original aggregates from RIS counts: Eupithecia spp., Oligia spp., and 'unidentified macro spp.'
- Sex information recorded when known; five specimens per sex were used for species with documented sexual dimorphism.

## Data sources and collection

- Primary data: 177 macro-moth species from RIS light traps (Bentley Wood and Porton Down III) in 2017.
- Image sources:
  - Natural History Museum (NHM) digitised specimens for measurement.
  - Skinner (2009) Colour Identification Guide plates when NHM records were unavailable.
- Selection: five specimens per species for NHM images; five per sex when dimorphism was significant; otherwise five images per species (and per sex if applicable) from Skinner.
- Quality notes: some species with dimorphism had incomplete sex data or missing unique identifiers; 15 records lack a Source_ID due to human error.

## Measurements and units

- Six morphometric traits measured in millimetres:
  - Forewing_length
  - Body_length
  - Abdomen_length
  - Thorax_length
  - Thorax_width
  - Abdomen_width
- Definitions provided for each measurement (base-to-apex, anterior/posterior margins, excluding certain features where possible).
- Measurements calibrated using scale bars in NHM images and measured with ImageJ (NHM) or Duratool digital calipers (Skinner plates).

## Data structure

- Single CSV file: RIS2017_macromoth_morphometric_data.csv
- 12 columns in order:
  1) Family
  2) Binomial
  3) Alternate_biniomial
  4) Sex (M or F)
  5) Source (NHM Database or Skinner)
  6) Source_ID (per NHM record URL or Skinner plate/specimen reference; NA if missing)
  7) Forewing_length
  8) Body_length
  9) Abdomen_length
  10) Thorax_length
  11) Thorax_width
  12) Abdomen_width

## Collection methods and instruments

- Instrumentation: ImageJ software for NHM measurements; Duratool digital calipers (resolution 0.1 mm, accuracy ±0.2 mm) for Skinner-derived measurements.
- Calibration: all NHM images include a scale bar enabling precise calibration in ImageJ.

## Location and timing

- Trap locations: Bentley Wood (Lat 51.0903, Long -1.6401) and Porton Down III (Lat 51.1444, Long -1.6826).
- Dates: 33 sampling dates across 2017 (11–14 & 31 May; 1, 14–21 & 25–27 June; 1–11, 17–18, 24–26 July).

## Data quality and limitations

- Quality control information is not provided (NA).
- Some records have missing Source_ID values due to human error.
- Macro-moth focus may limit applicability to micro-moth analyses.

## Context and purpose

- Data collected as part of a broader project to map standing insect activity and biomass using dual-polarization weather radar and to relate ground-level morphometric diversity to radar bioscatter signals.

## File-specific notes for data use

- The dataset provides traceability via Source_ID links to NHM records or Skinner plates, enabling source verification and potential remeasurement.
- Contains both sex-annotated and unannotated records; users should account for missing sex data where relevant analyses require sex-specific comparisons.

## References

- García-Barros E (2015) Multivariate indices as estimates of dry body weight for comparative study of body size in Lepidoptera. Nota Lepidopterologica.
- Natural History Museum (2014). Dataset: Collection specimens. NHM Data Portal.
- Schneider, C., Rasband, W. & Eliceiri, K. (2012). NIH Image to ImageJ: 25 years of image analysis. Nat Methods.
- Skinner, B. (2009). Colour Identification Guide to the Moths of the British Isles.