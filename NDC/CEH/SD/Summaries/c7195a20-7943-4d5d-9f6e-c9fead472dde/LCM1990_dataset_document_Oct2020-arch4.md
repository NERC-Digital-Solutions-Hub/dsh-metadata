# Dataset documentation

- LCM1990 is a parcel-based UK land cover map derived from two-date Landsat-5 imagery (30 m) and aligned with the LCM2007/LCM2015 spatial framework to enable long-term change analysis.
- Provides a range of data products (vector and raster) with rich metadata and uncertainty information, designed for diverse applications and user communities.
- Vector products are the core with 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland; raster products include 25 m and 1 km resolutions for broad-scale analyses.

## Data products and formats

- Vector data set
  - Each parcel (polygon) has key attributes: land cover class (text and integer), source image, per-polygon uncertainty, pixel counts per class, and modal class percentage (dominant class).
  - Attributes include gid (unique parcel identifier), _hist (class composition per polygon), _mode (recommended display class), _purity, _conf (mean confidence 0-100 from Random Forest), _stdev, _n (number of pixels), cmp (composite image used).
- Raster data sets
  - 25 m raster (GB and NI) with 3 bands: band 1 = dominant class per polygon, band 2 = mean per-polygon classifier confidence, band 3 = percentage cover of the dominant class.
  - 1 km raster products summarize 25 m data into dominant class and percentage cover for both target classes (21) and aggregate classes (10).
  - MMU: minimum mapped area >0.5 ha; small features dissolved into surrounding landscape.
- Data access formats
  - Data distributed as uncompressed GeoTIFFs (raster) and vector products (formats not specified here; full vector product available on request).

## Class structure and mapping

- LCM1990 comprises 21 target land cover classes based on UK Biodiversity Action Plan Broad Habitats (Jackson, 2000).
- Some Broad Habitats are subdivided for more detail:
  - Built-up Areas and Gardens → Suburban and Urban
  - Dwarf Shrub Heath → Heather and Heather grassland
  - Littoral Sediment Broad Habitat → Littoral sediment and Saltmarsh
- Land cover is mapped (not strictly land use) and uses a polygon-based framework reflecting real-world boundaries for consistency with other datasets.

## Metadata, uncertainty, and quality assurance

- Rich metadata accompanies each polygon, including dominant class, per-polygon class composition, and classification probabilities from Random Forest.
- Per-polygon uncertainty information (mean probability) is provided for both vector and 25 m raster products.
- QA checks cover projections, spatial completeness, modal class presence in polygons, value ranges (0-100 for rasters), and pixel size accuracy.
- Validation against other datasets (e.g., Countryside Survey, National Forest Inventory) is performed; results to be published separately.
- The dataset is built on the 2007 Ordnance Survey MasterMap framework with limited field boundary changes impacting accuracy only modestly.

## Technical details

- Projections and coordinate systems
  - Great Britain: British National Grid (EPSG 27700)
  - Northern Ireland: Irish National Grid (TM75 Irish Grid, EPSG 29903)
- Spatial extents and resolutions
  - Great Britain and Northern Ireland provided separately for GB 25 m and 1 km products.
  - 25 m pixel size; 1 km 1 km pixel extent (covers 1600 25 m pixels per 1 km cell).
- Data access and licensing
  - 25 m and 1 km rasters available via CEH Environmental Information Platform (https://eip.ceh.ac.uk/).
  - Full vector product available on request; licence fees may apply for some users/applications.
  - All products have individual DOIs for citation (Tables 5 and 6 list GB and NI DOIs).
- Documentation and references
  - Citing LCM1990 DOIs is recommended for reproducibility (example format provided in the document).
  - Appendix 3 provides a standard colour mapping for the 21 classes; Appendix 4 lists composite images.

## Access, licensing, and citations

- Access
  - Data can be accessed through the CEH Environmental Information Platform; vector data license on request.
  - Some user groups may incur license fees.
- Citations and DOIs
  - Each LCM1990 product has a DOI (GB vector, GB 25 m raster, GB 1 km targets and aggregates, NI vector, NI rasters, etc.).
  - Example citation: Rowland et al. (2020). Land Cover Map 1990 (vector, GB). NERC Environmental Information Data Centre. https://doi.org/10.xxxx/...
- Usage notes
  - Include author(s) and date in-text plus full DOI in references for reproducibility.
  - Data usage and citation guidelines are provided to support transparent reuse.

## Practical considerations for data leaders

- Governance and strategy
  - LCM1990 demonstrates robust data product design with versioned updates (e.g., 1.1 updating DOIs in Tables 5–6) and a clear data lineage from Landsat-5 inputs to updated LCM frameworks.
  - Rich metadata and per-polygon uncertainty enable informed decision-making and risk assessment for data products built on LCM1990.
- Data usability and dissemination
  - Vector products offer detailed attribute information and communication through the gid for unambiguous data sharing; raster products support scalable national modelling with consistent aggregation.
  - Coherent documentation (Appendices and Tables) aids standardisation of colour mapping, class definitions, and cross-dataset comparisons.
- Access and collaboration
  - CEH platform provides access, while licensing for the full vector product may require negotiation; DOIs facilitate cross-institutional citation and reuse.
  - The dataset is designed to be compatible with LCM2007/LCM2015, enabling long-term change analyses and collaboration across national datasets.

## Summary for decision-makers

- LCM1990 offers a comprehensive, well-documented land cover dataset for the UK (and Northern Ireland) with:
  - 21 detailed land cover classes linked to Broad Habitats, some subdivided for specificity.
  - Rich metadata, per-polygon uncertainty, and two-resolution raster products (25 m and 1 km) plus a full vector product.
  - Clear governance through DOIs, licensing notes, and citation guidance to support reproducible, auditable data use.
- For data strategy, it provides a reliable, standards-aligned data asset that can underpin policy analysis, impact assessments, and cross-network collaborations, with transparent data quality controls and clear access pathways.