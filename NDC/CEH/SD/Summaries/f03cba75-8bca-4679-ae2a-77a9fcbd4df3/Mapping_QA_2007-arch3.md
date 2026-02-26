# Mapping Quality Assurance Exercise

- Purpose and context
  - Evaluates QA of digital mapping data produced for Countryside Survey 2007 to ensure high-quality, compatible, and analysable national-scale habitat data.
  - Aims to enable rapid analysis, data integration in a geodatabase, and robust monitoring of environmental health.

- Mapping approach and QA framework
  - Transition from post-survey digitisation of paper maps to field-based digital mapping using Surveyor software.
  - Mandatory fields, prompts, and visit-status layers in the software reduce interpretation subjectivity and handwriting issues.
  - Early data checks via an interactive wiki; QA teams conducted field visits to ensure protocol compliance.
  - QA data compared against CS survey data across multiple scales and attributes to assess mapping quality.

- Extent and sampling
  - QA covered 23 one-km squares, selected to represent land classes and geographic spread across GB, with access refusals influencing surveyed areas.
  - QA squares largely varied in land class and location to ensure broad coverage.

- Analytical approaches
  - 4 primary QA methods:
    - Direct comparison of aggregate areas/lengths/points for whole squares (CS vs QA).
    - Raster comparisons: convert polygons to 10x10 m raster units to compare absolute area and spatial patterns of Broad Habitats.
    - 100-point grid: overlay to assess concordance of Broad Habitat codes at a common resolution.
    - Attribute-level analyses: reference IDs for polygon-level comparisons of species and habitat attributes.
  - Additional analyses included surveyor efficiency, feature-type consistency, and data capture completeness.

- Key findings: mapping quality and agreement
  - Broad Habitat (BH) agreement
    - In about 81% of squares, BH presence matched between CS and QA.
    - Mean differences in BH extents between CS and QA were generally small: many BHs showed less than 1–3.5 percentage-point differences; some variability noted (e.g., Improved/Acid Grassland, Dwarf Shrub Heath, Bog, Urban, Fen/Neutral overlaps).
    - Notable issues where discrepancies were larger: Blanket Bog (historic definitional debates), Dwarf Shrub Heath vs Blanket Bog, Urban vs Grassland classifications.
    - Upland mosaics and landscape mosaics added complexity to exact BH allocation; mosaicked landscapes could inflate mismatches when disaggregating into component BHs.
  - Raster data concordance
    - Overall raster agreement across squares averaged around 76%, with several squares showing high concordance (e.g., 364, 488) and a few with lower agreement (e.g., 261, 773).
    - Some BH-level disagreements were systematically higher in certain squares, linked to habitat definitions and local landscape context.
  - 100-point concordance
    - Most squares showed good concordance (frequent matches) with a broad pattern of positives; some squares displayed substantial mismatches (e.g., 773 only 19% concordance; 261 around 41%).
    - The 100-point approach demonstrated useful diagnostic insight into which habitats align between CS and QA and where definition/interpretation differences occur.
  - Species attributes within polygons
    - About 45% of QA polygons shared at least one listed species with their CS matches.
    - Species concordance varied by habitat type; higher concordance for woodlands and Improved Grassland, lower for Bracken and upland mosaics.
    - Where BHs matched, a majority (77%) also had a matching dominant species list; otherwise, differences often reflect species richness and dominance variability across habitats.
  - Points, linears, and change coding
    - Point features: generally high consistency in habitat codes between QA and CS; minor discrepancies mostly due to coding of “woodland/forest” categories.
    - Linear features: strong agreement on land-use theme allocations; most mismatches involved minor label differences (e.g., FO vs WNS) rather than fundamental disagreements.
    - Change coding: overall good agreement on change types (Real, Error, No Change); some complexity remains, especially for habitats where change interpretation is nuanced.

- Change recording and data governance
  - Introduction of an explicit change field (Real Change, Error Change, No Change) to update previous mappings and clarify data evolution.
  - The digital workflow facilitated field-based change recording and subsequent verification, though it added complexity for surveyors and QA staff.
  - Training and experience influenced alignment, particularly for challenging habitats (e.g., Blanket Bog, upland mosaics).

- Implications for monitoring frameworks
  - Demonstrates that digital mapping with integrated QA can yield high-quality, standards-compliant data suitable for policy evaluation and decision-making.
  - Highlights the value of multiple QA modalities (aggregation, raster, point grids) to triangulate accuracy across scales and habitat types.
  - Underscores ongoing challenges in habitat definitions, especially for boundary cases (e.g., Blanket Bog vs Dwarf Shrub Heath) and upland mosaics; indicates a need for continual refinement of keys and guidance.
  - Shows the importance of metadata, data provenance, and data governance to enable data sharing, reproducibility, and transparent QA processes.

- Practical considerations and limitations
  - Data gaps and access refusals can bias QA and require masking of unsurveyed areas to ensure fair comparisons.
  - Habitat definitions and classification boundaries can drive discrepancies between CS and QA, particularly in complex or transitional landscapes.
  - The scale of analysis (square-based vs mosaic interpretation) affects concordance and requires careful interpretation when reporting QA outcomes.

- Recommendations and next steps (as implied)
  - Continue refining habitat definitions, especially for Blanket Bog and related upland habitats, to reduce misclassification.
  - Maintain and strengthen data governance practices to support transparency, metadata completeness, and public sharing of underlying data where appropriate.
  - Invest in training and standardised field handbooks to minimize inter-team variability in habitat allocation, especially in mosaicked or transitional landscapes.
  - Leverage the integrated QA framework to inform iterative improvements in monitoring frameworks and national data harmonisation efforts.