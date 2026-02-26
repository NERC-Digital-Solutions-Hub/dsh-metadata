# NPMS_Locations_2016.csv NPMS_Samples_2016.csv NPMS_Sample_Attributes_2016.csv NPMS_Occurrences_2016.csv

## Overview
- A set of four related CSV datasets forming the NPMS 2016 data model: locations, samples, sample attributes, and occurrences.
- Designed to support linking spatial locations with sampled data, attributes, and observed taxa, enabling location-based biodiversity analysis over time.

## Data model and relationships
- Locations
  - NPMS_Locations_2016.csv
  - key fields: location_id (unique), location_type (describes location category)

- Samples
  - NPMS_Samples_2016.csv
  - key fields: sample_id (unique), survey_id (grouping code), date (format dd/mm/yyyy)
  - location_id (foreign key to NPMS_Locations_2016.csv) identifies where the sample was taken
  - entered_sref and entered_sref_system (spatial reference data provided for the sample)
  - created_on (timestamp) and created_by_id (foreign key to users) for provenance

- Sample Attributes
  - NPMS_Sample_Attributes_2016.csv
  - key fields: sample_attribute_id (unique), sample_id (foreign key to NPMS_Samples_2016.csv)
  - caption (description of the attribute) and text_value (attribute value)

- Occurrences
  - NPMS_Occurrences_2016.csv
  - key fields: occurrence_id (unique), sample_id (foreign key to NPMS_Samples_2016.csv)
  - taxonconversionkey (NBNT key for directly mappable taxa), taxon (taxon name sans authority)
  - domin (dominance score for the occurrence)
  - record_status (C = completed, V = verified, R = rejected) indicating data quality/approval state

## Key fields and data types (implications for data leaders)
- Unique identifiers: location_id, sample_id, sample_attribute_id, occurrence_id enable robust joins and lineage tracking.
- Foreign keys: location_id links samples to locations; sample_id links occurrences and attributes to their samples, enabling integrated analyses.
- Temporal data: date in NPMS_Samples_2016.csv supports time-series and trend analyses.
- Spatial data: entered_sref and entered_sref_system provide spatial references for mapping samples; requires standardization for cross-dataset use.
- Provenance: created_on and created_by_id capture data creation history for auditability.
- Taxonomy: taxonconversionkey and taxon allow both standardized mapping (NBNT) and human-readable taxonomy.
- Data quality indicator: record_status tracks lifecycle stage of each occurrence.

## Data governance and quality considerations
- Data provenance and traceability are supported by created_on/created_by_id and the record_status workflow.
- Spatial data quality depends on consistent spatial references (entered_sref/system); standardization is important for reliable mapping.
- Taxonomy mapping relies on taxonconversionkey where available; gaps may require mapping to NBNT or alternative taxonomies.
- Attribute data via NPMS_Sample_Attributes_2016.csv enables richer context but requires careful alignment with corresponding samples.

## How this supports data strategy for Data Leaders
- Enables a holistic view of biodiversity data across locations, samples, and observed taxa.
- Supports user-centered data products through linked data: location-centric analyses, sample-level context, and taxon-level insights.
- Facilitates data quality and governance practices by clearly delineating provenance, lifecycle status, and direct relationships between datasets.
- Encourages metadata discoverability and reuse by maintaining explicit keys and descriptive attributes.

## Practical next steps and actions
- Validate referential integrity across NPMS_Locations_2016.csv, NPMS_Samples_2016.csv, NPMS_Sample_Attributes_2016.csv, and NPMS_Occurrences_2016.csv.
- Standardize spatial references ( CRS and formats ) to ensure reliable geospatial analyses and interoperability.
- Assess completeness of key fields (dates, location_id, taxonconversionkey) and address any missing granularity issues.
- Establish metadata and data quality rules for record_status transitions (C, V, R) and implement an audit process.
- Build integrated data products (e.g., location-based dashboards) by joining samples to locations, attributes, and occurrences.
- Create a governance plan for taxonomic mapping and maintain an up-to-date NBNT mapping for taxonconversionkey.