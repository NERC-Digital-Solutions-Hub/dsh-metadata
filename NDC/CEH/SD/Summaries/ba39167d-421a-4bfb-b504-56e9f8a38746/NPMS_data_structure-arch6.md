# NPMS Data Model 2016 (Locations, Samples, Sample Attributes, Occurrences)

- Four CSV files define the NPMS data model for 2016:
  - NPMS_Locations_2016.csv
  - NPMS_Samples_2016.csv
  - NPMS_Sample_Attributes_2016.csv
  - NPMS_Occurrences_2016.csv

## Overview

- The dataset comprises locations, samples collected at those locations, attributes of those samples, and species occurrences linked to samples.
- Primary keys and foreign keys establish relationships between tables to enable integrated queries.

## Tables and Key Fields

- NPMS_Locations_2016.csv
  - location_id: unique location identifier
  - location_type: term describing the type of location

- NPMS_Samples_2016.csv
  - sample_id: unique sample identifier
  - survey_id: survey code
  - date: date of sample in format dd/mm/yyyy
  - location_id: foreign key to NPMS_Locations_2016.csv (identifies where the sample is)
  - entered_sref: spatial reference entered for the sample
  - entered_sref_system: system used for the spatial reference
  - created_on: timestamp when this record was created
  - created_by_id: foreign key to users table (creator)

- NPMS_Sample_Attributes_2016.csv
  - sample_attribute_id: unique sample attribute value identifier
  - sample_id: foreign key to NPMS_Samples_2016.csv
  - caption: caption for the sample attribute
  - text_value: value of the sample attribute

- NPMS_Occurrences_2016.csv
  - occurrence_id: unique occurrence identifier
  - sample_id: foreign key to NPMS_Samples_2016.csv
  - taxonversionkey: NBND taxon key (for directly mappable taxa)
  - taxon: taxon name (without authority)
  - domin: Domin score for the occurrence
  - record_status: status of this record (C = completed, V = verified, R = rejected)

## Relationships and Data Flow

- Location to Samples: NPMS_Samples_2016.location_id references NPMS_Locations_2016.location_id
- Samples to Attributes: NPMS_Sample_Attributes_2016.sample_id references NPMS_Samples_2016.sample_id
- Samples to Occurrences: NPMS_Occurrences_2016.sample_id references NPMS_Samples_2016.sample_id
- Provenance: created_on and created_by_id track who created a sample record and when

## Data Quality and Use Considerations

- Date format standardized as dd/mm/yyyy in the Samples table.
- Spatial references are captured via entered_sref and entered_sref_system for location-based analyses.
- Taxonomic data includes both a taxon name and a taxon conversion key for mapping to standardized taxonomies.
- Record status in occurrences allows filtering of incomplete or rejected data.
- The schema supports building dashboards and self-serve analyses that combine location, sampling events, sample attributes, and species occurrences. It enables location-based queries, attribute-driven insights, and occurrence summaries by location or survey.

## Notes for Data Support

- Ensure referential integrity across tables (locations, samples, attributes, occurrences).
- Validate spatial reference formats and systems if integrating with mapping tools.
- Maintain consistency of taxon keys and accompanying taxon names to support reliable cross-referencing.
- Monitor data provenance (created_on, created_by_id) to support auditability and user-facing explanations.