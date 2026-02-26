# CS Technical Report No 1/07: Field Mapping Handbook v1.0

- The document provides in-depth field-mapping guidance for Countryside Survey 2007 (CS2007), with a focus on Woodland Linear Features (WLF), line editing workflows in CS Surveyor, and dedicated pond mapping procedures. It also situates these within the broader multi-theme data architecture used for longitudinal habitat monitoring and policy-relevant biodiversity reporting.

## Key data model and data collection elements

- Woodland Linear Features (WLF)
  - Attributes to collect: height categories (Base height and canopy height), species composition (e.g., mixed species, dominance of hawthorn), evidence of recent management, line of stumps, vertical gappiness, left/right margin widths, presence of staked trees, and tree protectors.
  - Shape classification: WLFs can be coded as “unnatural shape” or “natural shape,” with guidance to adjust recording if canopy shaping is evident.
  - Height and composition guidance: modal height concepts and thresholds for gappiness and margins guide classification; if >2 m, ensure canopy can be cut or trimmed to shape; otherwise record as natural shape.
  - Examples and coding illustrations: visuals and coded examples demonstrate variations in base height, stumps, gappiness, species composition (e.g., hawthorn dominance), and management signs.
- Multi-theme data framework
  - CS2007 uses a cross-theme data model (areas, lines, points) with BH/PH classifications and woodland-related attributes, integrated with older datasets for time-series analyses.
  - Ponds are treated as a central data type with a dedicated recording framework (see Pond Mapping).
- Line editing and feature management
  - The Field Mapping Handbook provides detailed tablet-based editing workflows for creating, modifying, and managing lines, including events, margins, and boundary attributes.
- Ponds
  - Ponds are defined as standing water from 25 m2 to 2 ha, present for at least four months annually.
  - Boundaries are delineated using vegetation boundaries, water marks, banks, or winter waterlines; temporary ponds identified via wetland vegetation or other indicators.
  - Data captured per pond includes polygon ID, area, water presence, reasons for pond loss or creation, and notes.
  - Per-square pond mapping involves compiling all ponds on a CS2007 Pond Mapping Recording Sheet and selecting a survey pond for detailed condition assessment.

## Editing workflows and data governance

- Line creation and editing (CS Surveyor)
  - Create New Line: scale must be 1:5000 or smaller; lines must be within the survey square, minimum length 5.0 m, cannot self-cross; new lines start with an Unsurveyed/Missing Data event.
  - Modify Line: edit shape via vertices; manage end points and shared nodes; ensure topology integrity; certain edits (end nodes, intersections) require appropriate protocols.
  - Shared Nodes: repositioning a node moves connected lines; strict constraints prevent new intersections or invalid topology.
  - Cut Line: apply a cut polygon along the line to remove segments; limits on length and multiple cuts; the length to be cut is visually indicated.
  - Reshape Line: reshape via a following graphic that intersects the original line; can be done in two modes (Reshape 1 and Reshape 2) including shaping along copied boundaries.
  - Copy Tool: use features from other layers to form accurate cut-line sketches; supports inclusion/exclusion of features in the edit sketch.
  - Delete Line: lines can be deleted only when all attached events have valid Reason for Change data; scale restriction 1:5000+ for deletion.
  - Validation and quality controls: mandatory Reason for Change fields; checks to prevent invalid edits; MMU constraints apply to new features.
- Visit status and loops
  - Visiting status for linear features is tracked via a Select By Attributes workflow; unvisited lines are highlighted to guide field teams.
  - Loops (data integrity issue): loops in the dataset have corrupted event data; the protocol is to mark the loop events as Deleted Feature with Reason for Change: No Change, delete the lines, and then re-create the line(s) with correct attributes.
- Documentation and legacy data
  - Surveyors receive electronic Field Assessment Booklets (FABs) and can reference older CS2000/1990 field-handbooks electronically to aid interpretation and coding.
- Data integration and governance
  - The handbook emphasizes distinguishing real ecological change from data error (REAL change vs. ERROR change) and the integration of older datasets for refined vegetation attributes and PH allocations.
  - Post-survey GIS masks and PH masking are used to delineate PH extents; metadata, standard attribute structures, and change logs are essential for cross-theme consistency and longitudinal analyses.

## Pond mapping: methodology and data capture

- Pond mapping framework
  - Complete one CS2007 Pond Mapping Recording Sheet per square; record every pond present and note those no longer present from CS2000.
  - For squares with many ponds, continue on additional sheets; after listing, select a survey pond for detailed freshwater surveying.
  - Recording fields include pond polygon ID, area, maximum winter water level, current water presence, and reasons for pond loss or creation; optional notes provide context.
- Selection and data flow
  - The form guides the transition of pond data from mapping to detailed condition surveys by freshwater specialists.
  - Pre-selected ponds may be used; if not feasible, survey pond selection is guided by a predefined set of criteria.
- Annex and references
  - The pond mapping annex documents the format and flow for pond data collection and the handoffs to freshwater survey teams.

## Implications for Data Leaders

- The handbook defines a rigorous, time-series-ready data architecture with richly attributed features across polygons, lines, and points, including detailed WLF attributes and dedicated pond data workflows.
- Data Leaders should expect:
  - A robust schema supporting long-term habitat monitoring, with specific attention to WLF classification, line editing governance, and pond data integrity.
  - Strong data quality control mechanisms, including mandatory change reasons, edit validation, and procedures for corrupted loop data.
  - Comprehensive, cross-theme data governance to manage gaps, mosaics, and PH mask integration, plus guidance for coordinating practice across partners and datasets.
  - Attention to data access and sharing considerations, given potential paywalls or sector coordination challenges, and ongoing emphasis on building a cohesive data community for practice and reuse.