# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview
- Guidelines for field-mapping habitats and landscape features across 1km squares using a digital GIS/ArcMap workflow.
- Aims to report land cover change by Broad Habitats (BH) and Priority Habitats (PH) with enhanced detail for unenclosed upland habitats.
- Data are collected digitally (CS Surveyor) and edited within ArcMap to support biodiversity monitoring at national and UK scales.

## Data model and classification
- Core structure:
  - Polygons: BH or PH at polygon level.
  - Components: detailed attributes per eligible themes (physiography, vegetation, forestry, agriculture, etc.).
  - MMU: minimum mappable unit of 1/25 ha (400 m2); smaller fragments become lines unless part of a larger unit.
- Keys and allocations:
  - Vegetation Key: assigns BH/PH based on species composition and habitat indicators.
  - Key to Woodland Types/Features: classifies woody vegetation (woodland, belts, clumps, lines, etc.) using canopy/structure criteria.
- Habitat scope:
  - BH includes various woodland, grasslands, HEATH/PEAT, rivers/standing waters, urban, coastal, mosaic blends, etc.
  - PHs nest within BHs and are delineated post-survey using GIS masks to separate upland/lowland.
- Enclosed vs unenclosed:
  - Enclosed habitats editable within the 1998 framework; PHs may be newly attributed within existing BHs.
  - Unenclosed habitats include more detailed vegetation/species attributes; older datasets (CS1990/CS2000) often amalgamated for PHs.

## Data capture system and workflow
- CS Surveyor extension in ArcMap:
  - Built atop ArcMap; provides tools to view/edit point, line, and area features within a 1km square.
  - User login, audit trail, and issue reporting via helpdesk/wiki.
- Editing workflow:
  - Edit sessions: Edit → Landscape Feature Editing toolbox; work on Areas, Lines, or Points without leaving the session.
  - Saving and End Session options; data integrity focuses on accurate habitat/attribute representation.
  - Change status distinguishes REAL ecological changes from historical data errors (REAL vs ERROR).
- Recording and change management:
  - For unenclosed habitats, use 1990 CS data where applicable; for enclosed habitats, update with 1998 data as needed.
  - Each polygon records primary habitat and relevant primary/secondary attributes; include reason-for-change fields.

## Vegetation and woodland attributes
- Vegetation Key (allocations and attributes):
  - Based on plant composition, canopy cover, and related indicators; includes detailed NVC associations (e.g., W12–W15; W1–W7 subcommunities).
  - Guidance on classifying woody features (woodland, belts, clumps, lines) and PH/BH allocations.
- Key to Woodland Types/Features:
  - Distinguishes canopy, belts, clumps, woody linear features, and individual trees.
  - Rules for treating features as belts/lines/woodland; recording requirements include species, cover, DBH, and ancillary wood features (fences, regeneration, etc.).
- Data fields and attributes:
  - Polygon-level: BH or PH allocation.
  - Component-level: primary/secondary attributes, qualifiers, and species composition.
  - Species and cover: up to 4 species per polygon/component; cover categories (<10% to 95–100%).
  - Modal DBH: categories (<3 cm to >75 cm) for trees; used with species attributes.
- Non-native species:
  - Record presence of specified non-native species within habitats as supporting attributes.

## Arable and other open-habitat habitats (BHs)
- BH4 Arable/Horticultural; BH5 Improved Grassland; BH6 Neutral Grassland; BH7 Calcareous Grassland; BH8 Acid Grassland; BH9 Bracken; BH10 Dwarf Shrub Heath; BH11 Fen/Marsh/Swamp; BH12 Bog; BH13 Rivers/Streams; BH14 Standing Open Waters/Canals; BH15 Montane; BH16 Inland Rock; BH17 Urban; BH18/19 Supra-littoral; BH21 Littoral Sediment; BH22 Sea; BH23 Mosaic.
- Each BH has primary attributes and indicators tailored to its habitat type (e.g., margins, crops, grasses, indicator species, management qualifiers).

## Pond mapping and water features
- Ponds are a central feature; every pond in a square must be identified and described on the CS2007 Pond Mapping Recording Sheet.
- Definitions:
  - Pond: standing water 25 m2 to 2 ha, typically present for at least 4 months/year.
  - Temporary ponds may be dry at survey but recorded if seasonally wet.
- Survey design:
  - All ponds mapped; one pond per square chosen for detailed condition assessment (survey pond).
  - Preselected ponds used when possible; random selection via a random-number table if needed.
  - Pond attributes include area, water status, reasons for loss/creation, drivers (fishing, wildlife, golf, etc.).
- Conditions survey:
  - Survey pond sampled for plants, environment, and water chemistry.

## Points and lines: attributes and editing
- Points (trees, water features, ponds, etc.):
  - Added/moved/deleted with scale requirement (1:5000 or less); can have multiple components.
  - Tree/shrub features recorded with species, proportion, DBH, and buffer status; some points may represent multiple trees.
- Linear features:
  - Linear features: >20 m long and <5 m wide; include events (fences, hedges, ditches).
  - If line area exceeds MMU, map as an area (BH3) rather than a line.
  - Events edited individually; supports new lines, splits, merges, and copies.
  - Margins and hedgerows have dedicated attribute fields (height, margins, width, species).
- Woody linear features:
  - Distinguish natural lines of trees from hedges; record modal DBH and species composition.
  - Up to 10 veteran trees per square (max 2 per species) with detailed attributes.

## Data quality, change, and governance
- Emphasis on accurate habitat type/extent over precise spatial geometry.
- Change coding:
  - REAL change: genuine ecological change since last survey (1998/1990 data considered).
  - ERROR change: correction of previous misclassification.
  - New PH: subdivision or reclassification to a new PH within an existing BH.
- Reporting and feedback:
  - Outputs include self-serve data access and dashboards; outputs are refined via stakeholder feedback.
  - Focus on change detection and PH/BH allocations; spatial precision is secondary to correct habitat representation.

## Appendix highlights (conceptual)
- Field codes, pond sheets, and tables for random pond selection, vegetation indicators, and field-recording conventions.
- Guidance on harmonizing historic datasets (CS1990, CS2000) with the 2007 methodology for improved attribution and change detection.

## Practical implications for data support
- Integration and data merging:
  - Combine CS1990, CS2000, and CS2007 datasets to support PH/BH mapping and change analysis.
- Data quality assurance:
  - Implement validation for polygon/attribute consistency, MMU compliance, and reason-for-change fields.
- Data products:
  - Topic-specific dashboards and reports showing habitat extents, changes, and PH allocations; drill-down by square, habitat type, and feature type.
- Data governance:
  - Maintain thorough documentation of attribute schemas, codes, and hierarchies; track edits and changes through CS Surveyor workflows.

## Practical notes for data teams
- Expect multiple data formats and legacy datasets; plan integration strategies across CS1990/CS2000/CS2007.
- Prioritize semantic accuracy of habitat class and changes over pixel-perfect geometry.
- Leverage the detailed appendices and field sheets to support consistent, auditable data capture and change histories.