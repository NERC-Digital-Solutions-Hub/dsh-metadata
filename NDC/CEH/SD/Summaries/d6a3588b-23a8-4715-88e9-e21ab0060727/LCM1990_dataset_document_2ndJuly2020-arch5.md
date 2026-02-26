# Dataset documentation

## Overview
- Land Cover Map 1990 (LCM1990) is a UK parcel-based land cover dataset produced from Landsat-5 30m imagery.
- Provides a range of data products to support diverse user needs, with 21 land cover classes aligned to UK Biodiversity Action Plan Broad Habitats.
- Built to be compatible with LCM2015 and uses a polygon-based spatial framework to enable interoperability with other geospatial data.
- Core vector product with derived 25m raster and 1km percentage/dominant cover products; multiple data formats and resolutions are available.

## Data content and structure

- Vector data set
  - ~6.7 million polygons for Great Britain; ~0.9 million for Northern Ireland.
  - Eight key attributes per polygon including:
    - gid: unique geometry identifier
    - hist: list of classes within the polygon and pixel counts per class
    - mode: recommended LCM1990 target class (1–21)
    - purity, conf, stdev: uncertainty and classifier confidence
    - n: number of pixels in the polygon
    - cmp: composite image source
- 25m raster data
  - 3-band GeoTiff: band1 (dominant class per polygon), band2 (mean per-polygon confidence), band3 (percentage of polygon covered by the modal class).
- 1km raster data
  - Dominant cover (1 band) for target and aggregate classes; percentage cover (21-band target classes; 10-band aggregates).
  - Rounding may cause sums to deviate from 100; coastal pixels may sum to less than 100 due to mapping extent.
- Spatial framework
  - GB vector/raster use British National Grid; NI uses TM75 Irish Grid.
  - Minimum mappable unit: >0.5 ha; parcels <0.5 ha and linear features <20 m dissolved.

## Metadata, uncertainty, and quality

- Rich polygon metadata include dominant class details, per-polygon pixel breakdown, and mean probability from classification.
- Uncertainty information provided via per-polygon confidence metrics derived from the Random Forest classifier.
- A comprehensive QA regime checks projections, completeness, modal class presence in polygons, value ranges (0–100 for raster products), and pixel sizes.
- Full validation against other datasets (e.g., Countryside Survey, National Forest Inventory) with results to be published separately.
- Field boundary data are anchored to an updated UK/MMU framework to support cross-product compatibility.

## Data access and licensing

- Data access via the CEH Environmental Information Platform (eip.ceh.ac.uk).
- 25m and 1km rasters are openly accessible; the full vector product is available on request under licence.
- License fees may apply for some users/applications.
- Contact: spatialdata@ceh.ac.uk; more information at CEH LCM1990 pages.

## Citing and persistent identifiers

- Each LCM1990 product has a Digital Object Identifier (DOI) for citation and reproducibility.
- Example citation format: (Rowland et al., 2020) with the full DOI provided in references.
- DOIs are listed for GB vector, GB 25m raster, GB 1km products, and NI counterparts; DOI links are provided in the dataset documentation.

## Practical guidance and caveats

- LCM1990 maps land cover, not necessarily land use; some classes are spectrally similar and may require ancillary data for accurate interpretation of land use.
- The 1km products are summary statistics derived from the 25m raster; aggregation can introduce rounding effects.
- Certain ecological finer distinctions (e.g., Neutral vs Improved Grassland) can be challenging spectrally; users should consider class aggregation if appropriate.
- Documentation emphasizes retaining the gid and referencing the detailed metadata for unambiguous communication about parcels.

## Projections and map standards

- GB: British National Grid (EPSG 27700).
- NI: Irish Grid (TM75 / EPSG 29903).
- The vector and raster products are designed to be compatible with LCM2007 and LCM2015 methodology to enable long-term change analyses.

## Appendices and supplemental information

- Appendix 1–4 provide detailed class definitions, Broad Habitat mappings, standard color mappings, and the composite image dataset used during production.
- These appendices aid interpretation of the 21 LCM1990 target classes and their relationship to JNCC Broad Habitats.

## Further information and contact

- Data and metadata overview: CEH Environmental Information Platform (eip.ceh.ac.uk)
- Licensing and access details: https://www.ceh.ac.uk/services/land-cover-map-1990
- Queries: spatialdata@ceh.ac.uk
- References and related work: Jackson (2000); Morton et al. (2011); Rowland et al. (2020a, 2020b)
- Acknowledgement: NERC award NE/R016429/1 under the UK-SCAPE programme