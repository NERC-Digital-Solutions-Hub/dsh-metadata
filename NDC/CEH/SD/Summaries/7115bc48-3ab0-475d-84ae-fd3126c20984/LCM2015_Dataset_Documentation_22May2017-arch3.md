# Dataset documentation

- LCM2015: Land Cover Map 2015, a parcel-based UK land cover dataset created from satellite imagery (Landsat-8 30 m, AWIFS 60 m where needed) to classify into 21 Broad Habitat-based classes. It updates LCM2007 and uses a per-polygon spatial framework derived from generalised cartography, refined with rural boundary data.
- Purpose and cautions: designed to support a wide range of environmental monitoring and policy evaluation; differences from prior maps mean users should review the documentation to avoid misapplication (e.g., not recommended for current change mapping without careful validation).

- Data products and coverage
  - Core products: vector data (polygons with attributes), 25 m raster (two bands: classification and mean per-polygon probability), and 1 km raster products (dominant class, and percentage cover for 21 target or 10 aggregate classes).
  - Geographic split: separate datasets for Great Britain and Northern Ireland, with GB in British National Grid and NI in TM75 Irish Grid.
  - 1 km products include both 21-class and aggregated 10-class schemes to support broader-scale analyses.

- Classification and methodology
  - Algorithm: Random Forest classifier (replacing previous Maximum Likelihood Classifier). Benefits include handling multi-modal training data and improved performance.
  - Training data: stable areas defined as locations classified the same in 2000 and 2007; supplemented with coastal areas and classes historically challenging to map.
  - Ancillary data: integrated as part of input data (no post-classification KBEs in LCM2015; enables objective enhancements within the model).
  - Output and uncertainty: per-pixel probability estimates are provided as mean polygon probabilities in vector data and in band 2 of the 25 m raster; 1 km products do not include per-pixel probabilities.
  - Training details: single-pass per-polygon labeling; mixed woodlands are handled by summarizing pixel-level classifications to polygons, with potential modal_class assignments; training uses pure stands for coniferous/broadleaf classes.

- Differences from LCM2007 and methodological changes
  - Output data changes: Montane class removed (reclassified as Inland Rock or upland habitat in LCM2015); Rough Grassland removed; 25 m raster becomes two-band; probability data simplified; spectral sub-classes removed; segmentation-based spatial framework eliminated.
  - Methodological shifts: use of ancillary data as input; new training-area strategy; removal of segmentation in the spatial framework; direct per-polygon attribute-based uncertainty measures.
  - Habitat definitions: LCM2015 adheres to UK Broad Habitat classifications (JNCC), with some restructured groupings (e.g., Built-up Areas and Gardens split into Urban and Suburban; Dwarf Shrub Heath split into Heather and Heather grassland).

- LCM2015 classes and labeling
  - 21 target classes based on Broad Habitats (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Various Grassland types, Wetlands, Urban/Suburban, Coastal and Littoral classes, Inland Rock, etc.).
  - Some classes are further subdivided for enhanced detail (e.g., Built-up Areas and Gardens into Urban and Suburban).
  - Vector parcel identifiers (gid) provide unique IDs for unambiguous communication; per-polygon breakdown of pixel counts and mean dominance probability are available in metadata.

- Data quality, metadata, and uncertainty
  - Rich metadata: polygon-level attributes include dominant class, pixel counts per class within the polygon (pix_dist), uncertainty, number of pixels (npix), and modal_class (dominant class code).
  - Uncertainty: provided as mean per-polygon probability from the Random Forest classifier (unc) and its standard deviation (unc_stdev) where applicable.
  - The dataset is archived with Digital Object Identifiers (DOIs) for each product to support traceability and reproducibility.

- Data access and licensing
  - 1 km raster products available via the CEH Environmental Information Platform (EIP).
  - Full vector and 25 m raster products available on request under license from CEH; licensing fees may apply.
  - Data citations: each product (GB vector, GB 25 m raster, GB 1 km products, NI equivalents) has a DOI; publications should cite the DOIs and authors as specified.

- Data formats, scale, and mapping details
  - Vector: polygons with 9 attributes, including dominant class and detailed pixel breakdown; contains millions of polygons (GB ~6.7 million; NI ~0.9 million).
  - 25 m raster: two-band raster (band 1 = dominant class; band 2 = mean per-polygon probability).
  - 1 km rasters: dominant class (1 band) and percentage cover for both 21 target and 10 aggregate classes (multiple bands; integer values with rounding).
  - Minimum mapping unit: >0.5 ha; polygons smaller than 0.5 ha and line features under 20 m are dissolved to surrounding landscape.

- Projections and coordinate details
  - Great Britain: British National Grid (EPSG 27700 for GB data).
  - Northern Ireland: TM75 Irish Grid (EPSG 29903 for NI data).

- Usage notes and cautions
  - LCM2015 is not recommended for immediate change-detection mapping in its current state due to methodological and data-difference considerations with earlier maps.
  - Differences in output data formats and spatial frameworks between versions should be accounted for when combining with other datasets or conducting time-series analyses.
  - Users should reference the DOIs and accompanying metadata to ensure correct interpretation of class labels, probabilities, and aggregate/percentage products.

- Additional information and references
  - Documentation and further details available from CEH (land-cover-map-2015 and related pages).
  - Key references include Jackson (2000) on Broad Habitat definitions and Morton et al. (2011) on LCM2007 methods.
  - Appendices provide detailed class definitions, color mappings, and composite image information used in LCM2015.