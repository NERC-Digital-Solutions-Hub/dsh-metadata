# Final Report for LCM2007 - the new UK land cover map

- Overview
  - First continuous parcel-based UK land cover map (LCM2007) built from national cartography (OS MasterMap/LPS) with satellite imagery, aligned to Broad Habitats (BH) for UK biodiversity policy.
  - Outputs: 23 LCM classes (and 17 BHs) at multiple scales; vector land parcels plus 25 m and 1 km raster products; nationwide UK coverage with GB and NI distinctions.
  - Purpose: support habitat monitoring, policy, and ecosystem analyses; serve as a consistent base for change detection and landscape planning.

- Data sources and spatial framework
  - Satellite imagery: Landsat TM5, Landsat ETM+, LISS-3, SPOT-4/5; 60 m AWIFS backup; multi-date composites (summer + winter) with 20–30 m resolution.
  - Spatial framework: OS MasterMap generalised to minimum mapped unit, combined with agricultural boundaries to improve delineation; NI boundaries treated with a separate framework.
  - External data: digital elevation models, soils, urban boundaries, and agricultural boundaries to enhance knowledge-based enhancements.

- Processing and classification workflow
  - Pre-processing: cloud masking, atmospheric correction, georegistration (RMSE < 0.3 px), topographic correction; image composites created.
  - Segmentation and framework: parcel-based segmentation integrated with OSMM/AGC boundaries; NI has separate segmentation.
  - Classification: parcel-based supervised maximum likelihood classification using multi-temporal imagery; training data from ground references; top five class probabilities retained.
  - Knowledge-based enhancements (KBEs): seven automated KBEs plus terrain/soil adjustments applied after initial classification to resolve spectral confusion (e.g., different grassland types) and improve mapping to BHAs; manual edits where needed.
  - Output metadata: vector products include extensive processing history, spectral class probabilities (ProbList), KBEs (KBE), and source information.

- Outputs and data formats
  - Vector product: land parcels with attributes such as area, Broad Habitat (BH), BH sub-classes, KBE history, and processing details.
  - Raster products: 25 m resolution with 23 LCM2007 classes; 1 km rasters providing either percent cover or dominant class per pixel.
  - Accessibility: 1 km rasters via CEH Information Gateway; full vector and 25 m rasters available on request under licence; fees may apply.

- Validation, accuracy, and cautions
  - Ground reference validation: 9,127 points (2006–2008); overall accuracy around 83% for LCM2007 classes.
  - Class-specific variation: higher accuracy for Coniferous Woodland, Freshwater, Built-up Areas & Gardens, Calcareous Grassland; lower for Neutral and some Grasslands, Montane habitats, and others.
  - Comparison with Countryside Survey (CS) 2007
    - Very similar area estimates (within CS 95% confidence limits) for Coniferous Woodland, Freshwater, Built-up Areas & Gardens, Calcareous Grassland.
    - Similar area estimates for Broadleaved woodland, Acid Grassland, Inland Rock.
    - Dissimilar area estimates for Arable & Horticulture, Improved Grassland, Neutral Grassland, Dwarf Shrub Heath, Bog, Montane, and some coastal habitats.
    - Key drivers of differences: differences in definitions and spatial frameworks; spectral confusion; MMU effects; inclusion of boundary/linear features in LCM2007; temporal ranges and multi-year imagery; boundary feature mapping differences; misclassification between grassland types.
  - Change mapping challenges: complex to separate real change from methodological differences across LCM generations; reliance on aggregated classes or Broad Habitat associations discussed as coping strategies.

- UK-wide and country-level patterns
  - UK-level: over half the UK in intensive land use (Arable & Horticulture + Improved Grassland) or Built-up Areas; woodlands ~12% (split between Broadleaved and Coniferous).
  - Country-level variation: England highest intensive land use; Scotland shows more Coniferous Woodland and larger semi-natural and montane areas; NI and Wales show intermediate patterns with regional nuances.
  - Fen, Marsh & Swamp: large differences with CS due to mosaic nature and small patch sizes; many Fen areas mapped as Rough Grassland or Acid Grassland in LCM2007.

- Applications and uses
  - Habitat monitoring, biodiversity assessment, landscape planning, ecosystem service analyses, carbon accounting, and catchment management.
  - Basis for policy evaluation, habitat connectivity analyses, and cross-country comparisons.
  - Provides a common UK-wide spatial structure to support consistent future monitoring and change detection.

- Limitations and considerations for users
  - Spectral confusion and heavy reliance on KBEs mean some habitats (notably upland, mosaic landscapes) should be treated with caution.
  - Minimum mapping unit (MMU) excludes many small patches, potentially underrepresenting fine-scale features.
  - Differences in spatial frameworks between CS and LCM2007 affect areal accuracy and change detection; cross-walking via Broad Habitat Association (BHA) can aid interpretation.

- Data access and usage guidance
  - 1 km rasters accessible through CEH Information Gateway; full vector and 25 m rasters available on request under licence; licensing fees may apply.
  - The parcel-level metadata enables users to assess local data quality and the influence of KBEs; a probabilistic, flexible validation approach is recommended for site-specific applications.

- European context and future directions
  - LCM2007 supports European-scale reporting (e.g., Corinthine/Corine linkage) and sits within a broader European monitoring framework.
  - The report emphasizes integrating multiple data streams (EO, field surveys, LiDAR, soils, climate) for robust, policy-relevant land information systems and improved change detection.

- Key takeaways for analysts
  - LCM2007 delivers UK-wide, parcel-based land cover with improved integration to national frameworks and a suite of derived raster products.
  - Expect strong class-specific performance for certain habitats but notable variability across others due to spectral complexity and scale differences.
  - The Knowledge-Based Enhancements are central to thematic resolution but require user validation for high-stakes applications.
  - Use aggregated or Broad Habitat associations to interpret mismatches with Countryside Survey and for robust change interpretation.
  - Leverage parcel-level metadata to tailor validation and uncertainty assessment to your locality and use case.