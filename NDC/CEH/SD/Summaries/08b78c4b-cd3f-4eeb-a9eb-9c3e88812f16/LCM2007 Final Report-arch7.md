# Final Report for LCM2007 - the new UK land cover map

- Overview
  - First continuous parcel-based land cover map for the UK, with a linked suite of raster products (25 m and 1 km) and a rich vector product.
  - Maps 23 Broad Habitat-based land cover classes, aligned with UK Biodiversity Action Plan Broad Habitats; outputs include a vector product with extensive metadata, a 25 m raster, and 1 km aggregated rasters.
  - Spatial framework derived from national cartography (OS MasterMap for GB and equivalents for NI), enabling stable change detection and repeatable analyses.
  - Validation yields an overall accuracy of 83%; class accuracies vary due to spectral ambiguity and reliance on ancillary KBEs.

- Data sources and spatial frameworks
  - Primary spatial framework: OS MasterMap for GB and LPS Large-scale Vector for NI; additional integration with agricultural boundaries, urban outlines, soils, DEMs, and terrain derivatives.
  - Satellite imagery: Landsat, SPOT, and LISS-III (with AWIFS in some cases); multi-date composites and some single-date images used.
  - Ground reference: CEH field points and Countryside Survey (CS) Broad Habitat dataset used for cross-validation.
  - Knowledge-based inputs support hypothesis-driven refinements (soil, altitude, urban extent, etc.).

- Production of spatial frameworks
  - Great Britain: OS MasterMap-derived framework generalised to a minimum feature unit (MMU) of 0.5 ha and minimum width of 20 m; agricultural boundaries added to improve farmland delineation; image segments used to capture intra-field spectral variation.
  - Northern Ireland: LPS Large-scale Vector data generalised and integrated with image segmentation; agricultural boundaries integrated less extensively due to landscape differences.
  - Outcome: a continuous UK vector coverage enabling consistent spatial analysis and change detection.

- Image processing and segmentation
  - Pre-processing: cloud masking, atmospheric correction, geometrical rectification, and topographic correction; image composites created.
  - Segmentation: 60 composites segmented using a three-band approach; segments merged with OS MasterMap parcels and agricultural boundaries; NI segments include single-date segments.
  - Workflow is documented with traceable image-quality logs.

- Image classification and outputs
  - Parcel-based supervised maximum likelihood classification across 37 composites and 21 single-date images to classify into 23 LCM2007 classes tied to Broad Habitats.
  - Training sets derived from ground references; iterative reclassification; ProbList stores top class probabilities; manual edits used selectively.
  - Outputs:
    - Vector product: 23-class land cover with 10 polygon-level processing attributes plus detailed processing metadata.
    - 25 m raster: 23 LCM2007 classes.
    - 1 km rasters: for each class, (A) percentage cover and (B) dominant class across the 23 classes, plus 10 aggregate classes.

- Knowledge-based enhancements (KBE)
  - Purpose: resolve spectral confusion and increase thematic resolution beyond raw spectral signatures.
  - Inputs: urban context, coastal proximity, terrain, soil type; seven automated KBEs applied in sequence.
  - Benefits: improved discrimination for complex classes (e.g., various grasslands, bogs, montane habitats) and closer alignment with BH Broad Habitats.
  - Limitations: potential degradation of accuracy in some contexts; manual inspection and reversion capability to manage misclassifications.

- Scientific basis and product purpose
  - Provides a robust, consistent evidence base for habitat monitoring, biodiversity policy, landscape planning, and ecosystem services assessment.
  - Supports multi-scale analyses with a fixed spatial framework: 25 m raster, rich vector with processing history, and 1 km summaries.
  - Designed to assist policy, planning, and environmental monitoring across GB and NI, with cross-country comparability.

- Access, licensing, and data licensing
  - 1 km raster data sets available via the CEH Information Gateway.
  - Full vector and 25 m raster products available on request under licence from CEH (fees may apply).
  - Metadata-rich products enable users to track processing steps and applied KBEs for each polygon.

- Validation and accuracy
  - Overall accuracy: 83%.
  - Class-level accuracy varies; certain habitats (e.g., bog, some grasslands, coniferous woodland) show strong performance, while others (notably Neutral/Acid/Calcareous grasslands and some upland classes) show more confusion.
  - Both producer’s (map accuracy) and user’s (classification reliability) accuracies should be considered; aggregation (e.g., consolidating grassland classes) can improve reliability for some analyses.

- Comparison with Countryside Survey (CS)
  - CS 2007 data provide field-based baselines and national estimates; CS and LCM2007 agree variably across Broad Habitats.
  - Key issues driving differences:
    - Grassland: one-to-many relationships between observed land cover and Broad Habitats; spectral variability causes misclassifications.
    - Fen, Marsh and Swamp: large discrepancies due to mosaic nature and small patch sizes; some CS mappings map to rough grassland or acid grassland in LCM2007.
    - Boundary and linear features: CS maps include boundaries at finer scales; LCM2007 tends to dissolve narrow boundaries into adjacent polygons, affecting area estimates.
  - Grassland consolidation (treating all grasslands as a single class) improves CS-LCM correspondence substantially at broad levels.
  - Montane and upland habitats show particular discrepancies in some countries (e.g., Scotland) due to differences in survey classification and KBE interpretation.

- Key figures and product scope
  - 23 land cover classes, aggregated to 10 aggregate classes for 1 km rasters.
  - Continuous UK vector coverage with stable spatial units for change detection.
  - 25 m raster, 1 km raster products, and a metadata-rich vector product designed for policy, planning, and GIS analyses.

- Practical considerations for GIS specialists
  - Data structure: vector parcels with 10 polygon-level attributes, plus 25 m and 1 km raster products.
  - Change detection: fixed spatial framework based on generalised national cartography supports repeatable monitoring; be mindful of differences in spatial structure when comparing across CEH map versions.
  - Uncertainty handling: class-level accuracy varies; consider aggregation and cross-checking with KBEs; use ProbList for assessment and validation prior to analysis at subclass levels.
  - Access strategy: use CEH Information Gateway for 1 km data; request full vector/25 m products as needed, factoring licensing and potential fees.

- Practical implications for change detection and future work
  - Recognize challenges in reconciling LCM2007 with previous CEH maps due to differences in spatial structure and classification approaches.
  - Consider reorganising earlier CEH maps into a common spatial structure to facilitate robust change detection.
  - KBEs offer a pathway to improved classification but require careful validation and potential reversion if misclassifications occur.

- Example datasets and product formats
  - Vector product: parcel-based polygons with attributes including BH, BHSub, FieldCode, KBE history, ProbList, CorePixels, and construction metadata.
  - Raster products: 25 m and 1 km formats; 1 km rasters include both percentage cover and dominant class outputs.
  - Documented metadata and appendix tables describe class mappings, KBEs, and validation approaches.

- Broader context and impact
  - LCM2007 complements field surveys by providing coast-to-coast, wall-to-wall coverage; supports biodiversity policy, habitat connectivity analyses, and landscape-scale planning.
  - Serves as a reference framework for integrating multiple data sources (EO, field surveys, LiDAR, soils, climate) into policy-relevant land information systems.