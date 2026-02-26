# Data collected on Mt Etna during the field transplant in 2017

## Overview
- Field transplant study conducted on Mt Etna in 2017.
- Five genotypes sampled per species (two Senecio species) with four cuttings per genotype per transplant elevation; four leaves measured per plant.
- Measurements repeated on a second day to account for weather and measurement timing.
- Light response measured after 30 minutes of dark adaptation using an IMAGING-PAM M-series chlorophyll fluorometer.
- Primary analysis focuses on PI(total), the total photosynthetic capacity.

## Experimental design
- Species: AE = S. aethnensis; CH = S. chrysanthemifolius.
- Genotype: ID from individuals grown in the glasshouse (source for cuttings).
- TGSite: Elevation of transplant sites.
- TGBlock: Replicate experimental blocks in the field.
- Grid: Grid location of plants within each block; genotype randomized across grid locations.
- Day: Day of measurement.

## Measurements and data structure
- Instrument: IMAGING-PAM M-series chlorophyll fluorometer.
- Output: Columns 7–22 contain fluorometer data; only PI(total) used for analysis (representing total photosynthetic capacity).
- Data identifiers: Species, Genotype, TGSite, TGBlock, Grid, Day, and PI(total).

## Data governance and sharing considerations (Data Stewards)
- Metadata and standards:
  - Clear coding for species (AE/CH) and genotype IDs.
  - Documentation of TGSite, TGBlock, Grid, and Day.
  - Specification of PI(total) as the key dependent variable.
- Data quality and processing:
  - Ensure accuracy and consistency of measurements, especially PI(total).
  - Record any transformations or quality checks performed during cleaning.
- Provenance and context:
  - Capture measurement conditions: date, time, day, 30-minute dark adaptation, instrument version.
  - Link to field trial design (block structure, grid randomization).
- Data availability and lifecycle:
  - Upload datasets to appropriate portals/catalogues; establish update and versioning protocols.
  - Consider disclosure or embargo needs if data are sensitive or embargoed.
- Documentation and reuse:
  - Maintain accompanying metadata detailing collection methods, units, and any limitations.
  - Document data processing steps to support reproducibility.
  
## Potential challenges and considerations for reuse
- Aligning data from multiple systems or formats if integrated with other datasets.
- Ensuring timely data delivery and complete metadata for all variables.
- Managing large datasets and ensuring efficient transfer and storage.
- Handling legacy or outdated data sources if integrated with other studies.