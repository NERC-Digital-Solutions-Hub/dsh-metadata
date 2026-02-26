# Final Report for LCM2007 - the new UK land cover map

- Purpose and value for analysts
  - Introduces the first continuous parcel-based (polygon) UK land cover map (LCM2007) derived from national cartography to support consistent environmental monitoring and change detection.
  - Provides a standardized, repeatable evidence base for policy-relevant assessments of habitat extent, landscape planning, connectivity, and ecosystem services across the UK.
  - Combines a high-resolution vector parcel framework with raster outputs for flexible analyses and reporting.

- Data sources and spatial framework
  - Satellite imagery: Landsat TM5, IRS-LISS3, SPOT-4/5 (20–30 m resolution); AWIFS as backup; 6-band 2-date summer–winter composites plus some single-date imagery.
  - External cartographic and environmental layers: OS MasterMap topography (GB), OSNI/LPS (NI), agricultural boundaries, DEMs, soils, urban datasets.
  - Spatial framework specifics
    - Great Britain: OS MasterMap boundaries generalized to MMU of 0.5 ha; integrated with agricultural boundaries and image segments to form parcel-based units.
    - Northern Ireland: LPS boundaries polygonised from lines; integration with image segments; some boundaries included in GB but not NI due to landscape differences.
  - Image segmentation and integration: segmentation of multi-date imagery combined with generalized cartography to create a UK-wide segmentation framework, aligned with boundaries and spectral heterogeneity within fields.
  
- Production workflow and processing
  - Image preprocessing: cloud/shadow masking, atmospheric correction, georegistration, topographic correction; target RMSE < 0.3 pixel.
  - Segmentation: 60 composites segmented using winter NIR, summer red, summer MIR bands to produce segment-based polygons; integration with OSMM/LPS boundaries and agricultural data.
  - Classification: parcel-based supervised maximum-likelihood classification of 37 composites and 21 single-date images into 23 LCM2007 classes; training from ground reference points; iterative manual edits.
  - Post-processing: hole-filling with Landsat-7 ETM+ data; manual edits for rare classes or occluded/shadowed areas.
  - Quality assurance: logging of image quality/parameters; field validation used to tune classifications.
  
- Knowledge-based enhancements (KBE)
  - Seven automated KBEs to reduce spectral confusion and improve thematic resolution; applied sequentially to converge toward likely land-cover truth.
  - KBEs use context such as urban boundaries, coastal proximity, terrain, soils, and coastal/offshore rules; maintain traceability by preserving original spectral classification in polygon attributes.
  - Terrain and soils rules are particularly important for distinguishing various grasslands, bogs, montane habitats, etc.
  - KBEs can be suppressed or reversed; manual inspection and corrections are used where KBEs may misclassify.

- Outputs and data products
  - 23 LCM2007 land cover classes mapped to 17 Broad Habitats (BHs).
  - Vector product: parcels with 10 attributes documenting processing steps (Construct, ProbList, KBE history, etc.) and a CorePixels/TotalPixels framework; includes Broad Habitat sub-classes (BHSub) for enhanced tracing.
  - Raster products:
    - 25 m resolution: 23 LCM2007 classes.
    - 1 km resolution: two summary formats per location — (A) percentage cover by each class, (B) dominant class per 1 km pixel.
  - Minimum mapping unit: 0.5 ha.
  - Metadata-rich dataset to support traceability and reproducibility; UK-wide continuity with country-specific processing chunks.
  - Access and licensing: 1 km rasters via CEH Information Gateway; full vector and 25 m rasters/licensing on request from CEH (licence fees may apply).

- Accuracy, validation, and quality assurance
  - Ground reference validation: 9,127 points used; overall accuracy of 83% across classes; class-specific accuracies vary.
  - Key accuracy issues and explanations
    - Arable and Horticulture: differences in what is classified, spectral confusion, and boundary/linear features included in LCM2007’s area.
    - Improved/Neutral Grassland: discrepancies largely due to how neutral grassland signatures are allocated between classes.
    - Dwarf Shrub Heath and Bog: differences due to allocation between habitats; montane and coastal habitats show varying performance.
    - Fen, Marsh and Swamp: large discrepancies due to mosaic and small patch sizes; CS often records Fen as Rough Grassland or Acid Grassland in LCM2007, suggesting potential KBEs to reallocate some of these areas.
  - Counterpart comparisons
    - Countryside Survey (CS) 2007 used as independent validation at multiple levels (CS squares and Broad Habitat totals); LCM2007 shows varying agreement by Broad Habitat and country.
    - Grassland and upland mosaics are primary sources of mismatch; applying Broad Habitat Association (BHA) rules improves correspondences at aggregated levels.
  - Implications for analysts
    - LCM2007 provides a robust, repeatable base, but class-level accuracy varies; bespoke local validation recommended.
    - Use aggregated classes (e.g., BHAs) for improved comparability with CS and other datasets.
  
- Comparison with Countryside Survey 2007 (CS07)
  - Broad Habitat correspondence GB-wide around 62% (CS07 vs LCM2007) when assessed at the Broad Habitat level; higher (~76%) when using Broad Habitat Association rules.
  - Arable and Horticulture alignment is strong at 1 km CS squares, but CS estimates of Broad Habitat extent are generally lower or higher than LCM2007 depending on the metric used.
  - Fen, Marsh and Swamp shows order-of-magnitude differences due to patchiness and classification challenges; many CS Fen patches map to Rough Grassland or Acid Grassland in LCM2007.
  - Country-level variation reflects habitat-specific correspondences and the spatial structure of maps and field surveys.
  
- Implications for environmental monitoring
  - LCM2007 delivers a standardized UK-wide evidence base for tracking land cover and Broad Habitats over time, supporting habitat extent, connectivity, and ecosystem-service assessments.
  - The vector-plus-raster combination supports both detailed mapping and broad-scale summaries; caution advised for class-level application in local analyses.
  - The dataset enables policy-oriented analyses (habitat networks, Natura targets, catchment-scale assessments) and cross-country comparisons.
  
- Example areas (illustrative use cases)
  - Demonstrates performance across upland montane habitats, calcareous grasslands, urban parks, and fenland areas.
  - Illustrates areas with mixed or transition habitats and the interaction between spectral signals and KBEs.

- Change detection and future directions
  - LCM2007 provides a framework to monitor change over time, but comparisons with earlier CEH maps require sophisticated methods due to differing spatial structures and classifications.
  - Future work could involve re-aligning earlier CEH maps to a common spatial structure based on real-world land-use units and developing enhanced KBEs to better allocate mosaic habitats (e.g., Fen, Marsh and Swamp).
  - LCM2007 serves as a backbone for integrating multi-source data (EO, ecological modelling, LiDAR, ground surveys) for policy-relevant monitoring.

- Bespoke validation and data quality approach
  - Emphasizes fit-for-purpose validation using parcel-level metadata, KBE history, and probability lists to assess the likelihood of class assignments location-by-location.
  - Proposes a two-part validation approach (high-probability vs. moderate-probability parcels) and a fuzzy, Bayesian-like qualitative assessment, supported by a Python-based toolkit.

- Broad Habitat Association (BHA) insights
  - Provides class-by-class rules to better align LCM2007 classifications with Countryside Survey interpretations, acknowledging ecological continua and mosaic habitats.
  - Examples include Bog, Dwarf Shrub Heath, Montane Habitats, Built-up Areas and Gardens, Fen, Marsh and Swamp, Rough Grassland, Water, and tidal area considerations.
  - Rules are designed to be reciprocal where appropriate and to reflect known habitat adjacencies and transition zones.

- Data access, licensing, and documentation
  - 1 km raster data available via CEH Information Gateway.
  - Full vector and 25 m raster products available under licence on request from CEH; licensing fees may apply.
  - Documentation and metadata accompany products to support reuse and reproducibility.

- Context and European links
  - LCM2007 contributes to European-scale assessments (e.g., Corine Land Cover) by providing a UK-derived vector product that can be generalized for pan-European datasets.
  - Built upon IMAGE2006 SPOT/IRS data and European-level monitoring initiatives, enabling integration with wider European land-cover products.

- Final takeaway for analysts monitoring the environment
  - LCM2007 delivers a high-resolution, UK-wide, parcel-based land cover map with extensive metadata, standardization, and QA processes, enabling robust, policy-relevant environmental monitoring and change detection across the four UK countries.
  - While overall accuracy is strong, users should apply caution at the class level, leverage Broad Habitat aggregations for comparability, and consider bespoke local validation when applying LCM2007 outputs to local decisions.