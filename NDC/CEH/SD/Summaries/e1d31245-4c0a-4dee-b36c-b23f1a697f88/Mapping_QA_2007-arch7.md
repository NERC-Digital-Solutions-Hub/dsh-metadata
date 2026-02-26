# Mapping Quality Assurance Exercise

- Purpose: Assess quality and consistency of digital habitat and landscape feature mapping from Countryside Survey 2007, comparing field-survey data (Surveyors) with quality assurance (QA) mappings to enable rapid GIS analysis and integration with national spatial datasets.

## Overview of approach and context

- 2007 introduced field-based digital mapping (Surveyor software) to reduce interpretation errors and handwriting issues; data uploaded to an interactive wiki for early QA.
- QA expanded beyond prior methods, mapping entire squares and including area, line, and point features to test mapping efficacy at multiple scales.
- Mapping QA used three main analysis approaches and compared CS (Surveyors) against QA across 23 one-kilometre squares, with some areas inaccessible or refused.

## Data collection and QA process

- Field data: Surveyors mapped in the field with mandatory fields, prompts, and visit-status layers; data uploaded to a wiki for early office checks.
- QA process: QA teams mapped in-field in different squares from some survey squares; data collected on standard tablets and merged into a single geodatabase; unsurveyed or refused areas excluded from analysis.
- Data types analyzed: Broad Habitats (BH), other habitat types, areas, lines (linear features), and points; included quality checks of dominant species where present.

## Methodologies used (analyses)

- 4.1 Direct aggregation comparisons: Compare total areas/lengths/points per square between CS and QA using SAS.
- 4.2 Raster comparisons: Convert polygons to 10 x 10 m raster cells (10,000 per 1 km square) with dominant BH assigned; compare absolute BH amounts and locations.
- 4.3 100-point grid: Overlay a 10 x 10 grid; spatially match BH between CS and QA; score concordance per BH.
- 4.4 Attribute comparisons: Use reference ID layers to compare species attributes for matched polygons.
- 5.1 Surveyor efficiency: Evaluate visit-status coverage and species recording improvements with digital prompts.
- 7–9: Additional analyses for linear features, points, and change recording.

## Key findings: habitat-level agreement and issues

- Overall agreement:
  - 81% of squares had BH presence recorded by both CS and QA.
  - Mean differences in BH extent between CS and QA generally small (mostly <1–3.5%), with some habitats showing larger SDs indicating differential allocation (e.g., Improved grassland, Dwarf Shrub Heath, Bog, Urban).
- Habitat-specific issues:
  - Neutral vs Improved Grassland: overlapping species makeup caused allocation differences; generally balanced between CS and QA.
  - Broadleaf vs Coniferous woodland: definitional ambiguities noted; woodland mosaics (broad vs conifer) cause cross-category mismatches in mosaicked areas.
  - Upland habitats: mosaics and fine-scale variation led to mismatches when disaggregating mosaics into component BHs.
  - Blanket Bog: definitional debates and 2007 field-handbook revisions led to notable mismatches, especially in square 773; wet heath vs blanket bog differentiation caused discrepancies.
  - Machair on Scottish sand dunes: localised habitat with mixed recording patterns; treated as Neutral/Improved Grassland in practice.
- Raster and 100-point analyses:
  - Raster agreement across BHs averaged around 76% overall, with some squares very high (e.g., 364, 488) and others lower (e.g., 261, 773).
  - 100-point concordance: average concordance around 77%; notable poor matches in squares 261 and 773, indicating localised misalignment or habitat mosaics.
- Species attributes:
  - Polygon-level species matching: about 45% of QA polygons had at least one listed species matching the CS polygon in location.
  - Among matched polygons, 77% also had matching BH, suggesting species lists influence habitat coding.
  - Common species: Lolium perenne showed higher concordance (66%) when present, while many other species showed variable matches due to dominance and identification challenges.
- Notable habitat-level patterns:
  - Forestry-related codes (Broadleaved/Coniferous woodland) dominated point and polygon counts.
  - Blanket Bog and associated upland habitats posed the strongest definitional and mapping challenges.

## Key findings: linear and point features

- Linear features:
  - High consistency in land-use theme classifications between CS and QA; most features matched in theme, with few instances where QA recorded a feature CS did not (expected in field mapping).
  - Some confusion between similar forestry-related categories (FO vs WNS/WUS) but no systemic issues detected.
- Points:
  - Point-feature habitat codes showed strong agreement; buffering-based matching enabled cross-checks where precise location alignment existed.
  - Some minor confusion between woodland/forest codes remained, likely rooted in historical coding practices.

## Change recording and data management

- Change coding categories:
  - Real change: physical change since previous survey.
  - Error change: incorrect previous assignment rectified.
  - No change: no change from 1998 baseline.
- The digital workflow enabled detailed change codes, improving the ability to update past maps; some surveyors initially struggled, but overall change coding aligned with QA protocols.
- Findings indicate that, while change recording is complex in habitat contexts, the digital system improved data tidiness and update capability.

## Data quality in species attributes and polygon analysis

- Species within matched polygons:
  - About 45% of QA polygons had at least one matching species in the corresponding CS polygon; 77% of these had matching BH.
  - Woodland and Improved Grassland showed higher concordance for commonly recorded species; Bracken and upland mosaics showed more variability due to cover thresholds and habitat boundaries.
- Species-level concordance for commonly recorded species varied; Lolium perenne had relatively high concordance (66% for common occurrences).

## Implications for GIS specialists

- The shift to field-based digital mapping significantly enhances GIS-ready data quality and interoperability with national datasets through a geodatabase structure and standardized attributes.
- The QA exercise identifies definitional ambiguities (notably Blanket Bog, woodland classifications, and Machair-related habitats) that affect cross-seller consistency and downstream analyses.
- Mosaic and fine-scale habitat transitions pose challenges for exact BH alignment between CS and QA; results suggest benefits from ongoing training and potential refinements to habitat definitions and allocation rules.
- The 100-point and raster comparison approaches provide robust, scalable methods to quantify spatial agreement and guide iterative data cleaning and standardization.
- Change recording capability, enabled by digital inputs, improves the ability to track and update historical maps, though it introduces complexity requiring clear guidance and training.

## Conclusions and recommendations

- Digital QA demonstrates strong overall agreement between surveyors and QA mappings, with high consistency across many habitat types and data products.
- Persistent issues center on definitional clarity for specific habitats (notably Blanket Bog and woodland types), mosaic mapping in uplands, and region-specific habitats like machair.
- Recommendations:
  - Continue and enhance training on BH definitions, especially for Blanket Bog and woodland categories; consider revising field handbook guidance where necessary.
  - Maintain the digital change recording framework, with ongoing support to ensure surveyors apply change codes consistently.
  - Leverage raster and 100-point analyses to identify and address localised discrepancies; focus QA efforts on squares with lower concordance (e.g., 261, 773).
  - Use QA insights to refine BH allocation rules and improve consistency of habitat mapping in future surveys.
- Overall, the 2007 digital QA exercise supports reliable GIS-ready habitat mapping, while highlighting targeted areas for definitional refinement and training to further reduce discrepancies.