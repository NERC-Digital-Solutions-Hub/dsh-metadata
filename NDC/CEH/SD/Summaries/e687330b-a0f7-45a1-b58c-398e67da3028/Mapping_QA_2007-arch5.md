# Mapping Quality Assurance Exercise

- Aims and context
  - Deliver high-quality, compatible habitat and landscape data suitable for rapid analysis and integration with national-scale spatial datasets.
  - Implement a digital mapping approach (2007) to reduce interpretation errors and improve data quality, with QA processes to verify accuracy.
  - Use mandatory fields, prompts, visit-status tracking, and early data checks via a wiki to enhance data integrity.

- Data collection and QA workflow
  - Field mapping in 2007 used Surveyor software; surveyors input required attributes with prompts, improving handwriting, spelling, and data completeness.
  - Data uploaded to an interactive wiki for early data checking; QA teams conducted site visits to ensure protocol adherence.
  - Quality Assurance (QA) leveraged three digital QA approaches to compare mapped data against the Countryside Survey (CS) data: direct area/length comparisons, raster-based comparisons, and 100-point sampling, complemented by attribute and species analyses.

- Extent and methods
  - QA mapping covered 23 1-km squares, selected to represent land class diversity; common surveyed areas excluded where access was refused.
  - QA and CS data were aligned using a common-masked framework to enable valid comparisons.
  - Analysis approaches:
    - 4.1 Direct comparison of aggregateAreas/Lengths/Points for whole squares (CS vs QA aggregates).
    - 4.2 Raster data comparisons (1-km square subdivided into 10,000 10x10 m cells to compare dominant Broad Habitats).
    - 4.3 100-point grid overlays to assess concordance of Broad Habitats at a fixed resolution.
    - 4.4 Attribute-based comparison of areas/linears/points with shared reference IDs.

- Surveyor efficiency and data completeness
  - Digital system and wiki-based checks improved use of visit-status layers; very small proportion of land not visited (average ~0.4% in many squares).
  - Mandatory fields improved attribute recording; surveyors tended to record more species per area in 2007.

- Key findings: habitat agreement and discrepancies
  - Broad Habitat presence in squares: 81% of cases had both CS and QA recording the same habitat in a square.
  - Proportional differences (CS vs QA) for most Broad Habitats were typically small (mean differences <1–3.5%), with some habitats showing larger variations (e.g., Improved/Neutral Grassland, Dwarf Shrub Heath, Bog, Urban, and Fen-related categories), often due to interpretation differences or mosaic mapping in upland areas.
  - 6.2 Raster data comparisons
    - Overall raster agreement across squares averaged about 76%, with some squares showing high concordance (e.g., 364, 488) and others lower (e.g., 261, 773).
    - Agreement by Broad Habitat varied by square; some habitats showed strong concordance, others weaker, reflecting coding differences and spatial mosaic issues.
  - 6.3 100-point concordance
    - General good agreement for many squares; some notable mismatches in a few squares (e.g., 773 and 261).
    - Concordance rates for Broad and Priority Habitats generally around 70–80% in many squares, with some lower (e.g., 261 at 41%).
  - 6.4 Polygon species attributes
    - 45% of QA polygons had at least one species matching the CS polygon in the same location.
    - Species concordance was higher for woodlands and Improved Grassland; lower for Bracken and upland mosaics.
    - A wide list of commonly recorded species showed mixed concordance between QA and CS datasets; Lolium perenne had relatively higher concordance (66%) among the most common species.
  - 7–8: Linear and point features
    - Linear features: high consistency between QA and CS in land-use theme classification for lines; minimal cases where QA had a feature not mirrored by CS.
    - Points: high consistency in habitat codes for points; some confusion around woodland/forest codes due to legacy usage.
  - 9: Change recording
    - Change coding (Real change, Error change, No change) generally aligned between CS and QA across broad habitats and linear/point features.
    - The digital system allowed more detailed change coding, though some surveyors faced initial complexity.

- Notable methodological and definitional issues
  - Habitat definitions and classification differences
    - Important discrepancies in Neutral vs Improved Grassland; broadleaf vs coniferous woodland allocations; upland habitat mosaics leading to mismatches.
    - Blanket Bog proved particularly challenging due to evolving definitions; mis-matches often occurred with Dwarf Shrub Heath when both could appear in the same location.
  - Mosaic and spatial variability in upland habitats
    - Mosaic mappings and small-scale variability complicated direct one-to-one habitat allocation; disaggregation of mosaics could inflate mismatches.
  - Machair and Sand Dune variations
    - Machair in Scottish sand dunes represented an anomaly, often aligning with Neutral/Improved Grassland, highlighting location-specific habitat nuances.
  - Urban and grassland interactions
    - Some urban areas were recorded as Improved Grassland; ongoing review of field handbook guidance for urban classifications.

- Data governance and stewardship implications
  - Metadata and provenance
    - Maintain clear lineage: original CS data, field-collected QA data, digital processing steps, and any re-allocations due to change coding.
  - Standards and definitions
    - Reinforce consistent habitat definitions and woodland classifications across surveys; update field manuals as definitions are revisited (e.g., Blanket Bog, machair, urban grasslands).
  - Training and capacity building
    - Targeted training for challenging habitats ( Blanket Bog, upland mosaics, machair) to reduce misclassifications and improve inter-analyst concordance.
  - Data interoperability and storage
    - Continue geodatabase approach to enable integration with other national datasets; ensure versioning and change-tracking are preserved.
  - Usability and discoverability
    - Document QA outcomes, with clear notes on known issues and square-specific caveats; provide guidance for data users on interpretation of mosaic areas and habitat boundaries.

- Overall conclusions and opportunities for improvement
  - The shift to digital data collection and QA in 2007 substantially improved data quality, timeliness, and in-field validation compared with prior practices.
  - For the majority of Broad Habitats, QA and CS data show good agreement, indicating robust data governance and collection pipelines.
  - Some habitats and squares require refinement of definitions, more consistent application of habitat keys, and enhanced training to minimize discrepancies in future surveys.
  - Future work proposed includes refining habitat definitions (notably Blanket Bog), examining upland mosaics, and further analyzing species-level concordance to inform habitat allocation rules and potential field handbook updates.

- Practical takeaways for Data Stewards
  - Ensure ongoing alignment of habitat classification criteria between survey teams and QA assessments; update documentation accordingly.
  - Maintain robust metadata and lineage; track changes with explicit change-codes and rationale.
  - Invest in targeted training for difficult habitats and mosaic landscapes; consider additional QA rounds for high-variance squares.
  - Preserve and expose the digital QA workflow (Surveyor, wiki checks, geodatabase integration) to support reproducibility and future data governance across datasets.