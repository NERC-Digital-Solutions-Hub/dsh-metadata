# Derwent X-ray powder diffraction (XRD) Sediment Fingerprinting

## Overview
- A sediment fingerprinting dataset collected from the River Derwent Catchment, Yorkshire, UK.
- Aimed at understanding mineralogical composition of sediments via X-ray powder diffraction (XRD).
- Data are recorded as raw XRD outputs (2 theta values and counts) to support mineral phase identification.

## Collection, fieldwork, and instrumentation
- Sampling scope: grab samples from different soil types and instream sediment associated with river bars and banks.
- Field processing: samples dried, sieved, and powdered.
- Laboratory instrument: Bruker D8 XRD used for qualitative phase analysis.
- Quality control: instrument calibration noted; dataset provided as raw XRD output without phase-table processing.

## Data content, structure, and units
- Primary data in CSV format:
  - 2 theta (angle) values and corresponding counts for each sample.
  - Each record includes the sample site name and location data.
- Location information:
  - Numerous site entries with X and Y coordinates (some shown as 47953 0, 471158, 435964, etc.), indicating spatial referencing.
- Data structure notes:
  - File naming pattern appears as Derwent_XRD_SedimentFingerprinting_(n) for site groups.
  - An extensive list of site names and associated coordinates is present, though the text contains formatting irregularities and garbled lines that may affect parsing.
- Metadata scope:
  - Sample/site identifiers, site names, and coordinates are included, but accompanying metadata (dates, collectors, sampling protocols) are not clearly described in the provided text.

## Quality, provenance, and limitations
- Quality control:
  - XRD instrument calibration acknowledged; data are raw outputs not processed against phase tables.
- Provenance:
  - Data originate from field collection in the Derwent catchment and laboratory XRD analysis.
- Limitations and issues:
  - The text shows numerous formatting errors and incomplete lines, indicating potential data integrity challenges.
  - Some coordinate values and site entries appear garbled or truncated, necessitating data cleaning and validation before reuse.

## Metadata, governance, and sharing considerations for Data Stewards
- Metadata completeness:
  - Ensure a comprehensive data dictionary including: collection date, field methods, sample IDs, site names, precise coordinates, instrument settings (scan range, step size, counting time), and any preprocessing steps.
- Standardization and interoperability:
  - Harmonize field names (e.g., sample_id, site_name, X_coord, Y_coord, theta, counts), coordinate reference system, and units.
  - Validate and optionally convert coordinates to a consistent CRS; confirm numeric formats to prevent parsing errors.
- Data quality and processing:
  - Document any post-collection processing steps (even if none performed beyond calibration) and clearly distinguish raw vs. processed data.
  - Provide a data processing workflow or provenance to enable reproducibility of any mineral identification if phase tables are applied later.
- Access, licensing, and updates:
  - Define data access controls and sharing permissions; specify versioning and update cadence for the dataset.
  - Attach data license and attribution requirements for downstream users.
- Data stewardship actions:
  - Clean and validate the garbled entries, re-encode CSVs with consistent schema, and attach a metadata record (including method, QA/QC notes, and lineage).
  - Create or update a data portal entry to surface the dataset with usable search keys (e.g., site_name, coordinates, sampling method, instrument).
  - Provide guidance on using raw XRD outputs for mineralogical fingerprinting and what transformations would be needed for mineral identifications.

## Practical use and implications for users
- Suitable for researchers performing sediment fingerprinting and mineralogical source attribution using raw XRD data.
- Users should be aware that the current dataset contains raw 2 theta and counts without phase-table processing; additional processing will be required to infer specific minerals.
- Due to formatting irregularities, users should anticipate a need for data cleaning and validation prior to analysis.