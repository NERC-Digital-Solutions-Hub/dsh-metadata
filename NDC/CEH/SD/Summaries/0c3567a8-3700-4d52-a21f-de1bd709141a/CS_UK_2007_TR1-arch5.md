# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview
- Guides field mapping for Countryside Survey 2007 (CS2007), focusing on habitats, landscape features, and change over time in 1 km squares.
- Introduces CS Surveyor, a digital workflow integrated with ArcMap for standardized data capture, change reporting, and time-series analyses.
- Aims to provide detailed classifications and explicit data entry rules to ensure consistent, reusable data.

## Data model and classification structure
- Core framework centers on Broad Habitats (BH) and Priority Habitats (PH), with polygon-level BH/PH allocation and component-level attributes.
- Vegetation-driven habitat allocation using:
  - Vegetation Key linking composition to BH/PH.
  - Woodland/Features Key guiding classification of woody features (canopy, linearity, extent).
- Detailed BH types listed (e.g., BH1 Broadleaved Mixed and Yew Woodland, BH4 Arable and Horticultural, BH5/6 Neutral Grassland, BH11 Fen/Marsh/Swamp, BH13 Rivers/Streams, BH14 Waters, BH17 Urban, etc.).
- Woodland features subdivided (belt/line/clump/hedgerow trees, etc.) with primary attributes and qualifiers.
- Controlled vocabularies for vegetation & species (e.g., BRC lists) and standardized canopy/species cover proportions.
- Appendices provide standard codes and terminology to support cross-square comparability and time-series analyses.

## Data capture system and workflow
- CS Surveyor: a customised ArcMap extension used to capture and edit features (areas, lines, points) within each 1 km square.
- Workflow emphasizes recording extents and changes (genuine vs. error changes) across polygons, lines, and points.
- Pre-configured data layers and symbology; surveyors log in, select a square, and edit features via the Landscape Feature Editing toolbox (Areas, Lines, Points).
- System enforces change recording and BH/PH attribute consistency.

## Data quality, accuracy, and validation
- Minimum Mapping Unit (MMU): 1/25 hectare; features smaller than this are not mapped unless part of a larger feature.
- Each habitat polygon must have at least two recorded species (up to four) to ensure meaningful vegetation data.
- Spatial accuracy is not the primary focus; emphasis is on extent, change, and correct habitat attribution.
- Mandatory vs. optional fields are flagged; errors in spatial accuracy can be logged via attribute changes.
- Change categories and justification:
  - REAL change: genuine change since 1998.
  - ERROR change: correction of previous misallocations.
  - NEW BASELINE: subdivision of habitat type (e.g., hay meadow vs Neutral grassland).
- Historical data usage:
  - unenclosed habitats use 1990 CS1990 data; enclosed habitats use 1998 data for detail.
- Documentation of change rationale is integrated into editing processes.

## Ponds and water bodies data management
- CS2007 requires mapping all ponds within a square and recording basic attributes on a CS2007 Pond Mapping Recording Sheet.
- A survey pond (for condition assessment) is randomly selected per square from mapped ponds; preselected ponds may be used if present.
- When new ponds are recorded, the pond selection process ensures inclusion in the survey.
- Pond attributes include polygon ID, area (winter max), water presence, reasons for loss/creation, and notes.
- Detailed pond assessment is conducted on the selected survey pond by freshwater surveyors.

## Point and linear features data management
- Point features: elements smaller than 20x20 m; editing includes confirming, updating attributes, or deleting; one point at a time; scale ≤ 1:5000.
- Woody linear features (WLFs): hedges, lines of trees, belts, scrub, etc.; evaluation of natural vs managed shape.
- Line features: events (fences, woody features) with length and event attributes; events must be at least 5 m long.
- Attribute and event copying between features to ensure consistency.
- Margin and buffer data: record presence/absence and dimensions where relevant.
- Line editing tasks (Create, Modify, Cut, Delete, Reshape, Copy) with explicit spatial rules:
  - Lines must be edited at scale ≤ 1:5000; edits restricted to the survey square; minimum line length 5 m; lines cannot cross themselves.
  - Shared nodes allow coordinated edits across connected lines; modifications must preserve topology.
  - Cut and reshape tools allow precise geometric edits with live previews; edit sketches can be refined with vertex tools.
  - Copy features tool enables building edit sketches from existing landscape areas or features.
  - Deleting lines requires valid Reason for Change on all attached events.
- Visit status and quality checks: partially non-trivial process for linear features; unvisited lines highlighted via attribute queries.

## Data governance, provenance, and documentation
- Appendices accompany the handbook for standard coding and terminology (pond codes, field sheets, etc.).
- Vegetation and species data rely on controlled vocabularies and standardized canopy/species proportions.
- Post-survey GIS masks and time-series analyses supported; GIS masks applied after survey to estimate BH/PH extents.
- Non-native species are identified and flagged within habitats.
- Documentation supports data lineage, including habitat keys used, software version, and change rationales (REAL vs. ERROR vs. NEW BASELINE).

## Practical implications for data stewards
- Standardisation: enforce consistent use of BHs, PHs, and woodland keys to ensure cross-square comparability and time-series reliability.
- Metadata and provenance: maintain documentation of keys used, CS Surveyor version, and change rationales; capture lineage of edits (Split, Merge, Copy, Update).
- Data quality controls: enforce MMU rules, mandatory species per polygon, and properly populated change flags.
- Change management: govern REAL vs. ERROR changes and ensure justification is captured for consumers.
- Data governance during updates: use editing tools with clear provenance trails; ensure auditable records for pond mappings and updates.
- Pond data handling: complete pond mapping sheets, auditable survey pond selection, and linking of pond condition data to GIS attributes.
- Accessibility and reuse: GIS-based dataset designed for long-term monitoring and UK habitat reporting; supports policy-relevant analyses.

## Challenges and considerations for data stewards
- Incomplete user needs can affect metadata richness and attribute completeness; balance with standardized schemas.
- Timely data ingestion from field crews is crucial for up-to-date time-series; establish data ingress SLAs.
- Integrating data from diverse field systems and formats (e.g., historical 1990/1998 data) requires harmonisation and thorough documentation.
- Field-system bugs and software updates; maintain helpdesk and fault-logging workflows; monitor methodological updates.
- Fidelity of complex habitat classifications (especially unenclosed upland PH mapping) requires training and clear decision rules.

## Appendices and data integrity notes
- CS2007 pond mapping codes, field sheets, and related documentation are provided to standardise coding and terminology.
- Appendix 5 outlines veteran-tree girth-based relevance rules for selection and interpretation.
- Appendix 6 lists squares with loops and associated data integrity considerations; loops may require special handling to restore data consistency.
- The document includes guidance on CS2000 legacy mappings and how to integrate with CS2007 workflows.