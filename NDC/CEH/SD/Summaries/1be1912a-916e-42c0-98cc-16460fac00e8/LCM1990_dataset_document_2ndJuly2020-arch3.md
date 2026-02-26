# Dataset documentation

- LCM1990 provides a parcel-based UK land cover map with 21 classes, derived from Landsat-5 two-date composites at 30 m resolution.
- It is designed to support various land cover monitoring needs and to be compatible with later LCM products (e.g., LCM2015) to enable long-term change analyses.

## Data scope and purpose

- Parcel-based land cover map for the UK, mapped to 21 Broad Habitat classes based on UK Biodiversity Action Plan definitions.
- Aims to support monitoring, policy scrutiny, and future decision-making by providing detailed, traceable land cover information.
- Recreated using methods matching LCM2015 to enable construction of a 25-year land cover change product (1990–2015 for GB and NI).

## Data products and structure

- Vector data set (core product): polygons with extensive attributes per parcel.
- 25 m raster: derived from the vector; bands include dominant class, per-polygon uncertainty, and modal coverage.
- 1 km raster products: derived by aggregating 25 m raster outputs; include dominant cover (target and aggregate classes) and percentage cover for target and aggregate classes.
- Geographic coverage: separate datasets for Great Britain (GB) and Northern Ireland (NI).

## Key class structure

- 21 LCM1990 target classes based on Broad Habitats (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Improved Grassland, Neutral Grassland, etc.).
- Some Broad Habitats are subdivided into finer classes (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Saltmarsh and Littoral sediment).

## Attributes and labeling

- Vector attributes include:
  - gid: unique polygon identifier
  - hist: list of classes present in the polygon with pixel counts
  - mode: recommended dominant LCM1990 class
  - purity: percent area of polygon covered by the modal class
  - conf: mean per-polygon classifier confidence (0–100)
  - stdev: standard deviation of classifier uncertainty
  - n: number of pixels in polygon
  - cmp: composite image index used for classification
- Rich metadata accompanies polygons to support interpretation and reproducibility.
- Uncertainty information is provided as per-pixel probability from the Random Forest classifier, included in both vector (per-polygon mean) and 25 m raster.

## Data formats and resolution

- 25 m raster: 3-band GeoTIFF (dominant class, mean confidence, and percentage cover); 8-bit unsigned, uncompressed.
- 1 km rasters: aggregate percent cover (integer values) and dominant class (1-band); GB and NI are provided separately with their respective projections.
- Projections:
  - GB: British National Grid (EPSG 27700)
  - NI: TM75 Irish Grid (EPSG 29903)

## Accessibility and licensing

- Data access via CEH Environmental Information Platform (EIP): https://eip.ceh.ac.uk/
- Full vector product available on request; licensing may apply.
- All LCM1990 products have individual DOIs for citation (GB vector, GB 25 m raster, GB 1 km targets/aggregates, NI equivalents) to enable method transparency and reproducibility.

## Quality assurance and validation

- QA checks verify projections, spatial completeness, modal class presence in polygons (vector), data headings, value ranges (0–100 for percent rasters), and pixel size accuracy.
- Full validation against external datasets (e.g., Countryside Survey, National Forest Inventory) conducted and reported in a separate publication.
- The parcel framework draws on 2007 OS MasterMap data; field boundary changes are limited, reducing impact on accuracy.

## Geographic scope and data integration

- Data designed to be compatible with LCM2007 and LCM2015, enabling long-term change products (e.g., 1990–2015).
- Spatial framework aligns with earlier LCM editions to maximize cross-product comparability.

## Use considerations and caveats

- LCM1990 maps land cover rather than strictly land use; some classifications may not infer land use reliably (e.g., recreation grass vs. grazing land).
- Minimum mappable area: polygons >0.5 ha; dissolve smaller parcels and linear features <20 m into surrounding landscape.
- Some habitat classes (e.g., Fen/Marsh/Swamp, Bog) can be difficult to map accurately due to spectral similarity, patch size, and mosaic patterns; users should consult hist and uncertainty metadata for interpretation.
- Off-coast areas are limited by cartographic extent; coastal and littoral classes may be sensitive to slope and spectral conditions.

## Documentation and appendices (highlights)

- Appendix 1: Class-specific notes and mapping considerations for key Broad Habitats (e.g., Woodlands, Grasslands, Bracken, Heaths, Wetlands, Coastal and Littoral classes).
- Appendix 2: Summary of Biodiversity Action Plan Broad Habitats definitions (JNCC Jackson 2000) to aid interpretation and cross-walking with LCM1990 classes.
- Appendix 3: Standard LCM color mapping recipe for visualizing classes.
- Appendix 4: Details on composite images used during classification (image paths, dates, and identifiers).

## How this supports monitoring frameworks

- Provides a transparent, well-documented data lineage with rich metadata, uncertainty information, and DOIs, supporting level-of-effort assessments, reproducibility, and governance.
- Its compatibility with LCM2015 facilitates comparative monitoring across decades, enabling robust policy evaluation and informing future environmental health decisions.
- Clear data access, licensing, and citation guidance align with data governance requirements in monitoring frameworks.

## Additional information

- Access and contact: CEH Environmental Information Platform; spatialdata@ceh.ac.uk for further details.
- Related publications and data: Rowland et al. (2020) on Land Cover Change 1990–2015; Jackson (2000); Morton et al. (2011).