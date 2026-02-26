# Macroinvertebrates of the Thames catchment

## Overview
- Dataset describing macroinvertebrate communities in wadeable rivers within the Thames catchment, UK.
- Collected across three seasons in 2009–2010, with supporting habitat data.
- Aimed at enabling robust data governance, reuse, and discovery by others.

## Datasets included
- Macroinvertebrate community data
  - Macroinvertebrates of the Thames catchment - taxon data.csv
- Environmental variables
  - Macroinvertebrates of the Thames catchment - environmental variables.csv
- Supporting information
  - Macroinvertebrates of the Thames catchment - supporting information.csv

## Data collection and structure
- Sampling design
  - 18 sites in the Thames catchment; Autumn 2009, Spring 2010, Autumn 2010.
  - Not all sites sampled on every occasion; site-specific sampling details in supporting information.
- Methods
  - Kick net with 1 mm mesh; RIvPACS field protocol.
  - Field measurements: depth, width, substrate cover, macrophyte cover.
  - Samples preserved in 4% formaldehyde; later rinsed through 500 μm sieve; macroinvertebrates identified to lowest feasible taxonomic level (usually species).
- Taxonomic and coding standards
  - Taxon codes and names aligned with Davies, C. & Edwards, F.K. (2011) Code list for recording freshwater macroinvertebrates in the British Isles.
- Derived data
  - Map/environmental variables derived using Intelligent River Network (IRN) v17; method described by Dawson et al. (2002).

## Data standards, metadata, and references
- Site and sample identifiers
  - Samples defined by unique combination of site code and sample date.
  - Site code mappings provided in supporting information.
- Data validation and quality control
  - Data entry validated by crosschecking printed outputs with laboratory sheets.
- Documentation and accessibility
  - Supporting information documents site details and environmental context.
  - Taxon dataset includes: site code, sample date, season, taxon code, taxon name, life stage, abundance.
  - Environmental dataset includes site code, sample date, and various habitat and substrate variables.
  - Standardized taxon naming and unique taxon IDs enable interoperability with other datasets.

## Provenance and contributors
- Roles
  - Sample collection: Gearóid Webb, Peter Scarlett, Roger Baker, François Edwards
  - Laboratory analysis: Gearóid Webb, François Edwards, Helen Vincent
  - Supporting information: Peter Scarlett, Gearóid Webb, François Edwards
  - Planning and management: François Edwards, Michael Bowes
- Version history
  - Version 1.0 (28/06/2016): initial creation
  - Version 1.1 (07/07/2016): minor revisions
- Data stewardship context
  - Clear authorship and versioning support traceability and governance.

## Data quality, limitations, and considerations
- Temporal and spatial coverage
  - Multi-season data, but incomplete site coverage across seasons; this affects longitudinal analyses.
- Data completeness
  - Not all sites sampled at all times; users should account for missing samples in analyses.
- System and format diversity
  - Data spans multiple files with linked identifiers; careful cross-referencing required for integration.
- Usability notes
  - Supporting information provides critical context for site characteristics and sampling specifics aiding data reuse.

## Governance, sharing, and reuse
- Data standards and reuse
  - Adheres to established taxon coding and metadata practices, enabling reuse with other RIVPACS-related datasets.
- Updates and maintenance
  - Versioned releases indicate ongoing maintenance; users should refer to latest version for current metadata and fixes.
- Access considerations
  - Metadata and data dictionaries are provided through supporting information to facilitate discovery and interoperability.