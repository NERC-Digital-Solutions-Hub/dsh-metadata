# CP_Fish_SpeciesTable.txt

## Purpose and scope
- Provides a species mapping table for the Chempop project, tying Chempop fish codes to Latin and Environment Agency (EA) NFPD codes and common names.
- Intended to support GIS mapping and map-based data visualisations by ensuring consistent species labeling across datasets.

## Data content at a glance
- File: CP_Fish_SpeciesTable.csv
- Structure: 4 rows, 93 columns (wide table); 4 described variables
- Key variables:
  - Fish_SpeciesCode: unique Chempop code for each fish taxon
  - Latin_Name: scientific name from the EA NFPD
  - EA_SpeciesCode: unique EA NFPD taxon code
  - Common_Name: vernacular/common name from the EA NFPD
- Missing data: none reported for the described fields
- Note: While the table has 4 data rows and 93 columns, only the four variables above are described in the metadata

## How the data were produced
- Provenance: derived from the Environment Agency’s National Fish Population Database (NFPD)
- Chempop codes were adapted from EA species codes
- Data processing rules:
  - If a Chempop code maps to multiple EA codes (e.g., strains/variants), those EA codes are summed into a single Chempop code
  - Taxa categories such as "hybrids", "All species", "Salmonid species", and "Freshwater species" were not assigned a Chempop code and were removed from the DataTable

## Data structure and field definitions
- Fish_SpeciesCode: unique Chempop identifier for each fish species in this table
- Latin_Name: scientific taxon name as per NFPD
- EA_SpeciesCode: unique EA NFPD code for the taxon
- Common_Name: common/vernacular name used in the NFPD

## Relationships and usage in GIS
- Relationship: Fish_SpeciesCode in this table refers to species entries in the Chempop data tables
- Usage: Enables consistent labelling and symbolisation in map visualisations by linking map data to standardized species codes, Latin names, and common names

## Data quality and limitations
- The record count is small (4 rows), but the CSV contains 93 columns (undocumented in detail in this summary)
- No explicit QA procedures recorded in the metadata

## Authors and contact
- Rachel Ainsworth (r.ainsworth@hull.ac.uk)
- Andy Nunn (a.d.nunn@hull.ac.uk)