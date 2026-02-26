# NPMS_Locations_2015.csv

## Overview
- Defines the NPMS data schema (2015) across four CSV files: NPMS_Locations_2015.csv, NPMS_Samples_2015.csv, NPMS_Sample_Attributes_2015.csv, and NPMS_Occurrences_2015.csv.
- Aims to support environmental health monitoring for scrutinising policy, evaluating decisions, and informing future actions.
- Designed for use by managers within government or environmental bodies responsible for monitoring approaches, data quality, and governance.

## Data model and key tables
- NPMS_Locations_2015.csv
  - location_id: unique location identifier
  - location_type: descriptor of the location type
- NPMS_Samples_2015.csv
  - sample_id: unique sample identifier
  - survey_id: code for the survey
  - date: sample date (dd/mm/yyyy)
  - location_id: foreign key to locations (identifies the sample’s location)
  - entered_sref: spatial reference entered for the sample
  - entered_sref_system: system used for the spatial reference
  - created_on: timestamp when the record was created
  - created_by_id: foreign key to users (creator of the sample)
- NPMS_Sample_Attributes_2015.csv
  - sample_attribute_value_id: unique identifier for a sample attribute value
  - sample_id: foreign key to samples (identifies the associated sample)
  - caption: caption for the sample attribute
  - text_value: value of the sample attribute
- NPMS_Occurrences_2015.csv
  - occurrence_id: unique occurrence identifier
  - sample_id: foreign key to samples (identifies the sample for this occurrence)
  - taxonversionkey: NBNT taxon key (for directly mappable taxa)
  - taxon: taxon name (without authority)
  - domin: Domin score for the occurrence
  - record_status: status (C = completed, V = verified, R = rejected)

## Data relationships
- Occurrences link to Samples; Samples link to Locations.
- Attributes link to Samples, enabling contextual metadata per sample.

## Data quality, metadata, and governance considerations
- Metadata needs: ensure comprehensive metadata accompanies each table (definitions, data provenance, update frequency).
- Spatial data: entered_sref and entered_sref_system require standardization and validation for interoperability.
- Temporal data: date format must be consistent; consider time zones if applicable.
- Taxonomy: taxonconversionkey supports standardized mapping; maintain alignment with NBNT taxonomy updates.
- Provenance and audit: created_on and created_by_id provide an audit trail; consider expanding with data lineage.
- Data governance: explicit record_status supports workflow tracking (completed, verified, rejected); implement governance processes for status transitions and data sharing.

## Use for monitoring frameworks and policy evaluation
- Enables tracking of biodiversity sampling across locations and times, supporting policy evaluation of environmental health interventions.
- Facilitates measurement of spatial and temporal patterns in taxa presence via occurrences and their dominance scores.
- Provides structured data to inform dashboards, charts, and reports that communicate complex findings clearly to stakeholders.
- Supports data sharing and transparency while highlighting governance needs (versioning, access controls, metadata standards).

## Practical recommendations for implementation
- Enforce referential integrity: validate location_id and sample_id foreign keys across tables.
- Develop a standard metadata schema to accompany CSVs (data quality checks, lineage, update cadence).
- Implement data cleaning and transformation pipelines to maintain consistent spatial and taxonomic data.
- Create documentation and dashboards that link location types, sampling dates, taxa, and occurrence statuses to aid decision-making.
- Establish clear governance for data access, sharing, and public disclosure, balancing openness with sensitivity where needed.