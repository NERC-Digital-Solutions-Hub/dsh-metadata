# Dataset documentation

## Overview and scope
- Land Cover Map 2015 (LCM2015) is a parcel-based UK land cover map classifying satellite data into 21 land cover classes based on UK Biodiversity Action Plan Broad Habitat definitions.
- Produced from two-date image composites mainly using Landsat-8 (30 m) with AWIFS (60 m) as needed; updates the 2007 LCM.
- Outputs reflect real-world boundaries and are designed for easy interpretation and compatibility with other geospatial data.
- Maps land cover (not land use); e.g., arable crops indicate land cover type rather than use specifics.
- LCM2015 is a stable, archived dataset with individual DOIs for each product.

## Data products and structure
- Data formats and resolutions:
  - Core vector data (GB and NI) and a 25 m raster derived from the vector.
  - 1 km raster products derived from 25 m data (percent cover and dominant class).
  - Spatial frameworks: GB in British National Grid; NI in TM75 Irish Grid.
- Class structure:
  - 21 target classes, aligned to Broad Habitat types; plus 10 aggregate classes for 1 km products.
  - Some Broad Habitats are subdivided (e.g., Urban vs Suburban; Heather vs Heather grassland).
- Spatial detail and MMU:
  - Minimum mapped unit: >0.5 ha; polygons <0.5 ha and linear features <20 m dissolved into surrounding landscape.
- Vector data (GB and NI):
  - Approximately 6.7 million polygons (GB) and 0.9 million polygons (NI).
  - Attributes include: gid (unique parcel ID), BHAB (dominant land cover), pix_dist (counts per class within polygon), unc (mean per-polygon RF probability), unc_stdev, npix (pixels in polygon), modal_class (dominant class code), modal_prop (dominant proportion), Composite (composite image used).
- Raster data:
  - 25 m raster: band 1 = dominant class; band 2 = mean probability from Random Forest.
  - 1 km rasters: dominant class per 1 km cell; 21-band percentage covers (or 10 aggregate bands) depending on product.
- Provenance and labeling:
  - Each parcel has a unique gid; recommended to retain gid for unambiguous data communication.
- Data access and DOIs:
  - 1 km rasters available via CEH Environmental Information Platform.
  - Full vector and 25 m products available on request (licence may apply).
  - Each product has its own DOI; guidance provided for citing multiple GB and NI products.

## Methodology and key differences from LCM2007
- Classification method:
  - New Random Forest classifier replaces Maximum Likelihood; handles multi-modal training data and often improves performance.
- Training data:
  - Stable training areas identified from 2000 and 2007 classifications; coastal and difficult classes expanded with additional areas.
- Ancillary data integration:
  - Ancillary datasets (e.g., slope, distance to water) are part of the input data rather than post-classification enhancements.
- Output data and classes:
  - Montane and Rough grassland classes removed to improve change mapping consistency with updated class definitions.
  - Probabilities:
    - LCM2015 uses mean per-polygon probability (in vector) and band 2 of the 25 m raster; no probability data for 1 km products.
  - Sub-classing:
    - Spectral sub-classes removed; per-pixel classifications summarized to polygon level (reduces reliance on spectral sub-classes).
- Spatial framework:
  - No segmentation-derived polygons in LCM2015; aims for per-pixel classification with a stable framework, improving change-mapping potential.

## Uncertainty, quality, and caveats
- Uncertainty information:
  - Random Forest outputs per-pixel probability; represented as mean probability per polygon and in raster band 2.
- Change mapping considerations:
  - The differences between LCM products represent real change and classification error; not recommended to rely on LCM2015 alone for change mapping in its current state.
- Habitat-specific caveats:
  - Some confusion possible among grassland and certain habitat types; the document notes expected misclassifications and the influence of spectral versus ancillary data.
- 1 km products:
  - Percentage cover values are integers; sums may slightly exceed or fall short of 100 due to rounding and coastal area effects.

## Data formats, metadata, and accessibility
- Metadata and attributes:
  - Rich polygon-level metadata including dominant class, per-class pixel counts, uncertainty, and composite source.
- Coordinate systems:
  - GB: British National Grid (EPSG 27700); NI: TM75 Irish Grid (EPSG 29903).
- Data access and licensing:
  - CEH 1 km raster data via eip.ceh.ac.uk.
  - Full vector and 25 m products on request; licensing may apply; contact spatialdata@ceh.ac.uk or use CEH services page.
- Data citation:
  - Each product has its own DOI; recommended citation format provided for GB and NI products to support reproducibility.

## Usage guidance and practical notes for data support
- Product selection:
  - Use vector for detailed polygon-level analysis with rich metadata; use 25 m raster for a lighter-weight representation with no polygon boundaries.
  - Use 1 km rasters for national-scale modeling with aggregated class information.
- Data integration and mapping:
  - Align outputs with other geospatial layers using the appropriate national grid projection; ensure MMU and class aggregation considerations are accounted for in analyses.
- Documentation and references:
  - DOIs should be cited in publications; accompanying documentation and appendices provide class definitions and color mappings ( appendices relevant for color mapping and class definitions).

## Contact and further information
- Primary contact: spatialdata@ceh.ac.uk
- More information: CEH Lands Cover Map 2015 pages and CEH Environmental Information Platform
- Data paper and references provide detailed methodological context and class definitions.