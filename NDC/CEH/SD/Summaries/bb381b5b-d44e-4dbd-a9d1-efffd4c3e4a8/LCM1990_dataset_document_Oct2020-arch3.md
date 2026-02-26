# Dataset documentation

- LCM1990 (Land Cover Map 1990) is a parcel-based UK land cover map produced from Landsat-5 imagery (30 m) classifying into 21 Broad Habitat-based classes.
- Purpose: support diverse monitoring needs, enabling scrutiny of environmental policy and informing future decisions; includes preparation for a 25-year land cover change product in the UK.

## Data products and structure

- Vector data set
  - ~6.7 million polygons for Great Britain and ~0.9 million for Northern Ireland.
  - Core attributes include dominant class, per-polygon class breakdown, source image, uncertainty, and a unique geometry identifier (gid) to enable unambiguous communication.
- Raster data sets
  - 25 m raster: three-band product (dominant class per polygon, mean polygon confidence, percentage of polygon covered by the dominant class).
  - 1 km raster products: aggregate/percentage cover for both target (21) and aggregate (10) classes.
  - GB and NI data are provided separately due to different projections.
- Class mapping
  - 21 target classes aligned to UK Broad Habitats definitions (with some subdivisions to reflect spectral distinctions).
  - Aggregates available to produce 1 km products.
- DOIs
  - All LCM1990 products have individual DOIs for stable, citable referencing in publications.

## Metadata, uncertainty, and quality

- Rich metadata
  - Polygon-level metadata includes dominant class, per-polygon class breakdown, and processing details.
- Uncertainty
  - Random Forest per-pixel probability is provided as mean per-polygon confidence (and in the 25 m raster’s band 2).
- Quality Assurance
  - Defined QA checks for projections, spatial completeness, modal class presence, value ranges (0–100 in raster products), and pixel sizes.
  - Independent validation against external datasets (e.g., Countryside Survey, National Forest Inventory) with full validation study planned.

## Data specifications and mapping framework

- Spatial framework
  - GB: British National Grid; NI: Irish National Grid.
  - Vector-based parcels reflect real-world boundaries; raster products derived from these vectors.
- Minimum mapping unit
  - >0.5 ha; parcels smaller than 0.5 ha and linear features <20 m are dissolved into surrounding landscape.
- Temporal and methodological consistency
  - Recreated with methods aligned to LCM2015 to maximize cross-product compatibility and enable long-term change analyses (1990–2015/25 m raster).
- Coordinate and data format details
  - Core vector; 25 m and 1 km rasters; GeoTIFF format; 8-bit unsigned integer rasters; metadata includes projection details and coordinate anchoring (south-west corner convention for pixel coordinates).

## Access, licensing, and citation

- Access channels
  - 25 m and 1 km rasters: CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector product available on request under licence from CEH (licensing fees may apply).
- Citing data
  - Each product has its own DOI; publications should cite the DOI with author/date (e.g., Rowland et al., 2020) and include full DOI references.
  - Example citations provided for GB and NI vector and raster products.

## Use in monitoring and policy contexts

- Application in monitoring frameworks
  - Provides a robust, governance-friendly data source with rich metadata and explicit data provenance.
  - Supports monitoring policy outcomes and informing future decisions; designed to be interoperable with LCM2015 and future change products.
- Data governance and openness
  - Emphasis on data sharing where appropriate; DOIs facilitate reproducibility and traceability.
  - Some data access requires licensing; metadata and processing details help assess suitability and compliance.

## Limitations and considerations

- Mapping constraints
  - Certain Broad Habitat classes (e.g., Fen, Marsh and Swamp; Brackens) can be challenging to map spectrally; some misclassifications possible (e.g., Neutral vs Improved Grasslands).
- Granularity and interpretation
  - The dataset is complex; the 21-class scheme may require aggregation for specific analyses.
  - Built-in caveats: boundaries/linear features are not comprehensively captured in all LCM generations; some coastal and aquatic classes depend on spectral and slope data limitations.
- Spatial resolution vs. metadata
  - Vector products offer rich metadata but larger file sizes; raster products are more processing-friendly but carry less polygon-level metadata.

## Appendix highlights (context for understanding the mapping)

- Appendix 1 and 2 summarize Broad Habitat definitions and their mapping nuances, including distinctions among Woodland types, Grasslands, Bracken, Heath, Fen/Marsh/Swamp, Bog, Water bodies, and Coastal/ marine-related habitats.
- Appendix 3 provides standard LCM1990 colour mapping for visualization.
- Appendix 4 documents composite images used during classification.

## Contact and additional information

- Data access and queries: spatialdata@ceh.ac.uk
- Further information and data access: https://eip.ceh.ac.uk/lcm/lcmdata
- Acknowledgement: NERC Environmental Research Centre (UK-SCAPE) support