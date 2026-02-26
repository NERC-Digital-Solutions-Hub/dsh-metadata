# Dataset documentation

## Overview
- Land Cover Map 1990 (LCM1990) is a UK parcel-based land cover map classified into 21 classes, based on UK Biodiversity Action Plan Broad Habitat definitions.
- Created from two-date Landsat-5 composites (30 m resolution); designed to align with LCM2007/LCM2015 frameworks for cross-compatibility and long-term change analyses.
- Provides both vector (parcels with rich metadata) and raster (25 m and 1 km) products; aims to support a wide range of GIS applications.

## Data products and formats
- Vector data set
  - 6.7 million polygons for Great Britain; 0.9 million for Northern Ireland.
  - Key attributes per parcel include: land cover class (text and integer), source image, per-polygon pixel breakdown, dominant class, uncertainty, and geometry identifier (gid).
- 25 m raster
  - 3-band GeoTIFF: band 1 = dominant class per polygon; band 2 = mean per-polygon classifier confidence; band 3 = percentage area of polygon covered by the modal class.
- 1 km raster
  - Dominant cover (1 band) for target and aggregate classes.
  - Percentage cover (21 bands for target classes; 10 bands for aggregates) per 1 km pixel; values are integer and may not sum exactly to 100 due to rounding and coastal edge effects.
- Spatial details
  - GB and NI rasters use different projections: GB = British National Grid; NI = TM75 Irish Grid.
  - 25 m and 1 km rasters include metadata on extents, pixel counts, and coordinate origins.

## Data structure and attributes
- GID (geometry identifier) provides a unique parcel ID for communication across datasets.
- _hist attribute lists the classes present in a polygon and their pixel counts (e.g., "20:1, 21:9").
- _mode is the recommended display class (LCM1990 target class).
- _purity indicates the percentage of the polygon covered by the modal class.
- _conf and _stdev capture classifier confidence and its variability per polygon.
- _n is the number of pixels in the polygon; _cmp indicates the composite image source (99 = manual infill).

## Classification scheme and nuances
- 21 LCM1990 target classes are mapped from Broad Habitats definitions; some broad habitats are subdivided in LCM1990 (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Saltmarsh and Littoral sediment).
- LCM1990 maps land cover (not necessarily land use); spectrally similar land covers can be confounded with land use in some cases.
- Minimum mappable area: polygons >0.5 ha; line features <20 m dissolved into surrounding landscape during processing.
- Table mappings align LCM1990 classes with Broad Habitat concepts; Appendix 3 provides standard colour mappings for visualization.

## Data access and citation
- 25 m and 1 km rasters accessible via CEH Environmental Information Platform (eip.ceh.ac.uk).
- Full vector product available on request from CEH (licensing may apply).
- Each LCM1990 product has a DOI for citation; guidance provided for how to reference in publications (e.g., Rowland et al., 2020).
- Data usage and citation details are documented to support repeatability and traceability.

## Quality assurance and validation
- Data produced using defined methods and code by trained staff.
- QA checks cover projections, spatial completeness, modal class presence (vector), metadata headings alignment, value ranges (0–100 for raster), and correct pixel sizes.
- Validation has been conducted against other datasets (e.g., Countryside Survey, National Forest Inventory) with results to be published separately.

## Spatial framework and projections
- Vector and raster data for GB and NI use compatible spatial frameworks derived from Ordnance Survey MasterMap (GB) and Northern Ireland large-scale vector data.
- Projections: GB products in British National Grid (EPSG 27700); NI products in Irish Grid (TM75, EPSG 29903).

## Usage guidance and limitations
- The dataset provides rich, well-documented metadata per polygon, enabling detailed map-based analyses and communication of uncertainty.
- The 25 m raster is ideal for analyses requiring per-polygon detail with accompanying confidence metrics; the 1 km rasters are suited for national-scale modelling with aggregate/class percentage information.
- Users should be aware of potential misclassifications among grassland types and the challenges of representing complex habitats solely from spectral data.
- Small features below MMU or coastal edge effects may be dissolved or result in slight percentage summation discrepancies.

## Appendices (high-level highlights)
- Appendix 1 & 2: Descriptions of Broad Habitat definitions and mapping considerations; guidance on interpretation and potential aggregation of similar grassland classes.
- Appendix 3: Standard LCM colour mapping recipe for visualization consistency.
- Appendix 4: Composite image details used in LCM1990 production.

## Acknowledgement and references
- Funded by Natural Environment Research Council as part of UK-SCAPE National Capability.
- References include Jackson (2000) on Broad Habitat definitions and Morton et al. (2011) on LCM2007 methodologies, with subsequent LCM1990-related publications and DOIs.