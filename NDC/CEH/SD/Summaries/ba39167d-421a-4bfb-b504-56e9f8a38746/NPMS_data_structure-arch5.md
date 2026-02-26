# NPMS_Locations_2016.csv

- Overview
  - A set of related NPMS data tables capturing locations, samples, sample attributes, and occurrences for 2016.
  - Designed to support data governance, discovery, and reuse by ensuring standardised fields, provenance, and linkages between tables.

## Data model and key tables

- NPMS_Locations_2016.csv
  - location_id: unique location identifier
  - location_type: term describing the type of location

- NPMS_Samples_2016.csv
  - sample_id: unique sample identifier
  - survey_id: survey code
  - date: date of sample in format dd/mm/yyyy
  - location_id: foreign key to locations table (identifies where the sample is)
  - entered_sref: Spatial reference entered for the sample
  - entered_sref_system: System used for the spatial reference in entered_sref
  - created_on: timestamp for when this record was created
  - created_by_id: foreign key to users table (creator) identifying the submitting user

- NPMS_Sample_Attributes_2016.csv
  - sample_attribute_id: unique sample attribute value identifier
  - sample_id: foreign key to samples table (identifies the sample)
  - caption: caption for the sample attribute
  - text_value: value of the sample attribute

- NPMS_Occurrences_2016.csv
  - occurrence_id: unique occurrence identifier
  - sample_id: foreign key to samples table (identifies the sample for this occurrence)
  - taxonversionkey: NBP National Biodiversity Network taxon key (for directly mappable taxa)
  - taxon: Taxon name (without authority)
  - domin: Domin score for the occurrence
  - record_status: status of this record (C = completed, V = verified, R = rejected)

## Data relationships and provenance

- Relationships
  - samples are linked to locations via location_id
  - sample_attributes link to samples via sample_id
  - occurrences link to samples via sample_id
  - created_by_id links to a users table to identify who submitted the sample
- Taxonomy and keys
  - taxonversionkey provides a standardized key for directly mappable taxa; taxon provides the readable name (without authority)

## Data quality, standards, and governance considerations

- Data quality points
  - Ensure consistent date formats (dd/mm/yyyy)
  - Validate IDs (unique constraints on location_id, sample_id, sample_attribute_id, occurrence_id)
  - Ensure foreign keys are maintained (e.g., sample references to existing samples; location references to existing locations)
  - Confirm spatial references (entered_sref) and corresponding systems (entered_sref_system) are consistent and mappable
- Metadata and provenance
  - created_on and created_by_id support data provenance and auditability
  - Record_status in NPMS_Occurrences_2016.csv enables tracking of data quality and review stage
- Standards and interoperability
  - Use of taxonversionkey for taxonomic keys supports interoperability with NBPN/NBN standards
  - Consistent field naming and data types across related tables facilitate integration into portals and catalogs

## Practical considerations for Data Stewards

- Data intake and timing
  - Plan for timely submission of sample records and attributes; monitor for incomplete or delayed data from data creators
- Metadata completeness
  - Encourage complete metadata capture (captions for sample attributes, clear survey codes, precise spatial references)
- Access, sharing, and updates
  - Maintain rules for data availability, embargoes, and update mechanisms; ensure that updates propagate across related tables
- Data quality assurance
  - Implement validation rules for key fields; perform regular quality checks on relationships and provenance data
- Documentation and discovery
  - Document data lineage, definitions of fields (especially taxon-related fields and spatial references), and update procedures to aid discoverability and reuse

## Summary

- The NPMS_2016 data model comprises four interrelated tables capturing locations, samples, sample attributes, and occurrences with clear foreign-key relationships, provenance, and taxonomic keys.
- Data stewardship focus should be on enforcing standards, maintaining data quality, managing provenance, and ensuring discoverability and timely sharing across systems.