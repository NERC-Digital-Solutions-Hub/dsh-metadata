# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview
- Provides a fully digital, UK-wide habitat and landscape mapping framework for reporting land cover change and Priority Habitats (PHs) alongside Broad Habitats (BHs).
- Standardizes how habitat extent, change, and PH/BH classifications are captured, stored, and used for policy evaluation.
- Introduces robust data collection workflows, quality controls, and detailed guidance for mapping and attributing features.

## Mapping framework and data model
- Mapping units and data types:
  - Polygons/Areas: Broad and Priority Habitats (BHs/PHs)
  - Lines: Linear features (e.g., hedges, fences, walls)
  - Points: Woody features and discrete elements
- Minimum mapping unit (MMU): 400 m² (1/25 hectare). Smaller patches may be recorded only as lines or points unless MMU is met.
- Habitat types and classification:
  - BHs cover major habitat groups with primary/secondary attributes
  - PHs nested within BHs with detailed attribute rules
  - Non-vegetated elements can be recorded within BH/PH frameworks
- Vegetation and woodland keys support allocation to BHs/PHs and recording woodland components (canopy, DBH, species, cover)

## WLF Unnatural shape (example attribute coding)
- The document provides a detailed schema for Woody Linear Features (WLF), including:
  - Height categories (e.g., <1m, 1-2m, 2-3m, >3m, etc.)
  - Base canopy height, species composition (e.g., mixed species, >50% hawthorn)
  - Evidence of recent management (newly planted, cutting, laying, coppicing)
  - Line of stumps, vertical gappiness, and canopy margins
  - Staked trees and tree protection status
- Instructions emphasize distinguishing natural vs unnatural shapes and applying consistent coding, with example illustrations to guide field assessments.

## Data collection system and workflow
- CS Surveyor (ArcMap extension) used for data capture, attribute editing, and change logging.
- Editing capabilities:
  - Areas, Lines, Points with component-level attributes
  - Create, modify, cut, reshape, copy, delete, and shared-node edits for lines
  - Boundary and feature topology maintained via shared nodes and vertex editing
- Change logging:
  - DistinguishReal change vs. Error correction (REAL vs ERROR)
  - Logging reasons for change to support transparent change assessment

## Change designation and data quality
- Change is categorized as:
  - Real change: genuine habitat/feature change since prior surveys
  - Error change: correction of previous mapping errors
- PH extents may be constrained by GIS masks; emphasis on consistency with UK Biodiversity Action Plans
- Older data (CS1990) integrated with CS2000/CS2007 in unenclosed habitats to enhance PH assignment
- Emphasis on separating ecological change from earlier mapping mistakes and annotating accordingly

## Pond mapping and freshwater focus
- Ponds are fully recorded within each square; a survey pond is selected for detailed condition assessment.
- Recording sheets capture polygon ID, area, water presence, loss/creation reasons, and notes.
- Protocols distinguish ponds from other water bodies (ditches, streams) by boundaries and hydrological behavior.

## Linear features editing and loops
- Detailed line editing procedures include:
  - Creating new lines (minimum 5 m, within square, scale ≤ 1:5000)
  - Modifying lines and shared nodes
  - Cutting, reshaping, and following copied boundaries
  - Copying features from OS layers to refine edits
  - Deleting lines only when all events have valid Change for Reason
- Appendix 6 lists squares with loops; corrupted loop data requires special handling to delete and reinstate lines consistently

## Historical context and codes
- CS2007 builds on CS1990 and CS2000 themes:
  - CS1990 mapped five themes (Agriculture/Natural vegetation, Forestry, Buildings/Structures, Boundaries, Physiography) with no BHs
  - CS2000 expanded to six themes and introduced BV/HB architecture and parcel-based data recording
- Appendix material includes code sheets, code lists, and examples of old vs. new data recording practices (FABs), PH/BH coding, and BAP associations

## Practical guidance for analysts
- Standardized, time-series compatible workflow enables consistent monitoring of environmental condition and policy performance.
- Outputs include reports, maps, and charts; datasets are stored/uploaded to appropriate portals.
- Analysts are encouraged to integrate CS datasets with other data sources to increase their value and accessibility for broader use.
- Key limitations/challenges include maximizing data value through integration and improving data accessibility for users beyond the mapping team.

## Takeaways for environmental monitoring analysts
- CS2007 provides a comprehensive, standardized framework for digital habitat mapping, change detection, and PH/BH classification across the UK.
- It offers detailed attribute schemas (including WLF codes), robust line/area/point editing tools, and explicit data quality protocols.
- The approach supports transparent tracking of habitat extent and change over time, with built-in mechanisms to handle mosaics, PH extents, and pond-focused surveillance.
- Long-term data value hinges on integrating datasets and ensuring broad data accessibility for policy evaluation and environmental health monitoring.