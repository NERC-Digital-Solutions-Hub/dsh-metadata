# NPMS_Locations_2015.csv

- Overview
  - This document defines the schema for four NPMS 2015 CSV files that together capture locations, samples, sample attributes, and occurrences within surveys.
  - Primary goal from a Data Support perspective: enable data discovery, combination, and self-service analytics by clearly defining identifiers, relationships, and key fields.

- NPMS_Locations_2015.csv
  - location_id: unique location identifier
  - location_type: description of the type of location

- NPMS_Samples_2015.csv
  - sample_id: unique sample identifier
  - survey_id: survey code
  - date: date of the sample in format dd/mm/yyyy
  - location_id: foreign key to NPMS_Locations_2015.csv (identifies where the sample is located)
  - entered_sref: spatial reference entered for the sample
  - entered_sref_system: system used for the entered spatial reference
  - created_on: timestamp for when the record was created
  - created_by_id: foreign key to the users table (creator)

- NPMS_Sample_Attributes_2015.csv
  - sample_attribute_value_id: unique identifier for the attribute value
  - sample_id: foreign key to NPMS_Samples_2015.csv (identifies the associated sample)
  - caption: caption for the sample attribute
  - text_value: value of the sample attribute

- NPMS_Occurrences_2015.csv
  - occurrence_id: unique occurrence identifier
  - sample_id: foreign key to NPMS_Samples_2015.csv (identifies the sample for this occurrence)
  - taxonversionkey: NBNTaxon key for directly mappable taxa
  - taxon: taxon name (without authority)
  - domin: Domin score for the occurrence
  - record_status: status of the record (C = completed, V = verified, R = rejected)

- Relationships and data lineage
  - NPMS_Samples_2015.csv.location_id links to NPMS_Locations_2015.csv.location_id
  - NPMS_Sample_Attributes_2015.csv.sample_id links to NPMS_Samples_2015.csv.sample_id
  - NPMS_Occurrences_2015.csv.sample_id links to NPMS_Samples_2015.csv.sample_id
  - NPMS_Samples_2015.csv.created_by_id references a users table (creator)

- Data quality and format considerations
  - Date fields use the dd/mm/yyyy format; ensure consistent parsing for analytics.
  - Timestamps (created_on) provide data lineage and recency checks.
  - Foreign keys (location_id, sample_id, created_by_id) require referential integrity to maintain accuracy across files.
  - record_status in NPMS_Occurrences_2015.csv should be monitored to distinguish completed, verified, and rejected records.
  - taxonconversionkey supports mapping to NBNTaxon keys; ensure alignment with authoritative taxonomic data.

- Practical data product opportunities
  - Self-serve dashboards showing:
    - Occurrences by location, date, and taxon
    - Sample counts per survey and per location
    - Attribute-driven insights from NPMS_Sample_Attributes_2015.csv (e.g., descriptive attributes per sample)
  - Pivot tables and charts combining occurrences with sample metadata (survey, location, date)
  - Data quality reports identifying missing or inconsistent foreign keys, dates, or taxon keys

- Considerations for Data Support practice
  - Build and share a data dictionary covering each file, each field, and the relationships between files.
  - Implement ETL processes to enforce referential integrity and consistent date/time formats.
  - Provide guidance and templates for users to explore self-serve analyses while maintaining data governance.
  - Proactively note potential data gaps (e.g., incomplete spatial references, missing attribute values) and provide remediation strategies.