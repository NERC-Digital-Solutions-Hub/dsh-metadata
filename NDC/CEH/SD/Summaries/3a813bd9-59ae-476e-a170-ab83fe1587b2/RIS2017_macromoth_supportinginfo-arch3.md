RIS2017_macromoth_morphometric_data.csv

## Overview
- Dataset describing six morphometric traits for 177 macro-moth species from two Rothamsted Insect Survey (RIS) light traps: Bentley Wood and Porton Down III, collected on 33 dates in 2017.
- Primary data sources are digitised images from the Natural History Museum (NHM) and to-scale colour plates from Skinner (2009).
- Aims to characterise body size/shape and support linkage to bioscatterer signals on weather radar as part of a NERC project.

## Scope and species
- Focused on macro-moth species only; micro-moths underrepresented in RIS data and NHM digitisation, so excluded.
- Three aggregate categories from RIS data (Eupithecia spp., Oligia spp., unidentified macro spp.) are not included.
- Measurements include six traits, plus sex and taxonomic identifiers.

## Data sources and provenance
- Primary measurements from five randomly selected NHM digitised specimens per species; if significant sexual dimorphism existed, five specimens per sex were measured.
- When NHM digitised records were unavailable for a species, measurements were taken from Skinner (2009) colour plates.
- Measurements performed with ImageJ (ImageJ calibration via scale bars in NHM images) or with Duratool digital calipers (0.1 mm resolution, ±0.2 mm accuracy) for Skinner sources.
- All measurements are in millimetres.

## Collection methods and scope details
- RIS light traps: Bentley Wood (lat 51.0903, lon -1.6401) and Porton Down III (lat 51.1444, lon -1.6826).
- Dates in 2017: 11–14 May, 31 May; 1, 14–21, 25–27 June; 1–11, 17–18, 24–26 July.
- Data relate exclusively to macro-moth species; excluded micro-moths due to representation issues.

## Measurements and traits
- Six morphometric traits measured in millimetres:
  - Forewing_length
  - Body_length
  - Abdomen_length
  - Thorax_length
  - Thorax_width
  - Abdomen_width
- Trait definitions (e.g., Forewing_length from wing base to apex; Body_length from anterior patagium to posterior final abdominal segment; exclusions of head/hair fringes where possible).

## Metadata and data structure
- Single CSV file: RIS2017_macromoth_morphometric_data.csv with 12 columns:
  - Family
  - Binomial
  - Alternate_binomial
  - Sex (M/F, if known)
  - Source (NHM Database or Skinner)
  - Source_ID (per-record unique identifier or NA)
  - Forewing_length
  - Body_length
  - Abdomen_length
  - Thorax_length
  - Thorax_width
  - Abdomen_width
- Source_ID provides a permanent link to NHM records or plate/specimen numbers from Skinner (2009); some records lack a Source_ID due to human error (NA).
- Note: 15 records lack a unique identifier due to human error; otherwise identifiers enable traceability.

## Quality, limitations, and governance
- Quality control section marked NA; explicit metadata on data quality controls is not provided.
- Limitations and potential biases:
  - Some species had no NHM digitised images, necessitating use of Skinner plates, which may affect comparability.
  - Sexual dimorphism cases required sex-specific sampling; not always possible to obtain five per sex (in Skinner-derived data).
  - Some records missing Source_ID (traceability gaps) and some specimens with missing sex information.
- Metadata supports data provenance and reproducibility, aligning with monitoring framework needs for transparent data lineage and governance.

## Reuse and relevance for monitoring frameworks
- Provides standardized morphometric metrics for a substantial moth subset, enabling comparisons of body size/shape across species and temporal contexts.
- Supports integration with ecological modeling and radar-based biosignal studies by linking ground-truth morphometrics to large-scale atmospheric observations.
- Demonstrates a data governance approach: multi-source provenance, per-record identifiers, and clear measurement protocols, useful for designing monitoring data pipelines and metadata standards.

## References
- García-Barros E (2015). Multivariate indices as estimates of dry body weight for Lepidoptera.
- Natural History Museum (2014). Dataset: Collection specimens.
- Schneider, C., Rasband, W., Eliceiri, K. (2012). ImageJ.
- Skinner, B. (2009). Colour Identification Guide to the Moths of the British Isles.