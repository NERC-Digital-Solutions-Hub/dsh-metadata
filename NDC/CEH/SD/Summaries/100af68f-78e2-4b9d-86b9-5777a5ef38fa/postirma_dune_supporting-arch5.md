# Plant cover in foredunes following hurricane Irma: large scale surveys

## Overview
- Large-scale field dataset on plant cover by species in foredunes along the Florida-Georgia coast (Cape Canaveral, FL to Tybee Island, GA) following Hurricane Irma (Oct 2017).
- Sampling across up to 28 sites with three transects per site, measured on three occasions: Feb 2018, Jul 2018, and Jan 2019.
- Staff: John Griffin, Matthew Joyce.

## Data Collection and Design
- Experimental setup: Sites chosen in Feb 2018 based on accessibility, permitting, and a mix of coastal development levels; sites undergoing active restoration re-surveyed.
- Observations: Plant percentage cover by species, average plant cover, and species richness.
- Field protocol: At each site, transects perpendicular to the shoreline were placed at ~50 m intervals. Along each transect, 1 m intervals from dune crest to upper beach, percent cover of each species estimated visually within 0.5 x 0.5 m quadrats. Total cover is the sum of all species' covers; species richness is the count of species along a transect.
- Re-surveys: Transects 1-3 re-located to similar areas within ~10 m across time.
- Logistical notes: Not all sites revisited in every sampling round for practical reasons.

## Data Structure and Metadata
- Key variables: 
  - Sampling_date (month/year), Site, Lat, Long, Transect, Development (A: low, B: moderate, C: high).
  - Number of species recorded, Total.cover (sum of species covers), Uniola_paniculata mean cover, and 67 additional species-specific columns.
- Observations per site: Multiple transects per site; observations collected across three time points.
- File formats: Excel and CSV.
- Data checks: Distributions screened for unusual values; cross-checked against field notebooks; NA indicates not applicable; 0 indicates absence of a species or zero species richness.
- Data description fields: Header and Description included for dataset-level context.

## Quality Assurance and Provenance
- Procedures documented for data checking and validation against field notes.
- Clear handling rules for missing and zero values to support accurate analysis and reproducibility.
- Re-survey methodology ensures comparability of data across time points.

## Access, Format and Sharing
- Formats provided in Excel and CSV to support broad accessibility and reuse.
- Dataset includes explicit field-level descriptions to aid discoverability and reuse in data portals.

## Governance and Stewardship Considerations
- Development categorization (A, B, C) facilitates context on site conditions and potential data interpretation challenges.
- Multi-timepoint, multi-site design requires careful versioning and provenance tracking to maintain data integrity across updates.
- The large number of species-specific columns (67 additional species) may pose interoperability challenges with some systems; consider standardizing metadata and aligning with broader data standards where feasible.
- Potential needs for metadata extension (license, data use terms, repository location) to support long-term discoverability and responsible data sharing.
- Ongoing data stewardship tasks include ensuring timely sharing of updates, maintaining consistent naming conventions, and documenting any methodological changes over time.