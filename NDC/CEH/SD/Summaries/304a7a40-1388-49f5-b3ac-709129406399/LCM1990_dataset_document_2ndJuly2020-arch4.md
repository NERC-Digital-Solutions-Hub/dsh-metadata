# Dataset documentation

## Overview
- Land Cover Map 1990 (LCM1990) is a UK parcel-based land cover map created by classifying Landsat-5 satellite data into 21 land cover classes, aligned with UK Biodiversity Action Plan Broad Habitat definitions.
- Data are provided as a range of products: vector parcels and corresponding raster representations (25 m, plus 1 km aggregates) to support diverse usage.
- Built to be compatible with LCM2015 (and by extension LCM2007) methods to enable cross-temporal analysis (e.g., a 25-year change product).

## Data products and structure
- Core vector dataset: polygons with attached attributes, intended as the primary product; 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland.
- Raster products: 25 m raster derived from the vector, plus 1 km dominant and percentage cover products for both target (21) and aggregate (10) classes.
- Class and metadata: 21 target LCM1990 classes mapped from Broad Habitats; some classes are further subdivided (e.g., Urban vs Suburban; Heather vs Heather grassland; Littoral Sediment vs Saltmarsh).
- Key attributes (vector): gid (unique parcel ID), _hist (class composition within polygon), _mode (dominant class), _purity, _conf (classifier confidence), _stdev (uncertainty), _n (pixel count), cmp (composite image source).

## Classification framework and class structure
- 21 LCM1990 target classes derived from UK Broad Habitats; mapping notes and definitions provided (Appendices 1–3).
- Some classes are spectrally separable and thus subdivided (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland).
- Raster products include both target classes (21 bands) and aggregate classes (10 bands) for 1 km grids.

## Spatial framework, resolution, and extents
- Vector and raster data are produced for Great Britain (GB) and Northern Ireland (NI) using separate coordinate systems: GB is British National Grid (EPSG 27700); NI is Irish Grid (EPSG 29903).
- Minimum mappable area is >0.5 ha; polygons smaller than 0.5 ha and linear features under 20 m are dissolved into surrounding landscape during production.
- Raster structure: 25 m bands (three-band GeoTIFFs) and 1 km aggregated products; 1 km products summarize 25 m data to percent cover and dominant class per square kilometer.

## Metadata and uncertainty
- Rich metadata per polygon, including dominant class, per-polygon pixel breakdown, and mean probability from the Random Forest classifier.
- Uncertainty is captured as classifier confidence and per-polygon statistics; the 25 m raster includes mean confidence and modal coverage percentage.
- Each data product has documented metadata standards and a formal DOI for citation.

## Data access, licensing, and citation
- Access via the CEH Environmental Information Platform (eip.ceh.ac.uk) for the 25 m and 1 km rasters; full vector product available on request with potential licensing fees.
- All LCM1990 products have DOIs; GB vector and GB 25 m raster DOIs are provided; several 1 km products have DOIs or pending DOIs; NI products have DOIs as well.
- Data citation example: include author(s), year, and DOI in references; adopt journal-style citation for reproducibility.

## map projection, data management, and quality assurance
- Projections: GB data in British National Grid; NI data in Irish National Grid; coordinate details provided in metadata.
- Data management guidance includes retaining the gid and using the detailed metadata for communication and reproducibility.
- Quality assurance includes a suite of checks for projection correctness, spatial completeness, modal class presence in polygons, value ranges (0–100 for raster percent), and pixel size validation; a full validation against independent datasets is documented and forthcoming.

## Practical considerations for Data Leaders
- LCM1990 is designed for cross-era compatibility with LCM2015, enabling long-term change analysis and integration with other CEH datasets.
- The vector format provides rich attribute data and per-polygon uncertainty, but larger file sizes may complicate processing; the 25 m raster offers a lighter-weight option with slightly reduced metadata.
- Data discovery and access may require contacting CEH and adhering to potential licensing; DOIs should be used to cite and track data usage.
- Important operational practices: keep gid intact for unambiguous communication; utilize both 25 m and 1 km products for scale-appropriate analyses; reference the Broad Habitat framework and Appendix documentation for class interpretations.