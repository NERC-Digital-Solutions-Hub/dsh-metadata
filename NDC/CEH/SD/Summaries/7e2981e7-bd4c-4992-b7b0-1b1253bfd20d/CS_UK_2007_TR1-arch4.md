# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview
- Guides digital field mapping of habitats for CS2007, focusing on habitat extent and change across 1 km squares using a unified GIS-based model.
- Supports UK biodiversity monitoring and policy reporting through time-series data integration.
- Provides a standardized data model and workflow to enable cross-team and cross-network collaboration.

## Data Model and Schema
- Core entities:
  - Areas: polygons representing habitat units with Broad Habitat (BH) and Priority Habitat (PH) attributes; contain one or more Components.
  - Components: subdivisions within an Area carrying primary/secondary attributes (e.g., vegetation type, species, cover).
  - Lines: woody and non-woody linear features with events and attributes per event.
  - Points: discrete features (e.g., trees, ponds) with components and attributes.
- Special focus:
  - Ponds: mandatory mapping of all ponds within a square; a survey pond is selected for detailed condition assessment.
- Classification keys:
  - Vegetation Key: primary/secondary attributes for BHs/PHs based on plant composition.
  - Woodland Types/Features Key: classifies woody vegetation and canopy structure with explicit criteria.
- Data quality controls:
  - MMU (Minimum Mapping Unit) of 1/25 hectare (400 m2); smaller units generally not mapped as Areas.
  - Post-survey masks for PH ranges; changes vs. errors distinguished to maintain consistent baselines.
- Metadata and governance:
  - Detailed attribute schemas, change-tracking, and auditability to support governance reviews and cross-team usage.

## Data Collection Workflow and Tools
- CS Surveyor extension within ArcMap:
  - Enables data capture, change tracking, and on-the-ground validation.
  - Edit sessions: Save Session vs End Session; changes saved only when explicitly saved.
- Editing capabilities:
  - Areas: edit attributes, split/merge areas, modify boundaries, copy attributes.
  - Components: manage multiple components within an Area; attribute updates apply at Area or Component level.
  - Lines: manage line events, copy/edit events, modify geometry, and handle shared nodes.
  - Points: add/move/delete points; manage point components and attributes; record veteran trees and buffers where applicable.
- Line-specific workflows:
  - Create, modify, cut, reshape lines with strict constraints (minimum lengths, no self-crossings, proper handling of shared nodes).
  - Copy features from OS Mastermap or other layers to improve cutting accuracy.
  - Tools to check visit status for linear features and to identify unvisited segments.
- Data integrity emphasis:
  - Prioritize habitat extent and change accuracy over exact coordinates.
  - Require recording of multiple species per habitat polygon (2 minimum, up to 4).

## Pond Mapping and Sampling
- All ponds in every square must be recorded; a Pond Mapping Recording Sheet captures per-pond data.
- Survey pond selection:
  - A pre-selected pond is chosen for detailed sampling; alternatives are available if access or existence changes.
- Pond attributes:
  - Area, water presence, reasons for pond loss/creation, and whether the pond was sampled.
- Guidelines cover pond boundaries, temporary ponds, and distinguishing ponds from other water bodies (ditches, drains, etc.).

## Non-native Species and Woodland Features
- Explicitly lists non-native species to record within habitats.
- Clear definitions for trees, scrub, belts, clumps, and woody linear features; includes modal DBH data for veteran trees.

## Data Governance, Stewardship, and Interoperability
- Standardized CS2007 data model supports cross-team collaboration (policy, ecology, planning) and partner networks.
- Time-series readiness:
  - Camelback for PH/BH outputs supports national biodiversity reporting and action plans.
  - Change-tracking and metadata governance enable ongoing updates and auditability across years and regions (including Wales).
- Data quality controls embedded in workflow (MMU, REAL vs ERROR changes, post-survey masks) to ensure consistent asset management and comparability.
- Documentation of field keys, attribute schemas, and governance around areas/components/lines/points to support governance reviews.

## Challenges and Opportunities
- Challenges:
  - Complex habitat mosaics and boundary ambiguity, especially in unenclosed upland areas; requires robust keys and training.
  - Data gaps due to access restrictions or paywalls in external sources; reliance on field-collected data with clear governance around sources.
  - Maintaining consistency across large, multi-team deployments and long time-series (PH masking, post-survey adjustments).
  - Handling mosaics and rare PHs with GIS masks while balancing detail with mapping practicality.
- Opportunities:
  - Link habitat data with broader networks and governance frameworks to support regional and national biodiversity monitoring and policy needs.
  - Enhanced discoverability and updates through a unified data model and audit trails, enabling scalable usage across partners.

## Practical Takeaways for Data Leaders
- Adopt and enforce the CS2007 data model (Areas, Lines, Points with Components) to enable consistent cross-site analyses and time-series monitoring.
- Use the Vegetation Key and Woodland Types/Features Key to ensure coherent BH/PH classification, especially for woodland and linear features.
- Integrate pond mapping and sampling protocols to establish a robust freshwater data stream aligned with habitat mapping.
- Leverage GIS masks and post-survey adjustments to refine PH extent estimates and ensure comparability over time.
- Establish governance around change management, metadata, and updates to support scalable data use across networks and policy contexts.

## Appendices and Supporting Details
- CS2007 and CS2000 coding schemes, field sheets, and data sheets (including Field Assessment Booklets and older Fieldhandbook references) to support data entry and code mapping.
- Appendix coverage includes:
  - Pond Mapping Recording Sheet structure.
  - Codesheets and universal codes for cross-referencing attributes.
  - Girth-based veteran tree sizing guidelines (Appendix 5).
  - Squares with loops and data integrity considerations (Appendix 6).
- Practical notes on field editing workflows, data integrity checks, and handling of data loops/corrupted event data.