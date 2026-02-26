# PAHs concentrations and DOC partitioning data across sites and seasons

## Overview
- Dataset captures PAH concentrations and related variables across five sites and four seasons.
- Measured variables include total dissolved PAHs, freely dissolved PAHs, DOC-bound PAHs, and DOC concentration.
- A derived metric, log K_DOC, represents the water-DOC partition coefficient and is calculated from c_total, c_free, and c_DOC (exact formula referenced but not fully rendered in the text).

## Data structure and variables
- Site codes and names
  - 1 = Marshaw Wyre
  - 2 = Abbeystead
  - 3 = Dolphinholm
  - 4 = Six Arches
  - 5 = Garstang
- Season codes and dates
  - 1 = 19 August 2010
  - 2 = 6 December 2010
  - 3 = 6 March 2011
  - 4 = 6 June 2011
- Variables (units)
  - total dissolved PAHs [ng/L]
  - freely dissolved PAHs [ng/L]
  - DOC-bound PAHs [ng/L]
  - DOC [mg/L]
  - log K_DOC (dimensionless)
- Derived metric
  - log K_DOC; calculated from c_total (total dissolved PAHs), c_free (freely dissolved PAHs), and c_DOC (DOC concentration) per the provided (but not fully displayed) equation.

## Data governance and quality considerations
- Metadata to capture:
  - Site code and name, season code and date
  - Variable definitions, units, and measurement methods
  - QA/QC procedures and data processing steps
  - Data source provenance and versioning
- Quality checks:
  - Ensure unit consistency and valid ranges for all concentrations
  - Cross-check related fields (e.g., c_DOC vs PAH fractions)
- Provenance and lineage:
  - Track any transformations (cleaning, recalculations of log K_DOC)
  - Maintain version history and update records

## Access, storage, and sharing
- Storage and discovery:
  - Upload to relevant data portals/catalogues
  - Attach data dictionary, method documentation, and provenance information
- Documentation and licensing:
  - Provide a clear data dictionary, methodology, and usage license
  - Include citation details (e.g., DOI) for traceability

## Challenges and considerations for Data Stewards
- Incomplete understanding of user needs for this dataset
- Timely receipt of data from creators
- Standardization across multiple systems/formats and handling legacy databases
- Interoperability and scalability when integrating with larger data holdings

## Recommendations for action
- Develop and publish a comprehensive data dictionary with definitions, units, and valid ranges
- Establish consistent naming conventions and controlled vocabularies for sites, seasons, and variables
- Document measurement methods, QA/QC procedures, and any data transformations
- Implement automated data validation and quality checks
- Maintain data lineage and version history; plan for updates and catalog exports
- Define access controls, licensing, and ensure discoverability in data catalogs