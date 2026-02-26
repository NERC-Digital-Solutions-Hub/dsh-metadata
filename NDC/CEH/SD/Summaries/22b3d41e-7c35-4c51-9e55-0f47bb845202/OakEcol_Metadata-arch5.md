# Metadata for EIDC

## Overview
- Addresses OakEcol, a UK-focused dataset documenting oak-associated biodiversity.
- Objective: support data governance, discovery, and reuse by providing a well-documented metadata and data model.
- Project funded by Defra via BBSRC PuRpOsE (BB/N022831/1) with additional Scottish Government support.

## Data Scope and Purpose
- Focus: species that use Quercus petraea and Q. robur in the UK.
- Taxa covered: birds, bryophytes, invertebrates, fungi, lichens, and mammals (six groups).
- Database scope: records for approximately 2300 species, with an assigned level of association to oak (e.g., obligate, high, partial, cosmopolitan, uses).
- For each species, ecological uses of the oak are recorded (feeding, roosting, nesting, living space, etc.), parts used, age of tree, woodland type, tree form, season, and use of oak.
- Includes data on whether species use 30 alternative tree species and the strength of those associations.
- Conservation context captured (UK Red List status, IUCN status, BAP/priority statuses across UK countries, Birds of Conservation Concern).

## Data Model and Tables
- Central dataset: OakEcol, a relational database stored as CSV files.
- Core table: Species (Latin name, English name, association level, conservation status, native status, etc.).
- Supporting data: use and ecology tables (Woodland, Use, Age, Tree_part, Tree_form, Season), and tables for alternative trees (Alternative_Trees, Alternative_Tree_names).
- Definitions tables provide standardized metadata for:
  - Age
  - Association categories
  - Confidence of association data
  - Conservation status
  - Parts of the tree
  - Seasons
  - Species groups
  - Uses
  - Woodland types
- Data provenance and references are captured in a dedicated References table.
- Documentation for each table is provided (Table 3–Table 25) with explicit field definitions and cross-table linkages.
- Table 1 describes methodologies for assessing oak association; Table 2 lists all OakEcol tables.
- The data structure is designed to be reproducible (Figure 1 shows the relational diagram and how CSVs rebuild the database).

## Data Quality, Provenance, and Metadata
- Data sources include peer-reviewed literature, grey literature, unpublished information, and curated checklists.
- Quality indicators captured: data type (peer-reviewed vs other), UK vs non-UK origin, and confidence definitions for association.
- Comprehensive references are maintained (References table) with authors, year, title, publication, DOI, etc.
- An explicit “at risk to oak decline” index combines association level and conservation status (as per Mitchell et al. methods).
- Documentation emphasizes knowledge gaps and notes on data quality for each species entry.

## Access, Use, and Updating
- OakEcol data exist as separate CSV files per table, enabling modular access and updates.
- The database is designed to be rebuildable from CSVs using the published relational structure.
- Data include notes and comments on association and conservation status to aid interpretation.
- Contact for data and coordination: Ruth Mitchell (ruth.mitchell@hutton.ac.uk) and listed affiliations.
- Embargoes, proprietary constraints, or other sharing limitations are considered within the data model (through association and conservation status metadata).

## Documentation and References
- Extensive metadata and definitions accompany the data (OakEcol_Definitions_*.csv, etc.).
- Table 3 (Species) and related tables document fields and relationships; Tables 4–25 detail additional data elements.
- References are thoroughly recorded (References table) with full citation details and online resources where applicable.

## Funding, Acknowledgments, and Contacts
- Funded by Defra through the BBSRC PuRpOsE grant and the Scottish Government's Rural and Environment Research and Analysis Directorate.
- Authors and affiliations are provided; primary contact is Ruth Mitchell at The James Hutton Institute.

## Practical Implications for Data Stewards
- Emphasizes rigorous metadata and standardized definitions to support interoperability across datasets.
- Demonstrates a clear provenance trail from literature sources to database entries.
- Supports governance needs by recording data quality, confidence, and conservation context.
- Highlights the challenge of integrating multi-taxa ecological data with multiple data sources and formats, while maintaining a consistent, queryable data model.