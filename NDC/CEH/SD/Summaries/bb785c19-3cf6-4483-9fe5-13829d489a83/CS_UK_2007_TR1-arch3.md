# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview of Woody Linear Features (WLF) Data
- Unnatural shape and Line of stumps indicators are recorded, including height categories for the base canopy and overall height.
- Height categories include: <1m, 1-2m, 2-3m, >3m, 3-4m, 4-6m, >6m; base height <2m or >2m.
- Species composition flags: mixed species or dominance (e.g., >50% hawthorn or >50% other species).
- Evidence of management: none, newly planted, cutting (e.g., flail or saw <3 years), laying or coppicing (<5 years), or both.
- Line of stumps: recorded as Yes/No.
- Vertical gappiness: percentage of canopy-to-ground gaps (categories <10%, 10-<25%, 25-<50%, 50-<75%).
- Margins: width categories for left and right margins (e.g., up to 12m, 2-<4m, etc.).
- Staked trees and tree protectors: Yes/No indicators.
- Note: if base height >2m, check that woody species are trimmed or cut to maintain natural shape; if natural shape, record accordingly.
- Illustrative images provide guidance on coding various WLF configurations.

## Data Collection and Digital System
- Field data capture is conducted via the CS Surveyor, an ArcMap-based custom extension enabling consistent data entry and change logging.
- System features:
  - On/Load square data and edit points, lines, and areas with pre-set symbology.
  - Mandatory change recording with a “Reason for Change” field for auditability.
  - Helpdesk support and methodology updates via a Wiki and Latest News.
- Scale and accuracy considerations:
  - Editing polygons requires a map scale of at least 1:5000.
  - Emphasis on extent and change accuracy over precise geometric accuracy.
  - Minimum Mapping Unit (MMU) of 1/25 hectare (400 m2); smaller areas not mapped unless necessary (e.g., edge effects).
- Data governance and sharing:
  - Focus on data provenance, transparency, and sharing underlying data where appropriate.
  - Guidelines for metadata, data cleaning, transformation, and presentation (reports, charts, dashboards).

## Line Editing Tools and Procedures
- Create New Line:
  - Lines must be created within a survey square, at scale 1:5000 or better, minimum length 5.0 m, and cannot cross themselves.
  - A new line starts with a single Unsurveyed/Missing Data event along its length.
- Modify Line:
  - Edit by selecting the line and using vertex editing (insert/delete/move vertices).
  - End-point nodes shared with other boundaries can only be modified via Shared Node Modify.
  - Edits must avoid creating invalid intersections; minimum feature length checks apply.
- Shared Nodes:
  - Modify shared nodes carefully; moving a node updates all connected lines while preserving topology.
- Cut Line:
  - Use a cut polygon along the line to remove a segment; displayed lengths show cut and remaining portions.
- Modifying Edit Sketch:
  - Resize or reshape cut polygons by adjusting vertices to produce the required cut.
- Copy Tool:
  - Copy features from other layers (e.g., OS Mastermap) to form an edit sketch; can cut multiple lines accordingly.
- Delete Line:
  - Deletions require a valid Reason for Change on all attached events; otherwise editing is required first.
- Reshape Line 1 and 2:
  - Reshape edits follow existing lines or copied lines; must intersect start and end points of the target line.
- Checking Visit Status on Linear Features:
  - Use Select By Attributes to identify unvisited landscape events (VISIT_STATUS = 0).
  - Procedures exist for handling loops in event data (mark as Deleted Feature, set Reason for Change to No Change, complete visits, then re-create lines).

## Change Management, Quality Assurance and Governance
- Change attribution:
  - REAL change reflects genuine habitat or landscape change; ERROR change reflects corrections or mis-recordings.
  - For unenclosed habitats, baselines from 1998/1990 may drive attributes; Reasons for Change justify updates.
  - PH baselines can be updated post-survey using GIS masks to adjust extents.
- Data quality and consistency:
  - Require reporting of at least two species per polygon (up to four) to ensure robust vegetated polygons have data.
  - Emphasize transparent metadata, data cleaning, transformation, and clear presentation in outputs (reports, dashboards).
- Project-wide data governance:
  - Define processes for sharing underlying data where appropriate, while maintaining provenance and openness standards.
  - Document data models, attribute definitions, and mapping rules to support replication and auditability.

## Pond and Water Body Details
- Pond mapping protocol:
  - Every pond within a square is mapped; ponds are defined as 25 m2 to 2 ha with water presence for at least four months.
  - A Pond Mapping Recording Sheet captures pond ID, area, water presence, reasons for loss/creation, and notes.
  - A survey pond is selected for detailed condition assessment; preselected ponds support rapid fieldwork but may be adjusted.
  - Delineation guidelines distinguish ponds in fen/marsh/swamp, bogs, ditches, and dammed streams; emphasizes boundary determination using winter water levels or fringe vegetation.

## Implications for Monitoring Framework Authors
- Demonstrates a structured, rule-based approach to building a national environmental health monitoring framework:
  - Clear classification and attribute keys (BH/PH and woodland types) with explicit capture rules.
  - Emphasis on change detection, auditability, and time-series comparability via standardized digital tools.
  - Integration of field data with GIS to enable scalable, transparent policy-facing outputs.
  - Proactive handling of data gaps, data accessibility, and governance through metadata and data-sharing practices.
- Highlights key takeaways for authors of monitoring frameworks:
  - A digital, auditable data model supports tracking habitat extent and change over time.
  - Clear procedures address data gaps, silos, and metadata deficiencies via standardized keys and field protocols.
  - Methods for managing complex landscapes (upland unenclosed, mosaic habitats) with consistent, reportable attributes.
  - A flexible yet rigorous framework that supports national and UK biodiversity reporting and policy planning.