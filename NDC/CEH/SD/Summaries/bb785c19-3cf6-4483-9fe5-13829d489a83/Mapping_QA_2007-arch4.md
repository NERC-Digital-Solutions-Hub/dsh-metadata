# Mapping Quality Assurance Exercise

- Purpose: Assess the quality and consistency of digital mapping data for Countryside Survey 2007, comparing surveyors’ field data with QA team assessments using a standardized geodatabase and digital workflow.
- Context: Transition to field-based digital mapping (Surveyor software) to reduce interpretation errors and improve data quality, with early QA via an interactive wiki and on-site QA teams.
- Scope: QA across 23 1-km squares (predominantly different land classes) using multiple analytical approaches to compare habitat extents, linear features, points, and species attributes against the 1998 baseline.

## Data System and Workflow

- Digital mapping implemented in the field with mandatory fields and visit-status layers; data uploaded to a wiki for early quality checks.
- QA teams conducted quality assessments in parallel, often in different squares from field teams to reduce bias.
- Data were aligned and masked to ensure comparable datasets (common surveyed areas), with unsurveyed or access-refused areas excluded from analyses.
- The QA framework included three main analysis approaches: direct aggregate comparisons, raster-based comparisons, and a 100-point grid comparison, plus polygon-level species attribute analysis.

## QA Methodology and Analysis Approaches

- Direct comparison (aggregate areas/lengths/points) for whole squares, using habitat, linear, and point feature types.
- Raster analysis: convert polygons to 10 x 10 m cells, assign dominant Broad Habitat per cell, and compare QA vs. surveyor rasters; sampling via a resolution-point grid.
- 100-point grid: overlay a 10 x 10 point grid to assess concordance of Broad Habitats at a fixed resolution; identifies conspicuous mismatches across squares.
- Attribute-level analysis: reference IDs for areas/lines/points to compare species attributes between QA and surveyor datasets.
- Efficiency/accuracy indicators: evaluation of surveyor coverage (visited vs not visited areas) and the number of species recorded per area.
- Change recording: introduced a change-coding scheme (Real change, Error change, No change) to document updates to prior maps and identify potential corrections.

## Key Findings and Metrics

- Overall data quality and agreement
  - Direct aggregate area comparison: in 81% of squares, both CS (surveyors) and QA recorded the same Broad Habitat (BH) presence; average differences in BH proportions were typically under 3.5%, with most BHs showing small mean differences and low standard deviations.
  - Raster data concordance: average across squares ~76% agreement, with some squares showing very high concordance (e.g., 364: 98%, 488: 94%) and others showing notable disagreement (e.g., 261: 49%, 773: 23%).
  - 100-point concordance: varying results by square; several squares showed high concordance (359: 92%, 364: 96%, 364: 95%), while others showed low concordance (261: 41%, 773: 19-23%).
- Habitat-specific insights
  - Most habitat differences were small; notable exceptions included Neutral vs Improved Grassland, Broadleaf vs Coniferous woodland, and certain upland habitats (Acid Grassland, Fen/Marsh/Swamp).
  - Blanket Bog emerged as a challenging habitat with substantial mis-match potential, driven by evolving definitions and the presence of mosaics with Dwarf Shrub Heath; Scottish squares were particularly problematic.
  - Urban classifications occasionally overlapped with Grassland categories, suggesting recording-clarity issues for "Urban" vs "Amenity Grassland" in some cases.
  - Machair on Scottish dunes caused some anomalies (neutral/improved grassland labels) affecting habitat counts in a localized square.
- Species attributes and polygon-level analysis
  - 45% of QA polygons matched at least one listed species with the corresponding CS polygon (spatially matched polygons); overall species concordance across matched polygons was around 40%.
  - For commonly recorded species, concordance varied by habitat type; Lolium perenne showed relatively higher agreement (66% in CS vs QA for commonly recorded instances).
  - Species lists tended to be broader in QA data, reflecting more extensive in-field species listing.
- Change recording
  - Change coding generally aligned between CS and QA for most habitat types; however, a minority of cases showed discrepancies (e.g., Blanket Bog vs Dwarf Shrub Heath) due to habitat-definition ambiguities.
  - Introduction of the “change” field and more detailed change codes aided data maintenance but required training and clarity to minimize misclassification.
- Linear and point features
  - Linear features: high consistency in land-use theme choices (e.g., fences vs walls) with limited cross-category confusion; some Woody features (FO vs WNS/WUS) required careful interpretation.
  - Points: high agreement on habitat coding for points; few cases of woodland/forest misclassification due to historical coding practices.
  - Veteran trees showed the greatest discrepancy between CS and QA, reflecting the subjective nature of selecting dominant trees per species and the field directive to record up to a few significant trees.

## Habitat Classification Issues and Recommendations

- Definitions and standards
  - Blanket Bog and Dwarf Shrub Heath: need clearer, unified definitions to reduce cross-classification in upland mosaics.
  - Woodland classification: historical confusion between Broadleaved vs Coniferous, and the broader “Coniferous Woodland” vs “Broadleaf Woodland” definitions require refinement and consistent application.
- Mosaics and upland mosaics
  - Upland mosaics can produce matching questions across BHs; disaggregation into component BHs can lead to mismatches. Suggest improving mosaic-handling guidance and possibly probabilistic or fuzzy matching for mosaics.
- Urban and Grassland boundaries
  - Clarify criteria for recording Urban areas and for distinguishing between Neutral and Improved Grassland when urban edge effects exist.
- Localized habitats
  - Local habitats like machair require special-case guidance to avoid skewing national-scale analyses; maintain localized notes for region-specific habitat variants.
- Data governance implications
  - Standardized, clearly defined habitat keys and woodland definitions are essential for cross-survey comparability.
  - Training and guidance updates should accompany field manuals when definitions change or new habitats/variants are added.

## Species Attributes and Polygon-Level Findings

- Species-level concordance across spatially matched polygons is modest (around 40%), higher for certain habitat types (woodlands, Improved Grassland).
- QA data tend to record more species per area than CS data, but common dominant species show higher agreement (e.g., Lolium perenne, Calluna vulgaris, etc.).
- The presence of mosaics and habitat misclassification reduces the likelihood of matching species lists across QA and CS polygons.

## Change Recording and Data Stewardship

- Digital change recording enabled richer capture of change types (Real vs Error vs No change) and facilitated updates to prior maps.
- However, the complexity of change coding required upfront training and QC to ensure consistent use across teams.
- Change coding is more reliable for linear and point features than for some habitat-based polygons, highlighting the need for ongoing guidance on habitat-change interpretation.

## Implications for Data Leaders and Next Steps

- The digital, field-based Surveyor workflow significantly improves data clarity, timeliness, and the ability to QA against a geodatabase, but requires:
  - Clear, standardized habitat and woodland definitions to minimize cross-survey discrepancies.
  - Ongoing training and QA calibration, especially for complex habitats (e.g., Blanket Bog) and mosaic areas.
  - Region-specific guidance for localized habitats and variants (e.g., machair, urban grassland interactions).
- For data governance:
  - Maintain a robust metadata framework to document habitat definitions, data collection methods, and change coding decisions.
  - institutionalize the QA approaches (direct comparison, raster, 100-point) as standard practice for future surveys to ensure consistency and comparability.
  - Develop strategies to handle mosaics and uncertainty in upland areas, including potential probabilistic habitat assignments or higher-resolution validation in problematic squares.
- Future refinements:
  - Update field handbooks and training materials with lessons learned from Blanket Bog, urban grassland, and woodland classification challenges.
  - Explore enhanced approaches to species-level concordance, possibly integrating auxiliary data sources to improve matching of dominant species across polygons.
  - Consider scalable, automated reconciliation workflows to reduce manual reconciliation between CS and QA datasets while preserving traceability of changes.

- Overall takeaway: The 2007 mapping QA exercise demonstrates strong potential of a digital, QA-integrated data system for large-scale ecological mapping, with high overall agreement in many habitats and clear, actionable paths to address remaining gaps through standardized definitions, targeted training, and refined mosaic handling.