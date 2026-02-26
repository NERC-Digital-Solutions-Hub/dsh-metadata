# NPMS_Locations_2015.csv

## Overview
- Defines a simple, multi-file data schema for NPMS 2015 focusing on locations, samples, sample attributes, and occurrences.
- Four CSV files are described, each with a small set of fields designed to capture core dataset elements and relationships.

## Data Model and Key Fields
- NPMS_Locations_2015.csv
  - location_id: unique location identifier
  - location_type: term describing the type of location
- NPMS_Samples_2015.csv
  - sample_id: unique sample identifier
  - survey_id: survey code
  - date: date of sample (format dd/mm/yyyy)
  - location_id: foreign key to locations table (identifies the location this sample is at)
  - entered_sref: spatial reference entered for the sample
  - entered_sref_system: system used for the entered spatial reference
  - created_on: timestamp when the record was created
  - created_by_id: foreign key to users table (creator)
- NPMS_Sample_Attributes_2015.csv
  - sample_attribute_value_id: unique identifier for the attribute value
  - sample_id: foreign key to samples table (identifies the related sample)
  - caption: caption for the sample attribute
  - text_value: value of the sample attribute
- NPMS_Occurrences_2015.csv
  - occurrence_id: unique occurrence identifier
  - sample_id: foreign key to samples table (identifies the sample for this occurrence)
  - taxonversionkey: taxon key for mappable taxa
  - taxon: taxon name (without authority)
  - domin: Domin score for the occurrence
  - record_status: status of the record (C = completed, V = verified, R = rejected)

## Data Quality, Provenance, and Metadata
- Relationships:
  - Samples link to Locations via location_id
  - Sample Attributes link to Samples via sample_id
  - Occurrences link to Samples via sample_id
- Provenance:
  - created_on tracks when records are created
  - created_by_id tracks the submitting user
- Spatial data:
  - entered_sref and entered_sref_system capture spatial references and their reference system
- Data formats:
  - date uses dd/mm/yyyy format
  - record_status uses codes to indicate processing state
- Taxonomic data:
  - taxonversionkey provides a mappable taxon key; taxon provides the name (without authority)

## Data Availability and Sharing
- The schema supports cataloging and sharing of datasets across portals due to clear foreign keys and standardized fields.
- Attributes like created_on and created_by_id support auditability and provenance tracking for sharing decisions.

## Data Stewardship Considerations
- Ensure referential integrity across all four files (foreign keys: location_id, sample_id, created_by_id).
- Document field-level metadata (data types, allowed values, formats, units) for accurate interpretation.
- Standardize spatial references and their systems to improve interoperability.
- Maintain clear semantics for record_status to support data quality workflows (completed, verified, rejected).
- Implement and enforce data publishing/updates workflow to reflect current data availability and embargoes if applicable.
- Consider cataloging datasets and maintaining versioning for updates.

## Particular Challenges (aligned with data stewardship)
- Incomplete understanding of user needs and priorities for these datasets.
- Timely acquisition of data (especially samples and occurrences).
- Ensuring data creators provide complete metadata (e.g., spatial refs, date formats, and provenance).
- Handling multiple systems and formats, including potentially non-interoperable spatial references.
- Managing large datasets and ensuring efficient transfer, storage, and updating.
- Dealing with outdated databases that may require bespoke solutions to maintain interoperability.

## Recommendations for Action
- Implement a standardized metadata schema describing each field (data type, expected formats, valid ranges, and units).
- Enforce referential integrity checks and validation rules during ingestion (e.g., valid location_id, valid sample_id, consistent record_status).
- Align coordinate reference systems and document any transformations or conversions.
- Maintain a data catalog entry with links to the four related files and their interdependencies.
- Establish data publishing rules, including update frequency, embargoes, and notices for updated records.