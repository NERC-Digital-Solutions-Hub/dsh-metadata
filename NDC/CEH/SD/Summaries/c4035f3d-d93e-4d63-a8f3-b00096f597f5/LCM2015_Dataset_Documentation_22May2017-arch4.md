# Dataset documentation

- LCM2015 (Land Cover Map 2015) is a UK-wide, parcel-based land cover map produced from satellite imagery (primarily Landsat-8 at 30m, augmented with AWIFS at 60m) classified into 21 Broad Habitat-based classes.
- Purpose: provide a range of data products to support diverse user needs, with emphasis on per-polygon (vector) representations that align with real-world boundaries and support change mapping and integration with other spatial data.

## Key data products and structure

- Core products
  - Vector data: 6.7 million GB polygons and 0.9 million NI polygons, each with a rich attribute set.
  - 25m raster: two-band product (band 1 = dominant class per polygon; band 2 = mean per-polygon classifier probability).
  - 1km raster: aggregate products derived from 25m data, including dominant class and percentage cover for both 21 target classes and 10 aggregate classes.
- Attributes and metadata
  - Vector attributes include gid (unique parcel ID), dominant class (Modal_class), pixel counts per class (Pix_dist), uncertainty measures (unc, unc_stdev), and composite source image indicator.
  - Per-polygon uncertainty and per-pixel probability (from Random Forest) are provided.
  - Gid enables unambiguous communication between users; polygon-level metadata includes dominant class breakdown and mean probability.
- Spatial details
  - GB data in British National Grid; NI data in Irish National Grid.
  - Minimum mappable area: >0.5 ha; polygons smaller than this are dissolved into surrounding landscape.
  - Data formats span vector, 25m raster, and 1km raster products, with GB and NI distributed separately.

## Methodology and methodological changes since LCM2007

- Classification and algorithm
  - New Random Forest classifier replaces the previous Maximum Likelihood approach, improving handling of multi-modal training data and often performance.
  - Ancillary data (e.g., slope, distance to water) are integrated as inputs rather than applied post-classification, making knowledge-based enhancements objective and part of the classification process.
- Training data and spatial framework
  - Stable training areas derived from areas consistently classified across prior maps; coastal areas added to augment training.
  - No segmentation-based spatial framework in LCM2015; per-pixel classification with polygons reflecting real-world boundaries.
- Output and class specifics
  - Montane class removed; Inland Rock and other upland habitats used instead (Montane distribution available from LCM2007 if required).
  - Rough grassland removed; grassland types re-aligned with JNCC Broad Habitat definitions (no soil data used in LCM2015).
  - Mixed woodland training uses pure stands and per-pixel classification, with polygon labels determined by the modal_class; pix_dist allows exploration of potential misclassifications.
  - 25m raster now two-band; spectral sub-classes no longer used due to Random Forest flexibility.
- Dataset scope
  - LCM2015 maps land cover (not land use); notes that mapping is spectral rather than strictly biotically defined land use.
  - Stable, archived dataset with DOIs for all products.

## Data content and class structure

- 21 LCM2015 target classes, mapped from 21 Broad Habitats (with some subdivisions for practical use, e.g., Urban vs Suburban, Heather vs Heather grassland, Littoral subdivisions).
- Aggregation and compatibility
  - 1km rasters provide aggregate percentage covers for 21 target classes and 10 aggregate classes to support broad-scale analyses.
  - Table 1 (not reproduced here) outlines the mapping between LCM2015 target classes and aggregate classes used in raster outputs.
- Unique labeling and mapping
  - Each parcel has a unique gid; a detailed colour-mapping appendix exists to facilitate visualization.
  - The dataset provides an extensive Appendix with Broad Habitat definitions and mapping notes to help interpretation and alignment with field classifications.

## Data quality, uncertainty, and caveats

- Uncertainty and accuracy
  - Random Forest yields per-pixel probability; polygon-level mean probability is provided for vector data and used in the 25m raster band 2.
  - Users should treat change mapping with caution; differences between years reflect a mix of real change and classification shifts.
- Comparability and limitations
  - Differences from prior LCM products mean scripts and workflows designed for LCM2007 should be reviewed before use with LCM2015 outputs.
  - Some habitat distinctions (e.g., Montane, Rough grassland) were revised to improve change detection and align with spectral data; land cover estimates in certain categories may differ from older maps.
- Spatial considerations
  - 0.5 ha minimum mapping unit means smaller features are generalized or dissolved; per-pixel and per-polygon attributes provide detailed information for scale-up analyses.
- Documentation and citations
  - The dataset is documented with detailed appendices, including class definitions (Appendix 1), breadth of habitat definitions (Appendix 2), color mappings (Appendix 3), and composite image usage (Appendix 4).

## Data access, licensing, and citation

- Access
  - 1km raster products available via CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector and 25m raster products available on request under licence; licensing fees may apply.
- DOIs and citation
  - Each LCM2015 product has a DOI for GB vector, GB 25m raster, GB 1km target and aggregate classes, and NI equivalents.
  - When citing, include author list, year, and full DOI; see provided examples for preferred citation format.
- Projections and data packages
  - GB data in British National Grid; NI data in TM75 Irish Grid.
  - Data are distributed as vector (core product), 25m raster (derived from vector), and 1km rasters (percentage and dominant cover products).

## Practical notes for data leaders

- Governance and strategy alignment
  - LCM2015 offers a stable, richly described land cover dataset suitable for monitoring change, informing policy support, and integration with partner datasets.
  - The incorporation of ancillary data into the classification process supports objective governance and reduces reliance on post-classification rule sets.
- Data stewardship
  - Maintain gid and associated metadata to ensure traceability and reproducibility across projects and partner workflows.
  - Use the 1km percentage and dominant cover products for broad-scale analyses, while leveraging the 25m and vector details for finer-scale work or targeted policy questions.
- Community and standards
  - Adhere to the DOIs for data citation to support reproducibility and impact tracking.
  - Be mindful of differences from LCM2007 when migrating workflows; reassess scripts and change-mapping procedures accordingly.

Further information
- CEH pages: general LCM2015 information and data access details
- Contact: spatialdata@ceh.ac.uk
- See also related literature cited in the document for background on Broad Habitat definitions and previous LCM versions.