# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview
- Guidance for Countryside Survey 2007 (CS2007) mapping to document habitat extent and change using digital GIS data.
- Focus on Broad Habitats (BH) and Priority Habitats (PH) across squares, including upland unenclosed and enclosed lowland habitats; Wales scope; time-series reporting.
- Transition to digital data collection with a single digital map per 1 km square; emphasis on habitat extent and change validation with earlier surveys for consistency with biodiversity reporting.

## Data Model and Classification
- Core structure with two main classification layers:
  - Broad Habitats (BH) 1–19, plus Mosaic option; PH nested within BHs where applicable.
  - New PHs introduced for CS2007.
- Keys and attributes:
  - Vegetation Key: assigns primary/secondary habitat attributes from vegetation composition.
  - Woodland Key: classifies woody vegetation types and informs BH/PH attribution (e.g., woodland belts, clumps, lines).
- Thematic attributes (examples): Vegetation, Inland Physiography, Inland Water, Structures, Forestry, Agriculture/Natural Vegetation, Coastal features.
- Habitat descriptions:
  - BHs specify dominant vegetation, indicators, and context (e.g., various grasslands, bogs, rivers, urban areas).
  - PHs nested within BHs with detailed floristic/indicator rules.
- Woodland specifics:
  - BH1 Broadleaved Mixed and Yew Woodland; BH2 Coniferous Woodland; management and structure captured as primary attributes with qualifiers (Parkland, Understorey, etc.).
- Data capture rules:
  - Mandatory/optional attributes per habitat; typically record 2–4 species per polygon; polygons represent uniform habitat units above a minimum mapping unit (MMU).

## The CS Surveyor GIS System
- Platform: CS Surveyor extension integrated into ArcMap (ESRI components).
- Access and workflow:
  - Login, select square to edit, use Landscape Feature Editing toolbox for Areas (polygons), Lines (linear features), Points (point features).
  - Emphasis on repeated checks, attribute verification, and recording change against mapped features.
- Scale and editing:
  - Point edits require 1:5000 or finer; area/line/polygon edits follow similar scale requirements.
  - Spatial accuracy is not primary; focus on correct habitat representation and change metadata.

## Mapping Units, Scales and Change
- Minimum Mapping Unit (MMU):
  - Minimum polygon size 1/25 hectare (400 m2); smaller features not mapped as polygons unless edge of larger polygon or significant linear/point element.
- Change and baselines:
  - Change denotes genuine ecological change since last survey; ERROR changes correct mis-allocations from previous data.
  - REAL vs ERROR changes are crucial for unenclosed habitats when updating vegetation information.
- Post-survey masks:
  - GIS masks applied post-survey to delimit PHs and to refine country-wide extent estimates (upland vs lowland BH delineations).

## Area-based Workflow (Polygons)
- Polygon-level attributes:
  - BH/PH assignment (via vegetation key and habitat guidance).
  - Accuracy indicators for BH assignment.
  - Change status and visit status (In progress, Completed, Refused access).
- Component-level attributes:
  - Areas may contain multiple components with shared/distinct primary attributes; components can be added/copied/deleted.
  - Thematic grouping (Physiography, Inland Water, Agriculture/Natural Vegetation, Forestry, etc.) to streamline attribute selection.
- Editing operations:
  - Copy Area: copy attributes to multiple targets.
  - Split Areas: digitise splits; larger-than-MMU areas yield separate polygons; sub-MMU splits flagged.
  - Merge Areas: combine polygons with identical attributes; merged polygon inherits source attributes.
  - Modify Area: adjust boundary geometry; manage shared nodes/topology.
  - Update Areas: create new polygons by splitting/merging; may replace several areas.
- Best practices:
  - For woodland, map continuous canopy as woodland BH/PH; use belts/clumps/lines for woody features as appropriate.
  - Record at least two plant species per habitat polygon (max four); document species cover percentages.

## Point Features
- Point-level attributes:
  - Trees, standing water bodies, ponds, and other features recorded as points; points may have multiple components.
  - Buffer zones around features (ownership/protection) recorded as Yes/No.
- Veteran trees:
  - Up to 2 veteran trees per species per square; record DBH, morphology, health, epiphytic species, etc.
- Point editing:
  - Create Point, Move Point, Delete Point, Copy Point Attributes.
  - Points must be added at or below 1:5000 scale; not within 5 m of another point.
  - Points are stored with components and editable similarly to areas.

## Linear Features and Events
- Linear features:
  - Map features less than 5 m wide but requiring mapping; minimum length 20 m; may include multiple events (fence, hedge, woodland along length).
  - When a linear feature expands to form an area, map as BH3 (Boundaries and Linear Features).
- Events:
  - Each line stores events with attributes (e.g., fence type, height, condition, margin details).
  - Edits via Lines tool; events can be added, copied, deleted, or modified.
  - Event length/position controlled via map/attribute editor; mandatory fields apply.
- Margins:
  - Margins around hedges/linear features recorded (typical widths ~6 m); margins stored as separate attributes.

## Pond Mapping and Survey
- Pond definition:
  - Standing water 25 m2 to 2 ha, persisting for at least four months; temporary ponds may be dry during survey.
- Recording ponds:
  - All ponds in a square recorded on CS2007 Pond Mapping Recording Sheet.
  - A single pond per square chosen as the survey pond for detailed condition assessment (via Surveyor).
  - Preselected ponds may be used if present; random selection for new ponds or unsuitable preselected ponds.
- Boundaries and connections:
  - Boundaries defined by basins, waterlines, or slope breaks; connected ponds may affect pond status.

## Special Habitat and Woodland Details
- BH1 Broadleaved Mixed and Yew Woodland: includes beech, yew, mixed deciduous mosaics; parkland considerations noted.
- BH2 Coniferous Woodland: native pine woodland; coniferous plantations documented with primary/secondary attributes.
- BH3 Boundaries and Linear Features: large/narrow linear features mapped as areas if width > 5 m; else as Lines with events.
- BH4–BH8 and beyond: Arable/Horticultural, Improved Grassland, Neutral/Calcareous/Acid Grasslands; associated qualifiers (Ley, Mown, Setaside) and margins.
- Other BHs and related features: rivers/streams, standing waters, urban areas, coastline/sea features, mosaics, and related mask/post-survey adjustments.
- Non-native species:
  - List of non-native shrubs/species to watch for/record as qualifiers within habitats.

## Practical Notes for GIS Practitioners
- Data quality and governance:
  - Change management central; populate Reason for Change and BH accuracy fields when editing.
  - Maintain audit trail of area-level and component-level changes (REAL vs ERROR changes).
- Data integration:
  - BH/PH assignments informed by Vegetation Key and Woodland Key; cross-reference CS1990/CS1998/CS2000 to support change validation.
- Documentation and support:
  - CS Surveyor includes helpdesk contacts and wiki fault-logging; methodology updated via Latest News.
- Outputs and reporting:
  - Time-series reporting of Broad and Priority Habitats; masks applied post-survey to refine extent estimates.
- Field procedures:
  - Pond boundaries delineated carefully; adhere to CS2007 Pond Mapping Recording Sheet.

## Field Editing Procedures and Examples (Illustrative)
- Line editing tasks:
  - Create Line: draw new lines at 1:5000 or finer; minimum length 5 m; lines cannot cross themselves; new line starts with an Unsurveyed/Missing Data event.
  - Modify Line: edit vertices; manage shared end nodes via Shared Nodes; preserve topology and avoid invalid intersections.
  - Cut Line: define cut polygon to remove a segment; view length to be cut and length remaining; cuts must meet minimum length.
  - Copy Tool: use existing landscape areas as references to construct accurate cut-line sketches from multiple features.
  - Delete/Reshape: delete with valid Reason for Change; reshape to align with field features; ensure shared boundaries/topology remain consistent.
- Shared nodes and topology:
  - Shared nodes between lines require careful modification to avoid invalid intersections; edits performed through Shared Node Modify.
- Visit/status management:
  - Use attribute-based queries to identify unvisited linear features; blue highlighting indicates unvisited lines for follow-up.
- Ponds data collection:
  - Complete pond mapping forms per square; select survey pond for detailed assessment;boundary decisions rely on basins/waterlines.

## Legacy Data Context (CS1990/CS2000)
- CS1990 (older mapping):
  - Five themes; no BH mapping; feature records used single parcel-based sheets with coded attributes.
  - Change documentation used universal code values to indicate genuine changes or mis-recordings.
- CS2000:
  - Six themes; mapping included parcel-based codes for attributes; data sheets correspond to mapped features with coded attributes and species data.
- Cross-referencing:
  - CS2007 integrates/updates prior datasets; practitioners should cross-check with CS1990/CS1998/CS2000 to validate changes.

Appendix references (CS2007 related items)
- Pond Mapping Recording Sheet structure and selection of survey pond.
- WLF (Woodland/Line features) coding and imaging guidance.
- Veteran tree girth guidelines (Appendix 5) and square loop notes (Appendix 6) for data integrity.

Outputs and reporting emphasize time-series habitat extents and changes, supported by post-survey masks and robust change management to ensure data quality for GIS-driven map-based products.