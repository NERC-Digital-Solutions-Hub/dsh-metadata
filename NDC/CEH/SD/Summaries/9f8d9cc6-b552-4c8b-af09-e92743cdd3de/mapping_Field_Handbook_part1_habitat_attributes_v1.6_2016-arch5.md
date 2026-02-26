# Visit status

- Purpose and scope
  - Every Event, Point, and Area includes a VISIT STATUS field to indicate survey progress, access restrictions, and data availability for analysis.
  - Statuses help track where surveying is refused, where work is in progress, and where a feature has been fully surveyed.

- Status codes
  - 0 = unsurveyed
  - 1 = IN PROGRESS
  - 2 = COMPLETED
  - 3 = REFUSED ACCESS

- How statuses are used
  - REFUSED ACCESS marks areas with no data due to access restrictions.
  - IN PROGRESS acts as a reminder to complete species assignments or extent judgments across a feature.
  - COMPLETED should only be used when the feature is fully surveyed; if the far end or internal patches are unknown, keep as IN PROGRESS or not completed.
  - When a square is finished, every feature should be recorded as either COMPLETED or REFUSED ACCESS.
  - Statuses underpin layer colour/pattern changes and enable quick identification of survey gaps during analysis.

- Searching and filtering by VISIT STATUS (three methods)
  - FIND command
    - Select layer (Landscape Points, Landscape Events, Landscape Areas) and FIELD (VISIT STATUS).
    - Criteria use numbers (0–3); easy for quick filtering and to flash features on the map.
    - Can keep the Find window open during editing; features disappear from the list as they are updated.
  - SELECT BY ATTRIBUTE
    - Similar principle; allows multi-criteria search and in-map highlighting without a separate list.
    - Can search for multiple terms (e.g., 0 and 1) with OR logic; APPLY updates highlights while keeping the search box open.
    - Not suited for listing all matches; best when you want to visually select features across the map.
  - ATTRIBUTE TABLE
    - Opens a table of features; SHOW SELECTION to focus on selected items.
    - Supports single-criterion searches at a time; can be used in combination with inversion to find non-completed features.
    - Useful when surveying an entire square and you need a concrete list to work through.

- Working with MMUs (Minimum Mapping Units)
  - Do not map features smaller than the MMU.
  - If a small portion intrudes at a square edge, include it with the adjacent polygon.
  - To split/merge polygons without losing data fields, use UPDATE (a combined split/merge operation).
  - Use Copy+ to add to an existing selection from other layers or MasterMap; use Copy- to remove areas from a selection as needed.
  - Freehand drawing can be incorporated as an ADD TO SELECTION operation across layers to maintain correct topology and attributes.

- Ancient trees (guidance overview)
  - Ancient/veteran trees are identified by age-related characteristics, not just size.
  - Key indicators include: large girth for the species, substantial dead wood, hollow trunks, cavities, decay features, bark loss, and presence of epiphytic plants or multiple wildlife associations.
  - Girth measurements (at 1.3 m) are species-specific and paired with qualitative indicators; a tree may be considered ancient when girth thresholds are met in combination with other indicators.
  - Species-specific thresholds and cautions are provided; girth alone is not definitive due to species variation and management practices (e.g., pollarding).

- Data governance and privacy considerations
  - VISIT STATUS supports data privacy and access governance by clearly marking refused-access features and guiding data sharing decisions.
  - Status updates contribute to auditability and reproducibility of survey efforts across squares.