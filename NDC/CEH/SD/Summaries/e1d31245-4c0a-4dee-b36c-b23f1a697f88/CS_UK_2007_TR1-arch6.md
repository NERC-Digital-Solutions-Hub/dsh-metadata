# CS Technical Report No 1/07: Field Mapping Handbook v1.0

- Purpose and scope
  - Provides field mapping methodology for Countryside Survey 2007 (CS2007), including habitat and landscape feature mapping, change reporting, and data collection in a digital GIS framework.
  - Introduces CS2007 data model and workflows (CS Surveyor/ArcMap integration) to support policy monitoring, biodiversity reporting, and scientific analyses.
  - Covers field data capture for Woody Linear Features (WLF), line editing operations, pond mapping, and historical data integration (CS1990/CS2000 contexts).

- Woody Linear Features (WLF): data capture and coding
  - Key attributes to record for WLF:
    - Unnatural shape or line of stumps
    - Base height of canopy and overall height categories
    - Species composition (e.g., dominance thresholds such as >50% hawthorn)
    - Evidence of recent management (e.g., newly planted, cutting, laying, coppicing)
    - Line of stumps (Yes/No)
    - Vertical gappiness (proportion of gaps from canopy to ground)
    - Margin widths (left and right) and whether margins are present
    - Staked trees (Yes/No) and tree protectors (Yes/No)
    - Notes on natural vs. managed shapes (if base height indicates natural form)
  - Visual guidance: a set of example coding scenarios illustrate how to classify and record WLF features, including variations in height, composition, and management signs.
  - Practical rule: if the base height of the canopy > 2 m, components of the WLF should be cut or trimmed to a natural shape; if the feature is natural in shape, record accordingly.

- Editing workflow and tools (CS2007)
  - Create New Line
    - Map scale must be 1:5000 or smaller.
    - Lines must be created one at a time, with a minimum length and no self-crossing.
    - New lines start with a single Unsurveyed/Missing Data event.
  - Modify Line
    - Edit by selecting and moving vertices; end vertices with shared topology can only be edited via Shared Node Modify.
    - Edits must not produce intersections with other revised lines.
  - Shared Nodes
    - Modify shared nodes to adjust multiple connected lines; careful selection is required to preserve topology.
  - Cut Line
    - Use a cut polygon to remove a section of a line; show the length to be cut and the length to remain.
  - Copy Tool
    - Copy features from other layers (e.g., OS Mastermap) to build edit sketches; supports more accurate cuts by including external features.
  - Delete Line
    - Lines can be deleted only when all attached events have a valid Reason for Change; otherwise editing is needed first.
  - Reshape Line
    - Reshape edits follow the existing line, using a reshape graphic to define start/end points; ensures edits intersect the line appropriately.
  - Reshape Line (Follow Copied Line)
    - Allows moving a line to follow boundaries copied from another feature; original line remains unchanged during the preview.
  - Checking Visit Status for Linear Features
    - Use Select By Attributes to identify unvisited lines (VISIT_STATUS = 0) and highlight them.
  - Loop features caveat
    - Some data loops may be corrupted; surveyors are instructed to mark affected events as Deleted Feature with appropriate Reason for Change and then delete lines, before reinstating them as in-field features.

- Data quality, attribution, and governance
  - All line edits must maintain consistent event attributes and Reasons for Change.
  - Aimed to minimize erroneous edits and maintain a clear audit trail for real vs. mis-recorded changes.
  - Emphasis on field verification and documentation to support cross-square and cross-year comparisons.

- Pond mapping procedures (CS2007 Pond Mapping Recording)
  - Complete one pond mapping form per square for every pond, including ponds recorded in CS2000 that no longer exist.
  - Identify a survey pond from the mapped ponds for detailed freshwater surveys; select from a pre-listed or randomly chosen pond.
  - Record pond polygon ID, area, maximum winter water level, water presence, and reasons for pond loss/creation.
  - Include notes and categorize pond origins (e.g., creation for wildlife, fishing, golf hazard, etc.).
  - If more than 10 ponds exist, continue on additional sheets and staple them together; pre-selected pond status is documented and updated accordingly.

- Historical context and data integration
  - CS2007 integrates five hundred-year themes into a single editable GIS map; supports change attribution (REAL change vs. error) by leveraging prior datasets (CS1990, CS1998, CS2000) to refine habitat delineations and PH allocations.
  - Appendix and annex materials provide context for older mapping practices (CS1990/CS2000), field assessment books (FABs), and coding schemes used in historical data collection.
  - The document supplies guidance for reconciling past allocations, applying consistent attribute categorization, and using keys for vegetation and woodland types to ensure robust data products.

- Practical guidance for data processing and analytics
  - Emphasizes the use of vegetation and woodland keys to achieve consistent habitat classification across squares and years.
  - Encourages back-correcting past allocations when new field evidence supports a change, with documented justification.
  - Balances the need for detailed attributes (PHs, vegetation indicators) with practical mapping constraints, particularly in unenclosed upland areas.
  - Data management aims to enable robust cross-square/year analyses to support UK Biodiversity Action Plans and national/state reporting.

- Appendices and supplementary references
  - Annexes cover pond mapping sheets, old CS2000/1990 coding schemes, and example thematic maps for context.
  - Appendices include guidance on veteran tree girth (Appendix 5) and loops in square datasets (Appendix 6) to inform quality checks and data repairs.
  - Documentation also references field handbooks (FABs) and electronic references for field interpretation and data entry on tablets.