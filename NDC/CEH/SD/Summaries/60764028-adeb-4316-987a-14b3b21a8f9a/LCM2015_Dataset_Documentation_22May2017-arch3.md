# Land Cover Map 2015 (LCM2015)

## Overview
- UK parcel-based land cover map created from satellite imagery classified into 21 Broad Habitat classes (based on JNCC/Biodiversity Action Plan definitions).
- Supports monitoring needs for environmental health policy evaluation and informing future decisions.
- Data products cover Great Britain and Northern Ireland, with per-pixel classification primarily from Landsat-8 (30 m) and AWIFS (60 m).

## Data Products and Structure
- Vector data set
  - ~6.7 million polygons (GB) and ~0.9 million (NI).
  - Attributes include: gid (unique parcel ID), BHAB (dominant Broad Habitat), Pix_dist (distribution of all 21 classes within polygon), uncertainty measures, npix (pixels per polygon), Modal_class (recommended display class), Modal_prop (dominant class share), Composite (composite image source).
- 25 m raster
  - 2-band: band 1 = dominant LCM2015 class per polygon; band 2 = mean per-polygon probability from Random Forest classifier.
- 1 km raster
  - Dominant cover per 1 km cell (21 target classes and 10 aggregate classes).
  - Percentage cover per class (21 bands for GB NI separately; aggregate classes also available).
- Metadata and uncertainty
  - Rich metadata at polygon level; per-polygon probability (uncertainty) from Random Forest; per-polygon class breakdown (Pix_dist).
- Access and citations
  - DOIs exist for all products; vector and raster data available via CEH platforms; licensing may apply for some products.

## Methodology
- Classification approach
  - Random Forest classifier using satellite and ancillary data integrated as input.
  - Training areas built from a stable set identified in previous maps (LCM2000 and LCM2007) and extended for coastal areas and hard-to-map classes.
  - No spectral sub-classes; per-pixel classification summarized to polygon level.
- Ancillary data
  - Ancillary datasets (e.g., elevation, soils) used as inputs rather than post-classification rules, making enhancements objective.
- Spatial framework and changes from earlier maps
  - No segmentation-based polygons in LCM2015; per-pixel classification with per-polygon aggregation.
  - Changes aimed at improving change-mapping suitability and production speed.
  - Distinctions in output data versus prior series (e.g., no spectral sub-classes, different probability representation).

## Key Class and Product Details
- 21 LCM2015 target classes
  - Includes: Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Improved Grassland, Neutral Grassland, Calcareous Grassland, Acid Grassland, Bracken, Dwarf Shrub Heath (and Heather/Heather grassland), Fen/Marsh/Swamp, Bog, Standing Open Water, Rivers/Streams, Montane (now reclassified as Inland Rock or other upland habitats), Inland Rock, Built-Up Areas and Gardens (Urban and Suburban), Supra-littoral and Littoral zones, Saltmarsh, Littoral/Supra-littoral Sediments, etc.
  - Some Broad Habitats are subdivided (e.g., Built-up Areas into Urban vs Suburban; Dwarf Shrub Heath into Heather and Heather Grassland; Littoral Sediment into Saltmarsh and Littoral Sediment).
- Data products purpose
  - Vector and raster formats to support diverse monitoring applications, model inputs, and integration with other datasets (e.g., meteorology, species distribution).
- Notes on aggregation
  - 1 km products provide aggregated percentages and dominant classes, useful for national-scale modelling; coastlines may show under- or over-representation due to MMU and aggregation effects.

## Data Quality, Uncertainty, and Cautions
- LCM2015 is complex and not recommended for change mapping in its current state; differences between LCM products reflect both real change and classification/methodological changes.
- Differences from LCM2007/earlier maps may affect comparability; users should review Appendix 1/2 mappings and method notes.
- Some broad habitat classes can be spectrally similar and may require ancillary data or field validation for conclusive interpretation.
- Minimum mapping unit and dissolution
  - Parcels smaller than 0.5 ha and linear features under 20 m are dissolved into surrounding landscape during production.

## Metadata, Standards, and Data Governance
- Rich polygon-level metadata, including dominant class, pixel counts per class, and per-polygon mean probability.
- Uncertainty information provided via probabilistic outputs from the Random Forest classifier.
- Data is archived with DOIs to support reproducibility; per-product DOIs exist for GB and NI datasets.
- Data governance considerations are embedded in the methodology (integration of ancillary data as inputs; no post-classification knowledge-based rules in LCM2015).

## Projections, Coverage, and Data Access
- Projections
  - Great Britain: British National Grid (EPSG 27700)
  - Northern Ireland: Irish National Grid (TM75 Irish Grid, EPSG 29903)
- Access
  - 1 km raster data accessible via CEH Environmental Information Platform.
  - Full vector and 25 m raster products available on request under licence (may incur fees).
  - Contact or online application via CEH channels for licensing details.
- Citing the data
  - Each product has a DOI; citations should include authors and year, with full DOI in references.

## Practical Guidance for Monitoring Frameworks
- Use LCM2015 as a stable, archived land cover reference for UK-wide monitoring with rich attribute detail.
- Prefer 1 km products for national-scale modelling and cross-dataset integration; use 25 m raster for higher-resolution analysis when metadata is not required.
- Leverage the gid and Pix_dist attributes in the vector product to trace and communicate polygon-level composition and uncertainties.
- Consider consulting the Appendix materials for class definitions and color mappings to ensure consistent interpretation and visualization.
- Acknowledge methodological differences when comparing LCM2015 with earlier LCM datasets in policy evaluation and trend analyses.