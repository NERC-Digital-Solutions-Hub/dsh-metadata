# NPMS_Locations_2015.csv

- Overview
  - A set of four related CSV tables (NPMS_Locations_2015.csv, NPMS_Samples_2015.csv, NPMS_Sample_Attributes_2015.csv, NPMS_Occurrences_2015.csv) that model biodiversity survey data.
  - Captures locations, samples taken at locations, attributes describing samples, and species occurrences observed in samples.

- Data model and key fields
  - NPMS_Locations_2015.csv
    - location_id: unique location identifier
    - location_type: descriptor of the location type
  - NPMS_Samples_2015.csv
    - sample_id: unique sample identifier
    - survey_id: survey code
    - date: date of sample (dd/mm/yyyy)
    - location_id: foreign key to NPMS_Locations_2015.csv
    - entered_sref: spatial reference entered for the sample
    - entered_sref_system: spatial reference system used
    - created_on: record creation timestamp
    - created_by_id: foreign key to users (creator)
  - NPMS_Sample_Attributes_2015.csv
    - sample_attribute_value_id: unique attribute value identifier
    - sample_id: foreign key to NPMS_Samples_2015.csv
    - caption: caption for the attribute
    - text_value: value of the sample attribute
  - NPMS_Occurrences_2015.csv
    - occurrence_id: unique occurrence identifier
    - sample_id: foreign key to NPMS_Samples_2015.csv
    - taxonversionkey: mappable taxon key
    - taxon: taxon name (without authority)
    - domin: Domin score for occurrence
    - record_status: status (C = completed, V = verified, R = rejected)

- Relationships and data flow
  - Locations → Samples via location_id
  - Samples → Sample Attributes via sample_id
  - Samples → Occurrences via sample_id
  - Taxon data linked via taxonconversionkey and taxon; occurrence records carry a lifecycle status (record_status)

- Data quality, governance and stewardship considerations
  - Data integrity
    - Ensure foreign keys (location_id, sample_id) are valid; maintain referential integrity across tables.
    - Validate date formats (date) and consistency with any regional settings.
    - Track provenance with created_on and created_by_id for auditability.
  - Metadata and standards
    - Provide clear definitions for location_type, entered_sref, entered_sref_system, and fields in sample attributes.
    - Maintain consistent taxon mapping via taxonconversionkey; verify against authoritative taxon keys.
  - Data completeness and granularity
    - Check for missing location_id, date, or sample attributes; assess whether granularity supports intended analyses.
  - Discoverability and governance
    - Document data dictionary and lineage; ensure discoverability of all four tables and their interrelations.
    - Establish update/versioning processes to reflect changes in samples or occurrences.
  - Access and privacy considerations
    - Review who can create/update samples and occurrences; ensure appropriate access controls for sensitive location data.

- Implications for data strategy and use
  - Enables location- and time-bound biodiversity analyses by linking locations, samples, attributes, and species occurrences.
  - Supports data products for policy colleagues and partners through structured metadata and clear data lineage.
  - Highlights need for coordinated data standards across tables to enable reliable cross-table analyses and data sharing.