# Brief description of the data

- Scope: Morphometric trait data for 177 macro-moth species sampled by two Rothamsted Insect Survey light traps (Bentley Wood and Porton Down III) in 2017, across 33 dates.
- Purpose: Characterise body size and shape to support linking ground-level nocturnal insect morphology to bioscatterers observed on weather radar, as part of a NERC project.

## Data and sampling overview

- Taxa: Macro-moth species only (micro-moths excluded due to limited representation and digitisation).
- Sampling sites: Bentley Wood (Lat 51.0903, Lon -1.6401) and Porton Down III (Lat 51.1444, Lon -1.6826).
- Temporal scope: 33 sampling dates in 2017 (specific windows listed in the document).
- Specimens per species: Five specimens measured when NHM digitised images available; if significant sexual dimorphism was present, five per sex per species. For some species lacking NHM images, measurements from Skinner (2009) plates were used, with five images measured per species and per sex where applicable; in some cases fewer images were used when Skinner provided fewer.
- Aggregates excluded: Eupithecia spp, Oligia spp, and unidentified macro spp (not included in the dataset).

## Morphometric traits and measurement methods

- Six traits measured in millimetres:
  - Forewing length
  - Body length
  - Thorax length
  - Abdomen length
  - Thorax width
  - Abdomen width
- Measurement sources:
  - NHM digitised specimen images: Measurements taken with ImageJ; scale bar in each image calibrates measurements.
  - Skinner (2009) colour plates: Measurements taken with Duratool digital callipers (resolution 0.1 mm; accuracy ±0.2 mm).
- Sexual dimorphism:
  - When present, measurements include five specimens per sex per species.
  - For four species lacking sex information in NHM data, additional measurements from Skinner were used for five males and five females when available.
- Data quality control:
  - Specimens with missing/damaged parts or deformation excluded; replacement specimens chosen randomly.

## Data structure and content

- Primary dataset file: RIS2017_macromoth_morphometric_data.csv
- 12 columns:
  1) Family: taxonomic family of the specimen
  2) Binomial: current binomial name per RIS data
  3) Alternate_biniomial: alternate/classified binomial if reclassified
  4) Sex: M or F when known
  5) Source: 'NHM Database' or 'Skinner'
  6) Source_ID: permanent URL to NHM record or plate/specimen identifier from Skinner; 'NA' if missing
  7) Forewing_length: mm
  8) Body_length: mm
  9) Abdomen_length: mm
  10) Thorax_length: mm
  11) Thorax_width: mm
  12) Abdomen_width: mm

- Notes on data completeness:
  - 15 records lack a unique Source_ID due to human error (marked NA in Source_ID).

## Related methodological context

- Rationale for trait selection: Traits chosen to characterise overall size and shape and aligned with approaches used to estimate Lepidopteran body mass (García-Barros 2015).
- Calibration and measurement details:
  - NHM images include scale bars for precise ImageJ calibration.
  - Skinner-based measurements rely on calibrated digital calipers.

## Provenance and references

- Data provenance: Morphometric data collected from NHM digitised images and Skinner (2009) plates; linked to RIS light-trap records and 2017 sampling.
- References:
  - García-Barros E (2015) on multivariate body size indices
  - Natural History Museum data portal (collection specimens)
  - Schneider et al. (ImageJ)
  - Skinner (2009) Colour Identification Guide to the Moths of the British Isles

- Project context: Part of a NERC standard grant NE/S001298/1 investigating dual-polarization weather radar mapping of insect activity and linking morphometric diversity to radar bioscatter signals.