# Dataset documentation

- LCM2015 is a UK parcel-based land cover map produced from satellite data (Landsat-8 primarily, with AWIFS as needed) classified into 21 land cover classes based on UK Biodiversity Action Plan Broad Habitat definitions.
- It provides a range of data products to support diverse user needs: a core vector dataset, a 25m raster, and 1km aggregate products (dominant and percentage cover) in both Great Britain and Northern Ireland projections.
- The dataset is designed for monitoring environmental health and policy performance over time, offering detailed metadata and per-polygon uncertainty estimates derived from a Random Forest classifier.

- Data products and formats
  - Vector data set: polygons with 9 attributes, including dominant class, per-polygon pixel distributions (pix_dist), uncertainty, npix, and modal_class. Contains approximately 6.7 million polygons for GB and 0.9 million for NI.
  - 25m raster: two-band raster; band 1 = dominant LCM2015 class, band 2 = mean per-polygon probability from the classifier.
  - 1km raster: derived by summarising 25m data into:
    - Dominant class (1 band)
    - Dominant aggregate class (1 band)
    - Percentage cover per class (21 bands) and aggregate (10 bands)
  - Minimum mappable area: >0.5 ha; parcels smaller than 0.5 ha dissolved into surrounding landscape.

- Classification and methodology
  - New classification algorithm: Random Forest (instead of Maximum Likelihood in earlier maps).
  - Training data: stable training areas drawn from areas classified the same in 2000 and 2007, supplemented with coastal areas and hard-to-map classes.
  - Ancillary data: integrated as input alongside satellite data (no post-classification KBEs for LCM2015; enhancements are built into the classifier).
  - No spectral sub-classes; per-pixel classification with polygon-level summarisation.
  - Spatial framework: no segmentation-based polygons in LCM2015; per-pixel classification in GB NI; some upland segmentation adjustments and error fixes applied where needed.
  - LABelling and metadata: each parcel receives a unique gid; rich metadata per polygon including pixel counts per class, majority class, and associated probabilities.

- Classes and labeling
  - LCM2015 uses 21 target classes aligned with Broad Habitats (JNCC Jackson 2000). Some classes are subdivided for detail (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral categories into detailed coastal classes).
  - Special notes on mixed woodland: training uses pure stands; polygons reflect modal_class; pix_dist can be inspected to understand mixed pixels.
  - Object labeling: the gid attribute is retained for unambiguous communication.

- Data origins, access, and citation
  - Data are distributed with DOIs (distinct DOIs for GB vector, GB 25m, GB 1km percent, GB 1km dominant, and NI equivalents).
  - Data access: 1km rasters via CEH Environmental Information Platform; full vector and 25m products available on request under licence from CEH (licensing may apply).
  - Projections: GB data in British National Grid; NI data in TM75 Irish Grid.

- Uncertainty and quality
  - The Random Forest classifier provides per-pixel probability, reported as mean per-polygon probability (unc) and standard deviation (unc_stdev) for the polygon.
  - The 1km and 25m products include probability information; probability is not provided for some 1km products.
  - The 0.5 ha MMU and per-polygon aggregation mean that some spectral confusion at fine scales may persist, especially for classes with spectrally similar signatures.

- Key cautions for users
  - Do not rely on LCM2015 in its current state for change mapping; changes between maps reflect a combination of real change and classification/methodological differences between versions.
  - Differences from LCM2007 include removal of Montane and Rough grassland classes, a shift to a per-pixel Random Forest approach, removal of segmentation in the spatial framework, and revised handling of mixed woodland.
  - Users should review data products in their intended use area, particularly where segmentation, altitude, soil data, or coastal dynamics affect classification outcomes.
  - Cross-version compatibility requires attention to output formats, class definitions, and the absence/presence of segmentation.

- Documentation and references
  - LCM2015 dataset papers and DOIs provide citation guidance and methodological details.
  - Appendices (noting class definitions and colour mappings) offer guidance on how classes map to Broad Habitats and how to interpret the 21-class vs 10-aggregate classifications.