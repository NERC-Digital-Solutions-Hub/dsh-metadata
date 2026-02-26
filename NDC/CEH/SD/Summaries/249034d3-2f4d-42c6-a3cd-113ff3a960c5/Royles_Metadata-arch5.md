# Physiology and stable isotope ecology of moss growth for modelling spatial and temporal climatic signals NERCDMP-555 - monthly field and dark adapted PAM fluorescence measurements

## Overview
- Describes a field and laboratory study on moss physiology and stable isotope ecology to model spatial and temporal climatic signals.
- Data package comprises monthly in-field chlorophyll fluorescence measurements, water content metrics, and related lab analyses across multiple peatland sites (2017–2018), with structured metadata designed for data governance and reuse.

## Field sites, sampling, and provenance
- Locations: Dersingham Bog (primary), Brandon Country Park, Wicken Fen (UK); habitats include bog heathland, heathland, and shaded woodland.
- Target species: multiple moss taxa (e.g., Aulacomnium palustre, Dicranum scoparium, Sphagnum spp., Pleurozium schreberi, Polytrichum spp., etc.); voucher specimens were collected and verified by bryologists.
- Access and permissions: permissions obtained from landowners/managers prior to field work.
- Sampling cadence: approximately monthly from April 2017 to September 2018.
- Sampling procedure: for each visit, three 2x2x2 cm samples per target species; samples sealed and transported for analysis.

## Data collection methods and measurements
- Field measurements: chlorophyll fluorescence at moss tips using Walz MINI-PAM II; three in-field measurements per sample, followed by a minimum 30-minute dark adaptation and three additional dark measurements.
- Calculated metrics (in the field and dark-adapted conditions): 
  - Fluorescence yield in dark and light (Φ) using standard formulas.
  - Non-photochemical quenching (NPQ).
  - Electron transport rate (ETR) using 0.84*PAR*0.5*Φ with μmol electrons m^-2 s^-1.
- Water-related metrics:
  - Relative water content (RWC) calculated from fresh and dry weights (drying at 70°C).
  - Cellulose extraction from dried moss for isotopic/chemical analyses (Soxhlet method).
  - Cryogenic vacuum distillation to extract fresh water for stable isotope work.
  - Field precipitation recorded at Ely, near-field-site center.
  - Enzymatic photo-spectrophotometric sucrose content analysis on sub-samples.
- Dataset scope: 14 monthly sequential CSV files from 01_Jul_2017 to 14_Oct_2018; 18 data columns per record with paired Unit/Description metadata.

## Dataset structure and content
- File format and organization: 14 monthly CSV files (01_Jul_2017 → 14_Oct_2018).
- Metadata design: each data dimension described with two-column structure (Unit and Description) alongside data fields.
- Column naming convention (example patterns):
  - Session, Date, Sample, Site, Species, Notes, and measurement variables (F, Fm, Dark_Y, Field_F, Field_Fm, Field_PAR, Field_Y, Field_ETR, Field_NP).
  - Derived metrics: Φ (fluorescence yield), Field_Y (PAR-corrected yield), Field_ETR (electron transport rate), Field_NP (non-photochemical factors).
- Example column pairs indicate the type of value (mean / SE) and its contextual description.
- Method references embedded in dataset lineage:
  - Cellulose extraction technique (Loader et al., 1997).
  - Metabolite analyses in plant tissues (Stitt et al., 1989).
  - Water extraction times for stable isotope analysis (West et al., 2006).

## Provenance, quality, and processing
- Field-to-lab workflow: triplicate measurements per sample, followed by dark-adapted replication; mean and standard error calculated.
- QA considerations: explicit documentation of measurement conditions (field vs. dark-adapted), equipment used, and calculation formulas to ensure reproducibility.
- Documentation and references: dataset includes method references to allow replication and validation of analytic procedures.

## Metadata and governance considerations
- Data ownership and governance signals:
  - Clear site-specific metadata (location, habitat, species, collection dates).
  - Voucher specimens and taxonomic verification included.
  - Permissions secured for all field sites prior to sampling.
- Sharing and dissemination readiness:
  - Plan to upload datasets to relevant portals and catalogues; dataset is prepared with rich metadata (units, descriptions, session, sample, and location data) to support discoverability and reuse.
- Data management alignment:
  - Separation of unit and description columns supports consistent metadata interpretation.
  - Provenance and method references embedded to facilitate reproducibility and audit trails.

## Practical notes for data stewards
- The dataset emphasizes data governance readiness through: structured metadata, transparent provenance, reproducible measurement and calculation methods, and explicit permissions and site information.
- Potential considerations for future work:
  - Align taxon names and site coordinates to standardized gazetteers to enhance interoperability.
  - Maintain versioning and data release notes as the dataset evolves with updates or corrections.
  - Ensure continued alignment with data portals’ metadata standards (e.g., variable-specific controlled vocabularies, units, and measurement contexts).

## References
- Loader, N. J., et al. (1997). An improved technique for the batch processing of small wholewood samples to α-cellulose.
- Stitt, M., et al. (1989). Metabolite levels in specific cells and subcellular compartments of plant leaves.
- West, A. G., et al. (2006). Water extraction times for plant and soil materials used in stable isotope analysis.