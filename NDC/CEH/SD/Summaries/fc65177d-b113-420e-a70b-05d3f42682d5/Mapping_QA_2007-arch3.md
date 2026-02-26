# Mapping Quality Assurance Exercise

- Objective: Assess quality of digital field mapping from Countryside Survey 2007, ensure compatibility with previous approaches, and enable rapid analysis within a geodatabase.
- Context: Transition to in-field digital mapping using Surveyor software with mandatory fields to reduce interpretation error; data uploaded to an interactive wiki for early QA and guidance.
- Governance and openness: QA emphasized data provenance, metadata, and sharing outputs; notes barriers when datasets must be publicly shared.

## Data, Tools and QA Philosophy

- Digital mapping enabled immediate QA against CS team data; traditional post-processed digitisation was replaced by in-field mapping, reducing subjectivity.
- QA approaches used:
  - 4.1 Direct comparison of aggregated areas/lengths/points by Square
  - 4.2 Raster comparison (10 x 10 m cells per 1 km square) to assess habitat amounts and locations
  - 4.3 100-point grid to test agreement on Broad Habitats at fixed locations
  - 4.4 Attribute comparisons for areas, lines, and points via reference ID layers
- Data handling: unsurveyed or refused areas excluded prior to comparison; data stored in a single geodatabase.

## Extent and Practicalities

- QA mapped 23 1 km squares; chosen to represent Land Class and geography across Great Britain; some areas refused access.
- QA generally conducted in parallel with survey teams to minimize temporal vegetation changes and landowner disturbance.
- QA teams sometimes used multiple tablets, causing later data reconciliation and longer analysis.

## Findings: Methods and Outputs

- Surveyor efficiency and data quality:
  - Very small proportion of land not visited (average around 0.4%); most refusals/exclusions were accounted for in the analysis.
  - Mandatory fields improved recording of dominant species per area.
- Aggregated and raster comparisons (6.1, 6.2):
  - Overall concordance for broad habitat (BH) allocations between CS and QA is high; most squares show good agreement.
  - Mean differences in BH proportions between CS and QA are generally under 3.5% across many habitat types; some habitats show larger SDs, indicating potential differential allocation (e.g., Improved grassland, Neutral grassland, Dwarf shrub heath, Bog, Urban).
  - Specific discrepancies highlighted: Improved/Neutral Grassland overlap; Woodland definitions (Broadleaf vs Coniferous) and their key criterion; upland mosaic complexities; urban vs grassland ambiguity; and machair on some Scottish dunes.
  - Blanket Bog is notably challenging due to evolving definitions; some mis-matches occurred with Dwarf Shrub Heath, reflecting field vs QA interpretation in upland areas.
- 100-point concordance (6.3):
  - Majority of squares show good concordance between QA and CS; notable exceptions include squares 773 and 261 with lower concordance.
  - Agreement by BH/PH per square varies, with some squares showing high agreement (e.g., 364, 359, 355) and others lower (e.g., 773, 261).
- Species attributes in polygons (6.4, 6.5):
  - Of QA polygons matched to CS, about 45% had at least one matched species; species concordance is moderate overall, with higher concordance in woodlands and Improved Grassland and lower in Bracken and upland mosaics.
  - When species matched, correspondence with Broad Habitat was about 77% for matched polygons.
  - Commonly recorded species show mixed concordance; Lolium perenne and some large trees show relatively higher agreement, while many other species show lower QA-CS concordance due to identification challenges and varying dominance.
- Linear features (7.1, 7.2):
  - Aggregate lengths per square show minor differences; linear features categorized by land-use themes (e.g., Banks, Fences, Forestry belts, Walls) show high QA-CS consistency.
  - 7.2 Buffer-based matching indicates strong consistency in land-use theme classification for linears; few cases where QA logged a feature not seen by CS, generally expected.
- Points (8.1):
  - Totals per square show minor differences; points grouped by habitat themes (Forestry, Inland Physiography, Inland Water, Structures, Veteran Trees) are largely consistent.
  - Veteran trees show the greatest disparity due to field instruction allowing multiple trees; concordance is lower.
- Change recording (9):
  - Change codes introduced: Real change, Error change, No change.
  - Majority of habitats show broad agreement on change coding between CS and QA; some complexity exists for habitat-level change due to interpretation of what constitutes change.
  - Digital recording facilitated capturing more detailed change information, though some surveyors struggled initially; overall approach workable and beneficial for updating prior maps.

## Key Challenges and Explanations

- Data and metadata quality:
  - Occasional inadequate metadata and definition ambiguities in habitat classes (notably Blanket Bog, Urban vs grassland, conifer vs broadleaf woodland) contributed to mis-allocations.
- Habitat definitions and mosaics:
  - Upland mosaics and transitions between habitats increased matching difficulty; mosaicked areas disaggregated into constituent Broad Habitats, potentially inflating mismatches.
- Training and definitions:
  - Differences in field interpretation and familiarity with habitat keys (e.g., Blanket Bog definitions and wet heath vs blanket bog) highlighted the need for ongoing training and key updates.
- Machair and Scottish dune contexts:
  - Localized, uncommon habitats (machair) produced anomalies in grid-based comparisons; primarily treated as Neutral/Improved Grassland in the broader framework.

## Implications for Monitoring Frameworks

- Digital field mapping with integrated QA (including wiki-based checks and geodatabase integration) can substantially improve data quality, timeliness, and traceability.
- Clear, up-to-date habitat definitions and field-handbook guidance are critical to minimize cross-team inconsistencies, especially for problem areas like Blanket Bog, urban interfaces, and upland mosaics.
- Training and iterative refinement of classification schemes are essential when transitioning to new data capture and validation workflows.
- Data governance considerations (metadata, data sharing constraints, provenance) must be addressed early to avoid barriers to reuse and public dissemination.

## Recommendations for Monitoring and Data Governance

- Maintain and refine clear, explicit habitat definitions; document handling of mosaics and transitions between habitats.
- Invest in training for survey teams on updated keys and edge cases (e.g., Blanket Bog, urban grassland allocations).
- Continue digitized QA loops (in-field data capture to wiki/on-line QC) to improve timeliness and data integrity; ensure metadata standards accompany data releases.
- Develop transparent rules for data sharing and openness, balancing researchers’ needs with owners’ consent and privacy considerations.
- Use multi-scale QA outputs (square-level, raster, 100-point, and polygon-level analyses) to continuously assess and improve mapping consistency.
- Where significant discrepancies persist in high-priority habitats, conduct focused re-training and targeted re-surveys to reduce systematic bias.