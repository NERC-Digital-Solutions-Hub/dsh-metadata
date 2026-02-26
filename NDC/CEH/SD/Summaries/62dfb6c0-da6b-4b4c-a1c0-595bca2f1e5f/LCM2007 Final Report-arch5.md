Final Report for LCM2007 - the new UK land cover map

# Overview

- LCM2007 is the first UK-wide, continuous vector land cover map (parcel-based) for 2007, developed for Countryside Survey 2007.
- It integrates detailed national cartography (OS MasterMap for GB and LPS vector data for NI) with multi-temporal satellite imagery to produce both high-resolution vector and raster products (25 m and 1 km).
- Core outputs:
  - Vector: parcels with 10 processing/derivation attributes (including ProbList and KBE history).
  - Raster: 25 m with 23 LCM2007 classes; 1 km rasters with class percentages and dominant class.
- Spatial framework: nine GB/NI chunks merged into a seamless UK layer; minimum mappable unit 0.5 ha (MMU 0.5 ha), with segmentation and agricultural boundaries integrated to improve delineation.

# Data Structure, Provenance, and Access

- Vector data attributes:
  - Core attributes include Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, KBE (knowledge-based enhancements), ProbList (top five spectral class probabilities), Construct, ALT, CM, and other lineage metadata.
  - ProbList provides the five closest spectral variants; KBE history documents post-classification changes.
- Raster products:
  - 25 m: 23 LCM2007 classes.
  - 1 km: two summaries per pixel (percentage cover per class and dominant class).
- Data provenance and traceability:
  - Full processing chain documented; metadata-rich vectors support reproducibility and change tracking (including ProbList and KBE history).
- Access and licensing:
  - 1 km raster data available openly via CEH Information Gateway.
  - Full vector and 25 m raster data available on request from CEH (licensing may apply and fees may be charged).

# Methods: Image Processing, Segmentation, Classification and KBEs

- Pre-processing and image work:
  - Cloud/shadow masking, atmospheric correction, geo-registration (high precision), and topographic correction.
  - 34 two-date summer–winter composites (plus some single-date data) spanning Landsat, SPOT, LISS-3, and AWIFS sources.
- Spatial/frame construction:
  - GB frame built from OS MasterMap refined with agricultural boundaries; NI frame from LPS vector data with segmentation overlays.
  - Generalisation reduces polygon density to a practical MMU, forming the parcel-based framework.
- Segmentation and classification:
  - Image segmentation produces a segment-based vector framework integrated with cartography and boundaries.
  - Parcel-based supervised maximum likelihood classification using multiple date composites; iterative reclassification with ProbList-guided refinement.
  - Rare classes may receive manual edits to reduce misclassification.
- Knowledge-based enhancements (KBE):
  - Seven sequential KBEs applied to resolve spectral confusion and sharpen thematic resolution, drawing on urban context, terrain, soils, coastal proximity, and other contextual data.
  - KBEs reclassify around 20% of parcels; all KBEs are fully documented in the dataset; original spectral classification remains accessible via ProbList.

# Knowledge Base and Validation

- KB structure:
  - Contextual rules covering urban, coastal, terrain/soil, water, and other factors; designed to improve classification in challenging mosaics and transitional areas.
- Validation data:
  - Ground truth: 9,127 points used for validation; overall accuracy around 83%, with class-specific variations.
  - Validation acknowledges spatial misalignment and mixed-class polygons as sources of error.

# UK Coverage and Data Delivery

- UK-wide continuity:
  - LCM2007 is provided as a continuous UK vector product with GB and NI databases merged.
  - Nine processing chunks defined to organise and optimize classification, with overlaps resolved for improved accuracy.
- Outputs and access:
  - Vector: 10 attributes per polygon describing processing and classification lineage.
  - 25 m raster and 1 km rasters available; 1 km rasters via CEH gateway; vector and 25 m data on request (licensing may apply).

# Data Quality, Uncertainty, and Validation Insights

- Overall and class-level accuracy:
  - Broad Habitat comparisons with Countryside Survey (CS) show varying agreement by habitat type; some classes exhibit higher Producer/User accuracy than others (e.g., Bog high Producer, Neutral Grassland lower User accuracy).
  - The comparison is affected by CS’s patch-based nature, MMU differences, and spectral/seasonal differences between CS field surveys and LCM2007 imagery.
- Key uncertainty drivers:
  - Spectral confusion, temporal range of imagery (multi-year composites), and boundary features below the MMU being treated differently in CS vs LCM2007.
  - Grassland (Arable, Improved, Neutral, etc.) classifications show notable discrepancies due to spectral variability and how temporary grasses vs arable land are represented.
  - Fen, Marsh, and Swamp differences stem from mosaics and small patch sizes, leading to large UK-scale discrepancies.
- Broad Habitat Association (BHA):
  - BHA rules help map one-to-many CS-LCM correspondences, clarifying interpretability in mosaicked or transitional landscapes.
- Absolute limitations:
  - Some categories (e.g., upland montane mosaics, certain coastal/insular habitats) remain challenging due to spectral similarity and boundary delineation.
  - CS data are not a perfect ground truth for direct one-to-one mapping; both CS and LCM2007 provide complementary perspectives.

# Comparisons: Countryside Survey 2007

- 1 km square comparisons:
  - Good correspondences for Arable/Horticulture, Coniferous Woodland, Freshwater, Urban, Saltmarsh, among others; but overall Broad Habitat extents show larger differences (LCM2007 often higher in Arable and Horticulture).
- UK-wide vs country-level patterns:
  - England, Scotland, Wales show regional variations in correspondence, reflecting habitat composition and survey geometries.
  - Fen, Marsh and Swamp and Montane habitats show substantial discrepancies due to small patch sizes and mosaic nature.
- CS-derived extents vs LCM2007:
  - CS 95% confidence limits used to judge whether LCM2007 estimates fall within expected ranges; some LCM2007 extents fall within CS bounds for certain broad habitats, others exceed or fall below bounds, highlighting methodological differences.
- Broader interpretation:
  - LCM2007 provides a contemporary, repeatable, and scalable framework for national policy and landscape monitoring, while CS offers ground-truth-like field-based context useful for uncertainty analysis.

# Data Governance and Stewardship Implications

- Provenance and traceability:
  - Rich processing metadata and ProbList/KBE history enable traceability and reproducibility; suitable for audits and change-detection workflows.
- Data interoperability:
  - Spatial framework tied to national cartography supports integration with other national datasets and facilitates cross-country comparisons.
- Uncertainty management:
  - KBEs and ProbList offer avenues for bespoke validation and uncertainty quantification; data stewards should apply local validation, especially for county-scale assessments.
- Access and licensing:
  - Open 1 km rasters via CEH gateway; full vector and 25 m data available on request (licensing may apply), enabling controlled distribution for governance and policy use.
- Use-case guidance:
  - For policy, habitat monitoring, and landscape planning, LCM2007 offers a robust backbone with documented lineage; for detailed habitat inventories or fine-scale planning, supplement with local validation and CS data where relevant.

# Key Takeaways for Data Stewards

- LCM2007 delivers a comprehensive, traceable UK land cover dataset with strong governance features, built on a robust spatial framework and extensive multi-sensor imagery.
- The combination of high-resolution cartography, segmentation-based processing, and knowledge-based enhancements improves thematic resolution and spatial coherence, though several habitat classes remain challenging due to spectral variance and boundary delineation.
- The dataset includes rich metadata (including ProbList and KBEs) that supports validation, reproducibility, and tailored uncertainty analysis.
- Clear licensing paths exist for data access, with emphasis on transparency and traceability to aid national policy, monitoring, and environmental management efforts.