# Dataset documentation

- LCM2015 is a UK-wide, parcel-based land cover map produced from satellite imagery (primarily Landsat-8 30 m, supplemented by AWIFS 60 m) and classifies into 21 Broad Habitat classes aligned with UK Biodiversity Action Plan definitions.
- Products are available in multiple formats and resolutions to support diverse GIS needs: vector (core), 25 m raster, and 1 km raster products (dominant and percentage covers, aggregated classes).

## Key data products and formats

- Vector data set
  - 6.7 million polygons for Great Britain; 0.9 million for Northern Ireland
  - 9 attributes per polygon, including:
    - gid: unique polygon identifier
    - BHAB: dominant land cover class (text and integer)
    - Pix_dist: counts of pixels per class within the polygon
    - unc and unc_stdev: mean per-polygon uncertainty and its standard deviation
    - npix: number of pixels in the polygon
    - Modal_class and Modal_prop: recommended display class and its share
    - Composite: source composite image identifier
- 25 m raster
  - 2 bands: band 1 = dominant class per polygon; band 2 = mean per-polygon probability
- 1 km raster
  - Dominant cover (21-class and 10-aggregate options) and percentage cover (21 bands and 10 aggregates)
  - Percent values are integers; sums may deviate from 100 due to rounding
- Metadata and labeling
  - Each parcel has a gid to enable unambiguous communication
  - Rich metadata for each polygon; includes per-polygon breakdown of class pixels and mean probability
- Data access and DOIs
  - 1 km raster via CEH Environmental Information Platform
  - Full vector and 25 m raster available on request (licenced; fees may apply)
  - Each product has its own DOI for citation (GB and NI variants)

## Classification and methodology

- Classifier
  - Uses Random Forest; replaces the previous Maximum Likelihood approach
  - Handles multi-model training data; avoids spectral sub-class grouping
- Training data and stability
  - Initial training areas derived from areas consistently classified the same in 2000 and 2007; supplemented with coastal and poorly mapped classes
- Ancillary data integration
  - Ancillary datasets used as input features within the classifier (not post-classification rules)
  - Reduces reliance on manual knowledge-based enhancements
- Spatial framework and segmentation
  - No segmentation-based polygons in LCM2015 spatial framework (eliminates segmentation inconsistencies across LCM versions)
  - Segmentation removal mainly affects upland areas; NI is unaffected
- Grassland and Montane changes
  - Montane class removed; replaced by Inland Rock or other upland habitats (for change mapping suitability)
  - Rough grassland removed; matches JNCC Broad Habitat types; no soil data used
- Woodland classification
  - Mixed woodland defined by >20% deciduous cover; training uses pure stands; polygon labels derived from pixel-level results
  - Users can explore pix_dist for potential misclassifications
- Mapping scope
  - LCM2015 maps land cover (not strictly land use)
  - Aims to be stable and archivable; DOIs provided for citation

## Classes and data content

- 21 LCM2015 target classes based on UK Broad Habitats
  - Subdivisions for certain broad habitats (e.g., Urban vs Suburban; Heather vs Heather grassland; Littoral Rock/Sediment splits)
- Unique labelling
  - gid retained to allow unambiguous communication; crucial for developments and integration
- Data quality and uncertainty
  - RF produces per-pixel probability; provided at polygon level (vector) and in band 2 of 25 m raster
  - Uncertainty values scaled to 0–255; standard deviation also provided
- Aggregates and mapping to other products
  - 1 km products offer dominant and percentage covers for both 21 classes and 10 aggregates
  - GB and NI datasets use respective projections (British National Grid for GB; Irish National Grid for NI)

## Data access, use, and citation

- Access
  - 1 km raster: eIP CEH platform
  - Full vector and 25 m raster: on request from CEH (licensing may apply)
- Usage notes
  - LCM2015 is complex; not recommended for change mapping in its current state due to differences in methods and class definitions over time
  - Minimum mappable area is 0.5 ha; parcels smaller than 0.5 ha or linear features under 20 m are dissolved
  - LCM maps land cover, which may not directly indicate land use in all cases
- Citation and DOIs
  - Each product has a DOI for GB and NI variants (vector, 25 m, 1 km percentage/dominant classes, and aggregates)
  - DOIs should be cited in publications to ensure reproducibility

## Projections and data specifications

- Projections
  - GB vector and GB 25 m and 1 km rasters: British National Grid (EPSG 27700)
  - NI vector and rasters: TM75 Irish Grid (EPSG 29903)
- Data specifics
  - 25 m raster: 25 m pixel size; unsigned 8-bit data
  - 1 km raster: 1,000 m pixel size; unsigned 8-bit data
  - Extents and grid details vary between GB and NI datasets
- Documentation and references
  - Extensive appendices (class definitions, color mapping, composite image details, and mapping recipes) accompany the dataset

## Practical notes for GIS specialists

- The vector product provides rich attribute data at the cost of larger file sizes; use 25 m raster when a lighter-weight raster with similar class detail is preferred
- For change detection work, exercise caution due to methodological differences between LCM2015 and earlier maps
- Use the gid and pix_dist attributes to perform custom accuracy assessments or to reconcile mixed-class areas
- When combining with other datasets, ensure alignment with the stated coordinate systems and consider the 0.5 ha MMU in planning analyses