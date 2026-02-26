# NPMS_Locations_2015.csv NPMS_Samples_2015.csv NPMS_Sample_Attributes_2015.csv NPMS_Occurrences_2015.csv

- Overview
  - A four-table data schema for NPMS (2015) covering locations, samples, sample attributes, and occurrences.
  - Designed to enable linking spatial data with sampling events and observed taxa, including metadata and data quality indicators.

- NPMS_Locations_2015.csv
  - location_id: unique location identifier
  - location_type: term describing the type of location

- NPMS_Samples_2015.csv
  - sample_id: unique sample identifier
  - survey_id: survey code
  - date: date of sample (format dd/mm/yyyy)
  - location_id: foreign key to NPMS_Locations_2015.csv (identifies where the sample was taken)
  - entered_sref: Spatial reference entered for the sample
  - entered_sref_system: System used for the spatial reference
  - created_on: timestamp for when the record was created
  - created_by_id: foreign key to users (creator)

- NPMS_Sample_Attributes_2015.csv
  - sample_attribute_value_id: unique identifier for a sample attribute value
  - sample_id: foreign key to NPMS_Samples_2015.csv (the sample this attribute value refers to)
  - caption: caption for the sample attribute
  - text_value: value of the sample attribute

- NPMS_Occurrences_2015.csv
  - occurrence_id: unique occurrence identifier
  - sample_id: foreign key to NPMS_Samples_2015.csv (identifies the sample for this occurrence)
  - taxonversionkey: NBNTaxon key for directly mappable taxa
  - taxon: Taxon name (without authority)
  - domin: Domin score for occurrence
  - record_status: status of the record (C = completed, V = verified, R = rejected)

- Data relationships and navigations
  - Locations -> Samples: one-to-many (location_id in Samples)
  - Samples -> Sample Attributes: one-to-many (sample_id in Sample Attributes)
  - Samples -> Occurrences: one-to-many (sample_id in Occurrences)
  - Occurrences -> Taxonomy: taxonversionkey provides a link to NBNTaxon keys; taxon provides the name

- Key data quality and format notes
  - Date fields use format dd/mm/yyyy; ensure consistent parsing.
  - created_on is a timestamp; created_by_id may reference user records outside the dataset.
  - record_status in Occurrences indicates data validation state (completed, verified, rejected).
  - Spatial data (entered_sref and entered_sref_system) may require validation against a spatial reference system.

- Suggested analyses for analysts
  - Spatial distribution: map sample locations by location_type and analyze by geographic clusters.
  - Temporal trends: examine sample dates to identify sampling seasonality or trends over time.
  - Taxon-focused analysis: aggregate occurrence counts by taxon (using taxonversionkey) and compute dominance scores.
  - Data quality checks: filter by record_status to compare completed vs. verified vs. rejected records; assess missing dates or spatial references.
  - Attribute enrichment: join Sample Attributes to samples to contextualize sampling conditions (via captions and text_value).

- Practical considerations for data use
  - Utilize foreign keys to perform joined analyses across locations, samples, attributes, and occurrences.
  - Ensure taxonversionkey mappings are available when integrating with broader taxonomic datasets.