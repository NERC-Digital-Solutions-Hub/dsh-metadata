# LAND COVER MAP 2007 DATASET DOCUMENTATION

- Land Cover Map 2007 (LCM2007) is a parcel-based UK land cover classification using 23 Broad Habitat–based classes, derived from 20–30 m satellite imagery, and built to be compatible with GIS data and other datasets.
- It provides a range of data products (vector and raster) to support diverse applications, with detailed metadata and class relationships to aid users in selecting appropriate data.

## Data products and formats

- Vector data set
  - Contains about 8.6 million polygons for Great Britain and 0.9 million for Northern Ireland.
  - Each polygon includes 10 attributes: Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (class for display), KBE (processing history), ProbList (top 5 spectral classes with probabilities), CorePixels, Construct, TotPixels.
  - Features include unique Parcel_ID labeling for unambiguous communication.
- Raster data sets
  - 25 m raster: 23 LCM2007 classes; GB and NI provided separately with 25 m cells and associated metadata.
  - 1 km raster: derived from 25 m data; provides:
    - Dominant cover at 1 km for LCM2007 classes and for Aggregate classes
    - Percentage cover at 1 km for LCM2007 classes and for Aggregate classes
- Spatial and thematic detail
  - 25 m raster and vector data share a common thematic structure, with 23 classes and multiple subclassing options (BHSub).
  - 1 km products offer aggregated views suitable for national-scale modelling and integration with other datasets (e.g., meteorology, species distributions).

## Spatial details and coverage

- Geography
  - Great Britain (GB) and Northern Ireland (NI) datasets are provided separately due to different projections.
- Projections
  - GB: British National Grid (OSGB 1936) Projection (Transverse Mercator).
  - NI: Irish National Grid (older datum); NI is in the process of switching to Ireland Transverse Mercator (ITM).
- Minimum mapping unit and generalisation
  - Minimum mappable area: > 0.5 ha.
  - Parcels smaller than 0.5 ha or linear features under 20 m are dissolved into the surrounding landscape.
- Data scale and compatibility
  - Vector data polygons are designed to align with real-world objects (e.g., fields, woodland blocks) via OSMM or equivalent segmentation.
  - 25 m raster data provide the same land cover detail without polygon boundaries and metadata, useful for some analyses.
- Validation and accuracy
  - Ground reference validation using 9,127 polygons yielded an average accuracy of 83% (with local variation to be expected).

## How to use and interpret the data

- Class structure and mapping
  - 23 LCM2007 classes are tied to UK Biodiversity Action Plan Broad Habitats, with some sub-class distinctions (e.g., Built-up Areas and Gardens subdivided into Urban and Suburban; Dwarf Shrub Heath into Heather vs. Heather grassland).
- Sub-classes and interpretation
  - Broad Habitat sub-classes (BHSub) provide additional information but are not guaranteed to have the same QA level as the primary LCM2007 classes; apply your own validation if using BHSub level data.
  - ProbList includes the top 5 spectral matches for each polygon; useful for validation and post-classification refinement.
- Data integration and communication
  - Parcel_ID should be retained to ensure traceability of each polygon across datasets and analyses.
  - A cross-walk (Appendix 2) links Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes, aiding interpretation and cross-dataset comparisons.
- Change detection
  - Change mapping across CEH land cover products (1990, 2000, 2007) is complex due to class and spatial structure differences and typical spectral misclassification rates; LC M2007 is not well suited for reliable change detection.
- Display and colouring
  - Appendix 3 provides a standard colour mapping for visualisation; an ArcGIS .lyr file is available for convenience.

## Data access and licensing

- Access
  - 1 km raster data sets are available via the CEH Information Gateway (gateway.ceh.ac.uk).
  - The full vector product and 25 m raster product are available under licence on request from CEH.
- Licensing and fees
  - License fees may apply for some users and applications; access via CEH data portal or by contacting spatialdata@ceh.ac.uk.

## Data quality considerations and caveats

- Accuracy and variability
  - Overall QA indicates around 83% average accuracy; individual polygons may vary.
  - Broad Habitat sub-classes are provided but may have lower QA reliability; users should validate at the sub-class level if used for precise analysis.
- Change detection limitations
  - Cross-era comparisons are challenging due to differences in classes, spatial structure, and inherent classification errors (~20% typical for classified imagery).
- Minimum mapping unit and dissolution
  - Smaller features are dissolved, potentially affecting analyses requiring fine-scale detail.
- Spatial resolution considerations
  - 25 m and 1 km raster products trade detail for performance and compatibility with wider datasets.

## Appendices (highlights)

- Appendix 1: LCM2007 classes – descriptions and interpretations of Broad Habitats (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Various grasses and wetlands, Montane habitats, Inland rock, Urban/Suburban, Saltmarsh, Littoral and Fen/March/Swamp classes).
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (maps cross-walks for display and analysis).
- Appendix 3: Colour mapping recipe for standard LCM2007 visualization (class-based RGB values; includes display-ready mappings for ArcGIS).
- Appendix 4: Updates to products (Version 1.2, May 2014) – updates such as OS Tile HZ (Fair Isle) and OS Tile NW (Stranraer); addition of water class in 1 km dominant/aggregate products for GB.

## Version history and updates

- Version 1.0 (July 2011): Original release.
- Version 1.2 (May 2012; updated May 2014 as published): Dataset updates including new tiles (Fair Isle, Stranraer) and water-class inclusions; alignment with updated products and change-detection notes.

## Summary for Data Support perspective

- LCM2007 provides rich, well-documented land-cover data across GB and NI in vector and raster formats, enabling self-serve exploration and data product creation, with extensive metadata, class mappings, and validation.
- When supporting data users:
  - Emphasize the 23-class structure, high-quality metadata, and the Parcel_ID tracking for cross-dataset communication.
  - Highlight the availability of 1 km and 25 m raster products for broad and detailed analyses, respectively, and the option to access the full vector product under licence.
  - Caution on change detection suitability and the need for validation at the sub-class level due to QA variability.
  - Provide guidance on selecting GB vs NI datasets, projection differences, and the ongoing NI move toward ITM.
  - Point to Appendix resources for class definitions, colour schemes, and update history to aid integration and downstream data products.