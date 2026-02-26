# Dataset documentation

- LCM2015 is a parcel-based UK land cover map produced from Landsat-8 (30 m) with AWIFS (60 m) data, classified into 21 Broad Habitat-based classes and packaged as multiple data products to support map-based GIS use.
- It updates and replaces the LCM2007 framework, with a per-pixel classification approach and a focus on enabling change mapping in the future.

## Data products and formats

- Vector data set
  - Polygons with rich attributes: dominant class, gid (geometry ID), per-polygon pixel breakdown (Pix_dist), uncertainty (unc), number of pixels (npix), modal_class and modal_prop, and composite image source.
  - Approximately 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland.
- 25 m raster
  - Two-band raster: band 1 = dominant LCM2015 class; band 2 = mean per-polygon probability from Random Forest.
- 1 km raster
  - Summary products: dominant class per 1 km pixel (21 target classes or 10 aggregate classes) and percentage cover per class (21 bands for GB; 10 bands for aggregates).
  - Spatial extent split GB vs Northern Ireland with corresponding projections.
- Data extent and causes
  - Minimum mappable area: >0.5 ha; smaller parcels dissolved into surrounding landscape.
- Projections
  - GB: British National Grid; NI: TM75 Irish Grid (separate GB/NI datasets).

## Class structure and labeling

- LCM2015 uses 21 target Broad Habitat classes (based on JNCC definitions) with some sub-class refinements:
  - Built-up Areas and Gardens divided into Urban and Suburban.
  - Dwarf Shrub Heath divided into Heather and Heather grassland.
  - Littoral Sediment divided into Littoral Sediment and Saltmarsh (Priority Habitat).
- Unique object labeling
  - Each parcel has a gid to enable unambiguous data communication.
- Metadata and uncertainty
  - Rich polygon metadata; per-polygon mean probability (uncertainty) from Random Forest; probability values provided for vector and 25 m products.

## Methodology and key differences from LCМ2007

- Classification algorithm
  - Random Forest classifier replaces Maximum Likelihood Classifier; handles multi-modal training data and simplifies training data preparation.
- Training data and ancillary data
  - Stable training areas used as a starting point; coastal areas added; ancillary data (e.g., slope, proximity to rivers) are integrated as input data rather than post-classification rules.
- Spatial framework and segmentation
  - No segmentation-based polygons in LCM2015; per-pixel classification with a per-polygon summary; segmentation used in LCM2007 to break up large polygons is removed to improve change mapping consistency.
- Grassland and woodland refinements
  - Rough grassland removed; grassland types aligned with JNCC Broad Habitats without soil data reliance.
  - Mixed woodland labeling updated: training uses pure stands for Coniferous/Broadleaf with per-pixel classification and polygon-level modal labeling; pix_dist attribute can reveal nuances.
- Land cover vs land use
  - LCM2015 maps land cover; mapping may not always reflect land use (e.g., arable crops vs. actual use).
- Output data changes
  - Montane class removed; 25 m raster includes two-band structure; probability data reorganized (vector includes per-polygon mean probability; 25 m raster band 2 contains mean probability; 1 km products do not include probability).

## Data products overview and accessibility

- Core vector product
  - Rich attributes, gid-based parcels, and per-polygon composition data.
- 25 m raster product
  - Per-polygon dominant class with accompanying per-polygon probability.
- 1 km products
  - Dominant and percentage cover for both 21 classes and 10 aggregates.
- Data access
  - 1 km raster data via CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector and 25 m products available on license on request from CEH.
  - Licenses may apply; contact spatialdata@ceh.ac.uk for details.

## Documentation, DOIs, and citation

- LCM2015 products have individual DOIs for GB and NI (vector, 25 m, 1 km dominant/percentage products).
- The dataset provides guidance for proper citation to ensure replicability and traceability of usage.

## Usage cautions and recommendations

- LCM2015 is complex; differences and potential errors mean it should not be used for change mapping in its current state without consulting the accompanying documentation.
- Differences across LCМ products over time reflect both real change and classification differences; users should review the methodological notes when comparing with LCМ2007/LCM2000.

## Projections, units, and spatial details

- Great Britain: GB vector and 25 m rasters in British National Grid; 1 km products align with the same projection.
- Northern Ireland: NI vector and rasters in TM75 Irish Grid; 1 km products follow the NI projection.
- Coefficients, table references, and appendices provide details on class mapping and color schemes for visualization.