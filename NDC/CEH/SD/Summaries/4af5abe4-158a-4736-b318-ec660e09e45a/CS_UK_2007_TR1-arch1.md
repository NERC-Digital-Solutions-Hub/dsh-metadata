# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview and Aim
- Document the field mapping framework used in Countryside Survey 2007 (CS2007) to record land cover change, Broad Habitats (BH) and Priority Habitats (PH) at country and UK scales.
- Introduces a GIS-based workflow (CS Surveyor in ArcMap) for polygonal habitats, woody features, linear features, and points with strict data quality and change-detection requirements.
- Emphasizes repeatable baseline data, clear change classifications, and traceability of data sources.

## Data Model

- Features and data units
  - Areas (polygons): map habitat types; primary BH/PH allocation; component-level attributes.
  - Lines (linear features): woody linear features, hedges, walls, fences; recorded as events along lines; support edits like splits/merges.
  - Points (points): individual trees, shrubs, ponds, water features; components editable or copyable.
- Broad Habitats (BH) and Priority Habitats (PH)
  - BHs classify broad vegetation/landscape types; PHs nested within BHs where applicable; PH mapping post-survey with GIS masks.
- Vegetation and woodland keys
  - Vegetation Key assigns primary/secondary habitat attributes by species composition and canopy structure.
  - Woodland Types/Features differentiate belts, clumps, lines, and mosaics; enables multiple primary attributes per polygon.
- Thematic attributes
  - Agriculture/Natural Vegetation, Inland Physiography, Inland Water, Structures, Forestry Features, Recreation, Transport, Coastal features.
  - Explicit handling of non-native species and orchards.

## Mapping System and Workflow

- Digital platform and workflow
  - CS Surveyor (ArcMap extension) for viewing/editing points, lines, and areas with preset symbology.
  - User access, fault reporting, and data-frame conventions.
- Editing framework and MMU
  - Minimum Mappable Unit (MMU) for areas: 1/25 ha (400 m²); areas below MMU typically not mapped unless part of a larger unit.
  - Change handling: REAL change, ERROR change, or NEW BASELINE PH allocation with explicit justification.
  - Spatial editing capabilities: copy attributes, split/merge boundaries, and update areas via sketches or copied features.

## Woodland Landscape Features (WLF)

- Key attributes and coding guidance
  - Unnatural shape or line of stumps; base height; height categories; species composition (e.g., >50% hawthorn or other).
  - Evidence of recent management: newly planted, cutting (<3 years), laying or coppicing (<5 years), or both.
  - Line of stumps: yes/no; vertical gappiness (percent of breaks from canopy to ground) with defined ranges.
  - Margins (left/right), presence and width; staked trees; tree protectors.
  - Notes on natural vs. unnatural shape: if >2 m base height, ensure woody species are cut/trimmed to avoid unnatural shapes; record natural shape if applicable.
- Visual aids
  - Illustrative images accompany the section to aid coding decisions.

## Line Editing Tasks and Procedures

- Create New Line
  - Lines must be created within the survey square at scale ≤ 1:5000; minimum length 5 m; cannot cross itself; new line starts with a single Unsurveyed/Missing Data event.
- Modify Line
  - Extend/contract lines via vertex editing; add/delete/move vertices; shared boundary endpoints edited via Shared Node Modify; ensure topology remains valid.
- Shared Nodes
  - Modify shared nodes carefully to move adjoining lines; ensure edits do not create intersections with other lines.
- Cut Line
  - Use a cut polygon along the line to delete a segment; visualize cut length and remaining length; edits constrained to avoid invalid geometries.
- Copy Tool
  - Use features from other layers (e.g., OS Mastermap) to sketch accurate cuts; supports combining multiple features into an edit sketch.
- Delete Line
  - Deletes allowed only if all events have a valid Reason for Change; scale constraint applies.
- Reshape Line 1 and Reshape Line 2
  - Reshape lines by drawing a reshape graphic that intersects the start and end points of the target line; preserve topology; ensure minimum feature length is maintained.
- Checking Visit Status
  - Use Select By Attributes to identify unvisited landscape events; unvisited lines highlighted; procedures are provided for looped (corrupted) event data to be resolved by deleting and reinstating the feature.

## Pond Mapping (CS2007)

- Pond mapping and survey pond selection
  - All ponds in a square are identified; basic attributes recorded on the CS2007 Pond Mapping Recording Sheet.
  - One pond per square selected for detailed condition assessment (survey pond); preselected ponds listed on tablets; random selection used if necessary.
  - Data fields include polygon ID, area, water presence, loss/creation reasons, and notes.
- Pond definitions and boundaries
  - Pond: standing water 25 m² to 2 ha, typically water-filled for at least four months; boundary definitions may extend beyond the current water area.
  - Temporary ponds identified by wetland indicators (vegetation, waterlines); boundary distinctions include ditches, dammed streams, and connected ponds.
- Workflow
  - After mapping all ponds, select the survey pond for freshwater condition assessment.

## Practical Habitat and Woodland Detail Guidelines

- Habitat mapping specifics
  - Vegetation Key usage to map patches to BHs/PHs with attention to canopy cover, dominance, and species composition.
  - Woodland classifications emphasize canopy structure, belt width, clumps, lines, and mosaics; recording of secondary attributes.
- Management and ecosystem features
  - Documentation of management indicators (grazing, fencing, regeneration, windthrow, pollarding) within forestry-focused attributes.
- Orchards and woodland variants
  - Special notes for orchard recording; distinctions among beech/oak/mixed woodlands and upland/lowland distributions with relevant community references.

## Data Quality, Accessibility, and Outputs

- Data quality and reliability
  - Emphasis on distinguishing genuine ecological change from prior-data errors; integration of CS1990/CS2000 data to improve attribute accuracy.
  - Acknowledges potential CS Surveyor bugs and provides support channels.
- Scale and scope
  - Aims for country- and UK-level reporting of BHs and PHs; detailed, disaggregated habitat data support scientific analyses and policy.
  - Post-survey GIS masks used to estimate habitat extent; new PH classifications added when needed.
- Outputs, metadata, and reuse
  - Data products organized around BH/PH, woodland types, and other habitat attributes; metadata and provenance tracked via change reasons and source attribution.
  - Strategies discussed for making data discoverable and reusable to support reproducible analyses and model development.

## Challenges and Considerations for Analysts

- Right-scale data gaps
  - Addressed via granular, standardized digital workflows and explicit change-detection rules.
- Access to diverse data sources
  - Integrated CS Surveyor system consolidates terrain, vegetation, and habitat data across themes to reduce cross-system data wrangling.
- Standardization and interoperability
  - Structured keys, explicit attribute logic, and MMU rules enable cross-square comparability and trend analyses.
- Documentation and traceability
  - Detailed changeReason fields, component-level editing, and audit trails support robust data quality checks and reproducible analyses.

## Reference and Support

- User support
  - CS Surveyor helpdesk and a wiki-based fault logging process.
- Supplementary materials
  - CS2007 Pond Mapping Recording Sheet; Appendix references; field keys and extensive habitat attribute guidance.
- Historical context
  - References to CS2000 and CS1990 mapping themes and code frameworks; transition to BH/PH-based framework in CS2007.