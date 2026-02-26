# CS Technical Report No 1/07: Field Mapping Handbook v1.0

- Purpose: Establishes a standardized, digitized field-mapping framework for Countryside Survey 2007 to monitor land cover change and support biodiversity reporting across the UK (including Wales).
- Scope: Provides methodology for mapping habitat extent and change, including Broad Habitats (BH) and nested Priority Habitats (PH), with country-wide reporting and time-series comparability.

## Design goals and monitoring framework principles

- Stakeholder engagement: determine which measures give useful insight by consulting stakeholders and experts, and by learning from others to avoid duplication.
- Data provenance and openness: identify and verify data sources, document metadata, and share underlying data where possible; implement data governance from source.
- Data quality and standardization: ensure data are quality assured, cleaned, transformed, analyzed, and presented clearly; set data management standards at source.
- Long-term monitoring and policy relevance: enable robust tracking of habitat extent and change to inform policy and future decisions.
- Data accessibility barriers: anticipate challenges around metadata completeness, data sharing, and timely access; plan governance to mitigate these barriers.

## Mapping framework and habitat classification

- Two-tier habitat structure:
  - Broad Habitats (BH) and nested Priority Habitats (PH); PHs nest into BHs and may be mapped for new baselines.
- Habitat distinctions:
  - Enclosed vs unenclosed habitats; adjustments to PH allocations reflect historical data limitations.
- Time-series design:
  - Digital time-series design to maintain comparability with previous surveys (CS1990/CS2000) while enabling richer attribute data.
- Reporting scales:
  - Country-wide reporting at BH level and PH-level reporting where applicable.
- Wales and new baselines:
  - Inclusion of Wales squares and emphasis on PH reporting where feasible.

## Data model: polygon and component attributes; vegetation and change

- Dual data levels:
  - Polygon level: BH/PH classification.
  - Component level: detailed attributes organized by themes (e.g., Inland Physiography, Inland Water, Agriculture/Natural Vegetation, Forestry, Structures, etc.).
- Vegetation and habitat attributes:
  - Emphasis on primary and secondary vegetation attributes; guidance on when to subdivide polygons.
- Species recording:
  - At least two species per habitat polygon (up to four) to support ecological interpretation.
- Change attribution:
  - Clear guidance to distinguish real ecological change (REAL) from data issues (ERROR); PH/BH reallocations may require new baseline coding.

## The Two Keys: Vegetation Key and Woodland Types/Features Key

- Vegetation Key: assigns polygon vegetation to BHs or PHs based on species composition and canopy structure; supports decisions on retaining/changing habitat classifications.
- Woodland Types/Features Key: classifies woody vegetation into woodlands and components (e.g., Woodland/Forest, Belt of trees, Clump of trees, Woody Linear Features); aids in identifying woodland-derived BH/PH and supports mosaic approaches.

## The Digital Mapping System: CS Surveyor and ArcMap

- CS Surveyor: bespoke ArcMap extension for field capture, editing, and governance of habitat polygons, lines, and points.
- Core workflow:
  - Focus on extent and change of BHs/PHs; spatial accuracy is secondary to correct habitat attribution and change recording.
- Editing capabilities:
  - Area editing: split, merge, update, copy attributes, and update shapes.
  - Line editing: events along linear features (fences, hedges); add/copy/delete events; adjust lengths.
  - Point editing: add/move/copy points with nested attributes.
  - Strict stop-editing protocol; regular saves; session controls.
- Field guidance:
  - MMU constraints, editing scale (< 1:5000), handling of errors and spatial inaccuracies.

## Mapping methodology and rules

- Minimum Mappable Unit (MMU): 1/25 hectare (400 m2); polygons must meet this size to be mapped; lines used for features below MMU.
- Change and data integrity:
  - Real change vs error change; PH/BH reallocations may require new baseline coding.
  - Enclosed vs unenclosed habitat handling reflects historical data limitations.
- Mosaic mapping:
  - For spatially indiscernible patches or MMU constraints, use mosaics with component-level percentages summing to 100%.
- Habitat delineation specifics:
  - Enclosed BHs (lowland; often mapped from 1998 data) allow PH attribution on top of BH.
  - Unenclosed BHs may merge or require back-corrections to reflect finer vegetation data.
- Species and margins:
  - Record margins and buffer zones; woody features include belts, clumps, lines, and scattered trees with detailed attributes (e.g., DBH, canopy cover, percent cover).

## Habitat Descriptions by Broad Habitats (BHs)

- BH1 Broadleaved Mixed and Yew Woodland (includes various PH candidates and mosaics).
- BH2 Coniferous Woodland (native and non-native; detailed woodland attributes and species lists).
- BH3 Boundaries and Linear Features (primary attribute: wide linear feature; may be area-like if width >5 m).
- BH4 Arable and Horticultural (crops, margins, vegetation types, agriculture uses; includes margins and set-aside).
- BH5 Improved Grassland; BH6 Neutral Grassland; BH7 Calcareous Grassland; BH8 Acid Grassland.
- BH9 Bracken; BH10 Dwarf Shrub Heath; BH11 Fen/Marsh/Swamp; BH12 Bog.
- BH13 Rivers and Streams; BH14 Standing Open Waters and Canals; BH15 Montane; BH16 Inland Rock.
- BH17 Urban; BH18 Supra-littoral Rock; BH19 Supra-littoral Sediment; BH21 Littoral Sediment; BH22 Sea; BH23 Mosaic; BH24–BH31 (additional inland/shoreline habitats as applicable).
- Note: Each BH includes primary/qualifying attributes and guidance for PH allocations where applicable.

## Ponds: Mapping and Condition Survey

- Pond identification: all ponds in each square recorded on CS2007 Pond Mapping Recording Sheet.
- Survey pond: a randomly selected pond per square for detailed condition assessment; selection may change if ponds are added/removed.
- Boundaries and delineation:
  - Boundaries rely on winter water level extents; use vegetation changes and fixed features to delineate.
  - Distinctions among ponds, ditches, flushes, and connected water bodies defined to avoid misclassification.
- Attributes and sampling:
  - Record polygon ID, area, water presence, reasons for loss/creation, notes; survey pond undergoes detailed sampling by freshwater specialists.
- Survey pond selection:
  - Based on preselected pond lists; selection accommodates squares with new ponds, access refusals, or additional ponds.
- Data integration:
  - Pond condition data captured in the field and integrated into CS Surveyor.

## Points, Networks and Linear Features: Methodology

- Points: features under 20 m by 20 m; edit capabilities require scale < 1:5000.
- Lines: linear features under 5 m wide; segments and events edited via Landscape Feature Editing toolbox; mosaics of events supported.
- Line events: record detailed attributes (e.g., fence, hedge, woody features); can copy events between lines.
- Woody Linear Features (WLFs): categorize natural-shape vs hedged/managed forms; belts, clumps, and lines distinguished; handle buffers and gaps explicitly.
- Margins and buffers: record typical 6 m wide margins and canopy/species contributions; buffers noted for relevant woody features.

## Woodland Features and Veteran Trees

- Woodland components accommodate belts, clusters, and lines of trees with attributes (DBH, species, cover, etc.).
- Veteran trees: up to 10 per square (max 2 per species) with detailed attributes (buffer zone, DBH category, health, epiphytic species, ivy cover, canopy status, dead wood, scars, etc.).
- Buffer zones and accessibility of trees are recorded.

## Data Management, Integrity and Access

- Emphasizes metadata, data governance, and public sharing of underlying data.
- Acknowledges barriers to data sharing and metadata completeness; promotes consistent sharing practices to ensure data quality and currency.

## Practical usage and appendices

- Practical guidance for using ArcMap and the CS Surveyor extension; includes helpdesk details, update cycles, and emphasis on frequent saves during editing.
- Appendices cover random pond selection procedures, CS2000 CS theme codes, and field sheets.
- Addresses operational issues such as loops in the dataset and prescribed procedures to remediate corrupted loop data.
- Appendix 5 provides a systematic, species-by-girth-based framework for classifying veteran trees (rules of thumb for aging/veteran status).
- Appendix 6 lists squares with loop features and associated metadata for quality control.

## Data governance, openness, and impact for monitoring authors

- The handbook foregrounds transparent data provenance, metadata completeness, and governance to support reproducible habitat monitoring.
- It acknowledges practical barriers to data sharing and provides workflows to enable accessible, policy-relevant environmental reporting.
- The overall aim is to deliver a comprehensive, digitized, long-term monitoring framework that can inform biodiversity policy and management decisions.