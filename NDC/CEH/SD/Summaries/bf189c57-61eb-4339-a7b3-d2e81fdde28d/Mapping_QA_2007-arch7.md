# Mapping Quality Assurance Exercise

- Overview
  - 2007 Countryside Survey introduced digital mapping to provide high-quality, field-m mapped habitat and landscape feature data compatible with national spatial datasets (geodatabase).
  - Shift from post-survey digitisation of overlaid paper maps to field mapping with Surveyor software; mandatory fields and prompts reduced interpretation subjectivity and handwriting issues.
  - Early data checks via an interactive wiki; QA teams conducted field visits to ensure protocol adherence.
  - QA aimed to assess accuracy of mapped data against CS field data across 23 1-km squares, with broader implications for data quality, standards, and GIS analyses.

- Extent and data management
  - QA covered 23 1-km squares; some areas were inaccessible or refused access, so analyses focused on common inspected areas.
  - Whole squares mapped for QA and used a mask overlay to align with CS data; data uploaded to a geodatabase for analysis.
  - Digital system enabled visit-status tracking, enhanced species recording, and better attribute capture.

- Analytical approaches (sections 4.x)
  - 4.1 Direct comparison of aggregate areas/lengths/points for each square (CS vs QA data, by Square, Land Class, Broad Habitat).
  - 4.2 Raster data comparisons
    - Convert polygons to 10 x 10 m raster cells within each 1-km square; assign dominant Broad Habitat per cell.
    - Sample using a resolution point grid to compare absolute extents and locations of Broad Habitats.
  - 4.3 100-point grid analysis
    - Overlay a 10 x 10 grid; record concordance/discordance of Broad Habitats per point; highlights spatial agreement at comparable resolution.
  - 4.4 Attribute comparisons
    - Generated reference ID layers to compare species attributes within matched polygons (areas, lines, points).
  - Surveyor efficiency and data capture
    - Use of visit-status layers reduced missed areas; average not-visited areas very small (approx. 0.4% in some squares).
    - Mandatory fields increased recording of dominant species.

- Key results and interpretation (sections 6–9)
  - 6.1 Direct comparison of aggregate square-level habitat extents
    - In 81% of cases, the Broad Habitat in a square was recorded by both CS and QA.
    - Mean differences in proportions for many BH types were under 1–3%; some habitats showed larger deviations (e.g., Improved grassland, Dwarf Shrub Heath, Bog, Urban).
    - Notable issues linked to:
      - Neutral vs. Improved Grassland overlap in species composition.
      - Woodland classification definitions (Broadleaf vs Coniferous); potential misapplication of woodland thresholds.
      - Upland mosaic mapping leading to mismatches when mosaics are disaggregated into component BHs.
      - Machair on Scottish dunes as a local anomaly.
      - Blanket Bog definition revisions affecting comparisons, with major mismatches between Dwarf Shrub Heath and Blanket Bog in some squares (notably 773).
  - 6.2 Raster data comparisons
    - Across squares, raster agreement (Broad Habitat matches) ranged widely; average concordance generally high (e.g., 364: ~98%, 488: ~94%), but several squares performed poorly (e.g., 261: ~49%, 773: ~23%).
    - Table 6.2b highlights per-square agreement by BH type; most BHs showed substantial agreement, with some exceptions (e.g., Neutral vs Improved Grassland, Urban vs grassland, Sand Dune PHs in Scotland).
  - 6.3 100-point grid (primary land cover codes and habitats)
    - Overall concordance good for many squares; certain squares showed notable mismatches (773 and 261 again).
    - 6.3b matrix indicates most Broad/Priority Habitats matched, with some exceptions across specific codes (e.g., Sand Dune-related codes, Blanket Bog vs Dwarf Shrub Heath).
  - 6.4 Polygon species attributes
    - 1,081 QA polygons and 998 CS polygons matched spatially; 45% of QA polygons had at least one listed species present in the matched CS polygon.
    - Species concordance across matched polygons around 40%; Improved Grassland and woodlands tended to have higher species concordance.
    - Lolium perenne showed relatively high concordance (66% of common occurrences between QA and CS when present).
  - 7.1 Linear features
    - Length-based comparison showed generally small differences between QA and CS lines within squares.
    - Land-use themes for linears (e.g., fences, walls, hedges, belts of trees) showed high consistency; some confusion between FO (belts of trees) and WNS/WUS (woody lines) potential but not widespread.
  - 8.1 Point features
    - Summary of points by land-use themes showed minimal differences; a few habitats/sites differed (e.g., urban points, veteran trees) due to subjective field judgments.
    - Point codes generally well aligned between QA and CS datasets.
  - 9 Assessment of change recording
    - Change field introduced to log real changes, error changes, or no change; allowed updating previous maps when applicable.
    - Analysis showed good agreement for change coding across broad habitats, though some habitat-specific discrepancies (e.g., Blanket Bog) persisted.
    - The digital workflow helped surveyors tidy and verify change data in-field, but some surveyors required time to adapt to the new process.

- Implications for GIS practice
  - Digital mapping in 2007 improved data quality, standardization, and speed; however, challenges remain in:
    - Definitional clarity for certain habitats (notably Blanket Bog) and for mosaics in upland areas.
    - Handling of habitat intergradations and overlaps (Neutral/Improved Grassland; Broadleaf/Coniferous woodland).
    - Interpreting and reconciling 1-km square mosaics across scales and resolutions.
    - Training and consistency in applying habitat definitions to reduce misclassifications.
  - The QA framework demonstrates robust methods to quantify spatial agreement across multiple data representations (polygon, raster, point grid) and to diagnose specific problem areas for targeted improvement.
  - Data standardization, clear field keys, and ongoing calibration are essential for reliable GIS analyses using national-scale habitat datasets.

- Conclusions
  - The 2007 Mapping Quality Assurance Exercise shows substantial overall agreement between CS surveyors and QA assessors, with high data quality achieved through digital mapping, standardized fields, and proactive QA checks.
  - Some habitat-specific discrepancies (notably Blanket Bog, Sand Dune PHs, and upland mosaics) indicate areas for definitional refinement and training.
  - The combination of direct square comparisons, raster and 100-point analyses, and polygon-level attribute evaluations provides a comprehensive framework to ensure GIS-ready data quality and to guide future survey improvements and standardization efforts.