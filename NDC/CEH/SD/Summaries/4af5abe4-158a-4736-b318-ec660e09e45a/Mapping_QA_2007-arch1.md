# Mapping Quality Assurance Exercise

- Purpose: Assess QA of 2007 Countryside Survey mapped data by comparing field-survey data (Surveyors) with QA assessments across multiple scales and methods, using a digital workflow (Surveyor software, wiki checks) to improve data quality and interoperability with national datasets.

## Key context and approach

- Digital mapping in 2007 aimed to reduce post-survey interpretation errors and enable rapid analysis with a geodatabase.
- Surveyors used a dedicated Surveyor software with mandatory fields; data uploaded to an interactive wiki for early QA.
- QA covered 23 one-kilometre squares, selected to represent land classes and locations across Great Britain; QA often occurred in different squares from the survey to broaden coverage.
- Three main QA analyses:
  - Direct comparison of aggregate areas/lengths/points per square.
  - Raster data analysis: convert polygons to 10 x 10 m raster cells to compare broad habitats (BH) by dominant habitat per cell.
  - 100-point grid analysis: assess concordance of BH/PH (priority habitats) at ~100 points per square.
- Additional analyses included: attribute-level comparisons for areas/lines/points, surveyor efficiency metrics, and change recording (Real change, Error change, No change).

## Data and methods highlights

- Data types compared:
  - Broad Habitats (BH), habitat attributes, and species-level data within polygons.
  - Linear features and point features, plus 100-point habitat concordance and change coding.
- Processing and comparison techniques:
  - Aggregates: CS vs QA extents by square and BH.
  - Raster: 1 km squares divided into 10,000 cells; dominant BH assigned to each cell; matched via spatial sampling.
  - 100-point grid: presence of BH/PH at 100 points per square; concordance and mismatch tallied.
  - Reference ID layers created to align QA and CS polygons for attribute comparisons.
- Change coding:
  - Field-captured change categories included Real change, Error change, No change; QA compared change assignments to assess consistency.

## Key findings

- Direct comparison of aggregate areas (6.1)
  - 81% of squares had agreement on BH presence between CS and QA.
  - Mean differences in BH extent were typically under 1% for many BHs; 1–2% for a few; under 3.5% for the remaining two BHs.
  - Notable potential issues flagged for Improved grassland, Acid/Neutral grassland boundaries, Dwarf Shrub Heath, Bog, Urban, and products like Blanket Bog due to definitional and scale challenges.
- Raster data comparisons (6.2)
  - Overall raster agreement across squares averaged around 76%, with some squares high (e.g., 364 at 98%, 488 at 94%) and others low (e.g., 773 at 23%, 261 at 49%).
  - Variation by BH: some habitats showed high agreement, others exhibited notable discrepancies (e.g., Neutral vs Improved Grassland, Blanket Bog vs Dwarf Shrub Heath, urban assignments misaligned with grassland).
  - Examples of squares with high concordance: 364, 488, 359, 355, 1034, 1113, 1260; lower concordance in squares like 261 and 773.
- 100-point grid concordance (6.3)
  - Majority of squares showed good concordance, but several squares exhibited substantial mis-matches.
  - Notable problem squares: 773 (only 19–41% concordance depending on metric), 261 (often around 41%), with others ranging higher.
  - Issues discussed include: upland mosaics, overlayering of BHs (e.g., Blanket Bog vs Dwarf Shrub Heath), machair on Scottish dunes, and the challenge of disaggregating mosaicked upland habitats into discrete BHs.
  - Broad and Priority Habitat correspondence generally strong, but some systematic mismatches tied to definitional boundaries and local habitat peculiarities.
- Species attributes within polygons (6.4)
  - 1,081 QA polygons matched to 998 CS polygons; about 45% of QA polygons shared at least one listed species with the matched CS polygon (excluding mosaics).
  - Species concordance across matched polygons was about 40%; higher for certain habitat types (woodlands and Improved Grassland) where dominant species are more obvious.
  - Table 6.4 and 6.5 detail species-level concordance for common taxa; generally lower than habitat-level concordance due to mosaic and dominance effects.
- Linear features (7) and Points (8)
  - Linear features: very high consistency in land-use theme coding; minimal cases where QA recorded a feature not matched by CS, and low confusion between similar feature types (e.g., belts of trees vs woody belts).
  - Points: similar high alignment in habitat codes; some occasional woodland-code confusion noted.
  - Overall, digital capture aided consistency across linears and points, though some woodland coding ambiguities persisted.
- Change recording (9)
  - Change coding generally aligned with QA, with high agreement across broad habitat types (Tables 9.1–9.3).
  - Some remaining ambiguities in applying change codes to certain habitat types, highlighting the inherent difficulty of distinguishing change in complex, mosaicked habitats.
  - The digital change field helped update previous maps, though it added complexity for surveyors.

## Implications and interpretation

- The 2007 digital workflow markedly improved data quality control, with mandatory fields and wiki-based checks reducing handwriting/interpretation errors and enabling timely QA.
- Most BH definitions and classifications showed robust agreement between CS and QA, but key issues remained in:
  - Blanket Bog versus Dwarf Shrub Heath in upland contexts.
  - Overlaps and boundaries between Neutral and Improved Grassland.
  - Woodland vs Broadleaf/Conifer classifications and the historical use of woodland codes.
  - Localized habitats (machair, upland mosaics) requiring refined definitions and clearer field guidance.
- Training and experience matter: squares with less-experienced survey teams showed higher mis-matches in complex habitat types.
- Spatial scale and mosaic mapping challenges: small-scale variability and transitional habitats complicated precise mapping at 1 km and 10 m raster resolutions.
- The analyses demonstrate the value of multiple QA approaches (aggregate, raster, 100-point, and change assessment) to triangulate data quality and guide future methodological refinements.

## Limitations and considerations for future work

- Access refusals and landowner constraints limited the coverage in some squares, affecting the QA representativeness.
- Certain habitat categories (e.g., Blanket Bog) require ongoing refinement of definitions and backcasting approaches to improve consistency across surveys.
- High disparity in some squares suggests the need for targeted training or field- handbook clarifications, particularly around urban vs grassland classifications and upland mosaic mappings.
- Species concordance remains challenging; future work could focus on standardizing dominant-species selection protocols and expanding reference datasets.

## Summary takeaway for analysts

- The Mapping Quality Assurance Exercise shows strong overall alignment between Surveyors and QA, with 81% square-level BH agreement and substantial raster and 100-point concordance, though notable exceptions highlight definitional and scale challenges.
- Digital data capture and QA workflows significantly improved data quality and traceability, enabling more reliable integration with national datasets and informing habitat definitions and mapping protocols for future surveys.
- Key target areas for refinement include Blanket Bog vs Dwarf Shrub Heath definitions in uplands, Neutral vs Improved Grassland boundaries, and consistent Woodland/Broadleaf/Conifer classifications, reinforced by enhanced training and clearer field-handbook guidance.