# NPMS_Locations_2016.csv NPMS_Samples_2016.csv NPMS_Sample_Attributes_2016.csv NPMS_Occurrences_2016.csv

## Purpose and scope
- Defines the data schema for four NPMS 2016 CSV files: locations, samples, sample attributes, and occurrences.
- Establishes how location, sample, attribute, and occurrence data are organized and related to support environmental health monitoring analyses.

## Key data model features

- NPMS_Locations_2016.csv
  - location_id: unique location identifier
  - location_type: type/description of the location

- NPMS_Samples_2016.csv
  - sample_id: unique sample identifier
  - survey_id: code identifying the survey
  - date: sample date (dd/mm/yyyy)
  - location_id: foreign key to NPMS_Locations (identifies where the sample was taken)
  - entered_sref: spatial reference entered for the sample
  - entered_sref_system: system used for the spatial reference
  - created_on: timestamp of record creation
  - created_by_id: user who submitted the sample

- NPMS_Sample_Attributes_2016.csv
  - sample_attribute_id: unique identifier for a sample attribute value
  - sample_id: foreign key to NPMS_Samples (which sample the attribute belongs to)
  - caption: caption for the sample attribute
  - text_value: value of the sample attribute

- NPMS_Occurrences_2016.csv
  - occurrence_id: unique occurrence identifier
  - sample_id: foreign key to NPMS_Samples (which sample the occurrence is associated with)
  - taxonversionkey: NBNS taxon key for directly mappable taxa
  - taxon: taxon name (without authority)
  - domin: Domin score for the occurrence
  - record_status: status of the record (C = completed, V = verified, R = rejected)

## Relationships and data integrity
- Samples link to locations via location_id.
- Sample attributes link to samples via sample_id.
- Occurrences link to samples via sample_id.
- Taxonomic information is captured via taxon and taxonversionkey.
- Record_status in occurrences provides a simple data quality/validation workflow.

## Metadata, provenance, and governance implications
- Creation metadata (created_on, created_by_id) supports auditability and governance.
- Spatial and temporal fields (date, entered_sref, entered_sref_system) enable spatial-temporal monitoring analyses.
- The explicit foreign-key structure facilitates data integration across the four datasets and supports repeatable reporting.

## Practical considerations for monitoring frameworks
- Enables traceable, joinable datasets across location, sampling events, attributes, and biological occurrences.
- Supports quality control workflows through record_status and creation provenance.
- Highlights the need for consistent spatial reference handling and up-to-date taxonomic keys as part of data governance and metadata completeness.