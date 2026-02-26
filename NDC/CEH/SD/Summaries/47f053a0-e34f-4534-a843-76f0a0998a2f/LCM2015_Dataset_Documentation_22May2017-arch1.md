# Land Cover Map 2015 (LCM2015)

## Overview
- UK parcel-based land cover map created by classifying satellite data into 21 land cover classes aligned with UK Biodiversity Action Plan Broad Habitat definitions.
- Based on two-date composites, primarily using Landsat-8 (30 m) with supplementary AWIFS (60 m) data.
- Constructed from polygons reflecting real-world boundaries to aid interpretation and compatibility with other geospatial datasets.
- Encourages cautious use for change mapping; differences from previous maps arise from real changes and classification errors.

## Data products and formats
- Vector data set (core product): polygons with rich attributes (geometric ID, dominant class, pixel counts per class, uncertainty, etc.). GB and Northern Ireland totals: ~6.7 million polygons (GB) and ~0.9 million (NI).
- 25 m raster: two-band raster per polygon; Band 1 = dominant class, Band 2 = mean per-polygon probability from the classifier.
- 1 km raster: derived products summarising 25 m data to percentage cover and dominant class per 1 km cell; provided for both 21 target classes and 10 aggregate classes.
- Data access: GB 1 km raster via CEH Environmental Information Platform; full vector and 25 m products on request (licence may apply).

## Key features of the data
- 21 target land cover classes based on Broad Habitats; some classes split into subtypes (e.g., Urban vs Suburban; Heather vs Heather grassland).
- Each parcel (gid) has a unique label; attributes include dominant class, per-class pixel counts, and majority class probability.
- Per-polygon uncertainty: mean probability from Random Forest; standard deviation available.
- Spatial framework is per-pixel; no segmentation in the LCM2015 spatial framework (segmentation used in LCM2007 removed to improve change-mapping consistency).
- Contains metadata-rich information for reproducibility; each product has a DOI for citation.

## Classification methodology
- Core classifier: Random Forest (replaces previous Maximum Likelihood). Benefits include handling multi-modal training data and typically better performance.
- Training data: initially derived from stable areas classified the same in 2000 and 2007; supplemented with coastal areas and classes historically problematic (Fen, Marsh, Swamp; semi-natural grasslands).
- Ancillary data: used as inputs within the classification process (not post-classification refinements); contrasts with LCM2007 where ancillary data were applied post-classification.
- Outputs: per-pixel classification with polygon-level summaries; sub-class spectral distinctions removed as spectrally redundant with Random Forest approach.

## Differences from LCM2007 (highlights)
- Output data changes:
  - Montane class removed; replaced by Inland Rock or other upland habitats based on spectral data. Use LCM2007 for Montane distributions.
  - Rough grassland class removed; grassland types re-aligned with JNCC Broad Habitat types; no soil data used in LCM2015.
  - 25 m raster becomes a two-band image (classification band + mean probability in Band 2).
  - Probability reporting simplified: vector stores mean polygon probability; 25 m Band 2 stores mean probability; 1 km products do not include probability.
  - No spectral sub-classes used; Random Forest reduces need for sub-class training.
  - Spatial segmentation removed from framework; focus on per-pixel classifications to ease change mapping.
  - Mixed woodland classification adjusted: training uses pure stands; polygon label determined by modal class, which may affect certain mixed patches.
- Methodology changes:
  - Switch to Random Forest classifier.
  - Stable training areas expanded with coastal areas and difficult classes.
  - Ancillary data integrated into input and used by the classifier.
  - Output products and uncertainty information adapted to new framework.

## Class structure and aggregation
- 21 LCM2015 target classes mapped from Broad Habitats; certain Broad Habitats are subdivided in the LCM2015 scheme (e.g., Urban vs Suburban; Heather vs Heather grassland; Littoral categories).
- 1 km products provide aggregate classes to enable modelling at national scales; 1 km percentage cover is the sum of 25 m rasters within each 1 km cell.
- A well-documented mapping between LCM2015 classes, Broad Habitats, and aggregated classes is provided, including color mappings in Appendix 3 for visualization.

## Data quality, scale, and caveats
- LCM2015 is a stable, archived dataset with DOIs for citation; the 0.5 ha minimum mappable unit and dissolution of smaller features to the surrounding landscape affect some small parcels and linear features.
- Differences between land cover maps reflect both real change and classification errors; caution is advised when using LCM2015 for change detection without appropriate processing.
- The product includes uncertainty information per polygon and per-pixel probability values for the 25 m raster.

## Spatial reference and coverage
- Projections: GB data in British National Grid; Northern Ireland data in Irish National Grid.
- Table 3 provides detailed metadata for 25 m and 1 km products, including extents, pixel counts, coordinate origins, and EPSG codes.

## Metadata, citations, and access
- Each LCM2015 product has a DOI; guidance provided on how to cite in publications with author names and dates.
- Full vector and 25 m raster data are available on request; 1 km raster data accessible via CEH platform.
- Contact and additional information: CEH spatialdata team (spatialdata@ceh.ac.uk), with project pages for LCM2015 and data citation guidelines.

## Practical guidance for users (analysts)
- Use the vector dataset for detailed boundary and attribute analysis; use the 25 m raster when a lighter-weight dataset or faster processing is needed; use 1 km products for national-scale modelling.
- Retain gid and per-polygon metadata to enable unambiguous communication and reproducibility.
- When performing change mapping, understand that LCM2015 intentionally removes segmentation and that some class definitions have changed from LCM2007; consider cross-walking fields to ensure consistency.

## Appendices (summary)
- Appendix 1 and 2 provide definitions for Broad Habitats and their mapping in LCM2015.
- Appendix 3 provides standard LCM2015 color mappings for visualization.
- Appendix 4 lists composite images used in LCM2015, detailing date ranges and sensor information.