# Final Report for LCM2007 - the new UK land cover map

- The UK Land Cover Map 2007 (LCM2007) delivers the first continuous parcel-based (vector) land cover map for the UK, plus derived raster products at 25 m and 1 km resolutions. It supports nationwide habitat monitoring, biodiversity assessment, landscape planning, and policy analysis, with strong alignment to Broad Habitat (BH) and Biodiversity Action Plan (BAP) frameworks. The spatial framework is based on detailed national cartography, enabling better integration with other national datasets and future change detection.

## Data architecture and products

- Parcel-based vector product
  - Land parcels are polygons with rich metadata and a history of processing steps.
  - Attributes include area, input images, Broad Habitat (BH), Broad Habitat Sub-class (BHSub), FieldCode, KBE history, and a ProbList of the top spectral class candidates.
  - 23 LCM2007 classes mapped to 17 BH categories; 10 Aggregate classes used for higher-level analysis.
  - Knowledge-Based Enhancements (KBEs) are applied post-classification to improve thematic resolution and manage spectral confusion.
- Raster products
  - 25 m resolution: 23 LCM2007 classes.
  - 1 km resolution: two formats
    - Percentage cover per 1 km cell for each class.
    - Dominant class per 1 km cell.
- Data access
  - 1 km rasters available via the CEH Information Gateway.
  - Full vector and 25 m raster data available on request from CEH; licensing may apply.
- Data framework
  - Spatial structure derived from OS MasterMap and LPS Large-scale Vector; designed to be reusable for future monitoring and cross-border analyses.
  - Minimum mappable unit and segmentation approach (core pixels) designed to maximize classification reliability.

## Data sources and processing workflow

- Satellite imagery
  - Landsat-5 TM, Landsat-7 ETM+, SPOT-4/5, and IRS AWIFS/LISS-III; summer-winter composites preferred.
  - Approximately 91% of the UK mapped from multi-date composites; remaining areas from single-date imagery and manual hole filling.
- Ancillary data
  - Ground reference points (CEH) for training/validation; Countryside Survey Broad Habitat data for comparison.
  - External data: national cartography (OS MasterMap, LPS), agricultural boundaries, urban area data, soils, digital elevation models (DEMs), etc.
- Spatial frameworks
  - GB framework based on generalized OS MasterMap topography, refined with agricultural boundaries and image segments for scale consistency.
  - NI framework built from LPS Large-scale Vector and augmented with image segments; agricultural boundaries less integrated due to landscape differences.
- Classification and KBEs
  - Parcel-based supervised maximum likelihood classification using training data from ground references; iterative refinement until accuracy targets are met.
  - Seven automated KBEs to resolve spectral confusion and enhance discrimination (urban context, coastal proximity, terrain/soil, water, etc.), applied sequentially; changes recorded in vector attributes to enable reversion if needed.

## Validation, comparisons, and interpretation

- Validation
  - Ground reference points: 9127 used; overall Producer/User accuracy around 83% for LCM2007 classes; class-level performance varies (certain grassland and upland classes more challenging due to spectral ambiguity).
- Countryside Survey (CS) comparisons
  - Analyses include CS 2007 1 km squares and national CS extent estimates.
  - Agreement with CS varies by Broad Habitat; grasslands are particularly problematic due to one-to-many relationships with BH and the need for a Broad Habitat Association (BHA) cross-walk to improve interpretability.
  - LCM2007 vs CS: Arable and Horticulture areas can diverge due to temporal image requirements, boundary feature mapping, and spectral variability; Fen/Marsh/Swamp areas show large differences because fen is a mosaic of land-cover types and patch sizes are often below the mapping unit.
  - Montane and coastal habitats are poorly represented in CS, contributing to differences.
- Change mapping considerations
  - Changing definitions and spatial structures across LCM1990, LCM2000, and LCM2007 complicate direct change mapping.
  - Spectral confusion and different spatial frameworks can obscure real habitat changes; aggregation to BH/BHA levels can help mitigate interpretive differences.
- UK-wide and country-level context
  - LCM2007 indicates the UK is over half in intensive land use (Arable/Horticulture and Improved Grassland) or built-up areas; Scotland shows more Coniferous Woodland and Montane habitats; England shows substantial intensive land use; NI/Wales show similar but regionally distinct patterns.
  - LCM2007 provides a consistent UK-wide framework suitable for cross-border analyses and longitudinal monitoring when combined with other data.

## Change detection, limitations, and interpretation guidance

- Limitations
  - The LCM2007 spatial framework is not a direct reflection of land use, but land cover; some land-use interpretations require caution.
  - Certain habitat classes (e.g., Fen/Marsh/Swamp, Neutral Grassland, Montane) exhibit higher uncertainty and may require user-driven KBEs or supplementary data for refinement.
  - Boundary and linear features (hedgerows, narrow streams) are often below MMU/remote-sensing detectability and may be represented differently in CS vs LCM2007.
- Implications for data users
  - For robust analyses, use aggregated BH or BHAs when class-level matches are uncertain.
  - Leverage parcel-level KBEs and ProbList to assess the plausibility of classifications at high spatial resolution; consider informal Bayesian validation approaches with high/moderate confidence categories.

## Implications for Data Leaders and data strategy

- Strategic value
  - LCM2007 provides a robust, reusable, and extensible UK-wide land cover dataset aligned with BH/BAP frameworks, suitable for habitat monitoring, biodiversity assessment, landscape planning, and policy support.
  - The continuous UK-wide vector framework supports seamless integration and change detection across boundaries, enabling longitudinal studies and cross-border collaboration.
- Governance, metadata, and provenance
  - Rich parcel-level metadata, including KBE history and probability lists, enhances transparency, reproducibility, and reuse.
  - Strong emphasis on metadata traceability and documentation of processing steps, which is critical for auditability and governance.
- Collaboration and benchmarking
  - Cross-walk with Countryside Survey (BH/BHA associations) provides a framework for benchmarking national datasets against field surveys.
  - Potential to improve interpretation of grassland and fen-related habitats by incorporating additional data sources and knowledge-based rules.
- Access, licensing, and openness
  - Data access via CEH gateways with licensing considerations; balance openness with commercial or sensitive-use restrictions as needed.
  - Licensing strategies should anticipate downstream use, reuse rights, and cross-border sharing within a data community.
- Validation and uncertainty management
  - Maintain ongoing validation efforts and uncertainty quantification at the class level, with attention to high-uncertainty classes (e.g., Neutral Grassland, certain upland types).
  - Use KBEs and the ProbList to inform uncertainty assessments and support transparent decision-making.

## Key takeaways for Data Leaders

- Prioritize governance around rich metadata, provenance, and knowledge-based enhancements to support transparent reuse and reproducibility.
- Leverage the continuous UK-wide vector framework to enable cross-border data integration, change detection, and policy-relevant analyses.
- Use the Broad Habitat Association cross-walks with Countryside Survey to align national datasets and improve interpretability across habitats.
- Plan for ongoing validation and explicit uncertainty quantification, especially for grassland, fen, montane, and coastal classes.
- Develop data access and licensing strategies that balance openness with necessary restrictions for sensitive or commercial uses.
- Recognize the value of integrating LCM2007 with other data sources (e.g., CS, European datasets) to build a holistic evidence base for policy areas including biodiversity, climate, water, and landscape planning.