# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview
- Describes the Countryside Survey 2007 (CS2007) field mapping methodology for habitat and landscape feature changes, building on CS1990/CS2000.
- Aims to report land cover change by Broad Habitats (BH) and Priority Habitats (PH) with a digital, time-series approach.
- Employs a digital workflow for 1 km squares to support robust biodiversity and land-use monitoring; emphasizes time-series consistency, pond/woodland detail, and co-ownership of data products.

## Data Model and Classifications
- BH taxonomy covers a range of woodland and non-woodland habitats; PHs are nested under BHs where applicable.
- Vegetation keys (for polygon-level allocation) and a Woodland Types/Features key classify woody vegetation (e.g., Belt of Trees, Clump of Trees, Woodland/Forest).
- Habitat attributes include primary/secondary attributes, species/cover data, and habitat-specific qualifiers; component-level attributes enable mosaics within polygons.
- Data are organized into themes such as Inland Physiography, Inland Water, Agriculture/Natural Vegetation Use, Forestry, Structures, and Coastal Features.

## Digital Mapping System and Data Capture
- Uses CS Surveyor extension for ArcMap (customized tools) to capture/edit data; includes pre-set symbology and a Countryside Survey data frame.
- Minimum Mapping Unit (MMU) is 1/25 hectare (≈400 m2); smaller features are not typically mapped separately unless exceptional.
- Data are structured in Areas (polygons), Lines (linear features), and Points (feature points); change recording distinguishes real vs. error changes.
- Governance includes mandatory fields and change reasoning; edits require saving within dedicated editing tools.
- Data quality focuses on habitat extent and change accuracy; includes pond data management as a specialized workflow.

## Pond Mapping and Freshwater Data
- CS2007 Pond Mapping Recording Sheet captures all ponds in a square; one survey pond per square undergoes detailed freshwater condition assessment.
- Ponds defined by size (25 m2 to 2 ha), water presence, duration, and boundary conventions; distinctions made between ponds, ditches, flushes, streams, and dammed waters.
- Post-mapping workflow selects the survey pond and forwards data to freshwater teams for sampling.

## Methodology for Areas, Lines, and Points
- Areas (polygons):
  - Assign appropriate BH/PH using vegetation keys; continuous woodland canopy may be mapped as Woodland BH/PH.
  - Record at least two species per habitat type (up to four).
- Lines (linear features):
  - Width ≤ 5 m: mapped as lines with events (e.g., fence, hedge) or as areas if width exceeds MMU.
  - Line editing includes start/end positions, event management, and options like Copy Attributes, Split, Merge, etc.
- Points:
  - Individual trees, standing water bodies, ponds; points reflect current field observations.
  - Points may have multiple components; veteran trees data captured within limits.
- Woodland attributes:
  - Described with Primary attributes (e.g., Belt of Scrub, Belt of Trees, Woodland/Forest, Clump of Trees) and Secondary qualifiers; canopy and composition recorded (e.g., DBH, species mix).

## Woody Linear Features (WLFs)
- WLFs include hedges, lines of trees, belts, and scrub; categorized as natural-shaped vs managed-shaped.
- Attributes captured along lines: DBH, species, proportion, margin widths, and management indicators (e.g., stakes, windbreaks, fencing).
- Special notes on line structure (e.g., lines of stumps, base height, vertical gappiness, evidence of management) guide data coding.
- Example sections illustrate decisions about natural vs unnatural shapes and variations along the feature.

## Data Governance, Quality, and Change Management
- Change reporting framework:
  - REAL change: landscape change since 1998 allocation.
  - ERROR change: correction where 1998 allocation was wrong and remains wrong.
  - NEW BASELINE: new subdivision of land-cover (e.g., distinguishing upland hay meadow from Neutral grassland).
- Validation:
  - Polygon-level BH/PH accuracy checks; component-level attributes grouped for ease of selection.
  - Mandatory fields and change reasons required; edits saved via Save Session.
- Data integrity:
  - Editing across areas, lines, and points occurs in dedicated editors; scale requirements typically 1:5000 or finer.
  - Copy tools enable integration with external data sources (e.g., OS Mastermap) and controlled governance around model updates.
- Workflow controls:
  - Pre-field planning, field data capture, and post-field reconciliation ensure consistent BH/PH allocations and documentation of rationale.
  - Pond workflow includes selecting survey ponds and coordinating with freshwater specialists.

## Workflow and Processes
- Pre-field planning: establish BH/PH framework, keys, and coding schemes.
- Field data collection: digital capture via CS Surveyor; map all habitat types/features within each 1 km square.
- Post-field processing: reconcile BH/PH allocations with prior surveys; document changes with rationale.
- Pond workflow: complete pond mapping, select survey pond, then pass data to freshwater teams.
- Dissemination and updates: methodological updates and support helpdesk for field issues.

## Challenges and Considerations for Data Leaders
- Complexity of unenclosed upland habitats (PHs) and refined descriptive detail vs earlier methods.
- Achieving consistency across diverse habitats and teams; GIS masks for PHs post-survey may be required.
- Data discoverability and metadata within a multi-theme data model; integrating with external data sources.
- Balancing spatial accuracy with extent accuracy; prioritizing correct extent and change over precise geolocation.
- Managing data governance as data assets evolve and integrate with external datasets.

## Key Takeaways for Data Strategy
- A digitally driven habitat mapping framework with a clear BH/PH taxonomy and woodland typology supports robust, time-series biodiversity monitoring.
- The CS Surveyor workflow enforces consistent data capture, change documentation, and governance across 1 km squares.
- Pond and woodland detail are central, with standardized protocols for pond inventories and wood-related attributes.
- Emphasizes co-ownership of data products, ongoing user feedback, and iterative improvements to align with holistic data-system thinking and inter-organisational collaboration.