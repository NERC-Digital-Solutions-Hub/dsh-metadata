# Land Cover Map 2015

- LCM2015 is the UK-wide parcel-based land cover map, classifying satellite imagery into 21 Broad Habitat-based classes defined by JNCC/Jackson (2000).
- Built from two-date composite images, mainly using Landsat-8 (30 m) with AWIFS (60 m) as needed; updated from LCM2007 with a per-pixel, polygonal structure for consistency with change mapping.
- Projects include a per-pixel core vector dataset, a 25 m raster, and 1 km percentage/dominant products, with GB and Northern Ireland datasets provided separately.

## Data Products and Formats

- Core data products
  - Vector dataset: 6.7 million GB polygons and 0.9 million NI polygons, each with a rich attribute set.
  - 25 m raster: two-band product (band 1 = dominant class, band 2 = mean per-polygon probability).
  - 1 km rasters: (a) dominant class at 1 km for both 21 target classes and 10 aggregate classes; (b) 1 km percentage cover for both class sets.
- Class structure
  - 21 LCM2015 target classes, mapped to Broad Habitats; some classes are further divided (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland).
  - 10 aggregate classes for 1 km raster outputs.
- Attributes and metadata
  - Vector: gid (unique parcel ID), BHAB (dominant Broad Habitat class, text and integer), Pix_dist (counts per class within the polygon), unc (mean probability scaled 0–255), unc_stdev, npix (pixels in polygon), Modal_class (recommended display class, 1–21), Modal_prop (dominant class proportion), Composite (source composite image number).
  - The 25 m raster includes band 1 (dominant class per polygon) and band 2 (mean probability).
- Coverage and resolution
  - GB vector: 6.7 million polygons; NI vector: 0.9 million polygons.
  - GB 25 m raster; GB 1 km products; NI 25 m raster; NI 1 km products.
- Projections and extents
  - Great Britain: British National Grid (OSGB36).
  - Northern Ireland: TM75 Irish Grid.
  - Separate GB and NI datasets; coordinate extents follow their respective projections.

## Data Quality, Uncertainty, and Limitations

- Uncertainty information
  - Random Forest classifier provides per-pixel probability estimates, summarized as mean polygon probability (vector) and as band 2 in the 25 m raster.
- Minimum mapping unit
  - 0.5 ha minimum; parcels smaller than 0.5 ha or linear features under 20 m are dissolved into surrounding areas.
- Change mapping cautions
  - The document notes that LCM2015 is not recommended for change mapping in its current state; differences between LCM products over time reflect real change plus classification errors and methodological changes.
- Methodological shifts affecting outputs
  - Montane and Rough Grassland classes removed in LCM2015 to improve suitability for change detection and consistency with current methods.
  - 25 m raster expanded to two bands; spectral sub-classes removed (Random Forest handles multi-modal data; no need for sub-classes).
  - Spatial framework no longer uses segmentation; training areas built from a stable set (2000/2007) plus coastal and difficult classes; ancillary data integrated into input data rather than post-classification edits.
- Output interpretation
  - 1 km percentage totals may not sum exactly to 100 due to rounding; coastal areas may sum to less than 100 because water is not fully represented in land-only grids.

## Methodology Highlights

- Classification approach
  - Random Forest classifier (instead of previous Maximum Likelihood), enabling multi-modal training data and removing the need for spectral sub-classes.
- Training data and ancillary data
  - Initial training areas derived from areas consistently classified across 2000 and 2007, supplemented for coastal areas and challenging classes.
  - Ancillary data (e.g., altitude, soil data, slope) are included as input features, enabling data-driven, objective knowledge-based enhancements within the classifier.
- Data lineage
  - The vector product is the core dataset from which 25 m rasters are derived; 1 km products are aggregates derived from 25 m results.
- Output limitations
  - The Montane, Rough Grassland, and segmentation-related aspects of earlier LCMs are not present in LCM2015, to support stable change mapping and per-pixel classification.

## Data Structure and Class Mapping

- 21 LCM2015 target classes
  - Mapped to Broad Habitat definitions (e.g., Broadleaved Woodland, Coniferous Woodland, Arable, Various Grasslands, Wetlands, Urban/Suburban, Littoral and Inland coastal habitats, etc.).
  - Some target classes are further split or redefined for reporting and display (e.g., Urban vs Suburban; Heather vs Heather grassland; Littoral categories).
- Metadata richness
  - Each polygon contains detailed metadata about the dominant class, pixel composition, and uncertainty, enabling in-depth provenance and quality assessment.

## Access, Citation, and Licensing

- Access
  - 1 km raster products are publicly available via the CEH Environmental Information Platform (EIP).
  - Full vector and 25 m raster products are available under licence on request from CEH; licensing fees may apply.
  - Contact: spatialdata@ceh.ac.uk; online application through CEH information products.
- Citations and DOIs
  - Each product (GB vector, GB 25 m raster, GB 1 km target/dominant and aggregates, NI vector, NI 25 m raster, NI 1 km targets/aggregates) has a DOI for proper citation.
  - Data papers and metadata are maintained to support repeatability and scholarly use.
- Documentation and further information
  - Additional information available on CEH LCM2015 pages and the CEH data access portal.
  - The dataset is designed for broad use with accompanying documentation and appendices (class definitions, color mapping, and composites).

## Key Practical Takeaways for Data Leaders

- LCM2015 provides a comprehensive, multi-resolution, metadata-rich land cover dataset for the UK, suitable for broad-scale analysis, modelling, and integration with other data sources.
- The move to Random Forest and the inclusion of ancillary data enhance robustness and reduce reliance on spectral sub-classes, supporting more scalable and repeatable analyses across time.
- For governance and strategic data planning, LCM2015 offers clear lineage, uncertainty metrics, and DOIs to support citation, auditing, and reproducibility.
- Users should be aware of the current limitations for change detection in LCM2015 and rely on the documented guidance when designing longitudinal data analyses or policy evaluations.