# Final Report for LCM2007 - the new UK land cover map

## Overview for Data Leaders
- LCM2007 delivers the first continuous parcel-based UK land cover map, with a Vector (parcels) product and derived 25 m and 1 km raster products, designed to support policy, biodiversity, landscape planning, and ecosystem services.
- It uses a unified spatial framework derived from detailed national cartography (OS MasterMap, LPS Large-scale Vector) and multi-temporal imagery, enabling cross-border consistency and potential for change detection.

## Core data assets and architecture
- Vector product
  - Land parcels (polygons) with attributes: area, source images, Broad Habitat (BH), processing history, Construct, ProbList, and KBE history.
  - Broad Habitat sub-classes (BHSub) and FieldCode included for detailed validation and user interpretation.
- Raster products
  - 25 m resolution raster with 23 LCM2007 classes.
  - 1 km raster products: either percentage cover per class or dominant class per 1 km pixel.
- Metadata and traceability
  - Comprehensive processing history and KBEs (Knowledge-Based Enhancements) documented at polygon level; ProbList provides top spectral class candidates.

## Data sources and spatial framework
- Spatial framework
  - Great Britain: OS MasterMap topography generalised to MMU/MFW; agricultural boundaries integrated; image segmentation augmented boundaries.
  - Northern Ireland: Large-scale vector data generalised and integrated with image segments; urban boundaries via demographic data; agricultural boundaries largely not integrated.
- Data foundations
  - Satellite imagery: Landsat, SPOT, LISS-III, AWIFS; multiple date composites used for improved spectral consistency.
  - External data: national cartography, digital elevation models, soils, urban and agricultural boundaries, and other environmental layers.
  - Ground reference: CEH data (2006–2008) for training/validation; Countryside Survey Broad Habitat data for 2007 comparison.

## Processing, classification, and enhancements
- Pre-processing
  - Cloud/shadow masking, atmospheric correction, georeferencing, topographic correction; multi-date composites created.
- Image segmentation and integration
  - 60 composites segmented; segmentation leverages multispectral inputs (e.g., NIR, MIR, red) and is integrated with OSMM boundaries and agricultural boundaries to create homogeneous spectral regions.
- Classification approach
  - Parcel-based supervised maximum likelihood classification (MLC) applied to 37 composites and 21 single-date images, mapped to Broad Habitat classes.
  - Training areas from ground reference; iterative refinement with human review; probabilities for top five spectral classes captured.
- Knowledge-Based Enhancements (KBEs)
  - Seven automated KBEs applied sequentially to reclass parcels using contextual/ancillary data (urban context, proximity to coast, terrain, soils, etc.).
  - KBEs resolve spectral confusions and improve thematic resolution (e.g., differentiating various grasslands via soils and urban context).
  - About 20% of parcels are affected by KBEs; original spectral class preserved in vector attributes with documentation to disable specific KBEs if desired.

## Data quality, validation, and comparability
- Validation results
  - Ground reference: 9,127 polygons; overall accuracy around 83% across LCM2007 classes.
  - Class-level validation varies; notable examples include Bog, Improved Grassland, and other grassland types.
  - Validation context includes Countryside Survey (CS) 2007 squares and UK Broad Habitat estimates; CS-based correspondence tables show substantial alignment at aggregate and BH levels but variability across classes.
- Key comparability findings
  - Similar area estimates occur for Broadleaved woodland, Acid Grassland, Inland Rock.
  - Dissimilar area estimates occur for Arable and Horticulture, Improved Grassland, Neutral Grassland, Dwarf Shrub Heath, Bog, Montane habitats, and coastal habitats.
  - Differences explained by: definitional differences between CS and LCM2007, spectral confusions, inclusion of boundaries/linear features, MMU-related effects, and temporal imagery ranges that affect crop phenology and classification.
- Change detection and temporal considerations
  - Changing class definitions and spatial structures across LCM1990, LCM2000, and LCM2007 complicate change mapping.
  - Caution advised when using LCM2007 for change detection; consider aggregating classes or re-structuring past maps to a common framework.

## UK-wide distribution, country variations, and comparisons
- Broad distribution
  - UK: over half the area mapped as intensive agriculture or built-up areas; remaining mosaic includes coniferous woodland and semi-natural habitats.
  - England: highest intensive land-use share; Scotland: largest share of coniferous woodland and montane habitats.
- Temporal and spatial comparisons
  - LCM2007 shows differences from LCM2000 in arable and semi-natural grassland shares; some shifts may reflect changes in spatial framework and improved boundary delineation.

## Applications, impact, and policy relevance
- Scientific and policy utilities
  - Habitat monitoring, biodiversity assessment, habitat connectivity, landscape planning, and catchment management.
  - Serves as a contextual base map for higher-resolution habitat mapping and as a consistent UK framework for cross-country comparisons.
- Data integration
  - When combined with soils, terrain, urban boundaries, and other datasets, enhances land-cover interpretation and policy outputs.

## Accessibility, licensing, and stewardship
- Access pathways
  - 1 km raster datasets available via the CEH Information Gateway.
  - Full vector product and 25 m raster available on request; licensing may apply.
- Licensing and usage considerations
  - Some applications incur license fees; details available from CEH.

## Limitations and future directions
- Current limitations
  - Spectral limitations for complex habitats (e.g., grasslands with diverse species; montane habitats) and small patches limit full thematic resolution.
  - Dependence on external KBEs and soil data can affect class-level accuracy.
  - Change detection remains challenging due to differing spatial structures and spectral variability across years.
- Recommended enhancements
  - Refine KBEs, improve discrimination of grassland types, and advance change-detection methodologies.
  - Validate and integrate updated Countryside Survey data; explore additional data sources to better resolve fen and mosaic habitats.
  - Reorganize prior CEH maps into a common spatial framework based on real-world land-use units to facilitate robust change analysis.

## Broad Habitat Association (BHA) and validation context
- The report uses Broad Habitat Association rules to interpret associations between LC classes and CS data for improved crosswalks.
- Key associations address complex continua (e.g., Bog ↔ Dwarf Shrub Heath ↔ Acid Grassland) and account for seasonality, spatial structure, and boundary effects.
- BHA considerations help explain non-reciprocal correspondences and provide guidance for interpreting mismatches.

## Data products recap
- Vector: polygons with 10 processing attributes, ProbList, KBE history, BH/Sub-class, and FieldCode metadata.
- Raster: 25 m (23 classes) and 1 km (percent or dominant class) products.
- Accessibility: CEH Information Gateway for 1 km; vector/25 m on request; licensing applicable.

## Concluding note
- LCM2007 delivers a robust, cross-border, parcel-based UK land cover framework with rich metadata and validation context, enabling improved policy support and national-scale monitoring while acknowledging and guiding users through its limitations and areas for refinement.