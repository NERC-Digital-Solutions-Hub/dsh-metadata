# Final Report for LCM2007 - the new UK land cover map

- Purpose and scope
  - Introduces LCM2007 as the first UK land cover map with a continental parcel-based (vector) spatial framework, aligned with UK Broad Habitats and supporting 23 land cover classes (mapped to 17 Broad Habitats) plus 25 m raster and 1 km summary products.
  - Aims to support habitat monitoring, biodiversity assessments, landscape planning, ecosystem services, and catchment management; designed for reuse, change detection, and extensive metadata.

- Data sources and knowledge inputs
  - Satellite imagery: Landsat TM/ETM, SPOT-4/5, LISS-3 (23–60 m), AWIFS; 70+ images and composites; two-date summer–winter composites to maximize spectral contrast; timing largely 2005–2008.
  - Ground references and validation: CEH ground-reference points (2006–2008); Countryside Survey (CS) Broad Habitat data (2007) for cross-validation.
  - External spatial data: OS MasterMap Topography, NI equivalents; soils, DEM, coastal and contextual layers; agricultural boundaries; terrain and soil contextual knowledge inputs (KBEs).
  - Knowledge-based enhancements (KBEs): seven automated rules applied post-classification to refine thematic resolution using context like urban boundaries, proximity to coast, terrain, and soils.

- Spatial framework and integration
  - UK-wide integration with GB and NI-specific frameworks; 0.5 ha minimum mapping unit (MMU) for GB; NI augmented with image segments where polygon coverage is sparser; produced as a continuous vector for cross-border consistency.
  - Segmentation and parcel delineation: image segmentation combined with generalized cartography and agricultural boundaries; pre-processing includes cloud masking, atmospheric/topographic correction, and geo-registration.

- Classification and processing approach
  - Parcel-based supervised maximum likelihood classification applied to 37 composites and multiple single-date images, using ground-reference training areas.
  - Outputs per parcel include: Broad Habitat class, probability distribution for top five spectral variants, and a record of processing steps.
  - KBEs applied iteratively to reduce spectral confusion and enhance thematic resolution; approximately 20% of parcels reclassified via KBEs; terrain and soils crucial for distinguishing grassland types and bog/fen/swamp boundaries.
  - Validation and quality assurance: 9127 ground-reference points; overall accuracy around 83%; class-level accuracy varies by habitat type and region.

- Product types and access
  - Vector product: land parcels with 10 attributes documenting processing history and knowledge-based enhancements.
  - Raster products: 25 m resolution (23 LCM2007 classes) and 1 km summary rasters (percent cover and dominant class).
  - Access: 1 km rasters via CEH Information Gateway; full vector and 25 m rasters available under license from CEH (fees may apply).

- Comparative analysis with Countryside Survey (CS)
  - Very similar area estimates (within CS 95% confidence limits) for Coniferous Woodland, Freshwater, Built-up Areas and Gardens, and Calcareous Grassland.
  - Similar area estimates (UK level) for Broadleaved Woodland, Acid Grassland, and Inland Rock.
  - Dissimilar area estimates (UK level) for Arable and Horticulture, Improved Grassland, Neutral Grassland, Dwarf Shrub Heath, Bog, Montane Habitats, and coastal habitats.
  - Key drivers of differences:
    - Differences in habitat definitions and what is classified as Arable/Horticulture vs temporary grass, uncropped land, or boundaries.
    - Spectral confusion and temporal variability across multi-year image sets.
    - Differences in how boundaries and linear features are represented (field-level vs boundary-focused mapping).
    - Grassland category ambiguity (Improved vs Neutral vs Calcareous/Acid) and how KBEs mediate these.
    Fen, Marsh, and Swamp show major discrepancies due to mosaic/niche nature of fen areas and small patch sizes.
  - Implications for interpretation: CS broad habitat abundance and CS-derived 1 km square statistics may align with LCM2007 in some classes but diverge in others; aggregation level and BH/BHA frameworks aid interpretation.

- UK-wide and country-specific patterns
  - UK-wide summary: more than half of land is intensive use (Arable and Horticulture plus Improved Grassland) or Built-up Areas; Scotland features more Coniferous Woodland and montane/heath habitats; England shows high intensification; NI and Wales show substantial grassland and urban components.
  - Reasoned expectation: spatial and biogeographical variation influences correspondence with CS and interpretation of Broad Habitats.

- Change mapping and interpretation
  - Change detection between LCM2007 and earlier CEH maps (LCM1990, LCM2000) is complex due to differences in spatial structure, class definitions, and mapping units; robust change separation requires advanced methods and possibly re-structuring older maps to a common spatial framework.
  - KBEs and segmentation help stabilize spatial patterns, but robust, reliable change detection remains challenging.

- Practical guidance for analysts
  - Use Broad Habitat Associations (BHAs) to interpret correspondences with Countryside Survey outputs; consider aggregating Grassland into a single class if comparability with field surveys is critical.
  - Expect varying class-level accuracy; Grassland and upland habitats present notable challenges due to spectral and patchiness issues.
  - Leverage parcel-level metadata and KBE history to assess the plausibility of class assignments in specific locations.
  - Access licensing: full vector and 25 m rasters require CEH licensing; 1 km rasters are available via the CEH gateway.
  - Use the 1 km rasters for UK-wide modelling and combine with other datasets (meteorology, species distributions) for large-scale analyses.

- Example areas and products (brief)
  - Demonstrative areas illustrate upland, calcareous, urban, arable, fenland, and montane contexts.
  - Vector and raster product suites provided to support a range of analyses—from coarse UK-scale modelling to parcel-level habitat assessment.

- Summary implications for policy and research
  - LCM2007 delivers a consistent, UK-wide, parcel-based land cover framework aligned with Broad Habitats, improving change detection potential and cross-border comparability.
  - It provides essential data for biodiversity surveillance, landscape planning, ecosystem services assessment, and policy support, while acknowledging class-level uncertainties and the need for integrated data (CS, field surveys, and other environmental datasets) for robust interpretation.