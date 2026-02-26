# Land Cover Map 1990 (LCM1990) Dataset Documentation

- LCM1990 is a parcel-based UK land cover map classified into 21 classes, aligned with UK Biodiversity Action Plan Broad Habitats definitions.
- Based on two-date Landsat-5 composites (30 m resolution); replaces LCMGB and uses an updated LCM2007 spatial framework for compatibility with LCM2015.
- Designed to support diverse users (policy, environment, research) and enable long-term land cover change products (e.g., 1990–2015).

## Data structure and content

- Vector data set
  - ~6.7 million polygons for Great Britain; ~0.9 million for Northern Ireland.
  - Each polygon includes a unique geometry identifier (gid) and rich attributes:
    - Dominant class (mode), histogram of class composition within the polygon, per-polygon confidence, standard deviation, number of pixels, and composite image source.
  - Eight key attributes focusing on class, provenance, and uncertainty.
- Raster data set
  - 25 m raster derived from the vector data (three-band): dominant class per polygon, mean per-polygon confidence, and polygonal coverage of the modal class.
  - 1 km raster products provide dominant and percentage cover for 21 target classes and 10 aggregate classes.
- Minimum mapping unit
  - Parcels >0.5 ha; polygons <0.5 ha and linear features <20 m are dissolved into surrounding landscape.

## Data products and formats

- Core vector product and derived rasters
  - 25 m raster: 3-band GeoTIFFs (dominant class, confidence, percent coverage).
  - 1 km rasters: dominant covers (target/aggregate) and percentage covers (21 target bands; 10 aggregate bands).
- Spatial detail
  - 25 m and 1 km products available; Great Britain and Northern Ireland provided separately due to projection differences.
- Class structure
  - 21 LCM1990 target classes, mapped to UK Broad Habitats; some classes are split to reflect spectral nuances (e.g., Built-up Areas into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland).
- Metadata and uncertainty
  - Rich metadata per polygon; per-pixel probability from Random Forest classifier included as polygon mean probability (and in raster bands).
  - Uncertainty information captured (confidence, standard deviation) to aid interpretation.

## Spatial framework and comparability

- LCM1990 uses a spatial framework consistent with LCM2015, enabling cross-compatibility and future multi-decadal change analyses (e.g., 1990–2015).
- The framework is based on Ordnance Survey MasterMap topographic data (GB) and NI large-scale vector data; designed to align polygon boundaries with real-world features.

## Metadata, uncertainty, and quality

- Each data product has a Digital Object Identifier (DOI) for citation and reproducibility; DOIs provided separately for GB and NI products.
- Cited documentation emphasizes method provenance, per-polygon classification probabilities, and detailed metadata for transparency.
- Quality Assurance (QA)
  - Projections correctness, spatial completeness checks, modal class presence in polygons, axis-heading consistency, value range checks (0–100 for raster), and pixel-size validations.
  - Full validation against external datasets (e.g., Countryside Survey, National Forest Inventory) described; results to be reported in a separate publication.

## Access, licensing, and citation

- Data access
  - 25 m and 1 km rasters available via the CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector product available on request under licence; some applications may incur fees.
- Citation
  - All LCM1990 products have individual DOIs; use author and date in-text (e.g., Rowland et al., 2020) and include full DOI in references.
  - Example citation guidance provided for GB and NI products.

## Projections and data access details

- Map projections
  - GB vector/raster: British National Grid (OSGB 27700).
  - NI vector/raster: Irish Grid (TM75; EPSG 29903).
- Access channels
  - CEH platform for rasters; vector products via licence and request.
  - Contact: spatialdata@ceh.ac.uk for details.

## Class definitions (Broad Habitats)

- LCM1990 classes map to 21 Broad Habitats, based on JNCC definitions (Jackson 2000), including:
  - Broadleaved/ mixed/ yew woodland; Coniferous woodland.
  - Arable and Horticulture; Improved Grassland; Neutral Grassland; Calcareous Grassland; Acid Grassland; Bracken.
  - Dwarf Shrub Heath (split into Heather and Heather grassland); Fen/Marsh/Swamp; Bog.
  - Standing Open Water and Canals; Rivers and Streams; Montane.
  - Inland Rock; Built-Up Areas and Gardens (split into Urban and Suburban); Supralittoral Rock; Supralittoral Sediment.
  - Littoral Rock; Littoral Sediment; Inshore Sublittoral Sediment.
- The definitions reflect spectral-based mapping with considerations about field verification and potential misclassifications (e.g., mixing of grassland types, peat depth considerations for some broad habitats).
- Appendix-style guidance provides standard color mappings and notes on particular class interpretations.

## Practical notes for analysts

- Suitability
  - Use 25 m data for detailed, localized analysis; 1 km data suitable for UK-scale modelling with other datasets (climate, species distributions).
  - The 21-target class raster and 10-aggregate class rasters support flexible aggregation and modelling needs.
- Data interpretation
  - Expect some classification uncertainty; the per-polygon histograms and mean confidence aid reliability assessments.
  - The 0.5 ha MMU means small habitat patches may be generalized or dissolved.
- Future work
  - LCM1990 supports long-term change analyses with LCM2015 and beyond; validated findings will be published separately.