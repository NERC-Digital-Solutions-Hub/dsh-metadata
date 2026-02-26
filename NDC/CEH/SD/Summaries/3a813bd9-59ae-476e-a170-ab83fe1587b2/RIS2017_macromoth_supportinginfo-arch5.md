# RIS2017_macromoth_morphometric_data.csv

## Overview for Data Stewards
- A morphometric trait dataset for macro-moths from two RIS light traps (Bentley Wood and Porton Down III) in 2017, covering 177 species across 33 dates.
- Six body metrics collected in millimetres to characterize size and shape: forewing length, body length, thorax length, abdomen length, thorax width, abdomen width.
- Designed to support linking ground-level morphometrics with radar-derived insect signals as part of a NERC project.

## Data scope and purpose
- Primary focus: Macro-moth species; micro-moths were underrepresented and largely excluded.
- Purpose: Provide a usable, standardized morphometric dataset to enable comparability and downstream analyses (e.g., body mass estimations and ecological inferences).
- Data intended to support broader ecological and remote-sensing research, not just taxonomic work.

## Data sources and provenance
- Measurements primarily derived from images of 177 macro-moth species digitised by the Natural History Museum (NHM).
- For species without NHM digitised records, measurements taken from Skinner (2009) Colour Identification Guide to Moths of the British Isles.
- Data collected and curated by the project authors; dataset links to NHM records or Skinner plates as sources.

## Collection methods and instrumentation
- Image-based measurements:
  - NHM images calibrated using scale bars; measurements performed with ImageJ.
- Alternative sources (Skinner 2009) measured with Duratool digital callipers (0.1 mm resolution; ±0.2 mm accuracy).
- Five specimens measured per species; if significant sexual dimorphism, five per sex per species where possible.

## Traits, units, and data structure
- Six morphometric traits (all in millimetres):
  - Forewing_length
  - Body_length
  - Abdomen_length
  - Thorax_length
  - Thorax_width
  - Abdomen_width
- Additional fields:
  - Family
  - Binomial
  - Alternate_binomial
  - Sex (M/F when known)
  - Source (NHM Database or Skinner)
  - Source_ID (per NHM URL or Skinner plate/specimen; NA where missing)
- Dataset file: RIS2017_macromoth_morphometric_data.csv with 12 columns.

## Taxonomic scope and data completeness
- Excludes three aggregate groups originally present in RIS data: Eupithecia species, Oligia species, and unidentified macro spp.
- Four species had incomplete sex information in NHM records; supplementary measurements from Skinner were used to obtain five males and five females when possible.
- 15 records lack a unique Source_ID due to human error (marked as NA).
- Specimens with missing/damaged parts or deformations excluded from measurement.

## Data quality and governance considerations
- No dedicated quality control (QC) section; metadata notes indicate selective handling of missing data and reliance on scale calibration.
- Provenance traces to NHM (2014 dataset) and Skinner (2009); potential synonymy addressed via Alternate_binomial field.
- Clear documentation of measurement definitions and calibration procedures to support reproducibility.
- Licensing and data-use permissions are not specified; data stewards should verify rights for NHM-derived imagery and Skinner plates before sharing or reuse.

## Access, reuse, and maintenance implications
- Source_ID ensures traceability to original images/plates; however, some records lack identifiers (NA).
- Dataset supports reproducible morphometric analyses, but ongoing updates may be needed if NHM or Skinner records are revised.
- Suitability for integration with other datasets (e.g., radar bioscatterers) depends on consistent taxonomic naming and consistent measurement protocols.

## References and related materials
- García-Barros E (2015). Multivariate indices as estimates of dry body weight for Lepidoptera.
- Natural History Museum (2014). Dataset: Collection specimens.
- Schneider, C., Rasband, W., Eliceiri, K. (2012). ImageJ: image analysis software.
- Skinner, B. (2009). Colour Identification Guide to the Moths of the British Isles.