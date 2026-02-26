# Mapping Quality Assurance Exercise

- Overview
  - Evaluates the quality of digital habitat and landscape-feature mapping from Countryside Survey 2007.
  - Transitioned to field mapping with the Surveyor software to produce a geodatabase and reduce errors from post-survey digitising.
  - Data were compared with previous 1998 data to assess accuracy and consistency across scales and attributes.

- Digital mapping and QA workflow
  - Surveyors map in the field with mandatory fields and prompts; data uploaded to an interactive wiki for early QA.
  - QA teams visited survey squares, often in parallel with survey teams, to minimise temporal changes and disturbance.
  - Three QA approaches used for mapped data:
    - Direct, aggregate comparisons of areas/lengths/points (per square, per land class, per Broad Habitat).
    - Raster-based comparisons by converting polygons to 10 x 10 m grids (dominant Broad Habitat per cell) and sampling with a resolution grid.
    - 100-point grid comparisons to assess spatial concordance of Broad Habitats between CS and QA data.
  - Attribute comparisons used reference ID layers and masked common survey areas to create comparable datasets.

- Extent and sampling
  - QA covered 23 squares (1 km each); chosen to represent land classes and geographic coverage across GB.
  - Analyses focus on common surveyed areas where access was granted and data existed for both QA and CS datasets.

- Analysis and metrics
  - 4.1 Direct comparison: Aggregate areas/lengths/points across Broad Habitats (BH) and feature types (areas, lines, points).
  - 4.2 Raster data: 10,000 10x10 m cells per square; assignment to dominant BH; sampling with a grid to compare absolute amounts and spatial locations.
  - 4.3 100-point grid: Concordance (+) or discrepancy (-) per BH/PH; aggregated concordance rates per square.
  - 4.4 Attribute analysis: Comparison of species attributes within matched polygons via reference IDs.

- Surveyor efficiency
  - Digital workflow improved use of visit status layers; average not-visited land was low (about 0.4% in many squares).
  - Mandatory fields and prompts led to more comprehensive recording of dominant species (increase noted in Table 5.2 over previous surveys).

- 6.1 Direct aggregate comparison of whole squares
  - In 81% of squares, a BH was recorded by both CS and QA.
  - Mean differences in BH extent between CS and QA were typically under 3.5% (lower for most BHs; higher for a few). Some habitats showed larger SDs, indicating potential differential allocation (e.g., Improved/Acid Grassland, Dwarf Shrub Heath, Bog, Urban, Sub-littoral sediments).
  - General finding: overall similarity between CS and QA mappings with habitat-specific discrepancies.

- 6.2 Raster data comparisons
  - Across squares, raster-ensemble agreement varied; overall average concordance around 76%, with higher and lower outliers.
  - Some squares showed very high agreement (e.g., 364, 488); others low (e.g., 261, 773).
  - Per-square BH-level agreement highlighted typical mismatches and highlighted issues such as Urban vs grassland allocations, and upland mosaic areas.

- 6.3 100-point analysis
  - Majority of squares showed good concordance between QA and CS at the 100-point scale, but some outliers existed (e.g., squares 261, 773 with low concordance).
  - Matrix of BH/PH concordance identified several recurring issues:
    - Neutral vs Improved Grassland overlap.
    - Broadleaf vs Coniferous Woodland allocations.
    - Upland habitat mosaics causing mismatches when disaggregating mosaics into component BHs.
    - Machair on Scottish sands causing grassland-related misclassifications.
    - Blanket Bog vs Dwarf Shrub Heath disagreements, especially in highland squares; training and clearer definitions recommended.
  - Overall, most BH/PH categories showed good alignment; some habitats require definitional refinement and better handling of mosaics.

- 6.4 Polygon species attributes
  - 1081 QA polygons and 998 CS polygons matched spatially; 45% of QA polygons had at least one species listed also present in the matched CS polygon.
  - Species concordance varied by habitat; woodland and Improved Grassland showed higher concordance; Bracken and upland mosaics tended to be lower due to species composition and cover interpretation.
  - For matched polygons with species in common, 77% also had a matching BH, indicating species-level data influenced habitat coding in many cases.
  - Species-level concordance overall was around 40% for commonly recorded species; Lolium perenne showed higher agreement (66%) among the most common species.

- 7 Linear features
  - 7.1 Direct comparison of aggregate linear lengths showed generally small differences between QA and CS across most squares.
  - Land-use themes (banks, fences, forestry belts, inland physiography, etc.) were largely consistent; some confusion occurred between certain forest/woody feature classifications (e.g., belts of trees vs woody linear features).
  - Overall, high consistency with limited cases of misclassification between similar feature types.

- 8 Points
  - 8.1 Direct comparison of points showed small differences across most squares and themes (forestry, inland physiography, inland water, structures, veteran trees).
  - Veteran trees exhibited the largest disparity due to the field instruction to select up to two relevant trees per species; variability expected given multiple candidates in a location.

- 9 Change recording
  - Digital change coding captured real change, error change, and no change.
  - High agreement on change coding for many Broad Habitats and linears; more complex for broad habitats due to definitional nuances.
  - Electronic change field facilitated updating previous maps and linking with current data, though it added complexity for surveyors.
  - Overall, change coding adhered to protocols with a few habitat-level ambiguities.

- Habitat-definitional issues and recommendations
  - Neutral vs Improved Grassland overlap and decisions influenced by species composition and extent.
  - Woodland classification challenges between Broadleaf and Coniferous woodland; prior field handbook ambiguity contributed to discrepancies.
  - Upland mosaics and mosaicked mapping complicate precise BH assignment; more explicit handling of mosaics and definitions recommended.
  - Blanket Bog debates and definitional revisions in 2007 highlighted the need for clearer, consistently applied criteria, especially in highland areas.
  - Machair-related misclassifications indicate the need for regional habitat nuance and training.
  - Recommendation: refine habitat definitions, enhance training, especially for upland and mixed mosaics; maintain robust QA against both areas and attributes.

- Implications for GIS specialists
  - Transition to field-based digital mapping with enforced data standards improved data quality and analysis capabilities.
  - Geodatabase-based workflow supports integrated analyses with other national spatial datasets and efficient QA cycles.
  - Raster and 100-point analyses provide multiple avenues to validate spatial accuracy and detect systematic biases.
  - Documentation and training are critical to minimize habitat-definition disagreements and improve consistency across teams.
  - Change-tracking workflow adds value for temporal analyses but requires careful interpretation and clear guidelines.

- Takeaways for map-based GIS data products
  - High overall agreement between surveyors and QA mappings, with best performance in well-defined habitats and where mosaics are minimal.
  - Persisting challenges in specific habitats ( Blanket Bog, Neutral/Improved Grassland, Urban-Grassland distinctions, machair) suggest targeted refinements.
  - The digital approach (Surveyor, wiki QA, geodatabase) enables faster QA feedback loops and improved data integrity for map-based products.