# Mapping Quality Assurance Exercise

- Aim and context
  - Quality Assurance (QA) exercise for Countryside Survey 2007 delivering high-quality habitat and landscape data, compatible with prior approaches and suitable for rapid analysis in a geodatabase.
  - Shift to digital mapping in the field (Surveyor software) to reduce interpretation error, improve data clarity, and enable early data checks via a wiki.
  - QA integrated with field data collection through staff checks, QA visits, and early feedback loops to refine protocols.

- Data collection and tooling
  - Digital mapping conducted in the field using Surveyor; mandatory fields and prompts reduce handwriting/spelling issues; visit status layers track coverage.
  - Data uploaded to an interactive wiki for early data checking; QA teams conducted in-field visits to ensure protocol adherence.
  - Outputs stored in a geodatabase enabling direct comparisons with Countryside Survey (CS) data and other national spatial datasets.
  - 2007 QA covered 23 one-kilometre squares; QA squares were preferentially selected across land classes and locations to represent GB.

- QA approaches and analyses
  - 4.1 Direct comparison: aggregate areas/lengths/points by square, land class, and Broad Habitat (BH) types; SAS used for statistical comparison.
  - 4.2 Raster data comparisons: convert polygons to 10,000 10x10 m cells per square; compare absolute BH areas and locations; sampling via resolution grids.
  - 4.3 100-point grid: overlay 10x10 point grid per square to assess concordance of BH allocation; identifies mismatches at ~100-point resolution.
  - 4.4 Attribute comparisons: matched reference IDs to compare species attributes within polygons.
  - 6.1–6.4 Polygon, raster, and species analyses: examined congruence in BH allocations, species lists, and habitat coding; highlighted sources of discrepancy (e.g., Blanket Bog, upland mosaics, urban classifications).

- Key findings and interpretation
  - Overall high agreement between CS surveyors and QA data for many BHs; average concordance in raster-based BH maps commonly around 70–90% across squares; some squares showed lower agreement (e.g., 261, 773).
  - Minor yet notable differences in BH allocations across several habitats; issues often tied to:
    - Neutral vs Improved Grassland overlap and decisions at boundaries.
    - Woodland classification (Broadleaf vs Coniferous) and legacy coding practices.
    - Upland mosaics and mosaic-to-single-BH mappings causing mismatches.
    - Machair-related anomalies on Scotland’s sand dunes; largely contained to localised areas.
  - Blanket Bog posed particular definitional challenges; updated field handbook in 2007 led to mis-matches with Dwarf Shrub Heath; highlights need for clear, updated definitions and training for complex upland habitats.
  - Change recording (Real Change, Error Change, No Change) generally aligned between CS and QA, but some surveyors faced initial difficulties with the new digital change field; overall strong adherence to protocols.

- Outputs and data quality implications
  - Digital workflow and QA integration improved in-field data verification, enabling earlier identification of issues and potential reallocation of features.
  - The QA exercise demonstrated strong overall data quality with transparent documentation of discrepancies and potential definitional ambiguities to inform future survey iterations.
  - Findings informed recommendations for training, definition clarifications (especially for Blanket Bog and woodland classifications), and future QA design to handle mosaics and upland variability more robustly.

- Specific areas of attention for data support
  - Improved and Neutral Grassland distinctions require careful interpretation at boundaries; ensure consistent application across CS and QA.
  - Woodland definitions: reinforce 80% conifer cover criterion for Coniferous Woodland and ensure field handbook reflects current definitions to minimize misclassification.
  - Upland mosaics: account for co-occurring BHs within mosaicked areas; consider disaggregation approaches to improve match accuracy.
  - Urban classifications: clarify when amenity grassland over 1 ha should be recorded as Improved Grassland to reduce inconsistencies.
  - Blanket Bog: continue refining definitions and field guidance; acknowledge potential for overlap with Dwarf Shrub Heath in complex sites.

- Change recording and future work
  - The change field facilitated updating incorrect previous mappings; advances in data tidiness and field verification were achieved, though some surveyors needed time to adapt to the new system.
  - Ongoing analyses planned to refine BH definitions, improve inter-team consistency, and address identified hotspots of disagreement (e.g., Blanket Bog, urban, and upland mosaics).