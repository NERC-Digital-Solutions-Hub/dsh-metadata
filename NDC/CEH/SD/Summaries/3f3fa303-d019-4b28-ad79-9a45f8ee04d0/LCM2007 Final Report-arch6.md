# Final Report for LCM2007 - the new UK land cover map

- Aims and outputs
  - First continuous parcel-based UK land cover map (LCM2007) with vector and raster products.
  - 23 Broad Habitat land cover classes, plus 10 aggregate products; vector, 25 m raster, and 1 km raster summaries.
  - Vector polygons carry extensive metadata and processing history; aimed at supporting biodiversity, policy, and landscape planning.

- Data sources and spatial framework
  - Spatial framework largely derived from high-detail cartography: OS MasterMap (GB) and LPS Large-scale Vector (NI).
  - External data: agricultural boundaries, urban area boundaries, soils, digital elevation, coastline/shoreline, etc.
  - Minimum mapping units: MMU ~0.5 ha; minimum feature width ~20 m; designed for compatibility with 20–30 m satellite imagery.
  - Rationale: stable spatial structure enables change detection and cross-year comparisons; image segments add spectral detail.

- Data processing workflow
  - Image sources and segmentation
    - Multi-date composites and single-date images from Landsat-5, Landsat-TM, SPOT-4/5, AWIFS as backup.
    - 6-band summer–winter composites to improve contrast between land cover types.
    - Segmentation combines spectral data with cartographic boundaries; segments integrated with OSMM and agricultural boundaries.
  - Pre-processing
    - Cloud masking,Atmospheric correction, geo-registration, topographic correction using NEXTMap NI DEM.
    - Manual edits to address artifacts.
  - Classification
    - Parcel-based supervised maximum likelihood classification across 37 composites and 21 singles.
    - Training data mainly from ground references; iterative refinements;Post-classification manual edits.
  - Knowledge-based enhancements (KBE)
    - Contextual/ancillary data applied to resolve spectral confusion; applied to ~20% of parcels.
    - KBEs include terrain, urban context, coastal proximity, soil type; reclassifications tracked in polygon attributes.
  - Change mapping considerations
    - Complex when comparing LCM1990/2000/2007 due to class definitions and spatial structure; generally not a simple per-pixel change detection.

- Outputs: products and access
  - Vector product: primary product with 10 attributes documenting processing stages and KBE history.
  - Raster products: 25 m resolution with 23 LCM2007 classes; 1 km raster summaries with percentage and dominant-class options.
  - Aggregate classes: 10 aggregated classes for simplified interpretation.
  - Access and licensing
    - 1 km raster data via the CEH Information Gateway.
    - Full vector and 25 m data available on request under license; CEH data portal also referenced.
    - Licensing may apply; some data may be openly accessible.

- Quality assurance and validation
  - Ground reference validation: 9,127 points collected 2006–2008; overall accuracy ~83% across classes.
  - Accuracy varies by class and region; some habitats show higher producer/user accuracies (e.g., conifer woodland, arable land) and others lower (e.g., certain semi-natural grasslands, bogs, montane habitats).
  - Validation approach includes training/testing splits and confusion matrices; KBEs and external data can influence class accuracies.
  - Caveats: spectral confusion remains for grasslands; montane/coastal areas can be challenging; some classes rely heavily on KBEs/soil data.

- Comparison with Countryside Survey (CS) 2007
  - CS provides independent habitat estimates for GB, England, Scotland, Wales, NI.
  - Overall correspondence with CS (UK level):
    - 62% at Broad Habitat level.
    - 76% at Broad Habitat Association level when BHAs are considered.
    - 67% at the aggregate level.
  - Grassland and mosaic issues
    - When grassland variants are collapsed, correspondence improves to ~87–90% in some cases.
  - Capacity for differences
    - Country-level variation; upland/montane habitats contribute to mismatches.
    CS uses field surveys; LCM2007 uses spectral data plus KBEs; differences arise from classification, spatial structure, and patch sizes.
  - Notable areas of discrepancy
    - Arable and Horticulture: CS UK estimate ~46,574–46,090 km2 vs LCM2007 ~63,005 km2; likely due to inclusion of boundary/linear features and temporally variable crops; spectral variability in arable areas causes misclassifications.
    - Fen, Marsh and Swamp: CS estimates much higher than LCM2007 due to mosaic nature and difficulty mapping fen with spectral data; many CS fens appear as Rough Grassland or Acid Grassland in LCM2007.
    - Grassland sub-types (Improved/Neutral/Calcareous) show allocation differences between products.
  - Summary interpretation
    - LCM2007 provides coast-to-coast, consistent  UK-wide coverage and improved spatial structure, but differences with CS reflect definitional differences, spatial representation, and the challenge of mapping fine-scale, mosaicked habitats with spectral data alone.

- Practical implications and recommended uses
  - Supports habitat monitoring, biodiversity planning, and policy development; provides self-serve vector and raster outputs.
  - KBEs and soils/terrain context help achieve higher thematic resolution in complex landscapes.
  - Continuous UK-wide vector improves cross-year/regional analyses and change detection when combined with other data.
  - 1 km rasters enable quick regional assessments; 25 m rasters support local-scale analyses.
  - Use aggregated BH/BHA where appropriate to mitigate class-level accuracy variability.
  - When performing change detection or cross-product comparisons, account for spatial and thematic structural differences; consider reprocessing with common spatial structures if possible.

- Cautions and user guidance
  - Be mindful of class-specific accuracy variability; consult producer’s and user’s accuracy figures.
  Use aggregation to improve reliability for certain applications.
  Grassland and upland interpretations may diverge from field taxonomy; KBEs help but do not fully align with field surveys.
  For licensing and access, check CEH terms; 1 km data often open, full vector/25 m data may require a license.

- Notable validation and validation-friendly features
  - Parcel-level metadata enables users to inspect which KBEs were applied and to what extent.
  - Potential to apply a Bayesian-like informal validation against high-resolution imagery to assess plausibility and to derive upper/lower accuracy estimates with fuzzy categories.

- Appendices and context (highlights)
  - Broad Habitat Association (BHA) rules address mapping of complex transitions (e.g., Bog, Dwarf Shrub Heath, Montane Habitats) to improve cross-product comparability.
  - Discussion of data formats, KBEs, and validation approaches to support robust use of LCM2007 outputs.

- Summary takeaway for data support
  - LCM2007 delivers a high-resolution, coast-to-coast UK land-cover map with rich metadata and multiple data formats suitable for broad to detailed analyses.
  - It introduces a consistent spatial framework and knowledge-based refinements to enhance thematic accuracy, while acknowledging remaining challenges in grassland, fen, and montane classifications when compared to field-based surveys.
  - The dataset is a valuable evidence base for policy and planning, with clear guidance on interpretation, aggregation, and licensing.