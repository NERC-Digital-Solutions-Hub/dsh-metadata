# Dataset documentation

- LCM1990 is a parcel-based UK land cover map created from Landsat-5 data (30 m) and classified into 21 Broad Habitat-based classes. It is designed to be compatible with later LCM products (e.g., LCM2015) and supports 25 m and 1 km data products for diverse applications.
- The dataset is distributed as both vector and raster formats, with a stable, archived status and individual DOIs for citation.

## Data products and formats

- Vector data set
  - Approximately 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland.
  - Rich per-polygon metadata attached as attributes.
  - Key attributes: gid (unique parcel ID), hist (class composition per polygon), mode (dominant LCM1990 class), purity, conf (mean per-polygon classifier confidence, 0–100), stdev (uncertainty), n (number of pixels in the polygon), cmp (composite image source).
- Raster data sets
  - 25 m raster: 3-band GeoTIFF (dominant class per polygon, mean confidence, percentage cover by modal class).
  - 1 km rasters: dominant cover (1-band) and percentage cover (21-band for target classes; 10-band for aggregates). Coarser products derived from aggregating the 25 m data.
- Coverage and projection
  - Separate data sets for Great Britain (GB) and Northern Ireland (NI); projections are British National Grid (GB) and Irish National Grid (NI), respectively.
  - Minimum mappable unit: >0.5 ha; polygons smaller than 0.5 ha or lines <20 m dissolved into surrounding landscape.

## Class structure and mapping

- 21 LCM1990 classes are based on UK Biodiversity Action Plan Broad Habitats (Appendix 2 defines Broad Habitats).
- Some classes are subdivided to reflect spectral distinctions (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral/Supra-littoral classes).
- Table 2 (linking LCM1990 target/aggregate classes with Broad Habitats) and Appendix 1 provide detailed class mappings and interpretations.
- LCM1990 maps land cover (not strictly land use); some land-use inferences may be ambiguous from spectral data alone.

## Metadata, uncertainty, and quality assurance

- Rich metadata for polygons includes dominant class, per-polygon pixel breakdown, mean classification probability, and uncertainty indicators.
- Uncertainty is captured as per-pixel probability from the Random Forest classifier and summarized per polygon (conf and stdev).
- QA checks cover projections, spatial completeness, modal class presence, metadata consistency, value ranges (0–100 for rasters), and pixel sizes.
- Validation has been performed against external datasets (e.g., Countryside Survey, National Forest Inventory); full validation results will be reported separately.

## Data access and licensing

- 25 m and 1 km raster products are available via the CEH Environmental Information Platform (EIP): https://eip.ceh.ac.uk/
- The full vector product is available on request under licence from CEH; license fees may apply for some users/applications: https://www.ceh.ac.uk/services/land-cover-map-1990 and spatialdata@ceh.ac.uk.
- Data citation and DOIs are provided for each product (GB vector, GB 25 m raster, GB 1 km products; NI products with DOIs where available; some NI products pending DOIs).

## Citations and DOIs

- All LCM1990 products have DOIs to support reproducible research and proper citation.
- Example citation format: Rowland et al. (2020). Land Cover Map 1990 (vector, GB). NERC Environmental Information Data Centre. https://doi.org/...
- See Tables 5 and 6 for GB and NI DOIs corresponding to vector, 25 m, 1 km products (some DOIs pending).

## Practical notes for data governance and stewardship

- Data provenance and versioning: LCM1990 is documented with production methods consistent with LCM2015 to enable long-term change analysis (e.g., 1990–2015).
- Metadata completeness: vector products include extensive attributes (hist, conf, stdev, etc.) to support traceability, quality assessment, and reuse.
- Data availability and updates: rasters are provided in multiple resolutions; the vector product is available on request, enabling controlled access and licensing.
- Interoperability and reuse: alignment with the LCM spatial framework facilitates integration with other geospatial datasets; 0.5 ha MMU and dissolution rules should be considered when integrating with project-specific datasets.
- Limitations: land cover vs land use ambiguity; coastal mapping limitations; some grassland classes may be spectrally confounded; users should review Appendix 1–4 for class definitions and caveats.

## Further information and contacts

- Access, licensing, and additional details: CEH Environmental Information Platform (EIP) and CEH CEH data pages; licensing terms may apply.
- Queries: spatialdata@ceh.ac.uk.
- Acknowledgement: supported by NERC award NE/R016429/1 as part of the UK-SCAPE programme.

## Appendices and supplementary information (high-level)

- Appendix 1: Detailed interpretation and definitions of LCM1990 classes (examples and caveats for specific Broad Habitat groups).
- Appendix 2: Summary definitions of Biodiversity Action Plan Broad Habitats.
- Appendix 3: Standard LCM color mapping recipe for class visualization.
- Appendix 4: Composite images metadata used in LCM1990 production.