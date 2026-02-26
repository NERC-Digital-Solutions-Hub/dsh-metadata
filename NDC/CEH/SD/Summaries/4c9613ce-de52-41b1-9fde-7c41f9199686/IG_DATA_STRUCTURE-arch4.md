# UK Environmental Change Network (http://www.ecn.ac.uk) Ground Predators (IG)

## Overview
- Dataset documenting abundance of ground predators (Carabidae) using pitfall traps.
- Protocol monitors fortnightly from May to October; data quality information should be used when analyzing.
- Managed by ECN Data Centre with governance and funding from a consortium of UK government departments and agencies; acknowledgement and publication receipt are requested when data are used.

## Data Coverage and Protocol
- Purpose: monitor ground predator abundance and track environmental change indicators.
- Sampling cadence: fortnightly between May and October.
- Quality: includes accompanying quality information; unusual events may be recorded with quality code 999, with text explanations as needed.
- Protocol reference: monitoring and measurement details available at ECN protocol page.

## Data Structure and Schema
- Data are stored in an Oracle database, organized into site-specific tables.
  - Data capture tables: D1IG_xxx (one per site) for abundance data.
  - Phenology/date tables: D2IG_xxx (traps set dates) for timing information.
  - Habitat metadata: D3IG_xxx (habitat descriptions) for site-level habitat data.
- Table/field layout (common core fields):
  - SITECODE, LCODE (location code), SDATE (sampling date), FROMDATE (trap set date, in D2IG), TRAP (trap number), FIELDNAME (species code or quality code), VALUE (numeric count or measurement).
- Site codes (12 total): T01 through T12, each with site name, location, and dataset date range.
- Site details (highlights):
  - T01 Drayton
  - T02 Glensaugh
  - T03 Hillsborough
  - T04 Moor House - Upper Teesdale
  - T05 North Wyke
  - T06 Rothamsted
  - T07 Sourhope
  - T08 Wytham
  - T09 Alice Holt
  - T10 Porton Down
  - T11 Y Wyddfa - Snowdon
  - T12 Cairngorms
  - Date ranges span roughly 1993–2012 depending on site.
- Core metadata: separate metadata documentation exists for dataset structure and field definitions.

## Taxonomy and Quality Codes
- Fieldnames contain either species codes or quality codes.
- Species codes: extensive hierarchies covering many beetle genera and species (Carabidae and related groups), with mappings between codes and Latin names, ranks, and taxonomic groups.
- Quality codes: standard ECN quality codes (e.g., 100, 101, 102, …, 999) indicating data quality factors such as information gaps, sample issues, environmental conditions, and processing status.
- Quality code descriptions cover aspects from sample loss, contamination, and late or non-standard sampling to laboratory and hydrology-related notes.

## Data Use, Access, and Citation
- Acknowledge ECN data usage; report back with one reprint of any publication citing the dataset.
- Data access via ECN data centre; protocol and accompanying quality information are essential for appropriate analysis and interpretation.

## Metadata, Standards, and Governance
- Core metadata documentation available; dataset designed to support cross-site comparisons and ecosystem-level understanding of environmental change impacts on ground-dwelling predators.
- The data governance framework includes data provenance, site-level metadata, and standardized field/measurement definitions to facilitate discoverability and reuse.