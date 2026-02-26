# Mapping Quality Assurance Exercise

- The Countryside Survey 2007 introduced digital field mapping with Surveyor software to map in the field, backed by an interactive wiki for early data checking and QA teams visiting survey teams to ensure protocol adherence.
- QA compared surveyors’ mapped data (CS) with QA-derived data using multiple approaches to assess mapping accuracy, consistency, and change recording across habitats, linear features, and points.
- The QA aimed to test the efficacy of digital data collection, geodatabase integration, and in-field quality control in producing comparable, decision-supporting national-scale datasets.

## QA approach and workflow

- Coverage and data handling
  - QA mapped 23 one-kilometre squares across different land classes to represent GB across varied habitats.
  - Data from QA and CS were aligned using a mask overlay to compare common surveyed areas, excluding unsurveyed or refused areas.
- Analytic methods used
  - 4.1 Direct comparison of aggregate areas/lengths/points for whole squares.
  - 4.2 Raster data comparisons by converting polygons to 10 x 10 m raster units to assess broad habitat proportions and locations.
  - 4.3 100-point grid to evaluate concordance of Broad Habitat codes at a fixed resolution.
  - 4.4 Attribute comparisons for areas, lines, and points via reference IDs.
- Data capture and QA workflow
  - Digital recording and wiki-based checks enhanced real-time data verification.
  - QA teams aimed to visit squares near CS teams to minimize temporal vegetation changes and reduce landowner disturbance.
  - Analysis included both aggregate measures and spatially explicit comparisons (raster, grid, and polygon level).

## Key findings by analysis area

- 6.1 Direct comparison of aggregate areas for whole squares
  - 81% of squares had CS and QA agreeing on Broad Habitat presence.
  - Mean differences between CS and QA generally below 3.5% across most habitats; several habitats showed larger SDs indicating potential allocation differences (notably Improved and Neutral Grassland, Dwarf Shrub Heath, Bog, Urban, and Sub-littoral sediment).
- 6.2 Comparisons of raster data
  - Overall raster agreement varied by square; average agreement around 70–90% across many squares, with some squares as low as ~49% (e.g., square 261) or ~23% (square 773).
  - Agreement by Broad Habitat showed uneven patterns across squares, with several squares displaying strong concordance (e.g., 364, 488) and others showing substantial mismatches.
- 6.3 100-point sample grid - Primary land cover codes and habitats
  - General good concordance across many squares; some squares showed notable mis-matches (e.g., 261, 773) on the 100-point grid.
  - The matrix highlights that certain habitat pairs (e.g., Blanket Bog vs Dwarf Shrub Heath; Urban vs Grassland) contributed to mismatches, reflecting definitional and mosaic-mapping challenges.
- 6.4 Polygon analysis of species attributes
  - 1081 QA polygons and 998 CS polygons matched by location; 45% of QA polygons had at least one species present in the matched CS polygon.
  - Habitat-level matching: overall, 77% of matched polygons also had matching Broad Habitats; 23% had no BH match.
  - Species concordance across matched polygons was about 40% for commonly recorded species; some species (Lolium perenne, Calluna vulgaris, etc.) showed higher or lower concordance depending on habitat and dominance.
- 7.1 Direct comparison of aggregate linear features
  - Lengths of linear features per square were broadly similar between QA and CS, with some differences by land-use theme (e.g., fences, banks, walls, forestry lines).
  - Generally high consistency; occasional confusion between similar feature types (e.g., belts of trees vs woody linear features).
- 8.1 Direct comparison of aggregate points for whole squares
  - Point counts by land-use theme were similar between QA and CS, with small differences in totals per square.
  - Forestry-related points (FO) dominated; veteran trees showed the greatest discrepancy between CS and QA data, likely due to field-level decision making on which trees to record.
- 8.2 Point features habitat codes
  - Most points received the same habitat codes in QA and CS; minor inconsistencies mainly around woodland/forest coding.
- 9 Assessment of change recording
  - Change coding included Real change, Error Change, and No change, with an extra field for potential error changes.
  - Overall agreement on change coding was strong across broad habitats and linear/point features; some habitat-specific discrepancies occurred, reflecting complexity in applying change codes to certain vegetation types.
  - The digital system facilitated in-field confirmation and updating of previous maps, though it added complexity to the survey process.

## Notable implications and issues

- Overall data quality
  - The digital mapping and QA workflow substantially improved data clarity, speed of analysis, and the ability to compare CS data with QA data across scales.
  - High overall agreement between CS and QA for many habitat categories indicates robust mapping under the 2007 protocol.
- Areas needing attention
  - Blanket Bog, Dwarf Shrub Heath, Neutral vs Improved Grassland, and Urban vs grassland allocations showed notable discrepancies in several analyses, highlighting definitional and boundary challenges.
  - Mosaic upland habitats and mosaicked areas complicate exact 1:1 matches between CS and QA datasets; disaggregation may introduce mis-matches.
  - Machair habitats in Scotland posed a localized anomaly where grassland-based classifications intersected with dune/sand habitats; location-specific landscape context affected coding.
  - Blanket Bog definitions were revised for 2007, and the QA results underline ongoing need for clear, consistent definitions and training, especially for high-value habitats.
- Species-level concordance
  - Species-level agreement was moderate overall; dominant species tended to yield higher concordance, while more diverse or less-dominant assemblages reduced the likelihood of identical species lists in matched polygons.

## Data handling and recommendations

- The exercise demonstrates the value of integrated digital data capture, geodatabase storage, and multi-method QA (direct area comparison, raster, 100-point, polygon/attributes, and change analysis) to quantify mapping quality.
- For future surveys and QA cycles:
  - Maintain and expand explicit habitat definitions and training to reduce misclassification between similar Broad Habitats, especially for Blanket Bog, Neutral/Improved Grassland, and Urban classifications.
  - Continue mosaic handling strategies and consider additional cross-walks or split-mosaic mapping approaches to minimize mismatches between CS and QA data.
  - Expand in-field change coding training and guidelines to improve consistency, particularly for habitat-rich mosaics where change interpretation is challenging.
  - Enhance documentation and metadata to ensure datasets created (maps, polygons, attributes) are easily discoverable and usable in national geodatabases and portals.