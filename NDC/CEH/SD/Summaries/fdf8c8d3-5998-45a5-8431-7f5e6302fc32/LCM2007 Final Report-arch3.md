# Final Report for LCM2007 - the new UK land cover map

## Aim and scope
- Provide a national land cover map to support policy scrutiny, habitat monitoring, biodiversity assessments, and landscape planning across the UK.
- Deliver a robust, policy-relevant base for monitoring change and informing future decisions; enable cross-country comparisons and integration with other data sources.

## Data sources and spatial framework
- UK-wide spatial framework built from generalised OS MasterMap (GB) and NI equivalents, refined with agricultural boundaries and image segments.
- External data include national cartography, digital elevation models, soils, and urban boundaries to support knowledge-based enhancements (KBEs) and classification.
- Two separate data infrastructures for GB and NI to maintain continuous UK coverage.
- Satellite data: multi-sensor composites ( Landsat, SPOT, AWIFS, with backup assignments); date combinations chosen to maximize contrast between land-cover types.
- Ground truth and validation references: CEH ground reference points and Countryside Survey (CS) Broad Habitat areas for 2007 comparison.

## Production approach and data processing
- Builds on earlier maps with segmentation-driven classification; minimum mapping unit of 0.5 ha; minimum feature width of 20 m.
- Image pre-processing includes cloud masking, atmospheric/topographic correction, georegistration, and multi-date compositing.
- Segmentation combines image segments with OS MasterMap parcels and agricultural boundaries to better delineate spectral regions.
- Parcel-based maximum likelihood classification using field training data; manual edits and targeted hole-filling.
- Seven automated knowledge-based enhancements (KBEs) applied sequentially (e.g., terrain, soil, coastal proximity, urban context) to resolve spectral confusion and improve thematic resolution; KBEs reclassify a portion of parcels.
- Extensive metadata and processing steps are stored with the vector product for traceability.
- Output products: a main vector product (with 10 processing attributes), a 25 m raster with 23 LCM2007 classes, and 1 km raster products (percentage cover and dominant class); UK-wide coverage as separate GB and NI vector layers.

## Classification and knowledge-based enhancements
- 23 land cover classes mapped, aligned with Broad Habitats (BH) with some adjustments; 17 terrestrial Broad Habitats represented.
- Grassland differentiation uses KBEs to separate Rough from Neutral/Calcareous/Acid Grasslands, informed by soil and altitude data.
- Recognises limitations where optical data alone cannot fully disambiguate classes; KBEs improve accuracy but do not fully replace field verification.

## Product specification and data products
- LCM2007 maps land cover (not land use) with MMU 0.5 ha.
- Vector product includes detailed processing attributes; 25 m raster with 23 classes; 1 km rasters (percentage or dominant class).
- Access: 1 km rasters via CEH Information Gateway; full vector and 25 m data available on request under licence (fees may apply).

## Quality assurance, validation, and accuracy
- Ground validation yields an overall accuracy around 83% for LCM2007 classes; class-level accuracy varies.
- Validation accounts for polygon-level vs ground-reference alignment; acknowledges potential misalignment in natural/semi-natural areas.
- Change mapping between LCM2007 and earlier maps is complex due to class and spatial/temporal differences; robust attribution of real change remains challenging.

## Comparison with Countryside Survey (CS) 2007
- CS provides 591 1 km squares for broad habitat validation; CS area estimates benchmark UK habitat extents.
- Broad Habitat correspondence is variable across BHs; notable differences arise in grassland and fen/marsh/swamp categories.
- Arable and Horticulture area in CS often closer to CS upper limits, while LCM2007 tends to map higher estimates for arable areas due to spectral variability and boundary feature inclusion.
- Spectral confusion and boundary/linear feature mapping contribute to dissimilarities; grassland is particularly challenging due to one-to-many relationships with BHs.
- Montane and coastal habitats are poorly represented in CS, contributing to discrepancies; Grassland generalisation (collapsing types) improves CS-LCM correspondence in some analyses.
- England, Scotland, Wales, and Northern Ireland show country-level differences in correspondences reflecting habitat composition and mapping challenges.

## Access, licensing, and governance
- Primary 1 km raster data accessible via CEH Information Gateway; full vector and 25 m datasets available on request under licence (fees may apply).
- Governance and licensing considerations are important for cross-agency monitoring and data reuse.

## Implications for monitoring frameworks
- LCM2007 provides a robust, policy-relevant base for national and sub-national habitat monitoring, biodiversity assessments, ecosystem services evaluation, and landscape planning.
- Integration with Countryside Survey data offers opportunities for cross-validation, though differences in spatial and thematic structures must be carefully managed when comparing or combining outputs.
- Knowledge-based enhancements (KBEs) improve thematic resolution where spectral signals are insufficient, but users should account for potential biases in upland or mosaic landscapes.
- Strong emphasis on metadata, data provenance, and data governance supports transparency, reproducibility, and long-term monitoring continuity.
- European and national links (e.g., Corine Land Cover) are facilitated by the LCM2007 framework, supporting broader policy and monitoring integration.

## Key takeaways for monitoring practitioners
- LCM2007 delivers coast-to-coast UK land cover mapping with explicit metadata, traceable processing steps, and multiple data products suited to modelling, policy evaluation, and habitat connectivity analyses.
- The approach highlights trade-offs between spectral classification, spatial structure, and ground-truth data; careful interpretation is required when comparing with field surveys or alternative datasets.
- For effective monitoring, consider combining LCM2007 outputs with CS (and other) datasets, use Broad Habitat associations to interpret cross-product correspondences, and apply KBEs judiciously while remaining aware of potential biases in certain landscapes.
- Ongoing emphasis on data governance, metadata completeness, and accessible data-sharing practices is essential for sustained policy-relevant monitoring.