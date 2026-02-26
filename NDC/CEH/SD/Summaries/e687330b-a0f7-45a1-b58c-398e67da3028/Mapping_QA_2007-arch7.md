# Mapping Quality Assurance Exercise

- Purpose: Assess quality of digital habitat/landscape mapping from Countryside Survey 2007, ensuring compatibility with previous methods and enabling integration with national spatial datasets via a geodatabase.
- Context: Digital field mapping with Surveyor software reduces interpretation subjectivity, enables in-field data capture of mandatory attributes, and supports early QA via an interactive wiki.
- Scope: QA of 23 one-kilometre squares across GB, covering area, linear, and point features; multiple analytic approaches to compare surveyor data with QA assessments.

## Data, Tools and Processes

- Data and formats
  - Field data captured digitally on tablets; uploaded to a geodatabase; QA checks performed through an interactive wiki.
  - Spatial data includes Broad Habitats, linear features, and point features; attributes include primary and secondary habitat/feature data and dominant species.
- QA approaches
  - Direct comparison: aggregate areas/lengths/points per square (CS vs QA).
  - Raster comparisons: convert polygons to 10 x 10 m rasters within each 1 km square to compare abundance and spatial placement of Broad Habitats.
  - 100-point grid: overlay on each square to assess concordance of Broad Habitats at fine resolution; score matches/mismatches.
  - Attribute-level comparison: reference ID layers for polygon attributes to compare species and other primary attributes.
- Field and data quality
  - QA teams often surveyed on squares distinct from plot QA; used global masks to compare only common surveyed areas.
  - Visit-status layers and mandatory fields improved data completeness and consistency; small areas of “not visited” and “refused access” acknowledged.

## Key Findings by Analysis Type

- 6.1 Direct aggregate comparison (area/extent)
  - BH presence concordant in 81% of squares between CS and QA.
  - Mean differences for many Broad Habitats generally under 3.5% (some <1%), but several habitats show higher variability (e.g., Improved vs Neutral Grassland; Dwarf Shrub Heath; Bog; Urban).
  - Indicates overall good agreement with habitat allocations, though some habitat-specific discrepancies exist.

- 6.2 Raster data comparison
  - Overall raster agreement across squares averaged around 76% (varied by square; some high, some low).
  - Notable high agreement in squares like 364, 488; lower agreement in squares 261 and 773.
  - Habitat-by-habitat agreement tables show varying concordance; urban, bog, grasslands, and dune-related habitats frequently highlighted as areas with discrepancies; machair on Scottish dunes discussed as an anomaly.

- 6.3 100-point concordance
  - General good concordance for many squares; some squares show substantial mismatches (e.g., 773, 261).
  - Differences attributed to mosaics and upland habitats, which are more variable at small scales; mosaic disaggregation can produce mismatches when like BHs are broken into component BHs.
  - Blanket Bog and related upland habitat definitions (and differences between DVH and QC interpretations) identified as key sources of misclassification, with square-specific issues (e.g., 773).

- 6.4 Polygon/species attributes
  - 1081 QA polygons and 998 CS polygons matched spatially; only 45% of QA polygons contained at least one species also listed in the matched CS polygon.
  - Species concordance across matched polygons around 40% overall; higher for certain habitat types (woodlands, improved grassland) where dominant species are clearer.
  - Dominant species lists show substantial variation between QA and CS, often reflecting habitat-class decisions and dominance shifts; Lolium perenne and other common species show higher agreement.
  - Indicates modest concordance for species lists, with larger discrepancies for complex or diverse habitats, and stronger alignment for more homogeneous vegetation types.

## Other Analytical Findings

- Linear features (7) and points (8)
  - Linear features show high consistency in land-use theme allocations between QA and CS, with few cases where QA recorded a feature that CS did not.
  - Major distinctions mainly arise between closely related feature classes (e.g., FO vs WNS/WUS); overall consistency is high.
  - Points: high consistency in habitat codes for matched points; some confusion between woodland codes due to legacy classifications.

- Change recording (9)
  - Change coding (Real change, Error Change, No change) generally aligned between QA and CS; digital recording allowed more detailed change annotations.
  - Some surveyors struggled initially, but overall change coding agreement was good; change assessment remains challenging for habitat-based changes.

## Implications for GIS Practice

- Data quality and integration
  - Digital field collection, mandatory attributes, and wiki-based QA improve data consistency and facilitate integration with national-scale datasets in a geodatabase.
  - Habitat definitions and classification boundaries (e.g., Blanket Bog, Broadleaf vs Coniferous Woodland, Neutral vs Improved Grassland) require ongoing refinement to reduce misclassification, especially in upland mosaics and edge habitats.
  - Mosaic areas in upland/heath and machair contexts present particular challenges for strict BH allocation consistency; may benefit from revised rules or hierarchical classifications.

- Methodological considerations
  - Raster and 100-point analyses provide complementary views of agreement; reliance on a single method could mask spatial or thematic biases.
  - Training and clear field guidance are crucial to minimize interpretation differences (e.g., blanket bog criteria, urban vs improved grassland thresholds).

- Data quality takeaways for GIS specialists
  - Expect some habitat-level discrepancies in transitional zones and mosaics; plan for reconciliation steps when merging CS and QA data.
  - Use the 1 km grid, rasterized comparisons, and 100-point concordance to validate large datasets and to identify squares needing re-evaluation or definition refinement.
  - Maintain robust metadata on definitions, especially for contested habitats ( Blanket Bog, urban grasslands, dune habitats with machair) to support future harmonization.

## Conclusions and Recommendations

- Overall, the 2007 digital mapping QA demonstrates substantial agreement between surveyors and QA analyses, with high consistency across many habitat classes and features.
- The digital approach enabled more thorough QA and early data validation, improving data quality and readiness for national-scale GIS integration.
- Key issues to address in future work:
  - Refine habitat definitions and allocation rules for problematic habitats (e.g., Blanket Bog, Dwarf Shrub Heath, Neutral vs Improved Grassland; urban mappings).
  - Improve handling of upland mosaics and locally rare habitats (machair) to reduce cross-classification ambiguities.
  - Enhance training and guidance for field teams to minimize habitat misallocations and changes in interpretation over time.
  - Continue cross-validation using multiple QA methods (vector vs raster vs point grids) to ensure robust data consistency before broader dissemination.

- Overall takeaway for GIS specialists: the exercise validates the use of digital mapping and integrated QA workflows for reliable, map-based data products, while highlighting specific habitat-definition challenges that require ongoing refinement to optimize spatial analyses and decision support.