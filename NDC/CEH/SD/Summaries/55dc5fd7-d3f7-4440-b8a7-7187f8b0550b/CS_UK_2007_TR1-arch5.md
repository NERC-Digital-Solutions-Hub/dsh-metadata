# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview and purpose
- Documents Countryside Survey 2007 (CS2007) field mapping methodology for habitats and landscape features within 1 km squares.
- Introduces digital data capture via CS Surveyor integrated with ArcMap to report habitat extent and change, including Broad Habitats (BH) and Priority Habitats (PH).

## Data model and classification
- Habitat framework centers on Broad Habitats (BH) with nested Priority Habitats (PH); classifications cover woodland, boundaries/linear features, arable, grasslands, heath, wetlands, rivers/standing water, rocks, urban, etc.
- Woodland and woody features are defined with primary/secondary attributes; keys determine BH/PH allocations; mosaics and mixed woodland supported.
- Some PH delineations are post-survey or governed by GIS masks to standardize national extent (upland vs lowland, etc.).

## Data capture system and workflow
- CS Surveyor extension (ArcMap-based) enables field editors to view, edit, and attribute point features, linear features, and polygons within a 1 km square.
- Mandatory change recording: editors must distinguish genuine habitat changes from errors.
- Predefined themes organize attributes (e.g., Inland Physiography, Inland Water, Agriculture/Natural Vegetation, Forestry, Structures, etc.).
- Emphasis on habitat extent and change rather than precise geolocation; spatial edits allowed but prioritization is correct habitat representation.

## Polygon (area) data and workflow
- Polygon-level attributes include area, BH/PH designation, BH accuracy, reason for change, and visit status.
- Actions include copying attributes between areas, splitting/merging areas, boundary updates, and adjusting shared nodes.
- Rules govern when a new polygon is created (habitat-type change) versus internal changes (e.g., species composition) that warrant non-boundary updates.

## Species and vegetation data
- For each habitat polygon, record at least two plant species (up to four) to characterize vegetation.
- Species presence and cover recorded in intervals (<10%, 10–25%, 25–50%, 50–75%, 75–95%, 95–100%).
- Non-native species recorded where present (examples listed).

## Ponds and Inland Water data
- Ponds must be identified in every square; mapping uses CS2007 Pond Mapping Recording Sheet.
- Ponds are standing water 25 m² to 2 ha that hold water for at least 4 months.
- Every pond recorded; one pond per square selected as the survey pond for detailed condition assessment by freshwater surveyors.
- Preselected survey ponds used if present; otherwise a random selection with documented justification if re-selection occurs.
- Guidance covers identifying temporary ponds, distinguishing ponds from ditches, and boundary delineation for connected ponds.

## Points and lines features editing
- Point features: trees, shrubs, ponds, and other landscape elements; points edited one at a time with mandatory attributes.
- Line features: woody linear features, hedges, fences, walls, etc.; events along lines require detailed attribute editing; lines may be split, merged, or updated.
- Includes margin, buffer, and use-code entries across themes; lines edited at scale 1:5000 or smaller; shared nodes and topology management are emphasized.

## Data quality, validation, and governance
- A publishing-like mindset emphasizes consistent standards, metadata, data lineage, and version-controlled edits.
- Updates are published in Latest News for surveyors; acknowledges potential system bugs with helpdesk contacts.
- Spatial accuracy is secondary to accurate habitat representation; spatial edits are documented as attribute changes when needed.

## Practical considerations and challenges
- Key challenges include incomplete understanding of user needs, timely data delivery from data creators, achieving metadata/standard-compliant metadata across diverse systems and formats, and handling large datasets with legacy constraints.
- Post-survey GIS masks delineate upland vs lowland PH extents; certain BH/PH delineations rely on floristic keys and post-processing.

## End-to-end data lifecycle
- From square-level data capture (polygon/line/point attributes) to pond-specific condition data, through to post-survey GIS processing and BH/PH assignments.
- Documentation supports auditing, change detection, and reproducibility across survey cycles.

## Key user guidance and support
- Step-by-step instructions for editing areas, copying attributes, splitting/merging areas, and updating lines/points.
- Guidance on recording buffer zones, margins, and the broad set of attribute categories required for each habitat type.
- Clear rules for when to create new polygons, how to handle mosaics, and how to document genuine vs error changes.

## Appendices and related materials (overview)
- Detailed field assessment examples and editing workflows (e.g., WLF Unnatural/Natural shapes) including line editing tasks: create/modify/cut/reshape lines, shared node modifications, and copy tools.
- Procedures for handling loops and data integrity issues in line events.
- Pond Mapping Recording Sheet structure and instructions.
- References to CS2000/CS1990 themes and codes, providing historical context and codesheets.
- Annexes on veteran-tree girth assessment and other specialised data (e.g., loop squares) for advanced users.

## Governance and contact points
- The document is produced under NERC/CEH with Defra partnership support; includes guidance on metadata, data lineage, and version-controlled edits.
- Contact points and resources provided for data governance and data use within Countryside Survey.