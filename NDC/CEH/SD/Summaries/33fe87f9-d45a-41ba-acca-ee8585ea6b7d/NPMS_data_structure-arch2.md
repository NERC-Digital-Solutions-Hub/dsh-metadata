# NPMS_Locations_2015.csv

## Overview
- Four NPMS 2015 CSV files form a linked data model to monitor environmental health over time: NPMS_Locations_2015.csv, NPMS_Samples_2015.csv, NPMS_Sample_Attributes_2015.csv, NPMS_Occurrences_2015.csv.
- Purpose: present environment health indicators in a consistent format, enabling scrutiny of ecological health and policy performance through time.
- Analysts typically verify, clean, and transform established data sources; produce outputs (e.g., reports, maps, charts) and ensure datasets are stored and accessible via portals.

## Data model and relationships
- Locations: NPMS_Locations_2015.csv
  - location_id: unique location identifier (primary key)
  - location_type: describes the type of location
- Samples: NPMS_Samples_2015.csv
  - sample_id: unique sample identifier (primary key)
  - survey_id: survey code
  - date: date of sample (dd/mm/yyyy)
  - location_id: foreign key to NPMS_Locations_2015.csv (identifies where the sample is)
  - entered_sref: spatial reference entered for the sample
  - entered_sref_system: spatial reference system used
  - created_on: timestamp when the record was created
  - created_by_id: foreign key to users table (who submitted the sample)
- Sample Attributes: NPMS_Sample_Attributes_2015.csv
  - sample_attribute_value_id: unique attribute record identifier (primary key)
  - sample_id: foreign key to NPMS_Samples_2015.csv
  - caption: caption describing the attribute
  - text_value: value of the sample attribute
- Occurrences: NPMS_Occurrences_2015.csv
  - occurrence_id: unique occurrence identifier (primary key)
  - sample_id: foreign key to NPMS_Samples_2015.csv (which sample the occurrence belongs to)
  - taxonversionkey: NBNA taxon key (for directly mappable taxa)
  - taxon: taxon name (without authority)
  - domin: Domin score (an indicator for occurrence strength)
  - record_status: status of the record (C = completed, V = verified, R = rejected)

## How the data supports environmental monitoring
- Location-to-sample linkage enables spatial aggregation of observations.
- Sample-date and spatial reference info support temporal analyses and geospatial mapping.
- Sample Attributes provide flexible metadata for samples (context, conditions, methods).
- Occurrences capture observed taxa within samples, including taxonomic keys and quality indicators (record_status, Domin score) for reliability and trend analysis.

## Data quality, workflow, and governance
- Data provenance: created_on and created_by_id support audit trails for sample records.
- Data quality signals: record_status indicates workflow state (completed, verified, rejected).
- Standardized formats and relationships enable consistent cross-year analyses and comparability.

## Challenges and opportunities for analysts
- Challenge: increasing the value of datasets by integrating NPMS data with additional datasets (e.g., other environmental indicators) to avoid single-use data.
- Challenge: enabling access to underlying data used to generate outputs, supporting transparency and reusability.
- Opportunity: leverage the linked structure (locations, samples, attributes, occurrences) to build time-series, spatial trends, and policy-performance dashboards for environmental health monitoring.

## Practical implications for reporting and analysis
- Use location_id, date, and taxon information to track biodiversity trends by location over time.
- Employ Domin scores and record_status to assess data confidence and prioritize validated observations.
- Combine sample attributes with occurrences to enrich analyses (e.g., correlating environmental conditions with observed taxa).