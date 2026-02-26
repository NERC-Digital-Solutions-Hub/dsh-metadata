# Mapping Quality Assurance Exercise

- A 2007 quality assurance (QA) study of Countryside Survey mapping examined the switch to digital field mapping (Surveyor software) and the use of an interactive wiki for early data checks.
- Goals: assess mapping quality, compare surveyor data with QA data, and evaluate data handling, coverage, and the reliability of habitat and species attributes for robust national spatial analysis.
- Scope: QA of mapped data across 23 x 1 km squares in Great Britain, with focus on broad habitats, linear features, and point features, using multiple comparative methods.

## Data and Methods

- Digital mapping in the field with mandatory fields and prompts to reduce handwriting/interpretation errors; data uploaded to a wiki for early QA.
- QA approaches (4 analyses):
  - 4.1 Direct comparison of aggregate areas/lengths/points for whole squares.
  - 4.2 Raster data comparison by converting polygons to 10 x 10 m cells (1 km squares) with dominant Broad Habitat (BH) per cell; spatial and area comparisons.
  - 4.3 100-point grid overlay to evaluate commonality of BH at a fixed resolution; concordance/discordance recorded per square.
  - 4.4 Attribute analysis for areas/lines/points using reference ID layers to compare species attributes.
- Surveyor efficiency: evaluation of visit status, handling of “refused access” areas, and species recording frequency.
- Data handling: exclusion of unsurveyed areas and refused access to ensure comparability; alignment of CS and QA datasets to common surveyed areas.

## Overall Findings: Broad Habitat (BH) Agreement

- Direct aggregate areas: in 81% of squares, BH presence agreed between CS (surveyors) and QA; mean differences were generally small.
- Magnitude of differences by BH:
  - For 13 BHs, mean differences < 1%.
  - For 5 BHs, differences 1–2%.
  - For 2 BHs, differences < 3.5%.
  - Notable potential issues identified for Improved/Acid Grassland, Dwarf Shrub Heath, Bog, Urban, and Sub-littoral sediment.
- Key habitat discrepancy themes:
  - Blanket Bog: significant definitional challenges; recent field handbook revisions (2007) to improve consistency; large mismatches often involve Dwarf Shrub Heath vs Blanket Bog.
  - Grassland types (Neutral vs Improved): overlap in species; differences reflect perception of coverage or landscape context.
  - Woodlands: confusion between Broadleaf vs Coniferous woodland due to definitional ambiguities; mosaics in uplands can complicate classification.
  - Sand Dune habitats (machair): Scotland-specific issues; machair often aligns with Neutral/Improved Grassland, complicating BH allocation.
  - Urban areas: occasional misclassification as Improved Grassland; field handbook guidance under review.
- Mosaic and upland mapping: mosaics and small-scale variability in upland squares caused mismatches when disaggregating mosaics into component BHs; spatial vs thematic resolution affects concordance.

## Raster Data Comparison

- Overall raster agreement: average concordance around 76% across squares; some squares reached very high agreement (e.g., 364, 488), while others were poorer (e.g., 261, 773).
- Square-level variation in agreement by BH (example highlights):
  - Some squares show high BH agreement (e.g., 364, 488).
  - Others show lower agreement for many BHs (e.g., 261, 773).
- The raster approach provides a clear spatial view of where QA and CS differ, highlighting the same habitat-definition issues noted in 6.1.

## 100-Point Grid Concordance

- Concordance varies by square; majority show good agreement, but notable exceptions include:
  - Square 261: 41% concordance.
  - Square 773: 19% concordance (significant mismatch).
  - Square 359: high concordance (92%), 355 also high (84%), etc.
- Overall, most squares show good agreement, though some high-mosaic or upland squares reveal substantial mis-matches; these reflect definitional and mapping challenges rather than simple data-entry errors.

## 6.3: Primary Land Cover Codes and Habitats (100-Point Analysis)

- The 100-point analysis provides a resolution-based view of how often CS and QA mapped the same BH at corresponding points.
- Results indicate good overall agreement, with explicit examples of particular mis-matches driven by habitat definitions, landscape context, or mosaic areas.
- The analysis also generated matrices of BH/PH (Broad and Priority Habitats) to explore specific cross-checks; some codes showed higher concordance than others, with notable inconsistencies in sand-dune and certain upland habitats.

## 6.4: Polygon Analysis of Species Attributes

- Datasets: QA polygons (n~1081) vs CS polygons (n~998) matched by location.
- Result: 45% of QA polygons had at least one species in common with the CS polygon at the matched location (excluding mosaics).
- Species concordance by BH:
  - Broadleaved Mixed and Yew Woodland: high match rate (~92% of matched polygons).
  - Coniferous Woodland: ~89% matched species; 77% of matched polygons also shared BH.
  - Improved Grassland: relatively high species reporting; BH match ~77%.
  - Bracken and Fen/Marsh/Swamp: more mixed results; upland mosaics complicate species concordance.
- Listed species concordance (Table 6.5) shows overall around 40% concordance for commonly recorded species, with QA often identifying more species than CS; Lolium perenne showed relatively high concordance where common and dominant.
- Implications: differences in species lists are expected given habitat complexity, management practices, and the scale of mosaics; broader BH definitions can influence which species are recorded as dominant.

## 7: Linear Features: Lengths and Land-Use Themes

- 7.1 Direct comparison of aggregate linear lengths by land-use theme shows general agreement across CS and QA, with minor differences in most squares.
- 7.2 Land-use theme analysis indicates high consistency between QA and CS for linears; few instances where QA logged a feature but CS did not, aligning with expected differences in feature types (e.g., fence vs wall).

## 8: Points: Feature Counts and Habitats

- 8.1 Direct comparison of aggregate points shows small differences between QA and CS across most squares.
- Points were categorized into themes such as Forestry, Inland Physiography, Inland Water, Structures, and Veteran Trees; veteran trees showed substantial divergence due to field recording variability and the broad definition used.

## 9: Change Recording Assessment

- 2007 introduced a change field with three states: Real change, Error change, No change; plus an “error change” to correct previous mapping when needed.
- The analysis indicates:
  - General agreement on change coding across broad habitats (Tables 9.1–9.3).
  - Change assessment was more challenging for habitats than for linears/points; some surveyors struggled with the new digital change field.
  - The digital workflow allowed surveyors to update and verify change data in the field, improving data tidiness but adding complexity to QA.
- Overall, change coding followed protocols well, with some habitat-specific ambiguity in complex vegetation mosaics.

## Key Implications and Conclusions

- The 2007 mapping QA demonstrates substantial overall agreement between CS surveyors and QA assessments across BHs, habitats, linears, and points, validating the digital mapping approach.
- Some habitat-definition issues (e.g., Blanket Bog, dune/machair, urban grassland distinctions, and conifer vs broadleaf woodland) require ongoing refinement of definitions, field guidance, and training to reduce misclassification.
- Mosaic and upland habitats pose particular challenges at fine spatial resolutions; disaggregation into component BHs can create mismatches that reflect genuine spatial gradients rather than data quality failures.
- Species recording shows broader alignment at habitat level but limited concordance at the species list level, which is expected given habitat complexity and dominance criteria; however, agreements improve for easily identifiable or dominant species.
- The integration of the QA process with digital field data collection (Surveyor) and the wiki-based checks markedly improves data quality, traceability, and discoverability, while highlighting areas for ongoing methodological refinement and training.