# Land Cover Map 1990 (LCM1990)

- A UK parcel-based land cover map classifying Landsat-5 two-date composites at 30 m resolution into 21 Broad Habitat-based classes (aligned with UK Biodiversity Action Plan definitions).
- Built to support diverse LCM user needs with a focus on consistent, comparable outputs over time and compatibility with later LCM products (LCM2007, LCM2015) to enable long-term change assessments.

## Data and Methods

- Data source and approach:
  - Satellite imagery: Landsat-5 two-date composite imagery, 30 m resolution.
  - Classification: Object-based, polygon-wide assignment using a Random Forest classifier; probabilities provided per polygon.
  - Spatial framework: Uses LCM2007 framework aligned with OS MasterMap-based boundaries for GB and Northern Ireland topographic layers; designed to be directly comparable with subsequent LCM products.
- Class system and mapping:
  - 21 LCM1990 target classes (based on JNCC Broad Habitat definitions), with some subclass splits (e.g., Built-up Areas into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Saltmarsh and Littoral sediment).
  - Unique object labelling via a geometry id (gid) for unambiguous communication between users.
- Data quality and metadata:
  - Rich per-polygon metadata: dominant class, pixel composition, mean classification probability, and uncertainty (per-polygon mean vote from Random Forest).
  - Minimum mappable area: >0.5 ha; polygons <0.5 ha or linear features <20 m dissolved into surrounding landscape.
  - QA checks cover projections, spatial completeness, modal class presence, value ranges, and pixel size; validation against external datasets (e.g., Countryside Survey) is reported in a separate publication.
- Data scope and structure:
  - Vector product: ~6.7 million GB polygons and ~0.9 million NI polygons.
  - Raster products: derived 25 m raster (core) and 1 km percentage/dominant cover products.
  - 25 m raster bands: band 1 = dominant LCM1990 class; band 2 = per-polygon RF confidence; band 3 = percentage of polygon covered by dominant class.
  - 1 km products: dominant cover (target and aggregate classes) and percentage cover (target and aggregate classes) across each 1 km cell.

## Data Products and Access

- Core data formats:
  - Vector: Detailed polygon data with extensive attached metadata.
  - 25 m raster: Three-band raster (dominant class, confidence, percent cover).
  - 1 km rasters: Dominant cover maps and percentage cover layers for both 21 target and 10 aggregate classes.
- Geographic coverage and projections:
  - Great Britain: British National Grid.
  - Northern Ireland: Irish Grid (TM75).
- Access and licensing:
  - 25 m and 1 km rasters available via the CEH Environmental Information Platform.
  - Full vector product available on request from CEH; license fees may apply for some users/applications.
  - DOIs exist for all products to enable precise citation (GB vector, GB 25 m raster, GB 1 km targets, GB 1 km aggregates, NI vector, NI 25 m raster, NI 1 km targets/aggregates), with some DOIs listed as pending.
- Citation and reuse:
  - All products have DOIs; please cite with author/year and DOI in references (e.g., Rowland et al., 2020) to support methods, repeatability, and usage tracking.
- Documentation and access points:
  - More information and data access at CEH’s LCM1990 pages and eIP portal; contact spatialdata@ceh.ac.uk for details.

## Class System and Interpretation

- 21 LCM1990 classes mapped to UK Broad Habitats (per Jackson, 2000), with cross-walks to the Appendix classifications.
- Important distinctions:
  - LCM1990 maps land cover rather than strictly land use; spectral similarity can blur lines between some land uses (e.g., grassland used for recreation vs. grazing).
  - The vector dataset provides per-polygon breakdowns of all detected classes and the dominant class, enabling nuanced analyses beyond the single dominant label.
- Colour mapping and legend:
  - Standardized colour mapping (Appendix 3) for consistent visualization across products.

## Use in Monitoring and Analysis

- Temporal comparability:
  - Built to maximize compatibility with LCM2015 and LCM2007, enabling long-term land cover change analyses (targeting a 25-year change product).
- Data richness for analysis:
  - Per-polygon class composition and confidence enable uncertainty-aware analyses.
  - Availability of both detailed vector with metadata and lighter 25 m raster products supports a range of modeling and mapping needs.
- Data governance and reuse:
  - DOIs facilitate reproducible research and data provenance.
  - Data is ultimately suitable for environmental health monitoring, policy performance assessment, and cross-dataset data fusion, in line with the Analytic aim to demonstrate environmental condition in a standard, scrutiny-friendly format.

## Additional Information

- GIS and methodological notes:
  - LCM1990 is based on a 2007- era framework refined to maximize compatibility with later LCM products.
  - Areas identified as Neutral/Calcareous/Nor Acid Grassland can be spectrally confounded; users may aggregate grassland types as needed.
- Appendices and context:
  - Appendix 2 provides the biodiversity-units-based Broad Habitat definitions (for deeper interpretation of class labels).
  - Appendix 4 details composite imagery used for classification.

- Contact and acknowledgments:
  - CEH and NERC funding support; data access and citation guidelines available via CEH platforms.