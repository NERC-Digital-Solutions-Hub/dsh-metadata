# Mapping Quality Assurance Exercise

## Executive summary
- Evaluates the quality and consistency of digital habitat mapping from the Countryside Survey 2007 through a dedicated QA exercise.
- Field mapping used a purpose-built Surveyor system; data uploaded to an interactive wiki and stored in a geodatabase for analysis.
- QA compared Surveyors’ CS data with QA team data across multiple scales and methods to assess accuracy, consistency, and change recording.
- General finding: high agreement for many Broad Habitats, with substantial validation of the digital approach; some habitat-specific discrepancies identified, guiding future refinements.

## Context and aims for environmental monitoring analysts
- Demonstrates that standardized, digital mapping data can be produced and QA-validated to support monitoring of environmental health and policy performance over time.
- Highlights the value of integrating field-m collected data with national-scale spatial datasets and making underlying data accessible for scrutiny.

## Methodology and data workflow
- Digital mapping in 2007 using Surveyor software in the field; mandatory fields and prompts reduce handwriting/interpretation errors; visit status layers track coverage.
- Early data checks via an interactive wiki; QA teams conducted field QA visits to ensure protocol adherence.
- QA design: mapping QA conducted in different 1 km squares than plot/QA exercises to avoid bias; data masked to common surveyed areas when necessary.
- Analysis approaches:
  - 4.1 Direct comparison of aggregate areas/lengths/points per square (CS vs QA).
  - 4.2 Raster data comparison: convert polygons to 10 x 10 m raster units, sample with a resolution grid.
  - 4.3 100-point grid analysis to assess concordance at a standardized spatial resolution.
  - 4.4 Attribute comparison for areas/linears/points via reference ID matching and species attributes.
- Surveyor efficiency metrics and change-recording practices (including “change” codes: Real change, Error Change, No Change).

## Coverage and QA scope
- QA on mapped data covered 23 1 km squares, chosen to represent land classes and ensure broad spatial coverage across Great Britain.
- Some access refusals reduced surveyed area; analyses focus on common, accessible areas.

## Key analysis methods and outputs
- 4.1 Aggregate comparisons: extent/area proportions of Broad Habitats (BH) per square; CS vs QA concordance assessed.
- 4.2 Raster comparisons: per-square broad habitat agreement across 1 km squares; quantified as percent agreement.
- 4.3 100-point analysis: concordance of BH mapping at a fixed 100-point grid within squares; evaluates location-level agreement.
- 4.4 Attribute analysis: comparison of species attributes within matched polygons.
- Additional sections evaluate linear features (Section 7), points (Section 8), and change recording (Section 9).

## Main findings

- Habitat mapping agreement
  - 6.1 Direct aggregate comparison: in 81% of squares the BH recorded by CS and QA aligned; mean differences across BH types were typically small (often under 3–4%), with some high-variance cases indicating potential habitat-coding differences (notably Improved/Neutral Grassland, Dwarf Shrub Heath, Bog, Urban, and certain upland habitats).
  - 6.2 Raster data: overall raster agreement varied by square, but many squares showed high agreement (e.g., 364, 488); some squares (e.g., 261, 773) showed comparatively poor agreement.
  - 6.3 100-point concordance: overall good agreement for many squares, but notable mismatches in a few (e.g., 773 with only 19% concordance, 261 with 41%); separate matrices highlight specific habitat-code matching issues.
  - Major discrepancies often tied to:
    - Blanket Bog vs Dwarf Shrub Heath misclassifications, especially in upland squares and areas with mosaic habitats.
    - Definitions and field interpretation differences for certain habitat types; training and key-definition revisions (notably for Blanket Bog) influenced results.
    - Complexity of mosaics and fine-grained transitions between BHs in upland landscapes.

- Species and habitat attributes
  - 6.4 Polygon-level species concordance: 45% of QA polygons had at least one listed species matching the CS polygon at the same location.
  - Species concordance varied by habitat type; woodland and Improved Grassland tended to show higher matching species, while Bracken and upland mosaics showed more divergence.
  - Where species matched, 77% of polygons also had matching BH classification, indicating species-level data supports BH allocation but is not determinative on its own.
  - Species list concordance for widely recorded species (e.g., Lolium perenne) showed moderate agreement; broader species lists tended to diverge more due to dominance and identification nuances.

- Linears and points
  - 7.1 Linear features: highly consistent land-use theme choices between QA and CS; few cases where QA included a feature CS did not, generally expected (e.g., fence vs wall).
  - 7.2 100-point analysis for linears showed strong overall consistency; specific mismatches traced to feature-type interpretation (e.g., FO vs WNS/WUS) rather than fundamental data gaps.
  - 8.1 Points: similar pattern of high CS/QA agreement in point-feature habitat codes; overall consistency maintained, with some confusion around woodland/forest coding in rare cases.

- Change recording
  - Digital change coding allowed more detailed change information (Real Change, Error Change, No Change).
  - Overall change-coding agreement between CS and QA was strong across broad habitats and linear features, though some habitat-specific challenges persisted (notably Deeply nested upland habitats and complex mosaics).

## Implications for monitoring and data quality
- The digital, field-based mapping approach with embedded QA demonstrates strong potential for consistent, comparable environmental data suitable for national-scale monitoring and cross-dataset analyses.
- High agreement in many habitat categories supports confidence in using Countryside Survey data for trend analyses and policy performance evaluation.
- Identified challenges point to targeted areas for improvement:
  - Refinement of habitat definitions and coding rules for problematic categories (e.g., Blanket Bog, Acid/Neutral Grassland overlaps, Urban vs. Improved Grassland in some contexts).
  - Enhanced training and clear field-handbook guidance for upland mosaics and machair-like habitats.
  - Consideration of mosaic dynamics and fine-scale transitions when interpreting small-scale habitat maps.
  - Continued alignment of data collection procedures with downstream data portals and interoperability standards.

## Data stewardship and accessibility
- Data captured via Surveyor, QA checks, and wiki-enabled quality assurance routes were integrated into a geodatabase, supporting transparent QA and cross-dataset analyses.
- The QA framework demonstrates how underlying data can be scrutinised and compared over time, fulfilling the Analysts Monitoring the Environment archetype’s emphasis on reproducible, scrutinizable datasets and accessible underlying data.

## Conclusions and recommendations
- The 2007 Mapping QA Exercise validates the general reliability of digital field mapping for environmental monitoring and highlights areas for refinement in habitat classification and field interpretation.
- Ongoing training, methodological clarity, and refinements to BH definitions—especially for Blanket Bog and overlapping grassland types—will further reduce discrepancies.
- Future QA should continue to leverage multiple analysis scales (aggregate, raster, point, and change) to ensure robust data quality and to enhance data sharing, comparability, and integration with broader environmental datasets.