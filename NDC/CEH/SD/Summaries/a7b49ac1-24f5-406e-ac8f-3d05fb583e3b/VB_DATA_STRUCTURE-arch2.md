# UK Environmental Change Network (http://www.ecn.ac.uk) Vegetation: Baseline (VB)

## Aim
- Provide a baseline vegetation dataset for the ECN to monitor environmental health and change over time.
- Ensure data are formatted for consistent scrutiny of environmental change and policy performance.

## Data Origin, Ownership and Access
- Originator: ECN Data Centre, Centre for Ecology and Hydrology.
- Owners: ECN programme funded by a consortium of UK government departments and agencies.
- Access and acknowledgment: Data use must be acknowledged; request reprint of publications citing ECN data.
- Protocol reference: http://www.ecn.ac.uk/measurements/terrestrial/v

## Protocol and Sampling Design
- Sampling grid: Approximately regular grid coincident with the National Grid, ~400 sample grid positions per site; up to 100 random infill points to represent under-represented vegetation types.
- Plot design: 2 m x 2 m plots centered on grid/infill points; plots oriented N, E, S, W; permanently marked for ongoing monitoring when selected.
- Survey approach: One-off survey to generate vegetation map and select plots for long-term monitoring.
- Outputs: ECN coarse-grain, fine-grain, and woodland vegetation surveys available from ECN Data Centre and Environmental Information Platform.
- Quality: Users should apply accompanying quality information when using the data.

## Data Structure and Metadata
- Core data: Stored in 12 tables (one per site): D1VB_xxx (site-level metadata) and D2VB_xxx (plots).
- Key fields (examples): SITECODE, SYEAR (year), PLOTPID (plot ID), PLOTTYPE (S = standard, W = woodland), FIELDNAME (species or quality code), VALUE; plotting date (SDATE); FEATURES (presence codes); UNSURVEYED (percentage unsurveyed).
- Metadata: M_DESC and M_REFFIELD.
- Storage: Oracle database; site codes distinguish sites.

## Site Codes and Locations
- 12 sites (T01–T12) with names, coordinates, and data date ranges (1991–2000 across sites, with site-specific variations).
  - Examples: T01 Drayton; T02 Glensaugh; T03 Hillsborough; T04 Moor House - Upper Teesdale; T05 North Wyke; T06 Rothamsted; T07 Sourhope; T08 Wytham; T09 Alice Holt; T10 Porton Down; T11 Snowdon (Y Wyddfa); T12 Cairngorms.

## Data Content and Coding
- Features: Presence codes (e.g., P = Path, W = Wall, S = Stream, H = Hedge, D = Ditch, F = Fence, B = Bank, N = Natural boundary, X = No feature).
- Species and taxa: Extensive coding linking numerical species codes to Latin names, BR C concepts, and common names; includes mappings for numerous plant species (e.g., Salix spp., Sambucus nigra, Sphagnum spp., etc.).
- Purpose: Provides a detailed code-to-taxon mapping to support standardized cross-site and cross-year analysis.

## Quality Codes
- ECN quality codes accompany management of data quality (from a standard list). If an unusual event occurs not covered by codes, site managers attach text (quality code 999).
- Standard ECN quality codes include a comprehensive list (e.g., 100–513) with detailed descriptions (e.g., data loss, sample loss, equipment issues, environmental disturbances, non-standard sampling, taxon confidence, laboratory issues, etc.) and 999 for unusual events.

## Data Use and Citations
- Acknowledge ECN data usage.
- Researchers are asked to provide one reprint of any publication citing ECN data.

## Data Quality and Sustainability
- Data are accompanied by quality information to guide use and interpretation.
- ECN emphasises storing and uploading created datasets to appropriate portals to facilitate long-term accessibility and reuse.

## Key Analyst Challenges
- Increasing the value of monitoring datasets by integrating ECN data with other relevant datasets (avoiding single-use datasets).
- Enabling broader access to the underlying data used to generate outputs to enhance transparency and reuse.