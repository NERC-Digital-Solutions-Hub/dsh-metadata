# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Summary for Data Stewards

- Purpose and scope relevant to governance
  - Field mapping of habitats, landscape features, and water bodies using CS Surveyor (ArcMap-based) to produce interoperable, richly attributed data for biodiversity monitoring and policy reporting.
  - Data model centers on Areas, Lines, and Points with pond mapping as Inland Water features; emphasis on metadata, provenance, and change tracking.

- Data model, storage, and governance (practical governance details)
  - Core entities: Areas (polygons), Lines (linear features), Points (point features); ponds mapped under Inland Water with pond-specific attributes.
  - Change tracking: every modification requires a Change Reason; distinguish REAL (genuine ecological change) from ERROR (recording mistakes); provenance maintained (e.g., change type, reason, and who/when).
  - Data quality focus: accuracy of extent and attributes prioritized over pin-point geolocation; mandatory fields enforce data integrity; stop-editing workflows require saving to persist changes.
  - Data storage/edit workflow: CS Surveyor integrated with ArcMap; login controls; governance steps after survey (documenting changes, updating attributes, maintaining provenance).

- Field workflow and editing constraints (data lifecycle controls)
  - Editing capabilities include:
    - Area editing: boundary changes, attribute copying, splitting/merging areas, component management.
    - Point editing: add/edit/delete; points may have multiple components (e.g., trees, water bodies).
    - Line editing: add/edit events, manage lengths and attributes; copy/split/merge operations; mandatory change-reason fields.
  - Editing constraints to protect data integrity:
    - Lines have minimum length (5.0 m); edits must occur within survey square and at scale of 1:5000 or finer.
    - Endpoints of shared boundaries treated as shared nodes; some edits require “Shared Node Modify.”
    - Invalid edits (e.g., creating self-intersecting lines) are rejected; topology preserved.
  - Data quality gates:
    - Mandatory fields highlighted; errors block progression.
    - Visit status tracking for linear features to identify unvisited segments and manage unpublished data.

- Woody Linear Features (WLF) – attributes and interpretation
  - WLF classification types include lines of stumps, hedges, belts, belts/linears, and natural shapes; notes on management history.
  - Key attribute groups:
    - Height categories (e.g., <1 m, 1–2 m, 2–3 m, >3 m; base height for canopy), with potential reclassification if canopy height changes.
    - Species composition indicators (e.g., mixed species; >50% hawthorn; other dominance).
    - Evidence of management (e.g., newly planted, cutting, laying/coppicing within recent years).
    - Line characteristics (line of stumps: Yes/No; vertical gappiness as percentage ranges).
    - Margins and buffers (left/right margins in meters, presence of margins; buffer management indicators such as staked trees and tree protectors).
    - Management and protection markers (staked trees, tree protectors, underplanting, windthrow).
  - Images and decision aids accompany guidance notes to support consistent WLF coding.

- Ponds and Inland Water data (field procedures and longitudinal tracking)
  - All ponds in a survey square must be identified; a single survey pond is selected for detailed condition assessment using a randomized or pre-selected process.
  - Pond definitions rely on winter water level and hydrology; ponds from 25 m2 to 2 ha with water for at least 4 months may be recorded, including temporary ponds.
  - Pond data captured on CS2007 Pond Mapping Recording Sheet; attributes include polygon ID, area, water presence, loss/gain reasons, and notes; longitudinal consistency enabled by standardized pond identifiers across surveys.
  - Appendix-based procedures guide pond recording, randomization, and cross-survey comparability; pre-selected ponds may be used if still valid.

- Data governance, quality, and support
  - Methodology emphasizes clear documentation of ecological change versus prior data errors; Change Reason field required for justification.
  - Challenges acknowledged for data stewards include incomplete user needs, timely data acquisition, metadata completeness, interoperability across systems, handling large and diverse datasets, and integrating legacy datasets.
  - Practical support structures:
    - Helpdesk and fault-logging for CS Surveyor issues.
    - Access to guidance, appendices, and older fieldhandbooks for interpretation.
    - Documentation of data provenance and updated methodology notices to ensure transparency and reuse.

- Special notes for Data Stewards (policy, provenance, and reuse)
  - The handbook implements a policy-relevant data framework linking habitat mapping to biodiversity monitoring and reporting.
  - Strong emphasis on standardized attribute schemas, consistent use of keys, explicit change-tracking, and transparent data provenance to enable discovery, longitudinal analysis, and data reuse.
  - Data model supports integration into broader conservation reporting while maintaining rigorous, field-based data collection standards.