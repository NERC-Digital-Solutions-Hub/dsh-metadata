# Dataset documentation

- LCM2015 (Land Cover Map 2015) provides parcel-based UK land cover classified from satellite imagery into 21 Broad Habitat-based classes, using two-date composites primarily from Landsat-8 (30 m) with AWIFS as needed.
- Data are distributed as multiple products to support diverse users: vector (core), 25 m raster, and 1 km raster (dominant and percentage cover for both 21 target classes and 10 aggregates).
- Outputs reflect real-world boundaries and aim for compatibility with other geospatial datasets; outputs map land cover rather than land use and are accompanied by rich metadata and uncertainty information.

 Key data products
- Vector data set (core product)
  - Approximately 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland.
  - Each polygon includes attributes: gid (unique parcel ID), dominant class (Modal_class), pixel counts per class (Pix_dist), uncertainty (unc), number of pixels (npix), dominant class proportion (Modal_prop), and composite source (Composite).
- 25 m raster
  - Two-band raster: band 1 = dominant LCM2015 class per polygon, band 2 = mean per-polygon probability from the Random Forest classifier.
- 1 km raster
  - Derived from 25 m data to produce:
    - Dominant cover per 1 km (21 target classes and 10 aggregate classes)
    - Percentage cover per 1 km pixel for both target and aggregate classes
  - Rounding can cause sums to slightly exceed or fall short of 100; coastal areas may sum to less than 100.
- Spatial coverage and projections
  - Great Britain: British National Grid (EPSG 27700)
  - Northern Ireland: Irish National Grid (EPSG 29903)
  - Data are separated by GB and NI datasets to reflect different projections; minimum mapping unit is >0.5 ha.
- Access and DOIs
  - 1 km raster data: CEH Environmental Information Platform (eip.ceh.ac.uk)
  - Full vector and 25 m raster: available under licence on request from CEH
  - Each product has its own DOI for citation (GB and NI products provided in Tables 4–5 of the dataset documentation)

 Classification framework and dataset details
- Classification approach
  - 21 LCM2015 target classes aligned to UK Broad Habitat definitions (JNCC Jackson, 2000).
  - Classifier: Random Forest (per-pixel classification), enabling multi-modal training data and obviating spectral sub-class grouping.
  - Training data: initial stable-area data from 2000 and 2007, enhanced with coastal and difficult classes; ancillary data (e.g., slope, distance to water) integrated as inputs rather than post-classification rules.
- Data content and metadata
  - LCM2015 vector includes gid, dominant class (Modal_class), per-class pixel distribution (Pix_dist), and uncertainty metrics (unc, unc_stdev), among other attributes.
  - 25 m raster includes the dominant class and a second band with the mean probability for that polygon’s class.
  - 1 km products include both dominant and percentage-coverage outputs for 21 classes and 10 aggregates.
  - Rich metadata and uncertainty information accompany the vector data; uncertainty is derived from the Random Forest probabilities.
- Class structure and mapping
  - 21 target classes are defined/labelled and can be aggregated into 10 broader groups for 1 km products.
  - Built-up Areas and Gardens is split into Urban and Suburban in the 21-class scheme.
  - Some Broad Habitat types are further subdivided (e.g., Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Saltmarsh and Littoral sediment).
- Notable differences from prior LCMs
  - Montane class removed; upland areas reclassified as Inland Rock or other upland habitats based on spectral data.
  - Rough grassland class removed; grassland types now align with JNCC Broad Habitat types without soil-data-based KBEs.
  - 25 m raster now two bands (classification and mean probability); probability data simplified (vector band includes majority-class mean probability; 25 m band 2 holds the same).
  - No spectral sub-classes in LCM2015 due to Random Forest handling multimodal data.
  - Spatial framework: segmentation-derived polygons removed; per-pixel classification with a simpler, repeatable process intended to ease change mapping in the future.
  - Mixed woodland training relies on per-pixel classification with final polygon labels derived by modal_class, which may affect some polygons containing mixed woodland components.
- Output and usability considerations
  - LCM2015 is a stable, archived dataset with DOIs; users should cite DOIs when referencing products.
  - LCM2015 maps land cover, not land use; some spectral classes may not map cleanly to land use concepts (e.g., grass used for recreation vs. grazing).
  - To facilitate use, the 25 m raster provides a more lightweight option without polygon metadata; 1 km products are suitable for national-scale modeling with meteorological or species-distribution data.
- Citing and references
  - Data papers and DOIs provided for GB vector, GB 25 m raster, GB 1 km products (percentage and dominant target/aggregate classes), and NI products; DOIs enable clear, repeatable citation.

 Cautions and usage notes
- The document advises that LCM2015 is complex and not suitable for change mapping in its current state; differences between maps are due to real changes and classification errors, compounded by changing methods and data inputs across iterations.
- Some outputs (e.g., Montane and Rough grassland) have been reclassified or removed to improve change-mapping suitability and methodological consistency.
- Caution is advised when interpreting certain grassland and mixed woodland classifications; users may need to consult Appendix definitions and consider aggregating classes if appropriate.
- Outputs include uncertainty measures (probability) to aid interpretation of the dominant class and to gauge classification confidence.

 Use guidance and references
- The dataset includes extensive appendices detailing class definitions (Broad Habitat interpretations), colour mapping schemes, and composite image usage, along with references to Jackson (2000) and Morton et al. (2011) for background on broad habitats and previous LCM methods.

 Access, licensing, and further information
- Access to 1 km raster data via CEH platform; vector and 25 m products on request with potential licensing fees.
- Full metadata, processing details, and DOIs available via CEH and CEH EIDC resources; data users are encouraged to cite the DOIs in publications.