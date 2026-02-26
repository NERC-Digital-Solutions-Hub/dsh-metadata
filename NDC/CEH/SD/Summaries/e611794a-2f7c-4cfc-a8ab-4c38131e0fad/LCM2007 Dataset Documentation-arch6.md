# LAND COVER MAP 2007 DATASET DOCUMENTATION

- A comprehensive UK land cover dataset (LCM2007) providing parcel-based, 23-class land cover maps aligned to UK Broad Habitats.
- Based on summer-winter satellite composites at 20–30 m resolution; updates LCM2000 with a framework tied to OS master map data and image segmentation.
- Clarifies that LCM2007 maps land cover (not strictly land use) and uses a minimum mappable unit of >0.5 ha.

## Key purpose and audience
- Designed to meet diverse user needs with multiple data products (vector and raster) for broad application areas.
- Recommended as context for decision-making, planning, and environmental interpretation; consult the Final Report (Morton et al., 2011) for full methodology and limitations.

## Data structure and content

- Vector data set
  - Great Britain: ~8.6 million polygons; Northern Ireland: ~0.9 million polygons.
  - Each polygon has 10 attributes, including Parcel_ID, Broad Habitat (BH), Broad Habitat sub-class (BHSub), FieldCode, INTCODE (class number for display), Knowledge-Based Enhancements (KBE) history, ProbList (top 5 spectral class probabilities), CorePixels, Construct, TotPixels.
  - Unique Parcel_ID enables unambiguous communication; recommended to retain in analyses.

- Raster data sets
  - 25 m and 1 km products derived from the vector data.
  - 1 km rasters provide dominant and percentage cover for both LCM2007 classes and Aggregate classes.
  - GB and NI datasets use different projections (GB: British National Grid; NI: Irish National Grid).

## LCM2007 class scheme and labeling

- 23 LCM2007 classes tied to Broad Habitats; some classes subdivided into sub-classes (e.g., Built-up Areas into Urban/Suburban, Dwarf Shrub Heath into Heather/Heather grassland).
- Appendix 1 details each Broad Habitat class; Appendix 2 maps relationships between Broad Habitats, LCM2007 classes, and sub-classes.
- FieldCode provides a human-readable sub-class label; not all FieldCode-level distinctions are QA’d.
- ProbList provides the top five spectral variants for each polygon (user validation advised for sub-class usage).

## Data quality and validation

- Ground-reference validation: average accuracy ~83% across 9,127 polygons; regional/local accuracy may vary.
- LCM2007 validates at the thematic resolution of 23 classes; Broad Habitat sub-classes are not guaranteed to have the same QA robustness as the main classes.
- Important caveats:
  - LCM2007 maps land cover, not always exact land use.
  - Some grassland classifications (e.g., Neutral/Calcareous Grassland) may be misclassified as Improved Grassland; users should consult Morton et al. (2011) for guidance.
  - Montane, inland rock, and certain coastal classes may have classification complexities due to spectral similarity and altitude-based rules.

## Production details and metadata

- Rich polygon metadata capturing:
  - Processing history, polygon construction method (OSMM-based segmentation), raw spectral classification, and KBE history.
  - Knowledge-based enhancements (KBE) applied to refine classifications.
- The dataset emphasizes object-based polygons that reflect real-world features (fields, woodland blocks), aiding interoperability with other GIS layers.

## Data access and licensing

- 1 km raster data: accessible via the CEH Information Gateway.
- Full vector product and 25 m raster product: available on request under licence from CEH; online application process and potential licence fees apply.
- Users should cite the Final Report (Morton et al., 2011) for methodological details and follow attribution and licensing terms.

## Projections, extent, and file sizes

- Projections
  - Great Britain: British National Grid (OSGB 1936); NI: Irish National Grid.
  - NI is transitioning toward Ireland Transverse Mercator (ITM); re-projection supported by GIS tools.
- File sizes (guidance; varies by format)
  - Vector (shapefile, GB): ~4.13 GB; Vector (NI): ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - Raster 1 km: 21 MB to 49 KB (GB/NI, aggregate and percentage products vary).
- Data structure notes
  - 10 attributes per vector polygon; large vector datasets may be unwieldy for some workflows.
  - Some products provide detailed metadata for alignment with other data sources.

## How to use

- Product selection
  - Use vector data for detailed, attribute-laden analyses; use 25 m raster where simpler raster operations and reduced metadata overhead are preferred.
  - 1 km rasters are suitable for nationwide modeling and when integrating with large-scale datasets (e.g., meteorology, species distributions).
- Applicability guidance
  - For cross-dataset analyses, retain Parcel_ID to maintain traceability to source images and processing steps.
  - For applications requiring consistent, coarse-resolution inputs, consider 1 km aggregates; for detailed mapping and object-based analyses, use 25 m or vector data.
- Caution on interpretation
  - Distinguish land cover from land use; verify if a given class matches the intended application.
  - Validate Broad Habitat sub-classes if used for fine-grained analyses beyond the 23-class QA.
  - Review Appendix 1–3 and Morton et al. (2011) for colour mapping and detailed class relationships.

## Appendices and colour mapping

- Appendix 1: LCM2007 Class descriptions and Broad Habitat brief reviews (e.g., Broadleaved woodland, Coniferous woodland, Arable, Various grasslands, Fen/Swamp, Bog, Montane, Inland Rock, Saltwater, Freshwater, Coastal, Urban, etc.).
- Appendix 2: Detailed mapping relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (FieldCode values and class numbers).
- Appendix 3: Standard LCM2007 colour mapping (RGB values per LCM2007 class for visualization).

## Further information and references

- Primary documentation: Morton, D. et al. Final Report for LCM2007 – The New UK Land Cover Map. Countryside Survey Technical Report No. 11/07 (CEH, 2011).
- Broad Habitat guidance: Jackson, D.L. (2000) Guidance on interpretation of Biodiversity Broad Habitat Classification (JNCC Report 307).
- Acknowledgments cover data sources and licensing for Landsat, SPOT, AWIFS, Ordnance Survey, soils, elevation, and other datasets used in LCM2007.