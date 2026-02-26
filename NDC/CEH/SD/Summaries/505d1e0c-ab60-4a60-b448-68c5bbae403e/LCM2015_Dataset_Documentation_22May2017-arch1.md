# Dataset documentation

- LCM2015 is a parcel-based UK land cover map with 21 classes, produced from two-date Landsat-8 composites (30m, supplemented with 60m AWIFS as needed) and classified with a Random Forest classifier.
- Outputs include a core vector data set, a 25m raster product, and 1km aggregate products, for Great Britain and Northern Ireland. Projections: GB on British National Grid; NI on TM75 Irish Grid.
- The dataset is designed to support diverse users (policy, planning, academic) and provides rich metadata, per-polygon uncertainty, and per-polygon class breakdowns.

- Important caution for users: LCM2015 is complex and not suitable for change-mapping in its current state. Differences between maps reflect both real change and classification/classification-error components.

- Purpose and scope
  - Maps land cover (not land use) using 21 Broad Habitat classes derived from JNCC Broad Habitat definitions.
  - Aims to enable change mapping in the future but currently should not be used as a direct change map without careful validation.

- Data products and formats
  - Vector product
    - 6.7 million polygons (GB) and 0.9 million polygons (NI).
    - Each polygon has a rich attribute set (at least 9 attributes including dominant class, gid, pixel counts per class, modal_class, uncertainty, and composite information).
  - 25m raster product
    - 2-band raster per area: band 1 = dominant LCM2015 class; band 2 = mean per-polygon probability from the classifier.
  - 1km raster products
    - Dominant class per 1km pixel (21-class scheme) and dominant class for 10 aggregated classes.
    - Percentage cover per class (21-band GB; 21-band NI) with rounding, area sums may not exactly equal 100 due to aggregation.
  - Data scale and mappable area
    - Minimum mappable area: >0.5 ha; parcels <0.5 ha or line features <20 m dissolved into surrounding landscape.

- Class structure
  - 21 target LCM2015 classes align with UK Broad Habitats; some classes are subdivided (e.g., Urban vs Suburban; Heather vs Heather grassland; Littoral/sub-littoral distinctions).
  - A detailed mapping table links target classes to aggregate classes used in raster products.

- Methodology and innovations
  - Classification algorithm changed from Maximum Likelihood (LCM2007) to Random Forest (LCM2015), enabling multi-model training data without sub-classing.
  - Training areas built from a stable core (areas classified the same in 2000 and 2007) and supplemented for coastal zones and difficult classes.
  - Ancillary data (e.g., slope, distance to water) are integrated as input data rather than post-classification rules, improving objectivity.
  - No segmentation-based spatial framework in LCM2015 (removal of segmentation polygons); classification is per-pixel, with polygon-level labeling.
  - Mixed woodland training uses pure stands for training, with modal_class assigned to polygons; some mixed-woodland classifications may reflect dominant components in the polygon.
  - Stable, archived product with DOIs for citation.

- Output data details
  - Vector dataset: includes gid (unique parcel identifier), dominant class (BHAB and LCM2015 target class), per-polygon pixel distribution (pix_dist), uncertainty (unc), standard deviation (unc_stdev), number of pixels (npix), modal_class, modal_prop, and composite image indicator.
  - 25m raster: two-band raster with the classification and probability band; units and metadata described in the product tables.
  - 1km raster: dominant cover and percentage cover for both 21-class and 10-aggregate schemes; metadata and tabled relationships provided.
  - DOI-cited datasets for Great Britain and Northern Ireland products exist to support reproducibility.

- Data access and use
  - 1km rasters available via the CEH Environmental Information Platform (EIP).
  - Full vector and 25m products available on request under licence from CEH; licensing may apply.
  - Data citations required; each product has its own DOI (GB vector; GB 25m; GB 1km percentage and dominant targets; NI equivalents).

- Color mapping and documentation
  - Appendices provide standard color mappings for class visualization and descriptions of the 21 target classes and their Broad Habitat counterparts.

- Practical notes for analysts
  - When using LCM2015 data, consider:
    - The per-polygon uncertainty and the per-pixel probability bands for assessing confidence.
    - The aggregation steps from 21 classes to 1km percent-cover products and potential minor rounding effects.
    - The improved alignment with Broad Habitat definitions and the removal of previously segmented spatial frameworks to ease change mapping in the future.
  - Always cite the appropriate DOIs when publishing results derived from LCM2015 data.

- References and contact
  - Contact: spatialdata@ceh.ac.uk; CEH website for LCM2015 information and access.
  - Key references include Jackson (2000) for Broad Habitat definitions and Morton et al. (2011) for LCM2007 methodology.