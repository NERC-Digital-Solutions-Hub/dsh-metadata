# Mapping Quality Assurance Exercise

- A 2007 Countryside Survey QA study validating digital mapping quality, data consistency with previous methods, and suitability for integration into a national geodatabase.
- Focuses on data governance, metadata, and usability for analysis by others, using a digital workflow to improve data accuracy and traceability.

## Data and Systems

- Data captured with Surveyor software in the field; mandatory fields and prompts to ensure consistent feature data (areas, lines, points).
- Data uploaded to an interactive wiki for early data checks; QA teams conducted field visits to ensure adherence to protocols.
- Final outputs stored in a geodatabase; digital mapping enabled direct, post-field QA against 1998 CS data.
- Processes include masking unsurveyed/refused areas and aligning CS survey data with QA datasets for direct comparison.
- Analyses include direct area/length/point comparisons, raster-based habitat comparisons, and a 100-point grid concordance assessment.

## QA Methodologies

- 4.1 Direct comparison of aggregate areas for whole squares.
- 4.2 Raster data comparisons: 1 km squares subdivided into 10,000 cells (10x10 m); dominant Broad Habitat assigned per cell; comparison of habitat totals and locations.
- 4.3 100-point grid overlay: 100 sample points per square to assess concordance of Broad Habitats and compute agreement percentages.
- 4.4 Attribute comparisons: reference IDs used to compare species attributes within matched polygons.

## Key Findings

- Overall consistency: High agreement between CS surveyors and QA team across many habitat classes; discrepancies concentrated in a subset of habitat types and in upland mosaics.
- Square-level habitat agreement: 81% of squares had both CS and QA recording the same Broad Habitat; mean differences in proportional areas typically under 3.5% across many habitats; some habitats showed larger SDs indicating potential misallocation.
- Notable habitat-specific issues:
  - Blanket Bog vs Dwarf Shrub Heath: major source of mis-matches in uplands; revised 2007 field handbook influenced allocations.
  - Neutral vs Improved Grassland: overlap in species assemblages led to potential reallocation between these two BHs.
  - Woodland definitions: need for consistent application of Broadleaf vs Coniferous woodland; some confusion due to past allocation methods and changes in definitions.
  - Upland mosaics: mosaicked habitats led to mismatches when disaggregated into constituent Broad Habitats.
  - Urban vs grassland allocations: occasional ambiguity in classifying amenity grassland vs urban-related grassland.
- Raster data (percentage agreement per square): average agreement around 76%; some squares very high (364, 488) and others relatively low (261, 773).
- 100-point grid concordance: overall good agreement for many squares; notable poor matches in squares 773 (19%) and 261 (41%); general concordance varied by square.
- Habitat-by-habitat details (bit more context):
  - Broadleaved Mixed and Yew Woodland and Coniferous Woodland: substantial agreement but some misallocations.
  - Arable & Horticulture, Improved Grassland, Neutral Grassland, Acid Grassland, Bracken, Dwarf Shrub Heath, Fen/Marsh/Swamp, Bog, and Standing Open Water showed mixed levels of concordance depending on square and landscape context.
  - Some discrepancies linked to how machair (sand-dune-associated habitat) is categorized.
- Species attributes in polygons:
  - Matched species in 45% of spatially matched polygons; higher concordance in woodlands and Improved Grassland.
  - Overall species concordance ~40% across commonly recorded species; dominance of certain species (e.g., Lolium perenne) increased match likelihood.
- Change recording:
  - Digital system enabled richer change coding (Real change, Error change, No change); some surveyors initially struggled, but overall high agreement between CS and QA on change classifications.
  - Change logging supported updating previous maps, though habitat-level change assessment remained complex.

## Data Quality and Governance Implications

- Definitions and standards:
  - Need for clear, stable definitions for Broad Habitats (notably Blanket Bog, Dwarf Shrub Heath, and woodland categories) to minimize reallocation discrepancies.
  - Ensure woodland definitions align with field handbook criteria (trees/shrubs cover thresholds, coniferous vs broadleaved classification).
- Training and consistency:
  - Targeted training to address upland mosaics and the interaction between adjacent habitat types.
  - Emphasis on consistent handling of mosaics, especially where habitats grade into one another.
- Change management:
  - Robust change-coding framework (Real, Error, No Change) improves longitudinal data integrity but requires ongoing guidance and QA feedback loops.
- Metadata and provenance:
  - Digital workflow enhances data provenance (who changed what, when, and why) via wiki and geodatabase logs.
  - Tables and matrices (e.g., 6.3b, 6.2b) illustrate agreement levels by habitat, square, and data type; metadata should capture these QA metrics for future reuse.
- Data sharing and interoperability:
  - The geodatabase approach supports multi-dataset analysis and compatibility with other national spatial datasets, fulfilling the data steward aim of discoverable, reusable data with clear lineage.

## Challenges Highlighted

- Access limitations and mosaics leading to incomplete coverage in some squares.
- Complexity of comparing mosaicked upland habitats across different mapping approaches.
- Machair and other localized habitats may create edge-case misallocations due to unique community compositions.
- Higher complexity and potential mismatch when translating field-based habitat keys into consistent GIS codes across large, distributed survey teams.

## Endnotes and Recommendations

- The 2007 digital mapping approach substantially improved data quality and timeliness compared with prior methods, but some habitat definitions and upland mosaic mappings require ongoing refinement.
- Recommendations for Data Stewards:
  - Maintain and periodically update habitat definitions and the Field Handbook to reflect current scientific consensus and field experience.
  - Institutionalize ongoing training and QA reviews, especially for upland and mosaic habitats.
  - Preserve robust metadata, including detailed QA metrics by habitat, square, and data type, to support future reuse and governance.
  - Ensure clear documentation of change codes and workflows, with interfaces for updating previous maps as needed.
  - Leverage the wiki-enabled feedback loop to support collaborative data validation and rapid issue resolution.