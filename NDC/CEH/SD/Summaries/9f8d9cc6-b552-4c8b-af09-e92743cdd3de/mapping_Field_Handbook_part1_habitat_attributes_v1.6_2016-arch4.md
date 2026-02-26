# GLASTIR MONITORING & EVALUATION PROGRAMME MAPPING FIELD HANDBOOK Part 1: Habitat attributes

## Visit status and survey workflow
- Every Feature (Event, Point, Area) must have a VISIT STATUS: unsurveyed, IN PROGRESS, COMPLETED, or REFUSED ACCESS.
- REFUSED ACCESS marks areas you cannot survey; IN PROGRESS acts as a reminder to finish surveying and add species details later.
- COMPLETED should only be used when the feature is fully surveyed; if you cannot determine extent, continuity, or boundaries, use IN PROGRESS or REFUSED ACCESS.
- When a square is finished, all features should be recorded as COMPLETED or REFUSED ACCESS to indicate full survey status.
- The status influences how the square’s survey progress is tracked and will be visually distinguished in future layers.

## Searching and managing visit status (GIS workflow)
- You can search by VISIT STATUS using three layers: Landscape Points, Landscape Events, Landscape Areas.
- Four status codes to search for: 0 unsurveyed, 1 IN PROGRESS, 2 COMPLETED, 3 REFUSED ACCESS.
- Four main methods, each with pros/cons:
  - Find command (binocular icon): search by a single field (VISIT STATUS) per layer; type 0/1; click features to flash on map; useful for quick checks.
  - Select by Attribute: highlights features across the map; can search for multiple terms but does not produce a list; more complex queries available.
  - Attribute Table: list-based selection; can search by one criterion at a time; useful for working through features in sequence; supports INVERT to find non-completed features if appropriate.
  - Keyboard options and “use unique values” mode to simplify selecting 0–3 values.
- Tips:
  - Keep the Find window open during editing; features disappear from the list as you complete them.
  - Save search criteria for reuse, especially when surveying different parts of a square.
  - Clear selections easily via the clear selection tool.
  - The methods are not all cross-layer; you typically search one layer at a time.

## Dealing with MMUs (Minimum Mapping Units)
- You cannot map any feature smaller than the MMU; very small intrusions into a square should be included in an adjoining polygon.
- If you need to split off a small part of a larger polygon, use UPDATE to merge/split in a single operation rather than creating a new MMU-sized polygon.
- Use a combination of selection tools and Copy + operations to manage geometry across Mastermap and Landscape Areas:
  - Copy + to add areas from other layers.
  - Copy - to remove areas from a selection.
  - If a feature is not on Mastermap, you can still add it by selecting from Landscape Areas and copying into the polygon.
  - For freehand drawing of new areas, treat it as an “add to selection” operation so you can merge with existing polygons without losing data.
- The approach emphasizes maintaining consistent boundaries and attributes while avoiding the creation of MMU-sized, hard-to-manage polygons.

## Ancient and veteran trees: identification guidance
- Definition: Ancient (veteran) trees are old relative to their species; characteristics include large girth, substantial dead wood, and hollow trunks. Dead or non-native trees can also be important habitats.
- Girth-based criteria:
  - A species-specific minimum girth (recorded at 1.3 m height, measured with a girth tape) is used to inform potential ancient status; a detailed table provides species-by-species thresholds.
  - DBH (diameter at breast height) context is noted, with girth thresholds converted to approximate DBH equivalents in the guidance.
- Drawbacks of girth alone:
  - Trees may have large girths due to growth conditions or management (e.g., pollarding) and not be ancient.
  - Some ancient trees may not meet strict girth thresholds but exhibit other indicators.
- Other indicators of ancient trees:
  - Large dead wood in canopy; trunk cavities or hollowing progression.
  - Naturally forming water pools, bark loss, cracking, decay holes, or sap runs.
  - Presence of fungal fruiting bodies, epiphytic plants, and a high interdependent wildlife presence.
  - An overall “old look” and high aesthetic value; potential cultural or historic value; possible pollard form or evidence of past management.
- Practical guidance:
  - Do not rely on girth alone; assess a combination of features to determine ancient status.
  - A table of species-specific maximum girth thresholds is provided to guide “notable” designation; a rule-of-thumb threshold (> 0.5 of the max girth for some species in guidance) helps flag notable ancient trees.
  - The document includes species-specific examples (e.g., for common UK species) to illustrate how girth thresholds map to ancient status.
- The guidance references established sources (FEP handbook, English Nature references) and provides practical measures for field assessment and recording of veteran trees.

## Additional notes relevant to data governance and field data quality
- The VISIT STATUS field supports progress tracking, complete-square verification, and subsequent data analysis across partners.
- The workflow emphasizes consistent boundary delineation and attribute capture within the MMU framework, ensuring longitudinal comparability and better data governance.
- Photographic documentation and historic/cultural considerations are part of broader asset and condition assessments, contributing to richer metadata for data sharing and trend analysis.