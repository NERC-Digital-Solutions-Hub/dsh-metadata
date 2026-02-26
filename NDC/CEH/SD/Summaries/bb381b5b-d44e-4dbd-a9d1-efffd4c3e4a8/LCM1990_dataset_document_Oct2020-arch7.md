# Dataset documentation

- Version 1.1, 8/10/2020 (data paper updates: DOIs updated in Tables 5 & 6). LCM1990 is a complex dataset; familiarize yourself with this document to use it correctly.

## Overview and purpose
- Land Cover Map 1990 (LCM1990): UK parcel-based land cover map created by classifying two-date Landsat-5 composites (30 m resolution) into 21 classes.
- Classes based on UK Biodiversity Action Plan Broad Habitat definitions; designed to be compatible with LCM2007/LCM2015 frameworks.
- Provides products for diverse GIS applications and enables long-term land cover change analyses (with a 25-year change product context).

## Data model and classes
- 21 land cover classes (Table 2); some Broad Habitat classes subdivided (e.g., Built-up Areas and Gardens into Suburban/Urban; Dwarf Shrub Heath into Heather/Heather grassland; Littoral Sediment into Saltmarsh and Littoral sediment).
- Each vector parcel (polygon) has rich metadata and a unique geometry identifier (gid); recommended to retain gid for unambiguous communication.
- Per-polygon attributes include dominant class, pixel breakdown by class, and classification uncertainty.

## Spatial framework and comparability
- Built on the LCM2007 spatial framework to maximise compatibility with LCM2015.
- Provides a direct basis for a 25-year land cover change product (1990–2015) and facilitates cross-version comparisons.

## Data products and formats
- Vector data set
  - Polygons with attributes; GB: ~6.7 million polygons; NI: ~0.9 million polygons.
  - Eight key attributes (including gid, hist, mode, purity, conf, stdev, n, cmp) described in Table 3.
- Raster data sets
  - 25 m raster: 3-band GeoTIFF (band 1 = dominant class per polygon, band 2 = mean per-polygon confidence, band 3 = percentage of polygon area covered by the modal class).
  - 1 km rasters: dominant cover (1 band) and percentage cover (21 bands for target classes, 10 bands for aggregate classes).
  - GB and NI rasters provided separately with corresponding coordinate systems (GB: British National Grid; NI: TM75 Irish Grid).
  - MMU: minimum mappable area > 0.5 ha; polygons smaller than 0.5 ha and linear features < 20 m dissolved into surrounding landscape.
  - Edge cases near coast reflect aggregation and rounding (percentage sums may not equal exactly 100%).

## Data access and citation
- Access: CEH Environmental Information Platform (eip.ceh.ac.uk). Full vector product on request; licences may apply for some uses.
- Each product has a DOI for citation (Table 5 for GB, Table 6 for NI; DOIs provided for vector, 25 m raster, 1 km products, and aggregated/dominant classes).
- Example citation format includes author(s) and year, with full DOI in references; see provided examples in the document.

## Spatial references and projection
- Great Britain: British National Grid (EPSG 27700).
- Northern Ireland: Irish Grid (TM75; EPSG 29903).
- Vector and raster products are organized to support GB and NI projections separately.

## Quality Assurance
- QA involves checks for correct projections, spatial completeness, modal class presence in polygons (vector), heading consistency, value ranges (0–100 for rasters), and pixel size accuracy.
- Methodology follows the 2007 LCM framework; validation against external datasets (e.g., Countryside Survey) has been conducted; full validation results planned for publication.

## Provenance, processing, and references
- Derived from 2007 Ordnance Survey MasterMap-based parcel framework; field boundary changes are infrequent.
- Random Forest classifier used; pixel-level uncertainties captured as per-polygon statistics.
- Appendix materials provide detailed class notes, broad habitat definitions, color mappings, and composite image information to support interpretation and visualization.

## Usage notes and caveats
- LCM1990 maps land cover, not strictly land use; some classes (e.g., Neutral/Calcareous Grassland) may be spectrally mapped with ambiguity requiring ancillary data or field validation.
- Some broad habitat separations are challenging (e.g., bog vs. dwarf shrub heath); users should review Appendix 1 (class notes) and Appendix 2 (BAP Broad Habitats) for interpretation guidance.
- The 1 km products are best for regional modelling with other datasets (e.g., meteorological, species distribution); coastal and edge cases require careful handling due to rounding and coastal extent.

## Appendix highlights (quick reference)
- Appendix 1: Notes on how LCM1990 maps Broad Habitats and specific class caveats.
- Appendix 2: Summary of JNCC/BAP Broad Habitats definitions to aid interpretation.
- Appendix 3: Standard LCM color mapping recipe for visualization.
- Appendix 4: Composite images metadata used in LCM1990 production.

## Citing and references
- DOIs provided for all LCM1990 products (GB and NI) to support repeatable methods and usage tracking.
- Documentation and data access information available at the CEH eIP site; queries to spatialdata@ceh.ac.uk. A journal paper is in preparation with additional details.