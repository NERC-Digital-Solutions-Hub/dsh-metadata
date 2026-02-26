# Dataset documentation

- Purpose and scope
  - LCM2015 is a UK parcel-based land cover map produced from satellite data (Landsat-8 30m, supplemented with AWIFS 60m) to classify into 21 Broad Habitat-based classes.
  - Built to support diverse user needs and change mapping, with emphasis on a repeatable, per-polygon geometry framework and interoperable data products.
  - Noted caveat: Differences between LCM products mean differences in change signals; the dataset in its current state is not recommended for change mapping without careful consideration.

- Data products and structure
  - Core products and formats
    - Vector dataset: polygons with rich attributes; 6.7 million polygons (GB) and 0.9 million (NI); per-polygon metadata and uncertainty.
    - 25m raster: two-band raster (band 1 = dominant class, band 2 = mean per-polygon probability).
    - 1km raster: aggregate products providing dominant class and/or percentage cover per 1km cell.
  - Class structure
    - 21 LCM2015 target classes based on JNCC Broad Habitats definitions; certain Broad Habitats split into sub-classes (e.g., Urban vs Suburban, Heather vs Heather grassland).
    - Each parcel (gid) has a unique label for unambiguous communication; per-polygon breakdown of pixel counts by class (Pix_dist) and dominant class (Modal_class).
  - Spatial details and data scale
    - Minimum mappable area: >0.5 ha; smaller parcels dissolved into surrounding landscape.
    - Two separate national extents: Great Britain and Northern Ireland, with different coordinate systems (British National Grid for GB, Irish Grid for NI).
  - Documentation and metadata
    - Each product has DOIs for citation; extensive metadata per polygon including dominant class, pixel counts, and uncertainty measures.

- Methodology and differences from earlier maps
  - Classification approach
    - New Random Forest classifier (instead of Maximum Likelihood) enabling multi-modal training data and removal of spectral sub-classes.
    - Ancillary data (e.g., slope, distance to rivers) incorporated as input features rather than post-classification refinements.
  - Training and data handling
    - Stable training areas used as a base, augmented for coastal areas and challenging classes; reliance on per-pixel training rather than segment-based training.
  - Spatial framework and segmentation
    - No segmentation-based polygons in LCM2015; eliminates prior segmentation-based inconsistencies to better support change mapping.
  - Output data changes
    - Montane class removed; Rough grassland class removed; 25m raster uses two bands; per-polygon probability reported as mean polygon probability; no spectral sub-classes used; classification summary consolidated to 21 target classes.
  - Woodland classification
    - Mixed woodland handled differently: pixels classified for pure stands, then summarized to polygons; may assign some >20% Broadleaf to Coniferous class depending on pixel-level results.

- Data quality, uncertainty, and provenance
  - Uncertainty is quantified using Random Forest-derived per-pixel probabilities, summarized per polygon and in the 25m raster band 2.
  - Rich metadata for each polygon includes dominant class, full pixel distribution (Pix_dist), and confidence metrics.

- Access, licensing, and citation
  - Data access
    - 1km raster datasets available via CEH Environmental Information Platform.
    - Full vector and 25m raster products available on request under licence; licensing fees may apply.
  - Projections and coverage
    - GB products in British National Grid; NI products in Irish Grid; tabled metadata provides extents and pixel grids.
  - Citing LCM2015
    - Each product has its own DOI; users should cite the DOIs with full author/date info as per CEH guidance.
  - Contact and further information
    - Data queries via CEH spatial data team; project pages provide additional detail and updates.

- Practical considerations for data leaders
  - Governance and stewardship
    - LCM2015 provides a robust, richly documented vector and raster suite with per-polygon metadata, enabling traceability and auditability.
  - Data integration and interoperability
    - Multiple data formats (vector, 25m raster, 1km raster) and two national grids facilitate integration with other national datasets and modelling workflows.
  - Usage caveats
    - The dataset is complex; not recommended for direct change mapping without accounting for methodological and class-definition differences across time.
    - Users should refer to Appendix guidance and DOIs for precise class mappings and colour standards when visualising results.