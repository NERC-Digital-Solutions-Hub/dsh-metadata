# NPMS_Locations_2016.csv

## Overview
- A data dictionary for the NPMS 2016 dataset, encompassing four CSV files: NPMS_Locations_2016.csv, NPMS_Samples_2016.csv, NPMS_Sample_Attributes_2016.csv, and NPMS_Occurrences_2016.csv.
- Describes identifiers, relationships, and key attributes used to store sampling and occurrence information.

## Data schema by file

- NPMS_Locations_2016.csv
  - location_id: unique location identifier
  - location_type: term describing the type of location

- NPMS_Samples_2016.csv
  - sample_id: unique sample identifier
  - survey_id: survey code
  - date: date of sample (dd/mm/yyyy)
  - location_id: foreign key to NPMS_Locations_2016.csv (identifies where the sample was taken)
  - entered_sref: spatial reference entered for the sample
  - entered_sref_system: coordinate system used for the spatial reference
  - created_on: timestamp when the sample record was created
  - created_by_id: user account that submitted the sample (foreign key to a users table)

- NPMS_Sample_Attributes_2016.csv
  - sample_attribute_id: unique identifier for the sample attribute value
  - sample_id: foreign key to NPMS_Samples_2016.csv
  - caption: caption for the sample attribute
  - text_value: value of the sample attribute

- NPMS_Occurrences_2016.csv
  - occurrence_id: unique occurrence identifier
  - sample_id: foreign key to NPMS_Samples_2016.csv (identifies the sample for this occurrence)
  - taxonversionkey: NBNT taxon key for directly mappable taxa
  - taxon: taxon name (without authority)
  - domin: Domin score for the occurrence
  - record_status: status of the record (C = completed, V = verified, R = rejected)

## Key relationships
- Samples link to locations via location_id.
- Occurrences link to samples via sample_id.
- Sample attributes link to samples via sample_id.
- Taxonomic information is supported by taxon and taxonversionkey, enabling mapping to external taxonomies.

## Analytical opportunities
- Analyze species occurrences by location and sampling date.
- Assess dominance scores (domin) across taxa and surveys.
- Join taxonconversion keys to external taxonomies for broader biodiversity analysis.
- Filter by record_status to work with completed or verified records.
- Enrich samples with attributes (caption/text_value) to add metadata context.

## Data quality and considerations
- Year-specific dataset (2016); results may not generalize beyond this period.
- date format is dd/mm/yyyy; ensure correct parsing for time-series analyses.
- Spatial references are stored as entered_sref and entered_sref_system; may require standardization.
- Foreign keys (location_id, sample_id) assume consistent IDs across files.
- record_status semantics affect data inclusion (C, V, R statuses).
- Attribute data rely on caption/text_value for descriptive context; check for missing or ambiguous captions.

## Practical tips for analysts
- Construct robust joins: NPMS_Locations_2016.csv -> NPMS_Samples_2016.csv -> NPMS_Occurrences_2016.csv; optionally augment with NPMS_Sample_Attributes_2016.csv.
- Use created_on and created_by_id for provenance tracking and audit trails.
- Leverage taxonconversionkey to align taxa with external taxonomic databases.
- Validate and standardize date and spatial reference fields before analysis.
- Be mindful of potential data gaps at local scales and across datasets when interpreting results.