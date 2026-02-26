# Mapping Quality Assurance Exercise

## Overview and purpose
- 2007 Countryside Survey produced high-quality habitat and landscape feature data compatible with previous approaches and national spatial datasets via a geodatabase.
- Digital field mapping with Surveyor software reduced interpretation error, improved data clarity, and enabled in-field data prompts and mandatory fields.
- Early wiki-based data checks and QA visits supported protocol adherence and data quality.

## Scope and data structure
- QA covered 23 one-kilometre squares; squares were selected to represent different land classes and locations across Great Britain.
- Data collected by CS surveyors and QA teams used standard Countryside Survey tablets; data uploaded to a single geodatabase; unsurveyed and refused areas excluded for comparison.
- The QA approach compared data at multiple scales and formats to assess consistency.

## QA approaches (methods)
- 4.1 Direct comparison of aggregate areas/lengths/points for whole squares (CS vs QA).
- 4.2 Raster data comparisons: convert polygons to 10 x 10 m raster cells within each 1 km square, assign dominant Broad Habitat, compare QA vs CS.
- 4.3 100-point grid overlay to assess spatial concordance of Broad Habitats; positive/negative scoring per square.
- 4.4 Attribute-level comparisons for areas, lines, and points using reference IDs to compare species and other primary attributes.

## Key findings: habitat mapping and agreement
- Raster-based agreement (6.2): average 76% concordance across squares; some squares high (e.g., 364, 488) and others lower (e.g., 261, 773).
- Aggregate area comparisons (6.1): most Broad Habitats show mean differences <1–3.5% across squares; several habitats flagged for potential issues (Improved/Neutral Grassland, Dwarf Shrub Heath, Bog, Urban, and Blanket Bog) due to definitional or mosaic complexities.
- 100-point concordance (6.3): generally high agreement; notable mismatches in squares 261 and 773; 6.3b shows specific Broad/Priority Habitat matches and discrepancies.
- Species attributes in polygons (6.4): 45% of QA polygons had at least one species present in the matched CS polygon; overall, 77% of matched polygons also had matching dominant habitat, with higher concordance for woodlands and Improved Grassland; upland mosaics complicate species-habitat alignment.

## Key findings: linears, points, and change
- Linear features (7.1, 7.2): total lengths show minor differences; high consistency in land-use theme classifications (e.g., fences vs walls); some confusion between forestry belts (FO) and woody features (WNS/WUS) but overall consistent.
- Points (8.1): small differences in total points; trends similar to linears; veteran trees show large disparity due to field instruction limits and selection effects.
- Point habitat codes (8.2): high consistency in codes for co-located points; minor occasional confusion between woodland/forest coding.
- Change recording (9): digital approach allowed more detailed change coding (Real Change, Error Change, No Change); QA vs CS generally aligned, though habitat-change assessment remains challenging; complexity increased by the new digital workflow and the need for training.

## Practical implications for GIS practice
- Digital mapping improves data quality, streamlines QA, and supports timely data verification via wiki checks and visit-status layers.
- The approach enables robust cross-comparison with other national datasets and aids in identifying definitional or scale-related issues (e.g., Blanket Bog, Machair, urban habitat classification).
- Training and clearer habitat definitions are needed to reduce discrepancies in complex upland mosaics and in habitats with overlapping characteristics (Neutral vs Improved Grassland; Broadleaf vs Coniferous Woodland).
- Spatial differences due to mosaics or continuum of habitats highlight the importance of scale and disaggregation when comparing QA against surveyor maps.

## Limitations and considerations
- Some habitat disagreements are attributable to definitional updates (e.g., Blanket Bog) and to mosaic or transitional areas where multiple Broad Habitats co-occur.
- Machair and certain upland habitats present localized, atypical distributions that can skew square-level comparisons.
- Species-level concordance is lower than habitat-level concordance due to dominance effects and taxonomic ambiguity in complex swards.

## Conclusions
- The 2007 mapping QA demonstrated a generally high level of agreement between QA and CS survey teams across multiple analysis methods, with robust data quality improvements from digital tools.
- Common discrepancies were identified and linked to habitat definitions, upland mosaics, urban classification clarity, and training needs.
- The QA process supports confidence in the resulting geodatabase and its integration with national spatial datasets, while outlining targeted areas for future refinement and standardisation.