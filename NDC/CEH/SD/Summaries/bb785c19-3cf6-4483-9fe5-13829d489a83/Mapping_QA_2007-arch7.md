# Mapping Quality Assurance Exercise

- Objective: Assess the quality and consistency of digital habitat and landscape feature mapping produced during Countryside Survey 2007, enabling fast analysis and integration with national spatial datasets in a geodatabase.
- Context: Transition from post-survey digitisation of paper maps to field mapping with in-field data capture (Surveyor software) to reduce interpretation error and improve data clarity and attribute completeness.

## Data, Tools and workflow

- Field data collected and mapped in the Surveyor software; mandatory fields and visit status layers to guide data entry.
- Data uploaded to an interactive wiki for early QA and guidance; QA teams conducted site visits to ensure protocol adherence.
- QA included digital comparison between map outputs (surveyors) and validated CS methods, plus cross-checks against 1998 data (baseline).
- Data processing and analysis approaches:
  - Direct comparisons of aggregate areas/lengths/points per 1 km square.
  - Raster-based comparisons: converting polygons to 10 x 10 m raster cells to compare broad habitat extents and locations.
  - 100-point grid analyses to assess co-location agreement of Broad Habitats.
  - Attribute comparisons for areas/lines/points using reference IDs and species attributes.
  - Integration into a single geodatabase; unsurveyed or refused areas excluded from analyses.

## Scope of QA

- Extent: QA covered 23 1 km squares; effort spread across different land classes and locations in Great Britain.
- Data alignment: QA data and CS surveyor data were masked to common surveyed areas for robust comparisons.

## Key Analytical Approaches and Findings

- 4.1 Direct aggregate comparisons
  - Across squares, CS and QA largely agree on Broad Habitat extents; mean differences for many habitats are under 1–3.5%.
  - Some habitats show larger discrepancies (e.g., Improved vs Neutral Grassland, Dwarf Shrub Heath vs Blanket Bog, urban vs grassland) revealing definitional or mapping challenges.

- 6.2 Raster data comparisons
  - Overall raster agreement averages around 76%, with high concordance in several squares (e.g., 364, 488) and notable mismatches in others (e.g., 261, 773).
  - Agreement by Broad Habitat varies by square; some squares show strong agreement for many BH types, others show substantial disparities.

- 6.3 100-point grid analysis
  - For Broad Habitats, concordance varied by square; most show good concordance, but some (e.g., 773, 261) show lower matches.
  - The analysis highlights both general agreement and local mis-matches, informing habitat definition refinements.

- 6.4 Polygon species attributes
  - 1,081 QA polygons and 998 CS polygons spatially matched; about 45% of QA polygons had at least one species matching the CS polygon at the same location.
  - Higher species-match concordance in certain habitats (e.g., woodlands, Improved Grassland); mosaics and upland mosaics complicate species comparisons.

- 6.5 Species concordance within matched polygons
  - Species-level concordance around 40% for commonly recorded species; QA tends to record more species.
  - Dominant or conspicuous species (e.g., Lolium perenne) show relatively higher concordance.

- 7 Linear features
  - Aggregate lengths: generally small differences between QA and CS across most squares.
  - Land-use theme consistency: high agreement on linears (e.g., fences vs walls) with minimal mismatches; some potential confusion between belts of trees (FO) and woody features (WNS/WUS).

- 8 Points
  - Point feature totals across squares show minor differences; land-use themes for points (e.g., FO, IL, IW, ST, VT) are largely consistent between datasets.

- 9 Change recording
  - Change coding (Real change, Error change, No change) generally consistent with QA, but the “change” field is complex, especially for habitat-based changes.
  - Digital field change capture facilitated clearer documentation of changes and aided QA auditing.
  - Some definitional and training gaps remained, notably regarding Blanket Bog and urban vs improved grassland classifications.

## Habitat and Data Quality Insights

- Blanket Bog and upland habitats present the most challenging disagreements between surveyors and QA, driven by evolving definitions and fine-grained distinctions in field keys.
- Mosaics in upland squares (e.g., 261, 765, 1113) create matching difficulties when disaggregating to component Broad Habitats.
- Machair on Scottish sand dunes posed a local anomaly: neutral/ improved grassland proxies could misrepresent certain dune habitats.
- Woodland classification issues (Broadleaf vs Conifer) partly arise from historic field-handbook interpretations; most situations remain robust due to predominant habitat type dominance, but some edge cases require refinement.

## Implications for GIS Data Products and Standards

- Digital in-field mapping with mandatory attributes and visit-status workflows improves data quality and timeliness for GIS analyses.
- QA demonstrates strong overall alignment between field-collected data and QA assessments, providing confidence in map-based products and national spatial dataset integration.
- The study identifies specific areas where habitat definitions and recording rules need clarification or refinement (notably Blanket Bog, urban grassland allocations, and upland mosaic handling) to tighten standards for future surveys.
- Training and experiential learning reduce misclassification, particularly for complex habitats; ongoing guidance and updated field keys are warranted.

## Practical Takeaways for GIS Specialists

- Expect high overall agreement between field-mapped data and QA results, with most habitat types aligning closely at both aggregate and raster levels.
- Pay attention to habitat-definition nuances that drive misclassification (e.g., Blanket Bog, Neutral vs Improved Grassland, coniferous vs broadleaved woodland) when integrating 2007 data into modern GIS workflows.
- For change tracking in GIS pipelines, utilise the digital “change” field to maintain a robust audit trail, while acknowledging potential interpretation challenges in complex habitats.
- When aggregating data across mosaicked upland squares, implement careful handling to avoid over-interpretation of mis-matches arising from mosaic disaggregation.
- Use rasterized and 100-point analyses as complementary QA checks to validate spatial placement of habitats beyond simple area/length summaries.