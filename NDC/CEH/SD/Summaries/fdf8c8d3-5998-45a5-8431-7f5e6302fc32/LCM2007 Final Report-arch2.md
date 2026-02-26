Final Report for LCM2007 - the new UK land cover map

## Overview
- First continuous parcel-based UK land cover map (LCM2007) with 23 land cover classes, mapped to 17 Broad Habitats (BHAs).
- UK-wide vector data (~10 million land parcels; GB ~8.6 million, NI ~0.9 million); outputs include a 25 m raster and 1 km rasters.
- Data sources combine Landsat TM5, IRS LISS3, SPOT-4/5, with AWIFS as backup; multi-date summer–winter composites used to maximise accuracy.
- Overall accuracy validated against field data: 83% (class performance varies).

## Data products and structure
- Vector product: parcel-based polygons with 10+ attributes documenting processing steps, KBE history, and classification metadata.
- Raster products:
  - 25 m resolution raster with 23 LCM2007 classes.
  - 1 km rasters: (a) percentage cover per class, and (b) dominant class per pixel.
- Coverage continuity: UK-wide vector layer (GB and NI maintained separately); nine processing chunks with overlap handling to maintain consistency.

## Data sources and production methodology
- Image data: 20–30 m resolution from Landsat TM5, IRS LISS3, SPOT-4/5; AWIFS as needed.
- Composites: 91% of UK classified from two-date summer–winter composites; remainder from single-date imagery or hole-filling.
- Spatial framework: OS MasterMap (GB) and LPS Large-scale Vector (NI); 0.5 ha minimum mapping unit; integration of agricultural boundaries to improve delineation.
- Image processing: pre-processing (cloud masking, atmospheric/topographic corrections); segmentation combined with land parcels and agricultural boundaries.
- Classification: parcel-based supervised maximum likelihood using ground reference points; 37 composites and 21 single-date images; knowledge-based enhancements (KBEs) applied to ~20% of parcels to resolve spectral confusion; coastal/terrain/urban/soil rules also used.
- QA/validation: 9,127 ground reference points; overall accuracy 83%; class accuracies vary (e.g., bog/arable/high, some grassland types variable).

## Change and validation against Countryside Survey (CS)
- CS 2007 comparisons show variable agreement across BHAs.
- Grassland classifications are particularly challenging due to one-to-many mappings between grassland types and BHAs; Broad Habitat Association rules (BHAs) added to improve comparability.
- Fen, Marsh and Swamp areas differ dramatically between CS 2007 and LCM2007 due to mosaic nature and small patch sizes; many CS fen areas map to Rough Grassland or Acid Grassland in LCM2007.
- General conclusion: LCM2007 provides coast-to-coast UK coverage with policy-relevant consistency, but differences in spatial structure and definitions mean careful interpretation when comparing to CS.

## UK Land Cover distribution and country differences
- Over half of the UK is intensive land use (Arable and Horticulture + Improved Grassland) or Built-up areas.
- Woodland ~12% UK-wide (broadleaved and coniferous); remaining areas semi-natural (coastal, semi-natural grassland, montane, etc.).
- Country-level patterns vary: England highest intensive land use; Scotland has more coniferous woodland and montane/semi-natural areas; NI/Wales show different composition—reflecting regional land use histories.

## Applications for environmental monitoring
- Provides a consistent, policy-relevant base for monitoring habitat extent, fragmentation, and ecosystem services.
- Supports biodiversity policy implementation (e.g., habitat networks, connectivity), landscape planning, and catchment management.
- When used with additional data (e.g., CS, environmental models, LiDAR), enables robust assessments of environmental health and policy performance over time.

## Access, licensing, and data accessibility
- 1 km raster data accessible via the CEH Information Gateway.
- Full vector and 25 m raster data available on request; licensing may apply and fees may be charged.
- Contact CEH data portal or spacialdata@ceh.ac.uk for details.

## Applications to policy and monitoring (Analysts’ perspective)
- A standardized UK frame for evaluating habitat extent and change, enabling cross-country comparisons within policy contexts.
- Supports assessment of habitat connectivity and ecosystem services at multiple scales.
- The parcel-level metadata (KBE history andProbList) allows users to validate classifications locally and quantify uncertainty in targets and indicators.
- Encourages data integration: LCM2007 can be combined with climate, soils, hydrology, and socio-economic data to monitor environmental health and policy outcomes.

## Key figures and outputs
- 23 LCM2007 classes; 17 Broad Habitats; ~10 million UK land parcels (GB ~8.6 million; NI ~0.9 million).
- 91% UK classified from multi-date composites; 83% overall accuracy; 1 km rasters, 25 m raster, and vector products available.
- BHAs and Broad Habitat associations implemented to improve cross-map comparisons and interpretation.

## Example areas and visualization
- The report includes example areas across uplands, calcareous grasslands, urban areas, arable/fenland, and montane regions to illustrate LCM2007 performance in diverse landscapes.

## Bespoke validation and uncertainty management
- Acknowledges no absolute truth in geography; recommends fit-for-purpose validation.
- Proposes informal Bayesian-style validation using high-resolution imagery to classify parcel-level plausibility and produce upper/lower accuracy estimates.
- Appendix details a framework for bespoke validation and usage guidance.

## Broad Habitat Association (BHA) framework
- Provides class-by-class rules for cross-map correspondence (e.g., Bog ↔ Dwarf Shrub Heath, Acid Grassland; Montane ↔ Bog/Heath; Water classes ↔ CS water classes).
- Addresses transitional mosaics, mosaicked boundaries, and spatial structure differences between LCM2007 and CS.

## Access and data sources (European context and links)
- LCM2007 links to European datasets (Corine, LUCAS) and European-scale imaging data (IMAGE2006) to support pan-European environmental assessment.
- Emphasizes integration with broader data systems for comprehensive land information and policy-relevant monitoring.

Note: This summary highlights the aspects most pertinent to Analysts Monitoring the Environment: standardized data products, data quality, interoperability with other datasets, monitoring applications, and policy-relevant outputs, along with practical considerations for data access and uncertainty.