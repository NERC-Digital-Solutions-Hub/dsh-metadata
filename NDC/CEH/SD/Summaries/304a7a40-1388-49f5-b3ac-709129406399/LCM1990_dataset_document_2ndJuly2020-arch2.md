# Dataset documentation

## Introduction
- Land Cover Map 1990 (LCM1990) is a UK parcel-based land cover dataset created from Landsat-5 data (30 m) classified into 21 classes.
- The dataset uses the updated LCM2015 framework to maximise compatibility and to enable a 25-year land cover change product (1990–2015) for the UK.
- LCM1990 maps land cover (not strictly land use) and provides rich metadata, uncertainty information, and a documented processing workflow.
- The product line includes vector and raster formats (25 m and 1 km), with both GB and Northern Ireland coverage.

## Data products
- Core vector data set: polygons with attributes including dominant class, pixel breakdown by class, uncertainty, and a unique geometry identifier (gid). GB has ~6.7 million polygons; NI ~0.9 million.
- 25 m raster: three-band GeoTIFF per region (GB and NI) with band1 = dominant LCM1990 class, band2 = mean per-polygon confidence, band3 = percent coverage of modal class.
- 1 km raster products: dominant cover (for target and aggregate classes) and percentage cover (21 target classes and 10 aggregate classes) derived from 25 m data.
- 21 target LCM1990 classes (e.g., Broadleaved woodland, Arable, Improved Grassland, etc.) with specific subdivisions where applicable (e.g., Built-up Areas and Gardens split into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Littoral sediment and Saltmarsh).

## Data frameworks and comparability
- Uses a spatial framework aligned with LCM2007/LCM2015, enabling direct comparison across years and supporting long-term change analyses.
- The spatial framework is compatible with other UK land cover datasets to facilitate multi-temporal and cross-dataset analyses.

## Spatial framework and classes
- 21 land cover classes based on UK Biodiversity Action Plan Broad Habitat definitions.
- Some Broad Habitats are subdivided based on spectral signals (e.g., Built-up Areas and Gardens; Dwarf Shrub Heath; Littoral Sediment).
- Minimum mappable unit: >0.5 ha; polygons <0.5 ha and linears <20 m are dissolved into the surrounding landscape.

## Vector data details
- The vector product provides polygons with eight key attributes, including:
  - gid: unique parcel identifier
  - hist: list of classes present in the polygon with pixel counts
  - mode: recommended LCM1990 target class (1–21)
  - purity: percentage of polygon covered by the modal class
  - conf: mean per-polygon confidence from the Random Forest classifier
  - stdev: standard deviation of uncertainty
  - n: number of pixels in the polygon
  - cmp: composite image source
- Data access: full vector product available on request from CEH; licensing fees may apply.

## Raster data details
- 25 m raster: 3-band GeoTIFF (dominant class, per-polygon confidence, modal class percentage).
- 1 km rasters: percentage cover (21 target classes and 10 aggregate classes) and dominant cover for 1 km pixels.
- GB and NI rasters are provided in separate coordinate systems (British National Grid for GB; TM75 Irish Grid for NI).

## Aggregation and mapping
- Aggregate classes merge the 21 LCM1990 classes into 10 groups for 1 km products.
- The 1 km percentage cover values are integers; sums may exceed or fall short of 100 due to rounding and coastal edge effects.

## Data access and licensing
- Data are accessible via the CEH Environmental Information Platform (eip.ceh.ac.uk).
- 25 m and 1 km raster data are available; full vector product on request.
- Licence fees may apply; contact spatialdata@ceh.ac.uk for details.
- DOIs exist for LCM1990 products (GB and NI; vector and raster variants) to enable citation and reproducibility.

## Data formats and projections
- Raster: uncompressed GeoTIFFs (8-bit unsigned).
- Vector: polygon-based with detailed attributes.
- Projections:
  - GB: British National Grid (OSGB 27700)
  - NI: TM75 Irish Grid (EPSG: 29903)
- Metadata-rich: each polygon includes dominant class, per-class pixel counts, confidence, and other processing details.

## Quality assurance and validation
- QA checks cover projections, spatial completeness, modal class presence, data range checks (0–100 for rasters), and pixel size validation.
- A full validation against reference datasets (e.g., Countryside Survey, National Forest Inventory) was conducted; results are reported in a separate publication.
- The parcel framework is based on 2007 Ordnance Survey MasterMap data; field boundary changes are infrequent, limiting impact on accuracy.

## Usage notes and limitations
- LCM1990 maps land cover rather than precise land use; some land-use inferences (e.g., arable crops vs. grassland) may be ambiguous from spectral data alone.
- Some grassland and mosaic habitats may be misclassified; careful interpretation is advised, and ancillary data may improve accuracy.
- Fine-scale features narrower than 20 m are generally not captured; the MMU constraints affect narrow boundaries and linear features.

## Citing LCM1990 DOIs
- All LCM1990 products have individual DOIs for citation, enabling transparent methods and usage tracking.
- Examples provided for GB and NI products; proper citation should include author, date, and full DOI.

## Appendix highlights
- Appendix 1 and 2 provide detailed mappings between LCM1990 classes and Biodiversity Action Plan Broad Habitats, including guidance on spectral interpretation and field considerations.
- Appendix 3 describes the standard LCM colour mapping for class visualization.
- Appendix 4 lists the composite images used in LCM1990 production.

## Further information and contacts
- Access and data queries: spatialdata@ceh.ac.uk; https://eip.ceh.ac.uk/lcm/lcmdata
- Licence and access details: https://www.ceh.ac.uk/services/land-cover-map-1990

## Acknowledgements and references
- Supported by Natural Environment Research Council (NE/R016429/1) as part of the UK-SCAPE programme.
- Key references include Jackson (2000), Morton et al. (2011), and Rowland et al. (2020a,b).