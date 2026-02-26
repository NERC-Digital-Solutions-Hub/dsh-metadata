# Dataset documentation

## Overview and purpose
- LCM2015 is a UK parcel-based land cover map created by classifying satellite data into 21 land cover classes, aligned with UK Biodiversity Action Plan Broad Habitat definitions.
- Built from two-date composites, mainly Landsat-8 (30m) with AWIFS (60m) as needed.
- Updates and unification with prior LCM versions (notably LCM2007); designed for monitoring environmental health and policy performance over time with standardized outputs.
- Important caution: LCM2015 is complex; differences across LCM products mean it should not be used directly for current-state change mapping without understanding methodological changes.

## Data products and formats
- Vector data set (core): ~6.7 million GB polygons and ~0.9 million NI polygons, each with rich attributes (gid, dominant class, pixel counts per class, uncertainty, mean probability, etc.).
- 25m raster: two-band product per polygon; Band 1 = dominant class, Band 2 = mean per-polygon probability from the classifier.
- 1km raster: aggregate products including dominant class (21-class and 10-class aggregates) and percentage cover (21-band and 10-band aggregates). 1km products derived by summarizing the 25m raster.
- Spatial extents and projections: GB data in British National Grid; NI data in TM75 Irish Grid; separate datasets for GB and NI.
- Area threshold: minimum mappable unit >0.5 ha; parcels <0.5 ha or linear features <20 m dissolved into surroundings.
- Unique labeling: each parcel has a gid for unambiguous communication; 1km products express percentage covers; rounding may cause sums to differ from 100%.
- Metadata and uncertainty: polygon-level metadata include dominant class, pixel breakdown, and probability; uncertainty is provided as mean per-polygon probability and standard deviation.
- Access and citation: DOIs exist for each product; 1km raster is openly accessible via CEH Environmental Information Platform; vector and 25m products available on request/licence. Licensing fees may apply for some users.
- Colour mapping and documentation: Appendix 3 provides standard colour mapping; Appendix 1–2 cover class definitions; Appendix 4 lists composite images used.

## Key methodology and differences from LCM2007
- Classification algorithm: Early LCMs used Maximum Likelihood; LCM2015 uses Random Forest, which handles multi-model training data and simplifies training data needs.
- Training data: Uses an initial stable set of training areas (areas classified the same in 2000 and 2007) plus additional coastal and difficult classes; emphasizes objective inclusion of ancillary data.
- Ancillary data: In LCM2015, ancillary data (e.g., slope, distance to rivers) are integrated into the input and classification, reducing post-classification rule work.
- Spatial framework and segmentation: LCM2015 removes segmentation-based polygons; classification is per-pixel with no segmentation, improving consistency for change mapping.
- Output and class changes:
  - Montane class removed (reclassified spectrally as Inland Rock or upland habitats) to enable change mapping; Montane distributions from LCM2007 should be used if needed.
  - Rough grassland class removed; grassland types align with JNCC Broad Habitats without the Rough category.
  - 25m raster becomes two-band (classification band + probability band); probability data for vector and 25m raster simplified.
  - No spectral sub-classes used (due to RF classifier); reduced training complexity.
  - Mixed woodland training uses pure stands (per-pixel) with polygon-level modal class summarization; may reclassify some mixed stands.
  - Spatial framework no segmentation; upland improvements and some error fixes noted; primarily affects GB vector and 25m raster.
- Output scope: LCM2015 maps land cover (not land use); establishes a per-pixel, per-class approach with multiple data products to support diverse applications.

## Class structure and data interpretation
- 21 target classes based on Broad Habitats; some are subdivided for more detail (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather Grassland; Littoral Sediment into Littoral Sediment and Saltmarsh).
- 1km products provide 21-class or 10-aggregate-class outputs; aggregation helps scenarios requiring coarser resolution.
- Special notes on classification of woodland: pure stands used for training; modal class assigned per polygon; pix_dist attribute allows exploration of sub-polygon variability.
- UK Broad Habitats definitions (Appendix 1–2) guide interpretation of classes and their spectral distinctions.

## Data access, use, and citation
- Access points:
  - 1km raster data: CEH Environmental Information Platform (free access).
  - Full vector and 25m raster: available under licence on request from CEH.
- Data identifiers: each product has its own DOI to enable precise citation (GB and NI, vector, 25m, 1km, dominant/percentage/aggregate formats).
- Projections: GB vector/raster in British National Grid; NI data in TM75 Irish Grid.
- Documentation and contact: further information and queries at CEH (spatialdata@ceh.ac.uk) and the LCM2015 project pages.
- Usage guidance: cite DOIs in publications; adhere to licensing terms; refer to the dataset paper when available.

## Practical considerations for environmental analysts
- Designed for monitoring environmental health and policy performance across time with standardized, well-documented outputs.
- Suitable for multi-source integration due to comprehensive metadata and uncertainty information.
- Not recommended for direct change mapping in its current state without careful consideration of methodological changes and version differences.
- Enables cross-scale analyses via vector (detailed polygons) and raster (25m and 1km) products; 1km products facilitate regional-scale modelling with other data layers (e.g., meteorological, species distribution).

## Appendices and technical notes (highlights)
- Appendix 1–3 summarize Broad Habitat definitions, class-specific notes, and colour mappings to support consistent visualization.
- Appendix 4 describes the composite images used during LCM2015 production (for reproducibility and methodological transparency).
- The document emphasizes the need to review outputs and scripts against LCM2015-specific methods due to differences from earlier LCM versions.