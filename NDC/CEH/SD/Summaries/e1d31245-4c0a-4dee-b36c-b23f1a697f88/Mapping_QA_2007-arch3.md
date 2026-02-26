# Mapping Quality Assurance Exercise

- Purpose and context
  - Evaluates the quality and compatibility of digital mapping data from Countryside Survey 2007 with field survey data to enable rapid analysis and integration with national datasets.
  - Demonstrates how digital mapping reduces subjectivity and errors compared with post-survey digitisation of paper maps.

- Data collection and QA methods
  - In-field mapping using Surveyor software with mandatory fields and prompts; data uploaded to an interactive wiki for early QA; QA teams conducted field visits to ensure protocol adherence.
  - QA approaches used:
    - Direct comparison of aggregate areas/lengths/points for whole 1 km squares (CS vs QA data).
    - Raster data comparisons: converting polygons to 10 x 10 m cells, assigning dominant Broad Habitat, then comparing QA vs CS raster grids.
    - 100-point grid comparisons: overlaid points to assess concordance of Broad Habitats at a fine resolution.
    - Attribute-level analyses for areas, lines, and points using reference ID layers.
  - Additional analyses addressed surveyor efficiency (visit status layers, species recording) and data governance implications.

- Data and governance insights
  - Digital data collection enhanced QA capabilities and allowed direct digital comparisons; mandatory fields improved attribute recording; data sharing via wiki supported early checks.
  - Barriers noted for data sharing and metadata: public sharing requirements and metadata gaps can impede data use; governance processes are needed to ensure datasets meet standards and remain up-to-date.

- Key findings: agreement and discrepancies
  - 6.1 Direct aggregate comparison
    - In 81% of squares, Broad Habitats (BH) identified by CS and QA agreed on presence.
    - Mean differences in BH extents typically under 1–3.5% across habitats; larger SDs (>5%) flagged for certain habitats (e.g., Improved/Neutral Grassland, Dwarf Shrub Heath, Bog, Urban, and some upland types).
    - Notable definitional issues highlighted for Blanket Bog and related upland habitats, with some misclassifications due to habitat boundaries and evolving key definitions.
  - 6.2 Raster data comparisons
    - Overall raster agreement averaged around 76%, with highs in several squares (e.g., 364, 488) and lower agreement in others (e.g., 261, 773).
    - Discrepancies often linked to mosaic upland mapping, definitional nuances (e.g., Blanket Bog vs. Dwarf Shrub Heath), and local habitat peculiarities (machair in Scotland).
    - Differences by BH type documented; urban and dune-related habitats occasionally misaligned due to interpretation and landscape context.
  - 6.3 100-point concordance
    - Generally strong concordance across many squares; some outliers show substantial mismatch (e.g., squares 773 and 261).
    - Concordance and mismatch patterns summarized for both BH and priority habitats.
  - 6.4 Polygon analysis of species attributes
    - 45% of QA polygons had at least one matching species with the CS polygon at corresponding locations.
    - Higher species concordance for woodlands and Improved Grassland; more diverse flora in other grasslands reduced matching species.
    - Species concordance overall around 40%, with Lolium perenne and other common species showing varying levels of agreement.
  - 7 Linear features
    - Length-based comparisons showed generally small differences between QA and CS data; high consistency in land-use themes for linears with limited mismatches between surveyors.
  - 8 Points
    - Point feature comparisons indicated overall good alignment between QA and CS; some differences in habitat coding for point-based features (e.g., woodland codes) noted.
  - 9 Change recording
    - Change coding (Real Change, Error Change, No Change) collected in digital format; substantial agreement between CS and QA for most habitats and linear/point features.
    - Change assessment remains complex for habitat-level changes, but digital workflows improved data tidiness and update capabilities.

- Habitat-specific interpretive notes
  - Blanket Bog vs Dwarf Shrub Heath: major source of mismatches in upland squares due to evolving definitions; training and refined keys recommended.
  - Urban and Grassland classifications: some inconsistencies traced to recording guidance (e.g., amenity grass vs. Improved Grassland) requiring clearer field protocols.
  - Sand dune machair: Scotland-specific dune habitat caused anomalies; suggests localization considerations in habitat schemas.
  - Mosaic upland habitats: fine-scale mosaics complicate exact BH allocation and lead to mismatches when disaggregating mosaics into constituent BHs.

- Implications for monitoring frameworks
  - Data quality and standardization
    - Strong case for digital data capture and integrated QA to improve accuracy and speed of analysis.
    - Need for comprehensive metadata, dataset provenance, and open data practices to support reuse and auditability.
  - Habitat definitions and training
    - Evidence that consistent, clearly communicated habitat definitions and ongoing training reduce misclassifications (notably Blanket Bog, Dwarf Shrub Heath, Urban, and dune habitats).
    - Consideration of mosaic and continuum concepts; potential need to back-allocate or refine allocation matrices for woodland and other continua.
  - Data governance and openness
    - Recognize and address barriers to data sharing; establish governance processes that ensure timely data access, documentation, and versioning.
  - Methodological refinements
    - Validation across multiple scales (square, raster, 100-point, polygon) provides robust QA; future monitoring should adopt similarly tiered QA approaches.
    - Use QA findings to inform changes in field manuals, data capture templates, and habitat keys.

- Recommendations and conclusions
  - Maintain and enhance digital QA processes in future surveys to sustain high alignment between surveyors and QA assessments.
  - Invest in harmonizing habitat definitions, improving metadata, and strengthening data governance to minimize barriers to data sharing and reuse.
  - Targeted training and clarification of ambiguous habitat categories (e.g., Blanket Bog, urban grassland, sand dunes) should be prioritized.
  - Leverage QA results to refine monitoring frameworks, ensuring data are comparable across time, scales, and datasets, and that policy decisions are informed by consistently mapped, well-documented environmental health measures.