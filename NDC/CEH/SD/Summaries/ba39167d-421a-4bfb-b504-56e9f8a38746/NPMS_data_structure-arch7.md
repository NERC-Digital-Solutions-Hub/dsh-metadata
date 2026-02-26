# NPMS_Locations_2016.csv; NPMS_Samples_2016.csv; NPMS_Sample_Attributes_2016.csv; NPMS_Occurrences_2016.csv

## Overview
- Four NPMS 2016 CSV files describing locations, samples, sample attributes, and occurrences.
- Structures designed to support GIS mapping and spatial analysis of biological data.
- Emphasis on linking data to locations, temporal context, and taxonomic observations.

## Key Tables and Core Fields
- NPMS_Locations_2016.csv
  - location_id: unique location identifier (Primary Key)
  - location_type: term describing the type of location
- NPMS_Samples_2016.csv
  - sample_id: unique sample identifier (Primary Key)
  - survey_id: survey code
  - date: date of sample (dd/mm/yyyy)
  - location_id: foreign key to NPMS_Locations_2016 (identifies where the sample is)
  - entered_sref: spatial reference entered for the sample
  - entered_sref_system: system used for the spatial reference
  - created_on: timestamp of record creation
  - created_by_id: user who submitted the sample (foreign key to users)
- NPMS_Sample_Attributes_2016.csv
  - sample_attribute_id: unique attribute value identifier (Primary Key)
  - sample_id: foreign key to NPMS_Samples_2016
  - caption: caption for the sample attribute
  - text_value: value of the sample attribute
- NPMS_Occurrences_2016.csv
  - occurrence_id: unique occurrence identifier (Primary Key)
  - sample_id: foreign key to NPMS_Samples_2016
  - taxonversionkey: direct map to National Biodiversity Network taxon key (where applicable)
  - taxon: taxon name (without authority)
  - domin: Domin score (dominance) for the occurrence
  - record_status: status (C = completed, V = verified, R = rejected)

## Relationships and GIS Context
- Location-sample linkage via location_id in NPMS_Samples_2016.csv enables spatial joins to map sample points.
- Occurrences are tied to samples, allowing spatial visualization of taxa occurrences by location and date.
- enter_sref and entered_sref_system provide the spatial reference framework for projects, enabling coordinate system handling and GIS transformations.
- Created_on and created_by_id support data provenance and audit trails for GIS workflows.

## Spatial Processing and Visualisation
- Use entered_sref and entered_sref_system to construct geospatial geometries in GIS tools.
- Map points by sample location with attributes from NPMS_Sample_Attributes_2016.csv as additional layers or pop-ups.
- Visualize taxon occurrences with the taxonname and domin score; filter by date, survey, or location.
- Leverage taxonversionkey for alignment with external taxonomic databases where available.

## Data Quality, Standards, and Provenance
- record_status in NPMS_Occurrences_2016.csv indicates the reliability of each observation (C, V, R).
- date field in NPMS_Samples_2016.csv provides a temporal axis for analyses.
- Consistency across multiple tables is essential for accurate GIS mapping (foreign keys: location_id, sample_id, etc.).

## Practical Considerations for GIS Specialists
- Data integration: join NPMS_Samples_2016.csv to NPMS_Locations_2016.csv on location_id; join NPMS_Occurrences_2016.csv to NPMS_Samples_2016.csv on sample_id.
- Spatial reference handling: ensure entered_sref is converted to usable geometry in the target GIS (consider potential mismatches in entered_sref_system).
- Data cleaning: handle missing or incomplete records (e.g., missing date, location, or sample attributes) to avoid gaps in maps.
- Resolution and standardization: align data resolution and taxonomy across tables; use taxonconversionkey where available to harmonize taxonomic data.
- User and audit trails: utilize created_on and created_by_id for data governance in GIS projects.

## Potential Use Cases in GIS
- Create interactive maps showing sample locations and their taxon occurrences across time.
- Develop choropleth or heatmap visualisations of occurrence density by location type or survey.
- Link attribute-rich sample records to spatial features for policy or public outreach maps.