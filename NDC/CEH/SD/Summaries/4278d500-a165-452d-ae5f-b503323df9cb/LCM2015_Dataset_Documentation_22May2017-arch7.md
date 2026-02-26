# Dataset documentation

- LCM2015 is a parcel-based land cover map for the UK, created by classifying Landsat-8 (30 m) and AWIFS (60 m) data into 21 land cover classes, aligned with UK Biodiversity Action Plan Broad Habitat definitions. It uses two-date composite imagery and updates the LCM framework from 2007, reflecting a per-pixel approach with polygon summarisation.
- The dataset includes multiple data products and formats to serve a wide range of GIS applications.

## Data products and formats

- Core vector data set
  - ~6.7 million polygons for Great Britain; ~0.9 million for Northern Ireland
  - Each polygon has attributes including land cover class (text and integer), source image, per-polygon uncertainty, pixel counts per class, and dominant class proportion
  - Unique geometry identifier (gid) for each parcel
- 25 m raster
  - 2-band raster: band 1 = dominant LCM2015 class per polygon; band 2 = mean per-polygon RF probability
- 1 km raster products
  - Dominant class per 1 km pixel (for both 21 classes and aggregated 10 classes)
  - Percentage cover per class per 1 km pixel (21 bands for GB; 10 bands for aggregates)
- Data scope
  - Separate datasets for Great Britain and Northern Ireland with appropriate projections
  - LCM2015 is a stable, archived dataset with DOIs for each product

## Classification methodology

- Random Forest classifier used for per-pixel classification
  - Handles multi-modal training data; simplifies training data by removing spectral sub-classes
  - Ancillary data (e.g., altitude, soil, slope) used as input variables, integrated into the classification process
- Training data and stability
  - Initial training areas based on areas classified the same in 2000 and 2007
  - Supplemented with coastal areas and classes traditionally poorly mapped
- Post-classification processing
  - Ancillary data are part of the input; knowledge-based enhancements are not applied post-classification
- Output and summarisation
  - Per-pixel classifications are summarised to polygons for the vector product
  - Per-polygon mean probability is provided as uncertainty information
- Spatial framework
  - No segmentation in the 2015 spatial framework to improve consistency for change mapping

## Data structure and attributes

- Vector data attributes (Table 2)
  - gid: Unique parcel identifier
  - BHAB: Dominant land cover at Broad Habitat level (e.g., Improved Grassland)
  - Pix_dist: List of 23 numbers: pixels per class (21 classes), followed by npix (polygon size) and modal_class (dominant class)
  - unc: Uncertainty - mean per-polygon probability (0–255 scale)
  - Unc_stdev: Standard deviation of uncertainty
  - npix: Number of pixels in polygon
  - Modal_class: Integer code for the dominant LCM2015 class (1–21)
  - Modal_prop: Proportion of polygon classified as the dominant class
  - Composite: Identifier for the composite image used to derive the classification (99 = infill from LCM2007)
- Raster data
  - 25 m raster: band 1 = dominant class; band 2 = mean per-polygon RF probability
  - 1 km rasters: dominant class (1 band) and percentage cover (21 bands for classes; 10 bands for aggregates)
  - GB and NI rasters are provided separately with appropriate projections
- Spatial resolution and extent
  - Minimum mappable area: >0.5 ha
  - Small parcels (<0.5 ha) and very short linear features (<20 m) dissolved into surrounding landscape
- Projections
  - GB data: British National Grid
  - NI data: TM75 Irish Grid

## Land cover classes and aggregation

- LCM2015 maps 21 target Broad Habitat classes (based on Jackson et al., 2000)
- Some classes are subdivided for certain products
  - Built-up Areas and Gardens: Suburban and Urban
  - Dwarf Shrub Heath: Heather and Heather grassland
  - Littoral Sediment: Saltmarsh and Littoral sediment
- 1 km products include aggregated classes (10 aggregate classes) for broader analyses
- Labelling and colour mapping are provided; standard color mapping recipes are in Appendix 3

## Differences from LCM2007 and methodological notes

- Output data differences
  - Montane class removed (reclassified as Inland Rock or upland habitats); Montane distribution available only via LCM2007
  - Rough grassland class removed to align with JNCC Broad Habitat types
  - 25 m raster now two-band (classification and mean probability)
  - Probability information reorganised: mean polygon probability for vector; mean probability in band 2 of 25 m raster; not provided for 1 km products
  - No spectral sub-classes; segmentation removed from spatial framework
  - Mixed woodland classification updated: training uses pure stands; modal_class used for polygon labelling
- Methodology differences
  - Switch from Maximum Likelihood to Random Forest
  - Stable training areas used as a base, with additional coastal and poorly mapped classes
  - Ancillary data incorporated into input rather than post-classification edits
- Interpretation
  - LCM2015 maps land cover, not land use
  - DOIs are provided for all products; data are archived and citable

## Metadata, uncertainty, and data quality

- Rich metadata at polygon level
  - Includes dominant class, per-class pixel counts, and mean probability
  - Uncertainty and its standard deviation accompany each polygon
- Per-polygon dataset provides a transparent view of classification confidence
- Per-pixel and per-polygon uncertainty information are available in corresponding products

## Data access, licensing, and citation

- Access
  - 1 km raster products: CEH Environmental Information Platform (EIP)
  - Full vector product and 25 m raster product: available on request under licence from CEH
- Licensing may apply; contact CEH for permission details
- DOIs and citation
  - Each LCM2015 product has its own DOI (GB vector, GB 25 m, GB 1 km percentage and dominant classes, GB 1 km aggregate classes; NI equivalents)
  - Citing guidance provided in the dataset documentation
- Projections and coordinates
  - Great Britain: British National Grid (OSGB)
  - Northern Ireland: TM75 Irish Grid
- References and further information
  - CEH Land Cover Map 2015 pages and EIDC citing data guidance
  - Appendix references for class definitions and color mappings

## Cautions for users

- The LCM2015 series is complex; use documented guidance to avoid inappropriate change-mapping conclusions
- Differences between LCM products reflect both real changes and classification/methodological changes; careful interpretation is required for change analysis
- For detailed analysis, retain gid and Pix_dist attributes to understand polygon-level composition and uncertainty

## Appendices and supplementary information

- Appendix 1 and Appendix 2: Descriptions of Broad Habitat class definitions and mapping notes
- Appendix 3: Standard LCM2015 colour mapping by class
- Appendix 4: Composite image metadata used in LCM2015 production

## Contacts and further information

- CEH contact: spatialdata@ceh.ac.uk; www.ceh.ac.uk
- LCM2015 project pages and data access portals as listed in the document
- Data paper and DOI references provided for all products