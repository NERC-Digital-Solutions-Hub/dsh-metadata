# NPMS_Locations_2016.csv

- Purpose: Part of the NPMS data schema for 2016, capturing spatial locations used in environmental monitoring and associated sampling data.
- Scope across files: Describes how locations, samples, sample attributes, and occurrences relate to support monitoring analyses and outputs.

## Dataset Structure

- NPMS_Locations_2016.csv
  - location_id: unique location identifier
  - location_type: term describing the type of location

- NPMS_Samples_2016.csv
  - sample_id: unique sample identifier
  - survey_id: survey code
  - date: date of sample in format dd/mm/yyyy
  - location_id: foreign key to locations table; identifies the location for this sample
  - entered_sref: spatial reference entered for the sample
  - entered_sref_system: spatial reference system used for entered_sref
  - created_on: timestamp when this record was created
  - created_by_id: foreign key to the users table; identifies who submitted the sample

- NPMS_Sample_Attributes_2016.csv
  - sample_attribute_id: unique identifier for the sample attribute value
  - sample_id: foreign key to samples table; identifies the sample this attribute belongs to
  - caption: caption for the sample attribute
  - text_value: value of the sample attribute

- NPMS_Occurrences_2016.csv
  - occurrence_id: unique occurrence identifier
  - sample_id: foreign key to samples table; identifies the sample for this occurrence
  - taxonconversionkey: National Biodiversity Network taxon key for directly mappable taxa
  - taxon: taxon name (excluding authority)
  - domin: Domin score for the occurrence
  - record_status: status of the record (C = completed, V = verified, R = rejected)

## Data Relationships

- Locations serve as the base entity for samples via location_id in NPMS_Samples_2016.csv.
- NPMS_Samples_2016.csv connects to NPMS_Sample_Attributes_2016.csv via sample_id.
- NPMS_Samples_2016.csv connects to NPMS_Occurrences_2016.csv via sample_id.
- Taxonomic information is captured via taxonconversionkey and taxon in NPMS_Occurrences_2016.csv.

## Data Quality & Provenance

- Date formatting standardized as dd/mm/yyyy in samples.
- Spatial references captured with entered_sref and entered_sref_system to support geolocation analyses.
- Provenance tracked with created_on and created_by_id for auditability.
- Occurrence records include a clear lifecycle status (completed, verified, rejected).

## Monitoring Use & Outputs

- Data can be analyzed to assess environmental sampling across locations and times.
- Outputs commonly include reports, maps, and charts derived from the relationships among locations, samples, and occurrences.
- Datasets are stored and uploaded to appropriate portals to support sharing and transparency.

## Challenges & Opportunities for Analysts

- Increasing dataset value by integrating NPMS data with other relevant datasets (avoiding single-use datasets).
- Enabling access to underlying data used to produce final outputs for broader scrutiny and reuse.