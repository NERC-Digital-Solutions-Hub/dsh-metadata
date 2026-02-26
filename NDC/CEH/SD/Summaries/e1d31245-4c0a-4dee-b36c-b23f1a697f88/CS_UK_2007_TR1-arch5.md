# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview
- Documents digital data collection for the 2007 Countryside Survey, focusing on recording habitats and landscape features across 1 km squares and reporting change.
- Aims to support updates, describe Priority Habitats (PH) and Broad Habitats (BH), and inform UK Biodiversity Action Plans.
- Establishes data governance practices to ensure data can be discovered, reused, and kept up to date.

## Data Model and Structure
- Map elements: Areas (polygons), Lines (linear features), and Points (point features).
- Polygons contain BH or PH attributes; can include multiple components with primary/secondary attributes.
- Woodland features are described via a separate Woodland theme and can be recorded at polygon and component levels.
- Minimum Mapping Unit (MMU) is 1/25 hectare; areas smaller than MMU are not mapped separately unless part of a larger polygon.
- Mosaic mapping used when areas are indistinguishable or below MMU; splits percentages to total 100%.

## Keys and Attribute Systems
- Broad/Priority Habitat Keys assign primary and secondary BH/PH attributes based on vegetation composition.
- Woodland keys classify canopy forms and support BH/PH assignment at various feature levels.
- Habitat descriptions require multiple species records per polygon (minimum 2, maximum 4) with cover percentages.

## Habitat Types and Guidance
- BH types cover a wide range of habitat classes (e.g., broadleaved woodlands, grasslands, heaths, wetlands, aquatic habitats, urban, etc.).
- PH mapping adds priority designations and GIS masks to constrain ranges post-survey.

## Field Mapping System and Workflow
- CS Surveyor: a custom ArcGIS extension used to capture and manage habitat data within ArcMap.
- Workflows:
  - Area edits: manage attributes and components; assess change against baselines (e.g., 1990/1998).
  - Line edits: manage events along lines (e.g., fences, hedges); minimum line length 5 m; handle intersections and splits.
  - Point edits: edit/move/delete point attributes (e.g., trees, ponds).
- Scale constraints: editing areas/lines requires maps at 1:5000 or better; points likewise restricted.
- Change provenance: changes recorded as REAL (genuine) or ERROR (mis-recorded); integrates with legacy baselines and PH updates.

## Ponds and Water Bodies
- CS2007 Pond Mapping requires recording all ponds per square on a Pond Mapping Recording Sheet.
- A survey pond is randomly selected for detailed condition assessment; preselected ponds may be used if valid.
- Boundaries defined using winter water level and vegetation fringes; distinguish ponds from ditches/streams.
- Attributes captured include area, water presence, reason for loss/creation, and notes; ponds enter targeted condition assessments.

## Data Governance and Stewardship Implications
- Standardized data capture across large datasets to ensure consistency, interoperability, and reuse.
- Provenance and versioning embedded in change-tracking (REAL vs ERROR; 1990/1998 data integration; PH baselines).
- Detailed attribute schemas for BHs, PHs, woodland features, and water bodies enable robust metadata, lineage, and auditability.
- Ongoing methodology updates communicated via the system’s Latest News channel.

## Practical Challenges for Data Stewards
- Data completeness and timeliness: ensuring timely input from data creators/sharers and managing updates across habitats/layers.
- Interoperability: complex, standardized keys and evolving guidance require careful governance to maintain consistency.
- Handling large, diverse datasets: mosaics, multi-component polygons, and woodland/water features demand robust governance.
- Documentation of standards: extensive attribute lists and keys require ongoing governance to stay current.

## End-to-End Data Lifecycle
- Data capture: use standardized vegetation keys and BH/PH allocations; GIS-based digitization with MMU constraints.
- Change management: explicit recording of real changes vs corrections; document reasons at area/component levels.
- Data maintenance: regular updates, validation, and potential re-allocations as PHs/BHs or GIS masks change.
- Data publication and sharing: results structured for portal/catalogue sharing with robust metadata and provenance for reuse.

## Legacy and Appendix Context (High-Level)
- References to CS2000 and CS1990 themes and codes illustrate historical mapping contexts and code sheets.
- Appendix-like material provides coding schemes, species lists, and example data structures used to support standardized attribute capture and retrospective interpretation.