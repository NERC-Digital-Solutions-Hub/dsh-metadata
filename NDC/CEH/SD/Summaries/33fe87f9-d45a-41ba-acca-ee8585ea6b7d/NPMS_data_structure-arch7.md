# NPMS_Locations_2015.csv

## Purpose and scope
- Represents the NPMS data model for 2015, comprising four CSV files that together capture locations, samples, sample attributes, and occurrences.

## Key data files and fields

- NPMS_Locations_2015.csv
  - location_id: unique location identifier
  - location_type: term describing the type of location

- NPMS_Samples_2015.csv
  - sample_id: unique sample identifier
  - survey_id: survey code
  - date: date of sample (format dd/mm/yyyy)
  - location_id: foreign key to locations (identifies where the sample is located)
  - entered_sref: spatial reference entered for the sample
  - entered_sref_system: CRS/system used for entered_sref
  - created_on: timestamp when the record was created
  - created_by_id: foreign key to users (creator)

- NPMS_Sample_Attributes_2015.csv
  - sample_attribute_value_id: unique attribute value identifier
  - sample_id: foreign key to samples (identifies the related sample)
  - caption: caption for the sample attribute
  - text_value: value of the sample attribute

- NPMS_Occurrences_2015.csv
  - occurrence_id: unique occurrence identifier
  - sample_id: foreign key to samples (identifies the related sample)
  - taxonconversionkey: NBNTaxon key for directly mappable taxa
  - taxon: taxon name (without authority)
  - domin: Domin score for occurrence
  - record_status: status of this record (C = completed, V = verified, R = rejected)

## Data model and relationships
- Location-to-sample linkage: location_id in NPMS_Samples_2015.csv links to NPMS_Locations_2015.csv.
- Sample-to-attribute linkage: sample_id in NPMS_Sample_Attributes_2015.csv links to NPMS_Samples_2015.csv.
- Sample-to-occurrence linkage: sample_id in NPMS_Occurrences_2015.csv links to NPMS_Samples_2015.csv.
- Taxon mapping: taxonconversionkey (in NPMS_Occurrences_2015.csv) provides a key to map to taxonomy; taxon provides a display name.
- Audit and provenance: created_on and created_by_id capture record creation; entered_sref and entered_sref_system capture georeferencing details entered at the sample level.

## GIS usage and mapping considerations
- Integrate with a spatial layer for locations to provide geometries; the dataset includes location IDs but not explicit geometry in these files.
- Use entered_sref and entered_sref_system to place samples geospatially, with potential georeferencing recalibration if needed.
- Join operations:
  - NPMS_Locations_2015.csv with NPMS_Samples_2015.csv on location_id
  - NPMS_Samples_2015.csv with NPMS_Sample_Attributes_2015.csv on sample_id
  - NPMS_Samples_2015.csv with NPMS_Occurrences_2015.csv on sample_id
- Visualization ideas:
  - Map points for sample locations, colored or sized by date or domin score
  - Overlay taxonomy occurrences (taxonconversionkey/taxon) with filters on record_status
  - Popup attributes from NPMS_Sample_Attributes_2015.csv (caption/text_value)

## Data quality and preparation considerations
- Data are distributed across multiple files; ensure consistent foreign keys and referential integrity.
- Date fields use dd/mm/yyyy format; standardize to a consistent date type for analysis.
- Entered spatial references may require normalization to a common CRS before mapping.
- Record statuses (C/V/R) indicate data validation state; filter as needed for quality-controlled maps.

## Practical GIS workflows
- Import all four CSVs into a geospatial database or GIS, then:
  - Create a locations layer from NPMS_Locations_2015.csv (with geometry from another source or a linked geometry table).
  - Join samples to locations via location_id to create sample-point features.
  - Join occurrences to samples via sample_id to associate taxon data with each sample.
  - Join sample attributes to samples to enrich sample popups with captions/text_value.
- Apply filters by date, location_type, record_status, or taxonconversionkey to tailor map outputs for policy, clients, or public audiences.

## Temporal and provenance notes
- date (dd/mm/yyyy) provides sampling time reference.
- created_on and created_by_id offer an audit trail for data provenance and submission workflow.