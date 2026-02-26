# Final Report for LCM2007 - the new UK land cover map

## Summary of key points
- LCM2007 is the first continuous parcel-based UK land cover map, produced as part of the Countryside Survey 2007.
- It uses a robust spatial framework derived from national cartography (OS MasterMap and LPS) to create parcel-based land cover with 23 classes mapped to Broad Habitats; available as vector (parcels) and raster products (25 m and 1 km).
- Knowledge-based enhancements (KBE) refine spectral classifications, with extensive metadata capturing processing history and confidence.
- Three comparisons with Countryside Survey (CS) 2007 show varied agreement across habitats; Grasslands and some mosaics pose the biggest challenges.

## Data and methods
- Spatial framework: parcel-based vector with strong alignment to real-world land units; 25 m and 1 km raster products summarize the same thematic information.
- Classification: spectral data from multi-date imagery ( Landsat TM/ETM+, SPOT, LISS-III, AWIFS) plus post-classification KBEs; minimum mapping unit (MMU) of 0.5 ha.
- Attributes: each parcel includes Broad Habitat (BH), Broad Habitat sub-class (BHSub), FieldCode, KBE history, ProbList (top 5 spectral class candidates with probabilities), and pixel counts (CorePixels).
- Data products: 23 LCM2007 classes (vector), 25 m raster (23 classes), and 1 km raster (percentage and dominant class formats).
- Access: 1 km rasters via CEH Information Gateway; vector and 25 m raster/licensing on request from CEH.

## Validation and accuracy
- Ground reference data collected 2006–2008; 9127 points used for validation.
- Overall accuracy: 83% across LCM2007 classes; accuracy varies by class (e.g., Bog generally high; Neutral Grassland relatively lower due to spectral similarity with other grasslands).
- Validation supports both class-level and aggregate assessments; detailed producer’s and user’s accuracies are provided in the report.

## Comparison with Countryside Survey 2007
- Very similar area estimates: Coniferous Woodland, Freshwater, Built-up Areas and Gardens, Calcareous Grassland (Calcareous Grassland unexpectedly aligns well in some large mapped areas like Salisbury Plain and the South Downs).
- Similar area estimates: Broadleaved woodland, Acid Grassland, Inland Rock.
- Dissimilar area estimates (UK scale): Arable and Horticulture; Improved Grassland; Neutral Grassland; Dwarf Shrub Heath; Bog; Montane Habitats; Fen, Marsh and Swamp; coastal habitats.
  - Reasons include differences in what is classified as Arable/Horticulture, spectral confusion, inclusion of Boundaries/Linear Features in LCM, KBEs affecting grassland classifications, and the mosaic/patchiness of Fen areas.
  - CS patch sizes and spatial structure differ from LCM2007 MMU-driven parcels, influencing area estimates and correspondences.

## UK land cover distribution
- Across the UK, more than 50% of land is intensive (Arable and Horticulture plus Improved Grassland) or Built-up Areas; forests and semi-natural areas account for substantial portions (woodlands ~12% total; mountain, heath, bog; semi-natural grassland).
- England shows the highest level of intensive land use; Scotland hosts the largest share of Coniferous Woodland and the greatest proportion of Mountain/Metas; Northern Ireland and Wales have distinct patterns in grasslands and boundary features.
- Comparison with LCM2000 indicates shifts in Arable and Semi-natural Grassland proportions between the two maps.

## Data products and access
- Vector product: parcels with attributes including area, source images, BH, BHSub, FieldCode, KBE history, ProbList, CorePixels, and Construct.
- Raster products: 25 m (23 classes) and 1 km (dominant and/or percentage cover per class); metadata provided for 25 m and 1 km products.
- Access options: CEH Information Gateway for 1 km data; full vector and 25 m data under licence on request from CEH (licence fees may apply).
- Documentation and metadata enable traceability of processing steps and provenance.

## Change detection and interpretation
- LCM2007’s spatial structure (parcel-based, generalised cartography) differs from previous CEH maps (LCM1990, LCM2000), complicating direct change detection.
- Recommendations for analysts: focus on aggregated classes, use consistent spatial frameworks, and consider re-organising earlier maps into a common real-world units framework for robust change assessment.

## Applications and usage considerations for analysts
- LCM2007 provides a scalable, policy-relevant evidence base for habitat monitoring, landscape planning, biodiversity assessment, and ecosystem service analyses.
- Its vector-based, coast-to-coast UK coverage supports change detection and integration with other national datasets; however, interpretation should account for:
  - Variability in class-level accuracy, especially for grassland and Fen-related habitats.
  - Differences in CS vs LCM2007 methodologies when making cross-dataset comparisons.
  - Spectral confusion and boundary-related effects in Arable/Horticulture and Grassland classifications.
  - The need for context-specific validation using the ProbList and KBE history for targeted analyses.

## Data quality, limitations, and cautions
- No absolute truth in geography; map quality is use-case dependent. The parcel-level metadata enables targeted quality checks.
- Broad Habitat associations (BHAs) provide a structured framework to interpret correspondences, especially for complex mosaics (e.g., Bog, Dwarf Shrub Heath, Montane Habitats).
- Users should apply their own validation, potentially with high-resolution imagery, and use fuzzy categorisations (plausible/probable/possible) to bound accuracy expectations.

## European context and links
- LCM2007 contributes to European land cover assessment efforts (e.g., Corine Land Cover) and links to pan-European datasets like LUCAS; European-level data collaboration supports broader policy and research objectives.

## Appendix and validation approach
- Bespoke validation emphasizes fit-for-purpose accuracy and highlights the value of parcel-level metadata for targeted quality assessment and custom validation workflows (e.g., Bayesian-style checks with high/medium probability parcels).