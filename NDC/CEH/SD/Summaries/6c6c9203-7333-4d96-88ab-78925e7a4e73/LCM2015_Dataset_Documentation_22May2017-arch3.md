# Dataset documentation

- LCM2015 is a parcel-based land cover map for the UK, classified into 21 Broad Habitats and mapped primarily from Landsat-8 (30 m) with AWIFS (60 m) data using two-date composites.
- Purpose and scope: supports diverse monitoring needs, with a stable, repeatable framework designed for evaluating policy and informing future decisions.
- Output and data governance: includes rich metadata, per-polygon uncertainty, and a data governance approach to sharing underlying data where possible.

## Key data products and structure

- Core data sets
  - Vector data set: polygons with attached attributes (gid, dominant class, pixel counts per class, uncertainty, etc.). GB: ~6.7 million polygons; NI: ~0.9 million.
  - 25 m raster: two-band product (band 1 = dominant class, band 2 = mean per-polygon probability).
  - 1 km raster products: dominant class and percentage cover for both 21 target classes and 10 aggregate classes.
- Class structure
  - 21 LCM2015 target classes based on UK Biodiversity Action Plan Broad Habitats.
  - 10 aggregate classes used for 1 km rasters.
- Detail and provenance
  - Each parcel (polygon) has a unique geometry id (gid) and a rich set of attributes plus a breakdown of pixel counts per class (Pix_dist) and a mean polygon probability (unc, mean probability).
  - Data include per-polygon uncertainty measures and per-class probability information (where applicable).
- Spatial resolution and extent
  - Vector and 25 m data cover GB and NI with separate coordinate systems: GB (British National Grid), NI (Irish Grid).
  - 1 km products provide UK-wide aggregated or dominant-cover summaries.
- Data formats and access
  - 1 km raster data are available via the CEH Environmental Information Platform (EIP).
  - Full vector and 25 m products are available under licence on request from CEH.
  - DOIs exist for each product to facilitate citation and reproducibility.

## Differences from LCM2007 and methodological changes

- Output data changes
  - Montane class removed; upland areas reclassified using spectral data as Inland Rock or other upland habitats.
  - Rough grassland class removed; grassland types re-aligned with JNCC Broad Habitat types and no soil data used in LCM2015.
  - 25 m raster now a two-band image (classification band + band with mean probability); probability data simplified for vector data.
  - No spectral sub-classes used; Random Forest classifier eliminates need for sub-class grouping.
  - Spatial framework no longer uses segmentation; per-pixel classification with a simplified, repeatable spatial framework.
  - Mixed woodland labeled according to dominant spectral signatures rather than purely object-based training.
- Methodology changes
  - Classification algorithm: Random Forest (versus Maximum Likelihood previously).
  - Training data: initial stable training areas (areas classified the same in 2000 and 2007) supplemented with coastal areas and historically challenging classes.
  - Ancillary data (altitude, soil, etc.) are integrated as input data rather than applied post-classification, promoting objective, data-driven enhancements.

## Data quality, metadata, and uncertainty

- Metadata and uncertainty
  - LCM2015 provides rich polygon metadata, including dominant class, Pix_dist (per-class pixel counts), npix, modal_class, and mean polygon probability (unc).
  - Uncertainty is quantified as per-polygon probability (vector) and per-polygon mean probability (band 2 for the 25 m raster).
- Data integrity and mapping considerations
  - LCM2015 is designed for per-pixel land cover mapping and supports subsequent aggregation to 1 km with some rounding; sums may not always equal 100% due to rounding and edge effects, especially near coasts.
  - The dataset is intended for monitoring contexts; caution is advised for using LCM2015 directly for change mapping without considering methodological differences and the non-trivial separation between real change and classification error.

## Data access, citations, and provenance

- Access and licensing
  - 1 km raster products accessible via CEH EIP.
  - Full vector and 25 m raster products available under licence on request from CEH (licensing fees may apply).
  - Contact: spatialdata@ceh.ac.uk; additional information at CEH portals.
- Citation and DOIs
  - All LCM2015 products have DOIs to support reproducibility and proper citation.
  - Examples include separate DOIs for GB vector, GB 25 m raster, GB 1 km percentage and dominant classes (and their aggregates), and NI counterparts.
  - When citing, include author list, year, and DOI in references and in-text citations (e.g., Land Cover Map 2015 (vector, GB), DOI ...).

## Practical guidance for monitoring framework authors

- Use cases and cautions
  - LCM2015 provides consistent, repeatable land cover classifications suitable for monitoring policy impacts and informing future decisions, provided users familiarise themselves with the documentation and limitations.
  - Not recommended for direct change mapping in its current state due to differences in methodological consistency over time and between versions; interpret changes with caution and consult the differences and metadata.
- Data governance and reuse
  - Rich metadata and uncertainty information support transparent data governance, quality assurance, and evidence-based decision-making.
  - Data provenance (DOIs, versioning) facilitates reproducibility and audit trails in monitoring frameworks.
- Class definitions and mapping nuances
  - The mapping relies on JNCC Broad Habitat definitions; users should refer to Appendices for class definitions and mappings to Broad Habitats, and consider potential ambiguities in classes like mixed woodland, fen, bog, and upland habitats when integrating with other datasets.
- Access pathways and collaboration
  - Plan for licensing arrangements for the full vector and 25 m raster products; leverage the 1 km raster products for broad UK-scale analyses and modelling in conjunction with other data layers (e.g., meteorology, species distributions).