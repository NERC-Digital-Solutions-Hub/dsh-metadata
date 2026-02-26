# Data file name: FADOE_pollution.csv

## Overview
- Field experiment dataset measuring air pollutants and meteorological context around eight Free-Air Diesel and Ozone Enrichment (FADOE) rings.
- Pollutants tracked: nitrogen oxide species (NO, NO2, NOx) and ozone (O3) concentrations at ring centers.
- Treatments include diesel exhaust (D), ozone (O3), diesel exhaust plus ozone (D+O3), and a natural air control (CON).
- Data collected at high temporal resolution (every 60 seconds) with accompanying wind data from multiple around-field positions.
- Designed to support data governance, reuse, and discovery by data stewards, with potential for metadata-rich sharing.

## Data Content and Structure
- Pollutants and columns (example mappings):
  - NOx: Column S
  - NO: Column Q
  - NO2: Column R
  - O3: Column P
- Experimental treatments: Column E (values D, O3, D+O3, CON)
- Temporal identifiers: Year (Column A), Date (Column B), Time (Column C)
- Wind data from four ring-adjacent positions:
  - ws1/wd1 (Columns F/K)
  - ws2/wd2 (Columns G/L)
  - ws3/wd3 (Columns H/M)
  - ws4/wd4 (Columns I/N)
- Sampling cadence: 60-second intervals
- Instrumentation:
  - O3 measurements: Thermo Scientific Model 49i
  - NOx measurements: Thermo Scientific Model 42C
  - Automated switching system for sequential monitoring
- Platform and scope:
  - Centre of eight 8 m-diameter rings
  - Field of wheat environment
  - Measurements context includes whether data represent ring-centre concentrations and surrounding wind conditions

## Experimental Design and Collection/Instrumentation (Governance-Relevant)
- Experimental bays: four distinct pollution treatments across the eight rings, enabling comparison of emissions and atmosphere interactions.
- Data collection approach emphasizes standardized instrumentation and timing to support comparability and reusability.
- Metadata considerations implied by design (e.g., ring position, treatment mapping, instrument models) support traceability and data quality checks.

## Temporal and Spatial Coverage
- Years covered: 2018 and 2019
- Location coordinates (representative for each year):
  - 2018: latitude 51.482853, longitude -0.897749
  - 2019: latitude 51.482374, longitude -0.895855
- Spatial scope centered on ring locations around a field of wheat; captures ring-centered pollutant values and surrounding wind fields.

## Location and Site Details
- Field setting: near wheat crop, with wind measurements taken from four compass-oriented radii around the FADOE ring installation.
- Precise center-point measurements for pollutants per ring, with wind data captured at multiple positions to contextualize dispersion.

## Data Quality, Provenance, and Standards (Stewardship)
- Quality assurance and data cleaning steps anticipated before sharing:
  - QA, cleaning, and transformation of datasets prior to dissemination
  - Documentation of work performed on datasets to enable reproducibility
- Standards and interoperability considerations:
  - Clear variable definitions, units (pollutants in ppb), and instrument metadata to facilitate reuse across systems
  - Potential need for consistent metadata schemas to integrate with portals and catalogues

## Accessibility, Sharing, and Preservation
- Data sharing intent: upload to relevant portals and catalogue data holdings for discoverability.
- Documentation should accompany the dataset to support reuse, including methodology, instrument details, and treatment definitions.
- Update and maintenance considerations:
  - Mechanisms to reflect dataset updates or corrections
  - Versioning and data provenance to track changes over time

## Challenges and Recommendations for Data Stewards
- Common challenges to anticipate:
  - Incomplete understanding of user needs and priorities
  - Timely receipt and integration of data from multiple sources
  - Ensuring metadata completeness and consistency across formats
  - Interoperability across different systems and potential large data volumes
  - Handling legacy or bespoke formatting from field experiments
- Stewardship recommendations:
  - Maintain comprehensive metadata: variable definitions, units, column mappings, treatment codes, instrument details, site coordinates, time zone, sampling cadence
  - Establish data quality checks and QA procedures in the metadata
  - Document data processing steps (cleaning, transformations) and preserve a dataset lineage
  - Implement data versioning, updates, and embargo policies if applicable
  - Provide clear data access terms, licensing, and contact points
  - Ensure reproducibility by including a data dictionary and, if possible, sample scripts or workflows

## Summary Relevance for Data Stewards
- The FADOE_pollution.csv dataset embodies a well-defined, high-resolution field data product requiring strong metadata, provenance, and governance practices to maximize discoverability, interoperability, and reuse across researchers and platforms.