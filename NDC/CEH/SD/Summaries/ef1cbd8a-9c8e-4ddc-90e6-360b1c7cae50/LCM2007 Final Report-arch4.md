# Final Report for LCM2007 - the new UK land cover map

## Overview
- Introduces a continuous parcel-based UK land cover map (LCM2007) with cross-border coverage.
- Maps Broad Habitats (BH) rather than land use, using a 23-class classification aligned to UK Biodiversity Action Plan. 
- Provides both vector (land parcels) and raster products at 25 m and 1 km resolutions.

## Data assets and products
- Vector land parcels with 23 LCM2007 classes and 17 Broad Habitat associations, plus extensive metadata (source images, processing steps, KBEs history, ProbList, etc.).
- 25 m raster: 23 LCM2007 classes.
- 1 km raster: two summaries per pixel — (A) percentage cover per LCM2007 class and (B) dominant class.
- Minimum mapping unit (MMU) of 0.5 ha; includes Knowledge-Based Enhancements (KBEs) and field-derived validation data.
- Cross-country comparisons with Countryside Survey (CS) data using UK-wide and country-level breakdowns.

## Data sources and spatial frameworks
- Satellite imagery: Landsat-TM5, IRS-LISS3, SPOT-4/5 (20–30 m), AWIFS (60 m) as backup; multi-date composites (summer–winter) cover ~91% of the UK.
- Ground truth and external data: CEH ground reference data, CS Broad Habitat data (2007), OS MasterMap GB, LPS Large-scale Vector (NI), soils, elevation, boundaries.
- Spatial frameworks: GB-wide parcel structure built from refined OS MasterMap topography and agricultural boundaries; NI framework incorporates available data but with limited agricultural boundary integration.
- MMU and generalisation: Generalisation aligns with 0.5 ha MMU; heavy generalisation stabilizes change detection; segmentation augmented with image segments and KBEs.

## Processing, segmentation, and classification
- Pre-processing: cloud masking, atmospheric/topographic correction, geo-registration, six-band composites.
- Image segmentation: multi-band segmentation per image to create image segments; integration with OSMM and agricultural boundaries to form a segment-based framework.
- Classification: parcel-based supervised maximum likelihood classification using 37 composites and 21 single-date images; iterative re-training with ground data.
- Knowledge-Based Enhancements (KBEs): seven automated rules (terrain, soils, urban context, coastal proximity, water, etc.) applied post-classification to refine parcel classes. KBEs are auditable and can be disabled/overridden for user needs.
- Change detection: cross-time mapping (LCM1990 to LCM2000 to LCM2007) is challenging due to class/structure differences and typical per-parcel errors (~20%), with reliable change separation not yet established.

## Product specification and delivery
- 23 land cover classes mapped to 17 Broad Habitats.
- Lands cover mapped, not land use; 0.5 ha MMU; extensive metadata available.
- Access:
  - 1 km raster products via CEH Information Gateway.
  - Full vector and 25 m raster products available on request (licence may apply).

## Quality assurance and validation
- Ground truth: 9,127 CEH points used for validation; overall accuracy around 83%.
- Class-level performance varies (e.g., Bog, Neutral Grassland, Montane Habitats show variable Producer’s and User’s accuracies).
- Countryside Survey (CS) comparisons:
  - UK-wide comparison shows ~62% correspondence at Broad Habitat level; ~76% at Broad Habitat Association level.
  - Higher agreement (~87–90%) when grassland is treated as a single class.
  - Patterns vary by country (England, Scotland, Wales, NI) due to habitat prevalence and CS methodology.
- Fen, Marsh and Swamp and grassland categories show notable divergence; differences partly due to spectral confusion, MMU effects, and how boundaries/linear features are treated.
- CS CS-1990/2000 comparisons and UK-level scaling considerations discussed; patch-size effects and mosaics highlighted as factors in CS vs LCM comparisons.

## UK Land Cover scope and cross-cutting insights
- UK-wide summary: majority of land is intensive (Arable and Horticulture plus Improved Grassland) or built-up areas; remaining area is semi-natural.
- Country-level variations reflect land-use patterns and habitat distributions (e.g., Scotland with larger woodland and montane habitats; NI with montane and freshwater patterns).
- LCM2007 vs LCM2000 differences show shifts in arable and semi-natural grassland proportions and uncertainties due to framework changes.

## Data governance, access, and interoperability
- Strong emphasis on metadata, processing traceability, and KBEs to support reproducibility and user confidence.
- Collaboration with Countryside Survey and European datasets (e.g., Corine) to position LCM2007 within broader policy and monitoring contexts.
- Access rights and licensing considerations noted; data may require licensing for full vector and 25 m products.

## Practical implications for data leaders
- A robust, scalable UK-wide land cover data system with a unified spatial framework improves governance, data fusion, and repeatable monitoring.
- KBEs and parcel-level metadata enhance transparency, enabling users to validate classifications against high-resolution imagery (informal Bayesian-style validation).
- The 1 km and 25 m products support both broad-scale modelling and finer-scale decision-making, with licensing considerations for data sharing.
- Change detection remains methodologically challenging; recommended approaches include aggregating classes, focusing on consistently mapped classes, or reorganising prior maps into a common spatial structure for comparability.

## Example areas and data products
- Example regions illustrate diverse habitats and landscapes (upland montane, calcareous grassland, urban, arable/fenland) and demonstrate LCM2007’s capacity to map complex mosaics.

## Key outcomes and implications for data strategy
- Establishes the first continuous UK parcel-based land cover dataset, enabling cross-border continuity and repeatable monitoring.
- Provides a transparent, multi-source data fusion framework with detailed provenance for end users and partners.
- Highlights the need for bespoke validation at sub-national scales and encourages integrated use with field surveys for enriched habitat understanding.
- Sets a foundation for future updates and cross-dataset interoperability, including European and national policy applications (biodiversity, climate, water, urban planning, etc.).

## Access and contact
- UK 1 km raster data: CEH Information Gateway.
- Full vector and 25 m raster data: CEH on request; licensing may apply.
- Contact: spatialdata@ceh.ac.uk or CEH data portal.