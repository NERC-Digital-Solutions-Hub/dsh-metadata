# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview
- Describes the methodology and digital workflow for CS2007 field mapping of habitats and landscape features within 1 km squares.
- Focuses on reporting habitat change, mapping Broad Habitats (BH) and Priority Habitats (PH), and collecting detailed data in upland unenclosed areas.
- Introduces CS Surveyor, an ArcMap extension, for integrated digital data collection and map editing.

## Data model and classification framework
- Data structures:
  - Areas (polygons) represent habitat units and contain one or more components.
  - Components hold primary and secondary attributes and can be edited, split, merged, or updated.
  - Landscape features include Areas (polygons), Lines (linear features with events), and Points (point features).
  - Minimum mapping unit (MMU) is 0.25 ha; sub-units below MMU are generally not mapped unless edge-case exceptions apply.
- Thematic organization:
  - Attributes organized into Inland Physiography, Inland Water, Coastal features, Agriculture/Natural Vegetation, Forestry, Recreation, Transport, and Structures.
- BH/PH classification:
  - BH provides broad habitat types; PH offers finer, site-specific classes.
  - Enclosed vs unenclosed habitats influence attribute capture; unenclosed habitats may require integration of older CS1990/CS2000 data for detailed vegetation attributes.
- Keys and woodland attributes:
  - Vegetation Key assigns polygons to BH/PH based on species composition and vegetation attributes.
  - Woodland types (belt, line, clump, canopy) and woody features determine BH/PH eligibility.
  - Woodland components may be described at polygon or component level; primary/secondary attributes capture species and cover.

## Habitat descriptions and attribute details
- BH categories (BH1–BH19, BH21, BH22) plus Mosaic cover a wide range of habitats (woodlands, grasslands, bogs, fen, rivers, standing waters, coastal and urban features).
- Orchard guidance and non-specific attributes (bare ground, drainage, scattered trees) are incorporated.
- Detailed attribute structures support consistent data capture across habitat types.

## Ponds, ponds mapping, and survey procedures
- All squares with ponds must be mapped; a CS2007 Pond Mapping Recording Sheet records pond attributes.
- One pond per square is selected as the survey pond for detailed condition surveying.
- Preselected pond lists may be used; random selection is required if new ponds are found or preselected ponds are unavailable.
- Definitions and boundary considerations cover ponds in fen, marsh, bog, and other landscapes; temporary ponds may be included if they hold water for at least four months.
- Post-mapping workflow includes selecting the survey pond and transferring data to freshwater surveyors; ensure all ponds are accounted for before condition assessment.

## Data collection tools and mapping workflow
- CS Surveyor (ArcMap extension) enables data capture for Areas, Lines, and Points with change recording enforcement.
- Emphasis on extent and change over precise spatial location; spatial accuracy adjustable via attribute edits.
- Editing capabilities include split, merge, copy attributes, boundary updates, area updates, and component management.
- Version control and session management: save edits with Save Session; end editing when ready; log off after saving.

## Editing and attribute management
- Areas (polygons)
  - Allocate BH/PH using Vegetation Key; verify accuracy against prior allocations.
  - Classify changes as REAL (genuine habitat change) or ERROR (correction of past data).
  - Record visit status for areas (In progress, Completed, Refused access).
- Components and attributes
  - Each polygon may have multiple components; components can be copied, added, or deleted.
  - Theme structure guides attribute selection during tablet entry.
- Copy, split, and merge operations
  - Copy attributes between polygons/lines/points; split polygons with sketch-based edits; merge areas when attributes are identical.
  - Update areas via combined split/merge when needed; capture reasons for change.

## Points and linear features: data capture rules
- Points
  - Represent discrete features (e.g., trees, ponds); each point must have at least one component.
  - Edited at 1:5000 or finer; buffer zones may be noted; veteran trees limited (e.g., up to 10 per square, depending on species).
  - New points can be created, moved, or deleted with appropriate attribute edits and reasons.
- Woody linear features (WLFs)
  - Include hedges, lines of trees, belts of trees, etc.; classification depends on natural shape.
  - If a line has a natural shape, treat as a woodline; recently managed lines may be hedge-related.
  - If >5 m wide at the base or comprising multiple trees, may be mapped as belt or scrub; margins recorded as attributes.

### WLF Unnatural shape (example data fields)
- Height category (e.g., <1 m, 1–2 m, 2–3 m, >3 m, etc.)
- Base height (canopy base) category
- Species composition (e.g., mixed; >50% hawthorn; >50% other)
- Evidence of management (none, newly planted, cutting, laying/coppicing)
- Line of stumps (Yes/No)
- Vertical gappiness (percentage of breaks from canopy to ground)
- Margin Left and Margin Right (widths or presence)
- Staked trees (Yes/No)
- Tree protectors (Yes/No)
- Note: If any trees exceed natural shape, record as natural instead of unnatural; the page includes illustrative images and coding guidance for WLFs.

## Data quality, change logic, and time-series considerations
- Back-validated 2007 allocations using 1998 CS1990 data, especially for unenclosed upland habitats.
- Post-survey GIS masks delimit PH/BH extents for estimation.
- Surveyors are encouraged to merge, update, and refine polygons to reflect uniform vegetation types; sub-boundaries only when habitat type changes.

## Practical notes for data support teams
- CS Surveyor is new and may have bugs; contact helpdesk for field issues and monitor methodology updates.
- Outputs include habitat extent, change data, and detailed attribute libraries; ensure data products support planning, policy evaluation, and biodiversity reporting.

## ancillary references and resources
- Appendices and field sheets for pond recording; Appendix 4 (random numbers) and Appendix 5 (veteran tree rules) referenced for procedures.
- Detailed guidance notes accompany BH/PH keys and woodland attribute descriptors to aid consistent data capture.
- CS2000/CS1990 references illustrate historical mapping schemas and codes, including themes, parcel numbers, and data recording formats.

## Key emphasis for data support in practice
- Establish a standardized data model that supports integration, cleaning, and re-use across topics and organizations.
- Emphasize data provenance, change reasoning, and traceability through real vs. suspected vs. erroneous changes.
- Provide end-user ready outputs (extent, change data, attribute libraries) that support planning, policy evaluation, and biodiversity reporting.