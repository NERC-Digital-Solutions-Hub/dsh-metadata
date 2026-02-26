# Mapping Quality Assurance Exercise

## 1. Introduction
- Purpose: provide high-quality, policy-relevant habitat and landscape data compatible with prior approaches, enabling rapid analysis within a geodatabase.
- Transition to digital mapping in 2007 using Surveyor software to reduce interpretationSubjectivity and improve data quality.
- QA framework: data uploaded to an interactive wiki for early checks; QA teams conducted field visits to verify protocols; emphasis on transparency and data governance.

## 2. Extent
- QA mapping covered 23 one-kilometre squares, chosen to represent land classes and locations across Great Britain.
- Access refusals affected some areas; analyses restricted to common surveyed areas between CS and QA datasets.
- QA sampling prioritized whole squares and varied land classes to ensure broad coverage.

## 3. Approach
- QA teams mapped in near real-time using standard Countryside Survey tablets/software; data merged into a single geodatabase.
- Comparisons used masks to align surveyed and QA areas, excluding unsurveyed or refused sections.
- Quality assurance included concurrent field QA, unit-area/linear/point assessments, and cross-checks via wiki communications.

## 4. Analysis
- 4.1 Direct comparison of aggregate areas/lengths/points per square using SAS.
- 4.2 Raster analysis: convert polygons to 10,000 10x10 m cells per square; compare dominant Broad Habitat and locations.
- 4.3 100-point grid: assess broad habitat concordance at ~100 sample points per square.
- 4.4 Attribute analysis: matched reference layers to compare species attributes within polygons.

## 5. Surveyor efficiency
- Digital tools improved visit-status usage and recording of dominant species across features.
- Not-visited areas were small on average (0.4% per table); refused access remained a factor.
- Data recording improvements (mandatory fields) increased species counts per area compared with earlier surveys.

## 6. Habitat and broad-scale comparisons

### 6.1 Direct comparison of aggregate square areas
- 81% of squares recorded the same Broad Habitat (BH) by CS and QA.
- Mean differences in BH proportions generally below 3.5% for most habitats; a few habitats showed larger differences and higher variability.
- Notable potential issues: Improved/Neutral grassland overlap; Dwarf Shrub Heath vs Blanket Bog; upland mosaics causing mismatches; urban vs grassland classification ambiguities; machair on Scottish dunes causing local anomalies; Blanket Bog definitions updated in 2007, leading to mis-matches in some squares (notably 773).

### 6.2 Raster data comparisons
- Overall raster agreement across squares averaged around 76%, with some squares higher (e.g., 364, 488) and others lower (e.g., 261, 773).
- Agreement by BH varied by square; certain mismatches highlighted for further review (e.g., Neutral vs Improved Grassland, Urban vs Grassland, and various woodland classifications).

### 6.3 100-point grid – primary land cover codes and habitats
- Concordance varied by square; several squares showed high concordance, while others (e.g., 773, 261) showed substantial mismatches.
- Table 6.3b indicates differing match/mismatch patterns among BH/PH codes, with notable issues in Sand Dune/Strandline habitats and certain upland mosaics.
- Overall, 76–77% concordance observed across many BH/PH categories, with some sites showing lower alignment.

### 6.4 Polygon analysis of species attributes
- 1081 QA polygons and 998 CS polygons matched by location; 45% of matched polygons had at least one same listed species.
- Species concordance varied by habitat; Improved Grassland and woodlands showed higher species-matching rates (e.g., ~40–92% BH match with species) while other habitats showed lower concordance.
- Dominant species lists differed in many polygons; Lolium perenne showed relatively higher concordance (66%) among species with high dominance.
- Overall, 77% of polygons with a species match also had matching BH; the remaining differences reflect habitat allocation and mosaic complexities.

## 7. Linear features

### 7.1 Aggregate linear features
- Comparison of total linear lengths per square showed generally small differences between QA and CS data.
- Data categorized by land-use themes (e.g., Banks, Fences, Forestry belts, Inland Water, etc.). Overall alignment was strong, with few notable discrepancies.

### 7.2 Land use themes for linear features
- Buffered QA linears (5 m) matched to co-located CS linears to compare land-use themes.
- Very high consistency in land-use category choices (e.g., fences vs walls) with minor misclassifications mainly between forestry belts (FO) and woody linear features (WNS/WUS).

## 8. Points

### 8.1 Aggregate points
- Point data categorized by land-use themes (Forestry, Inland Physiography, Inland Water, Structures, Veteran Trees, etc.) showed very small discrepancies across squares.

### 8.2 Habitat codes for point features
- Buffered QA point features matched to CS point features; most points used the same habitat codes as CS points.
- Minor confusions between woodland/forest codes likely due to legacy usage or prior coding conventions.

## 9. Change recording
- Change coding fields captured: Real change, Error Change, No Change.
- Additional “error change” field allowed updates to previous data, but required careful interpretation.
- Surveys with digital tools improved data tidiness, though some surveyors initially found change coding complex.
- Tables 9.1–9.3 show generally strong agreement between CS and QA teams on change assignments across habitats, linear, and point features, with slightly lower alignment for broad habitats due to definitional complexities.

## 10. Conclusions and implications
- The 2007 digital mapping QA exercise demonstrates substantial agreement between QA and CS surveyors across most habitat types, linear features, and points, validating the monitoring framework and data governance processes.
- Some substantial discrepancies persist, especially in Blanket Bog and certain upland/mosaic habitats, highlighting definitional ambiguities and the need for ongoing training and refinement of habitat keys and allocation rules.
- The exercise underscores the importance of standardized metadata, data sharing, and transparent QA practices to support openness and comparability with national datasets.
- The shift to digital change recording and direct field verification enhanced data quality but introduced complexities that require continued methodological refinement and capacity-building for survey teams.