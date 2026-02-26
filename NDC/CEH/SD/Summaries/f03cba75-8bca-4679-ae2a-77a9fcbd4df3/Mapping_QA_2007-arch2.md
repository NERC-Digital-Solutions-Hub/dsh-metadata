# Mapping Quality Assurance Exercise

- The Countryside Survey 2007 aimed to provide high-quality, comparable habitat and landscape feature data suitable for national-scale analysis and integration with other spatial datasets via a geodatabase.
- Digital mapping in the field (Surveyor software) was adopted to reduce interpretation errors and improve data clarity; data were uploaded to an interactive wiki for early quality checks.
- QA involved multiple approaches to test mapping accuracy: direct comparison of surveyor-mac data with QA data, raster-based comparisons, and 100-point grid assessments, across various feature types (areas, lines, points) and attributes.

## Extent

- QA touchpoints covered 23 1-km squares, selected to represent different land classes and locations across Great Britain.
- Where access was refused, or areas were not surveyed, analyses focused on common surveyed areas to avoid bias.
- Whole squares were mapped for QA, mirroring the survey scope but with a broader inclusion of area, linear, and point features.

## Approach

- QA teams aimed to be in or near surveyors’ activities to minimize temporal vegetation changes and landowner disturbance.
- Mapping QA was conducted using standard Countryside Survey tablets; data from QA and CS were merged into a single geodatabase for analysis.
- Unsurveyed or refused areas were excluded prior to analysis; the two datasets were aligned using masks to create common areas for comparison.

## Analysis

- 4.1 Direct comparison: aggregate areas/lengths/points per square were exported to SAS for analysis by Square, Land Class, and Broad Habitat.
- 4.2 Raster data: polygons converted to 10 x 10 m raster cells; dominant Broad Habitat assigned per cell; compared absolute extents and spatial locations.
- 4.3 100-point grid: overlaid 10 x 10 grid to sample concordance of Broad Habitats at ~100 points per square; matched vs unmatched BH types recorded.
- 4.4 Attribute analysis: reference ID layers enabled comparison of species attributes for matched polygons.

## Surveyor efficiency and data quality

- Digital systems improved visit-status tracking and mandatory attribute recording; very small land not visited (average around 0.4% in several squares).
- More species were recorded per area under the digital approach.
- Some landowner access issues persisted and could impact coverage.

## 6.1 Direct comparison of aggregate areas for whole squares

- In 81% of cases, both CS and QA recorded a Broad Habitat (BH) in the same square.
- Mean differences between QA and CS BH proportions were generally under 1% for 13 BHs; most remaining BHs were under 3.5%.
- Notable potential issues identified: Improved grassland, Dwarf Shrub Heath, Bog, Urban, and Sub-littoral sediment showed larger SDs, suggesting some differential allocation between QA and CS.

## 6.2 Comparisons of raster data

- Overall raster agreement averaged about 76%, with some squares showing very high agreement (e.g., 364, 488) and others lower (e.g., 261, 773).
- Agreement varied by BH type across squares; e.g., some discrepancies concentrated in Neutral vs Improved Grassland, upland habitats, and urban vs grassland allocations.
- Table-based assessments highlighted specific BH-level agreement percentages per square.

## 6.3 100-point sample grid – Primary land cover codes and habitats

- The 100-point method showed good concordance for many squares, but some squares had substantial mismatches (e.g., 773, 261).
- Concordance rates by BH/PH generally high, but certain pairs (e.g., machair-related Neutral/Improved Grassland in specific squares) showed mismatches due to local habitat peculiarities.
- The matrix of broad and priority habitats revealed where QA vs CS tended to align or diverge in BH coding.

## 6.4 Polygon analysis of species attributes

- 1081 QA polygons and 998 CS polygons were spatially joined; 45% of QA polygons matched a CS polygon with at least one shared species.
- Species concordance varied by BH type; woodlands and Improved Grassland showed higher species-match rates; Bracken and upland mosaics showed lower concordance due to habitat complexity.
- Species-level concordance across matched polygons was around 40% overall; dominance by a few species (e.g., Lolium perenne) showed higher agreement.
- Acknowledges that species lists are influenced by the Broad Habitat allocated and that mosaics in upland areas complicate direct comparisons.

## 7.1 Direct comparison of aggregate linear features

- Lengths of linear features per square were generally close between CS and QA; minor differences dominated.
- Linears were categorized by land-use themes (e.g., Banks, Fences, Foreshore belts, Inland Water, Transport, Walls, Woody linears).
- The overall pattern showed strong consistency, with limited mismatches (e.g., between fences vs walls, or between forest belts and woody actual shapes).

## 8.1 Direct comparison of aggregate points for whole squares

- Point counts under different land-use themes (Forestry, Inland Physiography, Inland Water, Structures, Veteran Trees) were broadly aligned between QA and CS.
- The largest disparities occurred in the veteran trees category, reflecting the subjective nature and multiple candidates per species.

## 8.2 Habitat codes for point features

- Point-feature habitat codes were cross-checked via buffered spatial matching; most points matched the CS data in habitat code.
- A few instances of confusion between woodland/forest codes were noted, likely due to legacy coding practices.

## 9. Assessment of change recording

- 2007 introduced more detailed change coding: Real change, Error Change, No Change.
- Change-field usage showed substantial agreement between CS and QA across broad habitats, but some complexities remained, especially with habitat-level change.
- Some surveyors initially struggled with the change field; QC activities helped, and overall the digital change workflow supported data tidying and updating of maps.

## Key takeaways for Analysts Monitoring the Environment

- The digital QA exercise demonstrates high overall alignment between surveyors and QA assessments across most habitat types and feature classes, with average agreement generally strong in aggregate BH allocations, raster data, and linear/point features.
- Notable areas of discrepancy include Blanket Bog and Dwarf Shrub Heath versus Bog, Neutral vs Improved Grassland, urban vs grassland allocations, and certain upland mosaics where fine-scale boundaries are difficult to pin down.
- Habitat definitions and coding rules (especially for coniferous vs broadleaved woodlands, and for blanket bog) influenced agreement; training and updated field keys can reduce inconsistencies.
- Species concordance is moderate (around 40% for matched polygons), reflecting the complexity of species composition within mosaicked habitats and the subjective nature of selecting dominant species.
- The move to digital data collection and mandatory attributes improved data quality and the ability to perform cross-dataset QA and data integration with other national spatial datasets.
- The QA framework provides actionable insights for refining BH definitions, improving field guidance, and guiding future QA cycles to enhance consistency and data value for environmental monitoring over time.