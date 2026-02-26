# Dataset documentation

- Purpose and scope
  - Land Cover Map 2015 (LCM2015) provides a parcel-based UK land cover map classified into 21 classes, based on UK Broad Habitat definitions.
  - Supports a wide range of user needs, while advising that LCM2015 should not be used for change mapping in its current state.
  - Data types include GB vector, GB 25m raster, and 1km aggregated products; separate NI (Northern Ireland) datasets exist.

- Data sources and resolution
  - Derived from two-date composite satellite imagery, mainly Landsat-8 (30 m) with AWIFS (60 m) as needed.
  - A per-pixel (not strictly land use) land cover classification across Great Britain and Northern Ireland.
  - Minimum mappable area: >0.5 ha; polygons smaller than 0.5 ha and linear features <20 m dissolved into surrounding pixels.

- Classification framework and methodology
  - New Random Forest classifier (replacing previous Maximum Likelihood) to handle multi-modal training data and avoid sub-class grouping.
  - Ancillary data (e.g., slope, distance to rivers) are integrated as inputs rather than applied post-classification, enabling objective knowledge-based enhancements.
  - Training areas built from stable areas classified similarly in 2000 and 2007, supplemented with coastal and difficult classes; segmentation used in earlier versions removed to simplify change mapping.
  - Per-pixel probability uncertainty is provided via mean polygon probability (and stdev for some outputs).

- Outputs and data products
  - Vector data set
    - ~6.7 million GB polygons and ~0.9 million NI polygons.
    - Nine attributes per polygon, including dominant class, pixel counts per class, uncertainty, npix, modal_class, and Modal_prop.
  - 25 m raster
    - 2-band raster: band 1 = dominant LCM2015 class; band 2 = mean per-polygon probability of the dominant class.
  - 1 km raster
    - Dominant class and dominant aggregate class (1-band).
    - Percentage cover per class (21 bands for GB; 10 aggregate bands) with integer values (summations may not exactly total 100 due to rounding).
  - Spatial and metadata details
    - GB and NI data in separate coordinate systems: GB = British National Grid; NI = TM75 Irish Grid.
    - Rich metadata and per-polygon class breakdown (Pix_dist) available in vector products.
    - Unique geometry identifiers (gid) for unambiguous communication.

- Class structure and mapping
  - 21 LCM2015 target classes aligned with Broad Habitats (JNCC), with some internal subdivisions (e.g., Urban vs Suburban; Heather vs Heather grassland; Littoral sub-classes).
  - Tables and appendices provide mappings between LCM2015 classes, Broad Habitat definitions, and color mappings for visualization.
  - Some classes were reinterpreted spectrally in 2015 (e.g., Montane removed; Rough grassland removed; mixed woodland training focuses on pixel-level classification).

- Differences from earlier LCM versions (methodology and outputs)
  - Output data changes
    - Montane class removed; replaced with Inland Rock or upland habitats based on spectral data.
    - Rough grassland class removed to ensure alignment with JNCC Broad Habitats; no separate soil data reliance.
    - 25 m raster becomes a two-band product (classification + mean probability) instead of older probability formats.
    - Probability information simplified for vector; band 2 of 25 m raster carries mean per-polygon probability.
    - No spectral sub-classes; Random Forest obviates need for spectrally similar sub-classes.
    - Spatial framework without segmentation; segmentation from LCM2007 is not used in LCM2015.
  - Methodology changes
    - Transition to Random Forest classifier; improved handling of multi-model training data.
    - Stable training areas built from historical data (2000/2007) and expanded for coastal and problem classes.
    - Ancillary data incorporated as inputs rather than post-classification rules, making enhancements objective and integral.
  - Data representation
    - LCM2015 maps land cover; some land cover types may not map directly to land use.

- Data access and citation
  - 1 km raster data available via the CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector and 25 m raster products on request under licence from CEH; licensing fees may apply.
  - Each LCM2015 product has its own DOI for citation; guidance provided to correctly reference DOIs in publications.
  - Examples of DOIs cover GB vector, GB 25 m, GB 1 km (percent and dominant), and NI equivalents.

- Practical considerations for data leaders
  - Use across systems to support cross-sector data strategy, particularly for co-ownership of data products and stakeholder collaboration.
  - Be aware of the cautionary note on using LCM2015 for change mapping and align workflows accordingly.
  - Leverage the rich metadata, gid identifiers, and probability/uncertainty information to support quality assessment, auditing, and traceability.
  - Engage with the wider data community and maintain alignment with UK Broad Habitat definitions for interpretability and interoperability.

- References and additional information
  - Background references include Jackson (2000) on Broad Habitats; Morton et al. (2011) on LCM2007 methodology.
  - Detailed class definitions and colour mappings are provided in Appendix 1 and Appendix 3.
  - Further information and access details available at CEH websites and data portals.