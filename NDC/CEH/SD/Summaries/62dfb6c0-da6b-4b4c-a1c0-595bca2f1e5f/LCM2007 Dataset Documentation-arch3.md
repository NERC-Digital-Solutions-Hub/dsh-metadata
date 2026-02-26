# LAND COVER MAP 2007 DATASET DOCUMENTATION

- Land Cover Map 2007 (LCM2007) is a parcel-based UK land cover classification providing 23 classes derived from UK Broad Habitats, built from summer–winter satellite composites at 20–30 m resolution.
- Purpose: support environmental monitoring, policy scrutiny, and future decision-making; emphasises data quality, metadata, and clear communication of limitations.

## Product scope and classification

- Maps land cover (not land use) with a minimum mapping unit > 0.5 ha; parcels smaller than 0.5 ha or <20 m wide are dissolved into surrounding areas.
- 23 LCM2007 classes are aligned to UK Broad Habitats; certain Broad Habitats are subdivided for spectral reasons (e.g., Built-up Areas into Suburban/Urban, Dwarf Shrub Heath into Heather/Heather grassland).
- The dataset is validated at the 23-class thematic resolution; broad habitat sub-classes provide additional information but are not generally QA-validated at that level.
- Ground reference validation: evaluation against 9,127 polygons yielded an average accuracy of 83% (recognises local variations).

## Data products and formats

- Vector data set
  - 8.6 million polygons for Great Britain; 0.9 million for Northern Ireland.
  - Each polygon includes 10 attributes (e.g., Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, TotPixels, Construct).
  - Parcel_ID provides a unique identifier (recommended to be retained for communication; links to the input satellite image).
  - KBE (Knowledge-Based Enhancements) record processing history; ProbList shows top spectral class probabilities; FieldCode is a non-validated code.
  - Sub-classes (BHSub) and FieldCode used for classification and potential advanced analyses; validation cautioned for sub-class level use.
- Raster data sets
  - 25 m and 1 km products derived from the vector data; GB and NI provided in separate projections.
  - 25 m raster contains all 23 LCM2007 classes; 1 km raster products include dominant and percentage cover for both LCM2007 classes and their aggregate classes.
  - 1 km products useful for national-scale modeling and integration with other datasets (e.g., climate, species distribution).

## Map projection and spatial details

- GB vector/raster data: British National Grid (OSGB 1936).
- NI vector/raster data: Irish National Grid (Ireland 1965; NI transitioning to ITM).
- 25 m raster and vector products are aligned with respective national projections; explicit note on projection transition for Northern Ireland.

## Data access and licensing

- 1 km raster data sets are openly available via the CEH Information Gateway.
- Full vector product and 25 m raster product require licensing (application via CEH data portal; some use may incur fees).
- Data access supports data governance: underlying data may need to be shared with appropriate permissions; metadata and provenance aid traceability.

## Data sizes and management

- Vector: ~10 million polygons; large file sizes; example sizes (approximate) provided for guidance:
  - Vector shapefile (GB): ~4.13 GB; NI: ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - Raster 1 km: 21 MB to 49 KB (depending on dataset type).
- Data management considerations: high storage requirements; usefulness increases with retaining detailed attributes (especially Parcel_ID and KBE/ProbList).

## Data quality, limitations, and guidance

- LCM2007 provides rich metadata per polygon (processing history, spectral results, KBE history, probability lists) to support quality assurance and independent validation.
- Important caveats:
  - LCM2007 maps land cover; inferring land use may be inaccurate in some cases.
  - Sub-class level interpretations (BHSub) require user validation; not all sub-classes have QA-level validation.
  - Some grassland classifications (Neutral/Calcareous vs. Improved) can be misclassified; users needing fine-grained grassland types should rely on Section 3.9 and Chapter 4 of Morton et al. (2011) Final Report for context and consider aggregating classes as needed.
- The product relies on up-to-date metadata and data governance practices to keep datasets usable and comparable over time.

## Appendices (summaries)

- Appendix 1: LCM2007 Classes
  - Provides brief descriptions of each of the 23 classes (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Improved Grassland, Neutral Grassland, Calcareous Grassland, Acid Grassland, Fen/Marsh/Swamp, Bog, Montane Habitats, Inland Rock, Saltwater, Freshwater, Supra-littoral/Sand dune, Littoral Rock/Sediment, Saltmarsh, Urban/Suburban).
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes
  - Maps correspondence between Broad Habitat categories and LCM2007 class numbers, including sub-class associations (FieldCode, BHSub).
- Appendix 3: Colour mapping
  - Provides standard RGB color assignments for each LCM2007 class as used in the Final Report (Morton et al., 2011) for visualisation.

## Acknowledgements and references

- Acknowledges data sources (Landsat TM, SPOT, AWIFS, cartographic data from Ordnance Survey and other agencies) and licensing frameworks.
- Primary reference for methodology and full technical details: Morton et al. 2011 Final Report for LCM2007; additional guidance from Jackson (2000) on Broad Habitat classification.