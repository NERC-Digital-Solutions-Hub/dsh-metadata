# Dataset documentation

- LCM2015 is the Land Cover Map 2015 for the UK, produced by classifying satellite data into 21 land cover classes based on UK Broad Habitat definitions.
- Data products include a core vector dataset, a 25m raster, and 1km aggregated products (dominant and percentage cover for both 21 classes and 10 aggregates).
- The dataset is designed for a wide user community and emphasizes rich metadata, uncertainty information, and traceability via digital object identifiers (DOIs).
- Users are advised that LCM2015 should not be relied upon in its current state for change mapping; differences between maps reflect real change and classification differences as well as methodological updates.

## Data products and structure

- Vector data set
  - 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland.
  - Nine attributes per polygon, including:
    - gid (unique polygon identifier)
    - BHAB (dominant land cover at Broad Habitat level)
    - Pix_dist (list of 23 numbers: pixels per class 1–21, followed by npix and modal_class)
    - unc (mean per-polygon probability from classification)
    - Unc_stdev (standard deviation of uncertainty)
    - npix (number of pixels in polygon)
    - Modal_class (dominant LCM2015 class as an integer)
    - Modal_prop (proportion of polygon classified as dominant class)
    - Composite (source composite image)
- 25m raster data set
  - Two-band raster: band 1 = dominant LCM2015 class per polygon; band 2 = mean per-polygon probability from the Random Forest classifier.
  - Separate GB and NI datasets, aligned to respective projections.
- 1km raster data set
  - Derived from 25m data to provide:
    - Dominant cover at 1km (21-class and 10-aggregate classifications)
    - Percentage cover at 1km for both 21 classes and 10 aggregates
  - Integer percentage values with rounding; sums may deviate from 100 due to rounding and coastal proportions.
- Class mapping and labeling
  - LCM2015 uses 21 target classes based on JNCC Broad Habitat definitions; some classes are subdivided (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral into Littoral Rock/Sediment variants).
- Data availability and formats
  - 1km raster: available via CEH Environmental Information Platform (EIP).
  - Full vector and 25m raster: available on request under licence from CEH (licence fees may apply).
  - DOIs: separate DOIs exist for GB vector, GB 25m raster, GB 1km dominant cover, GB 1km percentage cover, GB 1km aggregate cover; NI counterparts also have DOIs.
- Spatial and coordinate systems
  - GB data: British National Grid (OSGB 27700)
  - NI data: Irish National Grid (TM75 Irish Grid)
  - Per product metadata includes pixel size (25m for 25m products, 1km for 1km products) and grid extents.

## Methodology and differences from earlier maps

- Classification approach
  - Random Forest classifier used for LCM2015 (replacing the previous Maximum Likelihood Classifier).
  - Ancillary data (e.g., slope, proximity to water) are integrated as inputs within the classifier, reducing reliance on post-classification knowledge-based rules.
- Training data and segmentation
  - Training areas built from a stable set of classifications that were consistent between 2000 and 2007, supplemented for coastal areas and classes historically difficult to map.
  - No image segmentation is used in the LCM2015 spatial framework (removal of segmentation-based polygons); this aims to simplify change mapping and improve consistency across time.
- Differences in output data and methodology (highlights)
  - Montane class removed; mapped as Inland Rock or other upland habitats based on spectral data (Montane data available only in LCM2007).
  - Rough grassland class removed; grassland types now align with JNCC Broad Habitat types.
  - 25m raster now two-band (classification band + probability band); probability data simplified to per-polygon mean probability for vector and provided in the second band of the 25m raster.
  - No spectral sub-classes used; spectral sub-classes are rendered redundant with Random Forest.
  - Spatial framework: segmentation used in LCM2007 was removed in LCM2015 to avoid segmentation misalignments; particularly affects GB vector and GB 25m raster.
  - Mixed woodland labeling updated: training uses pure stands for Coniferous/Broadleaf, with modal_class assigned at polygon level; users can inspect pix_dist for details.
- Output scope
  - LCM2015 maps land cover (not land use) and provides multiple product formats to support diverse applications, including per-polygon metadata and uncertainty.

## Citing and data governance

- Each product has its own DOI for citation, supporting reproducibility and traceability in publications.
- Data governance and access
  - CEH EIP hosts the 1km raster product; full vector and 25m raster licensing is required for access.
  - Contact: spatialdata@ceh.ac.uk and the CEH licensing portal for access details and fees.
- Documentation and metadata
  - Rich metadata captured for each polygon, including detailed attribute breakdowns, per-polygon probabilities, and composite source information.
  - The dataset is archived with DOIs to support scholarly referencing (cited examples provided in the document).

## Practical considerations for Data Stewards

- Data quality and uncertainty
  - Per-polygon mean probability (unc) and standard deviation (unc_stdev) accompany the vector data, enabling users to assess classification confidence at the local level.
  - 1km and 25m products summarize per-polygon probabilities, but coarse-scale products may mask sub-polygon variability.
- Temporal and change considerations
  - Differences between LCM2015 and prior maps reflect methodological updates as well as real land cover changes; use caution when performing change detection across generations.
  - The 0.5 ha minimum mapping unit and dissolution of small features ensure printer-friendly, analysis-ready outputs but may omit very small features.
- Metadata richness and data stewardship
  - The dataset includes extensive metadata (including gid, dominant class, per-class pixel counts, and probability metrics) to support data governance, provenance, and interoperability.
- Data use and interoperability
  - Vector vs. raster trade-offs: vector provides rich attributes but larger file sizes; 25m raster offers a simpler, boundary-free representation suitable for many analyses; 1km rasters facilitate regional- to national-scale modelling with aggregated information.
- Compatibility and guidance
  - Users should review Appendix 1–3 (class definitions, color mappings, and composite image details) to ensure proper interpretation and visualization of the LCM2015 classes.

## Appendices and ancillary information

- Appendix 1–3 include detailed class definitions, standard colour mappings for visualization, and the composite image recipe used in LCM2015 production.
- The documentation also outlines the relationship between LCM2015 classes and Broad Habitat definitions, with notes on ambiguities and areas where spectral data may not fully distinguish certain habitats.

## Access, citation, and contact

- Data access
  - CEH EIP provides 1km raster data; full vector and 25m raster are available on licence on request.
  - Online application and contact: spatialdata@ceh.ac.uk; http://www.ceh.ac.uk/services/informationproducts
- Citing LCM2015
  - Each product has individual DOIs; citations should include author(s), date, and full DOI in the references.
  - Example citation format and DOIs are provided in the document (for GB and NI products).

- Further information
  - Official information pages: https://www.ceh.ac.uk/services/land-cover-map-2015 and https://eip.ceh.ac.uk/lcm
  - Queries: spatialdata@ceh.ac.uk