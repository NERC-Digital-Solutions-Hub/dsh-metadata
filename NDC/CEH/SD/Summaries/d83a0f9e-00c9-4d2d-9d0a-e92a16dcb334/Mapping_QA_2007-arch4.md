# Mapping Quality Assurance Exercise

## Introduction
- Purpose: Assess quality and comparability of digital mapping data from Countryside Survey 2007, ensuring data are analysis-ready and compatible with national spatial datasets (geodatabase).
- Approach: In-field digital mapping using Surveyor software with mandatory fields; early data checks via an interactive wiki; Quality Control (QA) teams conducted field QA visits to ensure protocol compliance.
- Rationale: Digital mapping reduces interpretation subjectivity, enhances data clarity, and enables rapid QA feedback and iterative improvement.

## Extent and Approach
- QA coverage: Mapping QA conducted in 23 x 1 km squares, selected to represent land classes and locations across Great Britain; some areas refused access, so analyses focused on common surveyed areas.
- Parallel QA: QA mapping largely occurred in different squares from plot/freshwater QA to avoid landowner burden; where possible, QA teams mapped alongside surveyors to minimize temporal vegetation changes.
- Data processing: Data collected with standard Countryside Survey tablets, uploaded to a geodatabase; unsurveyed or refused areas excluded from both QA and CS datasets; two datasets were aligned for comparability via a mask overlay.

## Methodology and QA Methods
- Analysis approaches:
  - Direct comparisons of aggregate areas/lengths/points per square (CS vs QA).
  - Raster comparison: polygons converted to 10x10 m rasters (dominant Broad Habitat per polygon); analyzed with raster sampling grids.
  - 100-point grid: overlaid points to assess concordance of Broad Habitats at a fixed resolution; aggregation across squares.
  - Attribute analysis: reference ID layers for comparing species/attribute data between datasets.
- Feature types: Analyses conducted for areas, lines (linear features), and points (feature locations) with appropriate matching strategies.

## Surveyor Efficiency and Data Quality
- Visit coverage: Not visited areas were minimal on average (often near 0%); some squares included refused-access zones.
- Data capture improvements: Mandatory fields led surveyors to record more species and dominant species per area; enhanced data reliability and usability.
- Change recording: Digital recording allowed detailed change coding (Real change, Error Change, No change); some surveyors required guidance to use the change field consistently.

## Key Findings: Direct and Raster Comparisons
- 6.1 Direct comparison of aggregate areas (BH by square):
  - In 81% of squares, a Broad Habitat (BH) was recorded by both CS and QA.
  - Mean differences in BH proportions were generally small (mostly under 3.5%), with some habitats showing larger variability and potential coding biases (e.g., Improved grassland, Neutral grassland, Dwarf Shrub Heath, Bog, Urban).
  - Noted issues where mosaics or upland mosaics complicate precise alignment of BH types (e.g., Blanket Bog vs Dwarf Shrub Heath).
- 6.2 Raster data comparisons:
  - Overall raster agreement averaged around 76% across squares, with higher concordance in many squares (e.g., 364, 488) but marked discrepancies in others (e.g., 261, 773).
  - Agreement by BH varied by square; some squares showed high mismatch for certain habitats due to local context (machair, upland mosaic, urban definitions, etc.).
- 6.3 100-point grid analysis:
  - Concordance varied by square; good agreement in several squares (e.g., 364, 359, 355), but poor in others (e.g., 773, 261).
  - Overall, Broad Habitat concordance in the 100-point analysis indicated generally solid agreement with notable exceptions linked to habitat definition and mosaic mapping challenges.
- 6.4 Polygon analysis of species attributes:
  - 1081 QA polygons and 998 CS polygons matched spatially; 45% of QA polygons had at least one listed species also present in the matched CS polygon.
  - Species concordance varied by Broad Habitat; higher concordance in woodlands and Improved Grassland, lower in Bracken and upland mosaics.
  - 77% of polygons with matching species also had matching BH, suggesting species composition often aligns with the allocated habitat but with notable exceptions.
- 6.5 Listed species concordance:
  - Species-level concordance around 40% overall; QA tended to record more species per polygon; Lolium perenne and other common species showed higher agreement where dominant species were easily identifiable.

## Habitat and Species Insights
- Overall data quality: High level of consistency between CS and QA for most Broad Habitats; some substantial discrepancies are habitat-specific and context-driven (e.g., Blanket Bog vs Dwarf Shrub Heath, Neutral vs Improved Grassland, urban vs grassland classifications).
- Notable challenging areas:
  - Blanket Bog: definitional changes and field interpretation created discordance, particularly where wet heath overlays bog — training and refined keys recommended.
  - Upland mosaics: mosaicked habitats increased mismatch potential when disaggregating mosaics into component BHs.
  - Machair/sand dune contexts: localised, uncommon habitats showed localized effects on classification.
  - Woodland classifications: inconsistencies around coniferous vs broadleaved woodland definitions; old field-handbook practices may have influenced code usage.
- Species considerations: Dominant species choices influenced BH allocation; polyphytic grasslands and upland plant communities yielded lower species-level concordance.

## Linear and Point Features
- 7.1 Direct comparison of aggregate linear features:
  - Lengths by land-use theme (banks, fences/forestry, hedges, etc.) showed strong overall agreement between QA and CS; most mismatches aligned with plausible feature renaming (e.g., fence vs wall).
  - Minor inconsistencies between forestry belts (FO) and woody features (WNS, WUS) acknowledged but not widespread.
- 7.2 Land use themes for linear features:
  - 100-point-like matching for linears showed high consistency in land-use classification across surveyors and QA, reinforcing robust mapping of linear features when buffered and matched.
- 8.1 Direct comparison of aggregate points:
  - Point features (forestry-related, inland physiography, water bodies, structures, veteran trees) showed general alignment; the largest variability occurred in veteran trees due to field instruction to select up to two relevant trees per species.

## Points, Change Recording, and Overall Data Integrity
- Change coding:
  - Change categories reproduced across CS and QA with high agreement for many feature types; some habitat-related change coding showed more variance, reflecting complexity in habitat interpretation.
  - Digital change-field usage enabled in-field updating and cross-checking, though it added complexity requiring training and practice.
- Overall data integrity:
  - The digital QA workflow improved data discoverability, metadata consistency, and cross-survey comparability, supporting better governance of data products and more reliable downstream analyses.

## Implications for Data Leaders
- Demonstrates that end-to-end digital QA processes can substantially improve data quality, consistency, and timeliness for large-scale data collections.
- Highlights the importance of:
  - Clear, standardized definitions and keys (e.g., for woodland types, bogs, and sand-dune habitats) to reduce cross-survey variability.
  - Ongoing training and documentation to manage edge cases (upland mosaics, machair, Blanket Bog revisions).
  - Maintaining robust metadata, versioning, and data provenance to enable reproducibility and cross-network collaboration.
  - Integrating feedback loops between survey teams and QA to iteratively refine data collection protocols and habitat keys.
- Reveals that even with high overall agreement, certain habitat types and rare/complex landscapes benefit from targeted review and potential redefinition for future surveys.

## Recommendations and Next Steps
- Strengthen definitions and training for problematic habitats (e.g., Blanket Bog, upland mosaics, urban vs grassland boundaries).
- Continue iterative refinement of woodland classifications and ensure alignment with current field handbook guidance.
- Enhance QA analytics to better explain square-level discrepancies and provide targeted guidance to field teams.
- Maintain digital change recording workflows with ongoing QA support to further reduce misclassification of changes.
- Leverage the 6.4 and 6.5 species concordance insights to calibrate species selection criteria and improve habitat-specific species keys.