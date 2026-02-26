# Mapping Quality Assurance Exercise

- The document reports on a 2007 quality assurance (QA) exercise for the Countryside Survey (CS) mapping, focusing on mapping habitats and landscape features using digital field mapping and a dedicated QA workflow.
- Aims were to produce high-quality, comparable national-scale spatial data that could be analyzed alongside other datasets in a geodatabase, while reducing subjectivity and transcription errors inherent in post-survey digitisation of paper maps.

## Scope and Approach

- 2007 introduced field-based digital mapping using Surveyor software to capture mandatory attributes directly in the field, with data uploaded to an interactive wiki for early in-office QA.
- QA coverage: mapped data across 23 1-km squares (intended broader coverage, with some access refusals). QA squares were chosen by land class and location to span GB.
- QA teams worked in parallel with field surveyors, targeting both areas and features (areas, lines, points) and including visit status and dominant species attributes.

## QA Methodologies (4.1–4.4)

- 4.1 Direct comparison of aggregate areas/lengths/points for entire squares between CS and QA data.
- 4.2 Raster data comparisons: polygons converted to 10 x 10 m raster cells within each 1 km square; dominant Broad Habitat assigned per cell; enabled assessment of total area and spatial concordance.
- 4.3 100-point grid analysis: overlaid 10 x 10 grid to assess concordance of Broad Habitats at fixed sample points; results summarized per square with concordance/ discrepancy scores.
- 4.4 Attribute-level comparisons: reference IDs and species attributes compared for matched polygons/areas/lines/points to examine attribute concordance.

## Data Collection and QA Workflow

- Digital data collection enabled direct digital QA against CS datasets, with masks excluding unsurveyed or access-refused areas to ensure comparability.
- Data were exported to SAS for statistical analysis; alignment and masking ensured comparable datasets across CS and QA efforts.
- QA involved in-field joint visits where feasible to minimize temporal vegetation changes and owner disturbance; different QA staff sometimes focused on separate feature types to improve efficiency.

## Key Findings by Evidence Type

- 6.1 Aggregate areas for whole squares
  - In 81% of cases, a Broad Habitat (BH) was recorded by both CS and QA in the same square.
  - Mean differences in BH proportions between QA and CS were typically under 1–3.5% across most BH types; some habitats showed larger SDs indicating potential biases or mapping challenges (e.g., Improved/Neutral Grassland, Dwarf Shrub Heath, Bog, Urban, Sub-littoral Sediments).
  - Notable issues discussed include differences in Blanket Bog definitions and mosaic vegetation in uplands, and misalignment between coniferous vs broadleaved woodland classifications.

- 6.2 Raster data comparisons
  - Across 15+ squares, overall raster agreement (matched BH per square) averaged about 76%, with some squares showing high concordance (e.g., 364, 488) and others lower (e.g., 261, 773).
  - Agreement by BH type varied by square; some habitats showed high concordance (e.g., Standing Open Water, Urban, Sea) while others (e.g., Neutral vs Improved Grassland, certain upland habitats) were more variable.

- 6.3 100-point grid (primary land cover codes and habitats)
  - Concordance across 100 points generally strong, with most squares showing good agreement; some squares exhibited substantial mismatches (e.g., 773 with very low concordance; 261 with moderate concordance).
  - Matrix analysis highlighted areas where particular BH/PHs tended to be misclassified between QA and CS (e.g., Grassland categories, Sand Dune/Strandline habitats, blanket bog vs dwarf shrub heath).

- 6.4 Polygon analysis of species attributes
  - 1081 QA polygons and 998 CS polygons matched spatially; about 45% of QA polygons had at least one listed species also present in the matched CS polygon.
  - Species concordance varied by BH type; woodland and Improved Grassland showed higher species-match rates, while other habitats (e.g., Bracken, uplands with mosaics) showed lower matches.
  - A substantial portion of species-level concordance differences could reflect differences in dominant species selection linked to BH allocation rather than measurement error.

- 7.1 Linear features and 8.1 Points
  - Direct comparison of aggregate linear feature lengths showed generally small differences between QA and CS data at most squares, with broad consistency across land-use themes (banks, fences, forestry belts, etc.).
  - Linear features analysis indicated high consistency in land-use theme allocation (e.g., fences vs walls) with minimal instances of CS recording features QA did not, and some potential confusion around forestry vs woody features.
  - Points: overall totals across squares were very similar; some discrepancies in specific point types (e.g., urban points, water bodies) were noted but generally small.

- 9 Change recording
  - 2007 introduced a more detailed change-coding approach (Real change, Error Change, No change), with an “error change” field to help update previous data.
  - Most habitat-level change coding showed good agreement between CS and QA surveyors, though change assessment was more challenging for habitats than for linears or points due to habitat overlaps and evolving definitions.
  - The digital workflow facilitated in-field data tidying and field verification, despite added complexity.

## Implications for data use and Analytics

- Overall data quality improved with digital field mapping, in-field QA, and transparent provenance via metadata; robust cross-validation against CS data supports downstream analyses.
- The exercise identifies several recurring challenges for analysts:
  - Local-level data gaps and the need for consistent, scale-appropriate definitions of Broad Habitats (notably Blanket Bog, Acid/Neutral Grassland, Urban allocations, and woodlands).
  - Spatial mosaics and edge effects in upland and transitional habitats leading to potential misclassification in small-scale mapping.
  - Variation in data accessibility and the necessity to standardize fieldhandbook interpretations to minimize cross-team discrepancies.
  - The importance of training and experience in accurately handling complex habitat types (e.g., Blanket Bog vs Dwarf Shrub Heath) and mosaic landscapes.

## Conclusion

- The 2007 Mapping Quality Assurance Exercise demonstrates high overall concordance between CS surveyors and QA assessors across multiple data dimensions (habitat extents, raster and point concordance, linear features, and species attributes), with areas of notable but explainable discrepancy.
- Digital data capture, in-field QA, and standardized change recording substantially improved data quality and traceability, while highlighting persistent definitional and scale-related challenges that require ongoing refinement of habitat classification, training, and data integration practices for future surveys.