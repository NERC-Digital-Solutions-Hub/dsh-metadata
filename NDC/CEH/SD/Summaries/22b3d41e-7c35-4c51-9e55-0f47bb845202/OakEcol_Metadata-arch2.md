# Metadata for EIDC

## Overview
- Documents an oak-focused environmental dataset (OakEcol) aggregating data on species associated with UK oaks (Quercus petraea and Q. robur).
- Scope: 2300 species across six taxon groups (birds, bryophytes, fungi, invertebrates, lichens, mammals) with varying levels of association to oak.
- Purpose aligned with monitoring aims: standardised data to assess environmental health and the status of oak ecosystems and their dependent biodiversity.
- Includes conservation status integration and an “at risk to oak decline” index.

## Data scope and content
- Global concern: oak health decline and unknown impacts on associated biodiversity; UK-focused compilation to elucidate oak-linked biodiversity.
- For each species: level of association with oak (obligate, high, partial, cosmopolitan, uses) and ecological details.
- Ecological data captured: part of tree used, how the species uses the tree (feeding, roosting, breeding), age of tree, woodland type, tree form (coppice, pollard, natural), and season of oak use.
- Comparative data: use/association with 30 other tree species (alternative trees) also captured.

## Experimental design, materials, and methods
- Literature review conducted in 2016/17; comprehensive search of published and grey literature plus unpublished information.
- Taxa limited to six groups; algae/bacteria/micro-organisms not included.
- Data structured around a predefined common framework and stored in a relational database (OakEcol); CSV table format for each table.
- Association levels defined with explicit criteria (obligate, high, partial, cosmopolitan, uses) and table definitions provided (OakEcol_Definitions_Association.csv and related definition files).
- Conservation status captured across multiple schemes (UK conservation lists, IUCN, Red Data Book, Biodiversity Action Plans, Birds of Conservation Concern) and combined to produce an “at risk to oak decline” index.
- Data quality indicators recorded (peer-reviewed vs. other sources, UK vs non-UK) and all data sources documented (References table).

## Data structure and accessibility
- OakEcol relational database stored as CSV files; 25 tables with explicit relationships illustrated (Figure 1 in the document).
- Key table: Species (main table; links to many other tables for ecology, usage, age, tree parts, forms, seasons, woodland types, alternative trees, etc.).
- Other tables include: Age, Use, Tree_part, Tree_form, Season, Woodland, Ecology_notes, Invert_fungi, Alternative_Trees, References, Only_Woodland, and several Definitions tables (Age, Association, Conservation_status, Part, Season, Species_Group, Use, Woodland).
- Each table is cross-referenced via Latin species names and reference numbers to enable reconstruction of the database from CSV files.
- Data sources and table descriptions are comprehensively documented (e.g., OakEcol_References.csv, OakEcol_Definitions_*.csv).

## Outputs and monitoring relevance
- Data are designed to be stored, quality assured, and accessible for ongoing monitoring and analysis.
- Outputs include structured datasets and metadata suitable for reports, maps, and charts, enabling scrutiny of oak-associated biodiversity and policy-relevant indicators.
- The dataset supports evaluating ecosystem risk by integrating oak decline status with species-level associations and conservation considerations.

## Particular challenges and opportunities for analysts
- Challenge: increasing the value of oak-associated datasets by integrating with other relevant data sources (beyond single-use applications).
- Challenge: enabling broad access to underlying data used to generate final outputs, enhancing reproducibility and policy monitoring.

## Funding and acknowledgments
- Funded by Defra through the BBSRC grant Protecting Oak Ecosystems (PuRpOsE): BB/N022831/1.
- Additional funding support from the Scottish Government’s Rural and Environment Research and Analysis Directorate (2016-2021 strategic programme).

## References and data provenance
- Extensive literature sources across birds, bryophytes, fungi, invertebrates, lichens, and mammals; full references catalogued in the References table.
- Data sources include well-known taxon-specific checklists and biodiversity databases, with explicit provenance for each association assessment and conservation status determination.