# Mapping Quality Assurance Exercise

- Overview
  - 2007 Countryside Survey aimed to produce high-quality, field-m mapped data compatible with national datasets in a geodatabase.
  - Transition to digital mapping in 2007 using Surveyor software to reduce interpretation errors and handwriting issues.
  - Early use of an interactive wiki for data checking; QA teams performed field and office checks to ensure protocol compliance.
  - QA compared surveyors’ mapped data against a QA dataset across 23 1-km squares, aiming to assess mapping quality and identify data issues.

- QA Scope and Extent
  - QA covered 23 squares (representing diverse land classes and locations across Great Britain); some areas were refused access.
  - QA activities largely occurred in squares different from those used for plot and freshwater QA to broaden coverage.
  - Data were collected via standard CS tablets and software, then combined into a single geodatabase; analyses used common surveyed areas.

- Methodology and Analyses
  - Direct, aggregate comparisons: CS (surveyors) vs QA data compared for areas, lengths, and points within each square using statistical methods (e.g., SAS).
  - Raster data comparisons: 1 km squares subdivided into 10,000 10x10 m units; dominant Broad Habitat (BH) per unit used to compare absolute and spatial distributions; sampling grids enabled cross-dataset comparisons.
  - 100-point grid analysis: overlaid 10x10 point grid to assess concordance of BH/PH mappings at a consistent, prior QA resolution; measured concordance and discrepancies per square.
  - Attribute-level analyses: reference ID layers enabled comparisons of species and habitat attributes across matched polygons.
  - Linear features: 100-point analyses were less suitable; linear features buffered (5 m) and compared by land-use themes; results showed strong consistency in land-use classifications.
  - Point features: buffers used to compare habitat codes at feature points between QA and CS datasets; generally high agreement.
  - Change recording: new digital change fields captured Real Change, Error Change, and No Change; surveyors and QA teams compared change classifications to assess consistency.

- Key Findings: Habitat Extent and Agreement
  - Overall agreement for Broad Habitats (BHs) between CS and QA was high in aggregate analyses; many habitats showed differences below 1–3% of square extents.
  - 81% of squares had CS and QA both recording the same BH in a given square; remaining cases showed small but notable differences.
  - Some BHs showed larger discrepancies or higher variability (SD > 5%) in certain habitats:
    - Improved grassland, Neutral grassland
    - Dwarf Shrub Heath, Bog
    - Urban areas and sub-littoral sediments
  - Blanket Bog and its relationship to Dwarf Shrub Heath posed definitional and mapping challenges, particularly in upland squares; 2007 field handbook revisions highlighted these issues.

- Key Findings: Raster and 100-Point Analyses
  - Raster data concordance varied by square; average agreement across squares was around 76%, with higher concordance in some squares (e.g., 364, 488) and lower in others (e.g., 261, 773).
  - 100-point concordance averaged around 77% across BHs/PHs, with notable outliers:
    - Squares 773 (low concordance ~19%) and 261 (~41%) highlighted substantial mismatches.
    - Other squares ranged from ~53% to ~95% concordance, indicating generally good but variable alignment.
  - Cross-square analyses (6.3b) showed common misallocations between certain habitats (e.g., Neutral vs Improved Grassland, Broadleaf vs Coniferous woodland) and highlighted the complexities of upland mosaics and machair-like habitats.
  - Woodland classification issues were noted due to ambiguous definitions and historical practices; this affected a subset of squares and required further clarification.

- Key Findings: Species Attributes and Polygons
  - Species-level concordance within spatially matched polygons was moderate:
    - About 45% of QA polygons had at least one listed species present in the matched CS polygon.
  - For matched polygons,Overall species concordance was around 40% across commonly recorded species (e.g., Lolium perenne, Calluna vulgaris, Juncus spp.); some species showed higher agreement (e.g., Lolium perenne ~66% in common data).
  - Polygons with same BH often did not have the same dominant species recorded, reflecting differences in species composition and in how dominant species were selected.
  - A substantial portion of discordance was attributed to habitat-driven species selection and mosaics of habitats within polygons.

- Key Findings: Linear Features and Points
  - Linear features: strong consistency in land-use theme choices between QA and CS; most matched classifications were identical or highly compatible (e.g., fences vs walls).
  - Some potential confusion between forestry belts and woody linear features, but overall no systematic issues.
  - Points: strong agreement in habitat codes for matched point features; occasional confusion between woodland/forest coding due to legacy practices.

- Key Findings: Change Recording
  - Digital change fields allowed more detailed coding of changes (Real Change, Error Change, No Change).
  - Most habitat types showed good agreement in change coding between CS and QA, though some habitat types (notably Blanket Bog vs Dwarf Shrub Heath) showed higher disagreement due to definitional complexity.
  - The digital workflow improved the ability to update prior maps when errors were identified and to validate new data in the field, despite added complexity.

- Challenges and Notable Issues
  - Definitions and classification of certain habitats (notably Blanket Bog, Neutral vs Improved Grassland, and Woodland types) caused mismatches between CS and QA data.
  - upland mosaics and large habitat mosaics introduced mismatches when disaggregated into component BHs for comparison.
  - Machair-like sand dune habitats presented localized anomalies due to unique vegetation; these did not generally skew overall results but highlighted landscape-specific complexity.
  - Differences in species lists were influenced by habitat assignment and dominance criteria; equal habitat mapping did not always yield identical dominant species.

- Implications for Data Leaders and Data Strategy
  - The digital mapping and QA framework substantially improved data quality, timeliness, and the ability to compare across datasets; it supports better data governance, metadata clarity, and data discoverability.
  - High overall concordance demonstrates robustness of the mapping protocol, while identified areas for improvement inform updates to field handbooks and habitat definitions.
  - Training and experience significantly affect boundary cases (e.g., Blanket Bog, upland mosaics); ongoing staff development and clearer allocation rules are essential.
  - The results underscore the importance of standardized definitions, transparent metadata, and cross-team collaboration to maintain consistency across national datasets and partner networks.

- Recommendations and Next Steps
  - Refine and harmonize key habitat definitions (e.g., Blanket Bog, Broadleaf vs Coniferous woodland) and provide explicit guidance for mosaics and transitional habitats.
  - Extend and standardize training to reduce interpretation differences, especially for upland/mosaic areas and contested habitats.
  - Continue leveraging digital data capture and wiki-based validation to enable near-real-time quality checks and faster feedback loops.
  - Consider targeted follow-up QA in squares with low concordance (e.g., 261, 773) to understand context-specific drivers of disagreement and update methodologies accordingly.
  - Use the change-recording insights to further streamline field processes and improve historical map alignment with current data.

- Conclusion
  - The Mapping Quality Assurance Exercise demonstrates strong overall alignment between surveyors and QA teams across multiple data dimensions (habitat extents, raster and point data, linear features, and change records) while also identifying key definitional and regional challenges.
  - The digital QA framework provides a robust foundation for ongoing data quality improvements, with clear opportunities for refining habitat definitions, improving training, and enhancing collaboration across data networks.