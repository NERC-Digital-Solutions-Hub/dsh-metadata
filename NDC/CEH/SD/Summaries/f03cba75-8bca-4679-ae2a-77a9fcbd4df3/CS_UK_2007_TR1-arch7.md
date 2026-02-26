# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview and aims
- Provides a GIS-based method to map habitats, landscape features, and change across 1 km squares for national field surveys.
- Facilitates reporting by Broad Habitats (BH) and Priority Habitats (PH), with time-series capabilities and cross-country consistency.
- Emphasizes ground-truthing, change detection since baseline surveys, and clear presentation of spatial features in map formats.

## Data model and mapping approach
- Habitats mapped as BHs (broad categories) and PHs (finer-scale types); PHs may nest within BHs.
- Minimum mapping unit (MMU) rules govern when a feature is mapped; mosaics used when precise delimitation is not possible.
- Spatial data combines themes (e.g., forestry, agriculture/vegetation, boundaries, structures, physiography) into a single digital map; components may be polygons, lines, or points.
- Emphasis on extent and change rather than exact spatial accuracy; components and attributes reflect ground truth.

## GIS system and editing environment (CS Surveyor)
- CS Surveyor integrates with ArcMap, operating within a Countryside Survey data frame with pre-set symbology.
- Editing sessions are managed via the Landscape Feature Editing toolbox with separate tabs for Areas (polygons), Lines, and Points.
- Regular saves and session management are essential; accuracy of attributes and extents is prioritized over pixel-level geometry.

## Editing workflows

### Polygon (Area) editing
- Key attributes at polygon level: Area, Broad/PH habitat, BH accuracy, reason for change (Error vs Real), visit status (In progress, Completed, Refused access).
- Determining change: options include no change to 1998 allocation, real change since 1998, error correction of 1998 data, or a new PH baseline.
- Component-level attributes: polygons may consist of multiple components with thematic groupings (Physiography, Inland Water, etc.); components can be added, copied, or deleted.
- Mapping rules: continuous woodland maps to BH/PH with woodland attributes; MMU rules apply; changes in primary habitat require new polygon; species composition changes within the same habitat may not require a new polygon.

### Line editing
- Create Line: map scale must be 1:5000 or finer; lines must be 5.0 m minimum; lines cannot cross; intersections split lines; new line starts with an Unsurveyed/Missing Data event.
- Modify Line: edit vertex positions, add/delete/move vertices; end-point shared boundaries require Shared Node Modify; topology constraints apply (no new intersections among revised lines).
- Shared Nodes: modify intersection points where multiple lines meet; careful selection and movement propagate to connected lines.
- Cut Line: delineate cut segments along a line using a cut polygon; the length to be cut is highlighted; large edits may require multiple cuts.
- Reshape Line: redraw along existing lines using reshape graphics; ensure edits produce the desired final shape without violating minimum length constraints.
- Copy Tool: import existing features from other layers (e.g., OS MasterMap) to guide line edits; build edit sketches with multiple features before finalizing cuts.
- Deletion: lines with valid Reasons for Change may be deleted one at a time; lines with invalid reasons cannot be deleted.
- Checks and constraints: minimum linear feature length; shared endpoints and topology restrictions; line edits must not create invalid intersections.

### Point features and woody linear features
- Points: attributes cover discrete features such as trees, standing water, veteran trees; points may have multiple components; buffers and protection measures recorded.
- Veteran trees: up to 10 per square, max 2 per species; DBH and epiphytic details recorded for vetting.
- Woody Linear Features (WLFs): natural lines of trees or hedges; attributes include modal DBH, species composition, evidence of historic management, margins, staked trees, and tree protectors.
- Line events: capture management along lines (fences, hedges, changes) and must be 5 m or longer; lengths are editable on the map.

## Ponds and water features
- All ponds in a square are recorded on a CS2007 Pond Mapping Recording Sheet; one pond per square is selected as the detailed survey pond (random selection with preselected options available on the tablet).
- Pond boundaries rely on winter water level, delineation, and vegetation signals; temporary ponds may be recorded if they hold water for at least four months.
- After mapping, ponds are subject to detailed freshwater condition surveys by specialists.

## Habitats: Broad Habitats and Priority Habitats
- BH categories cover broad vegetation/landscape types (e.g., woodland types, arable, grasslands, wetlands, uplands, urban, coastal).
- PHs provide finer-scale habitat types within or across BHs; PH extents can be constrained by post-survey GIS masks.
- Mosaic polygons are used when precise delimitation is not possible; each mosaic component has a primary attribute and a cover percentage totaling 100%.

## Orchards and non-native species
- Non-native species are recorded where they occur within habitats.
- Orchards have special handling; they may belong to PH or be recorded as Orchard (Agriculture/Crops) or Gardens/Ground with trees depending on location and management.

## Appendices and practical guidance
- References to older field assessment resources (FABs) and CS2000/CS1990 mapping practices; guidance on field sheets, codes, and documentation.
- Pond Mapping Recording Sheet details and instructions for pond selection and reporting.
- CS2000 and PH/BH coding guidance, code sheets, and example datasets to aid consistent classification and data entry.

## Practical tips for GIS specialists
- Prioritize accurate habitat attribute assignment and change classification to support UK Biodiversity Action Plan reporting; ensure PHs are captured where relevant.
- Use vegetation and woodland keys to quickly classify areas; base BH/PH decisions on canopy cover, species composition, and woody feature context.
- Maintain data quality with a clear log of real changes vs. errors; document reasons for changes.
- Apply MMU and mosaic rules to handle complex landscapes and mosaics, especially in upland unenclosed habitats.
- Regularly back up edits, validate polygon boundaries against ground truth, and annotate spatial accuracy caveats within attributes.

## Data quality, issues, and governance
- Loops and data integrity: Appendix 6 lists loops in the dataset; specific procedures address loop corruption, including deletion of faulty events and reintegration of correctly edited lines.
- The handbook emphasizes transparent change management, traceability of edits, and adherence to predefined codes and attribute schemas.
- The document reflects a collaborative, multi-agency effort (CS 2007) and is intended to support standardized, map-based biodiversity reporting.