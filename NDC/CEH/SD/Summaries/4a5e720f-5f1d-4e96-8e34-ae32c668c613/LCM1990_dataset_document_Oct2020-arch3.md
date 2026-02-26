# Dataset documentation

- Land Cover Map 1990 (LCM1990) provides a parcel-based land cover map for the UK, classified into 21 land cover classes based on UK Biodiversity Action Plan Broad Habitat definitions.
- Data products are designed to support diverse user requirements and enable cross-compatibility with other LCM editions (notably LCM2015) to enable long-term change analyses.

## Overview of aims and scope for monitoring framework readers

- Purpose: to document data products, processing methods, metadata, and access for monitoring environmental health and informing policy decisions.
- Emphasis on data provenance, quality assurance, openness, and clear communication of uncertainty to support governance and decision-making.

## Data products and structure

- Vector data set (core product) plus derived raster products:
  - 25m raster: three-band product (dominant class, mean per-polygon confidence, percentage area of modal class).
  - 1km raster: dominant cover (target and aggregate classes) and percentage cover (for 21 target classes and 10 aggregate classes).
- Spatial coverage and formats:
  - Great Britain and Northern Ireland provided separately with respective projections.
  - Vector products contain 6.7 million GB polygons and 0.9 million NI polygons.
  - Data distributed as uncompressed GeoTIFFs; licensing may apply for some users; vector full product available on request.
- Data lineage and compatibility:
  - Built to align with LCM2015 methods to enable a 25-year land cover change product (1990–2015) across the UK.

## Class structure and mapping

- 21 LCM1990 classes mapped from Landsat-5 imagery (30m resolution).
- Classes are based on Broad Habitats (JNCC Jackson 2000) with some subdivisions for spectral distinctiveness (e.g., Urban vs Suburban; Heather vs Heather grassland).
- LCM1990 maps land cover (not strictly land use); some land-use inferences may be uncertain from spectral data alone.
- Relationships to Broad Habitats provided (Appendix) to aid interpretation and cross-walking with biodiversity classifications.

## Metadata, uncertainty, and data quality

- Rich polygon metadata:
  - gid (unique parcel identifier), hist (composition of class pixels within a polygon), mode (dominant class), purity (percent of polygon covered by the dominant class), conf (mean per-polygon RF vote confidence 0–100), stdev, n (pixel count), cmp (composite image used).
- Uncertainty information:
  - Per-pixel probability from Random Forest classifier, summarized per polygon and in the 25m raster.
- Quality assurance:
  - Defined QA checks for projections, spatial completeness, modal class presence (vector), value ranges (0–100 for raster percent), and pixel sizes.
  - Validation against external datasets and a separate published accuracy assessment plan.

## Data access, citation, and governance

- Access:
  - 25m and 1km rasters via the CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector product available on request from CEH.
- Citations and DOIs:
  - Each LCM1990 product has an individual DOI for citation and reproducibility (GB and NI variants).
  - Guidance provided for citing DOIs in publications (author list, year, DOI).
- Projections:
  - Great Britain: British National Grid (EPSG: 27700).
  - Northern Ireland: Irish Grid (EPSG: 29903).

## Practical considerations for monitoring and governance

- Open data and data sharing:
  - Rich metadata and explicit data provenance support transparency, reproducibility, and governance; however, some data-sharing aspects may require careful data governance and licensing considerations.
- Data currency and maintenance:
  - LCM1990 is a stable, archived dataset with ongoing metadata availability; regular updates or cross-walking with newer products (LCM2015) enable long-term trend analyses.
- Documentation depth:
  - Includes extensive technical appendices (class definitions, color mapping recipes, and method notes) to facilitate correct interpretation and cross-analysis with biodiversity/broad habitat frameworks.

## Additional information and support

- Access to more information and data: CEH Environmental Information Platform (eip.ceh.ac.uk) and CEH spatialdata contact.
- Acknowledgement and funding: NERC award under UK-SCAPE for National Capability; forthcoming journal publication detailing validation and methodology.