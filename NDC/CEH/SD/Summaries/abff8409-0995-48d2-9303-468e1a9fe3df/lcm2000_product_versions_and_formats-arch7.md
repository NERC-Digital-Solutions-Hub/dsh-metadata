# LCM2000 specification

- LCM2000 is a parcel-based thematic classification of satellite imagery covering the entire United Kingdom, upgrading the Land Cover Map of Great Britain (LCMGB) 1990 and providing an all-UK dataset that includes Northern Ireland. It is produced as both vector (parcels) and raster formats, with multiple detail levels and resolutions. It uses a hierarchical nomenclature aligned with the Joint Nature Conservation Committee (JNCC) Broad Habitats classification and includes additional detail where possible.

- Available product versions and formats:
  - Vector data (parcels) with attributes
    - Level 2: 26 LCM2000 Subclasses (standard, most widely used)
    - Level 3: up to 72 Variant level detail (special arrangement required; more user support)
    - Standard vector format: ESRI shapefile
  - Raster data (derived from vector)
    - 25 m grid: 26 Subclasses
    - 1 km grid: two detail levels
      - Subclass level: 26 Subclasses
      - Aggregated values: Dominant and Percentage within 1 km cells
    - 1 km resolution also provides Aggregate class level (10 simplified aggregates) with dominant and percentage values
    - Standard raster format: GeoTIFF
  - Note: Raster data are not directly comparable with LCM1990 due to different construction methods; not suitable for estimating change over the 10-year period.

- Dataset coverage and structure:
  - Compiled on a 100 km tile basis; parcels are classified and added to their 100 km tile.
  - Tiles may be merged for construction efficiency; land parcels straddling tile edges can be present in adjoining tiles.

- Hierarchical nomenclature and codes:
  - Vector data provide Subclass (Level 2) and Variant (Level 3) with corresponding codes and Alpha codes (e.g., D for broad-leaved/mixed woodland, Db for woodland variants, 4.1 for arable cereals variants, etc.).
  - Level 3 Variant detail is dependent on dominant land cover at imaging time and may vary in accuracy across regions.

- Vector polygon attributes (per parcel):
  - SegID: unique parcel identifier (required for traceability)
  - BHSub: dominant land cover type (Level 2 Subclass code)
  - BHSubVar: dominant level 3 variant code (if present)
  - PerPixList: per-pixel list by percentage area of top spectral subclasses (Level 3 only)
  - OpHistory: processing history (image dates, KBC rules, etc.)
  - TotPixels: total number of pixels in the parcel
  - CorePixels: number of pixels in the core area used for classification

- OpHistory attribute (processing history description):
  - Encodes input scene, sensor, acquisition dates, and processing steps (including knowledge-based correction and rule application)
  - Includes a sixth field for special statuses (e.g., edge erosion, voids filled, edge overlaps)
  - Scene entries are enumerated with sensor types (e.g., TM, IRS) and acquisition dates; a 0 value indicates manually created/edited areas

- Colour recipes for mapping:
  - 26 Subclasses each have recommended display colors (Hue, Saturation, Value or RGB equivalents) to aid map readability and interpretation

- Broad Habitat descriptions (high-level categories):
  - Broad-leaved/mixed woodland
  - Coniferous woodland
  - Arable and horticulture
  - Improved grassland
  - Neutral grassland
  - Calcareous grassland
  - Acid grassland
  - Bracken
  - Dwarf shrub heath
  - Fen/marsh/swamp
  - Bog
  - Standing open water and canals
  - Rivers/streams
  - Montane habitats
  - Inland rock
  - Built-up areas and gardens
  - Coastal/shoreline habitats ( Supra-littoral and Littoral categories )
  - Inshore sublittoral/submerged categories are not individually distinguished

- Edge overlaps and artefacts (Appendix 1 overview):
  - Edge overlaps occur because of mosaic imagery and cloud-hole patching; multiple layers of parcels exist within a 100 km tile
  - Overlaps are removed through erosion/merging to yield a single parcel layer; some edge parcels may be duplicated across adjacent tiles
  - Artefacts (less than ~0.1% of parcels) can arise; users may visually tidy edges by dissolving boundaries between adjacent parcels of the same class
  - When merging tiles, the first input tile generally has priority for edge parcels; dissolving or union operations can affect parcel-level attributes and Level 3 data
  - Practical guidance includes clipping to tile edges, using dissolve with caution (preserving Level 3 bhsubvar), and selective dissolving to retain attribute integrity

- Slivers and small parcels:
  - Parcels smaller than the minimum mappable unit or created by edge handling can occur; approaches include visual removal, dissolving with adjacent same-class parcels, or intelligent dissolving based on shared boundaries

- Customisation and data stewardship:
  - LCM2000 is intended as a data storage and analysis framework; users are encouraged to modify and expand while preserving provenance
  - Each parcel has a unique SegID to maintain traceability with the data management team
  - Production philosophy emphasizes retaining as much information as possible; maintain lineage by keeping original attributes or storing changes in new attributes

- Production philosophy and accuracy:
  - The dataset is information-rich; users should document changes and acknowledge inherent inaccuracies due to data model, scale, resolution, interpretation, or class definitions
  - LCM2000 does not guarantee perfect accuracy; differences may reflect methodological factors rather than errors

- Further information and references:
  - Land Cover Map home page: www.ceh.ac.uk/data/lcm
  - Contact: spatialdata@ceh.ac.uk or phone 01491 692315
  - Key methodological references:
    - Fuller et al. 2002; Smith et al. 2001; Jackson 2000
  - Detailed Broad Habitat classification descriptions are provided (Table 6)

- Appendix 2 (Good practice) status:
  - Mentioned but not detailed in the available text; intended to provide further guidance on best practices

- Useful takeaways for GIS specialists:
  - Choose vector Level 2 for broad mapping or Level 3 for detailed variant information (with caveats)
  - Use the 100 km tile framework and be aware of edge overlap artefacts when integrating tiles
  - Preserve SegID and parcel-level metadata for traceability and reproducibility
  - Leverage the color recipes and broad habitat descriptions to create clear, policy-relevant map products
  - Recognise that raster outputs are not suitable for change detection with LCM1990 and plan analyses accordingly