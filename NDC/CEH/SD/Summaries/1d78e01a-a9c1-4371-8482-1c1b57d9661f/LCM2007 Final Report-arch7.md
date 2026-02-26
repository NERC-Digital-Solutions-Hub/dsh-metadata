# Final Report for LCM2007 - the new UK land cover map

- A comprehensive, map-centered land cover product for the UK, aligned with Broad Habitat classifications and produced by CEH for Countryside Survey 2007. It integrates parcel-based vector data with 25 m and 1 km raster formats and uses multiple satellite sensors and knowledge-based enhancements to improve thematic resolution and cross-year comparability.

## What LCM2007 is and what it contains

- A continuous UK-wide land cover map mapped to 23 LCM2007 classes, aligned with Broad Habitats (BH) rather than land use.
- Two main data formats:
  - Vector product: 23 land cover classes with 10 processing attributes per parcel (e.g., spectral class, KBE history, provenance).
  - Raster products: 25 m resolution (23 classes) and 1 km resolution (percent cover and dominant class for the 23 classes).
- Metadata-rich polygons track processing steps and knowledge-based enhancements (KBEs) to support auditability and reproducibility.
- Nine-processing-chunk approach ensures UK-wide seamless coverage and cross-boundary consistency.

## Spatial framework and data sources

- Spatial framework
  - Great Britain (GB): OS MasterMap topography layer refined with agricultural boundaries; aims to preserve stable land parcels for change detection.
  - Northern Ireland (NI): LPS Large-scale Vector data, generalised and integrated with image segments.
- External and ancillary data
  - National cartography: OS MasterMap (GB), LPS vector (NI).
  - Agricultural boundaries, urban classifications, soils, and hydrology datasets from UK government bodies.
  - DEM: NEXTMap Britain; soils from NSRI and others.
- Imagery and ground data
  - Core sensors: Landsat-TM5, IRS-LISS3, SPOT-4/5 (20–30 m), AWIFS as backup.
  - 91% of GB mapped from 2-date summer-winter composites; remainder from single-date imagery.
  - Ground references: CEH field points (2006–2008) and Countryside Survey Broad Habitats data (2007).

## Production workflow and KBEs

- Image pre-processing
  - Cloud masking, atmospheric/topographic corrections, geo-registration, and composites; full traceability via processing logs.
- Segmentation and spatial framework assembly
  - Segments integrated with OSMM/NI cartography and agricultural boundaries; NI required polygon generation from line data; segmentation augmented boundaries.
- Image segmentation and classification
  - 37 composite images and 21 single-date images; segmentation uses winter NIR, summer red, summer MIR bands; parcel-based supervised maximum likelihood classification with ground references.
  - Iterative refinement with feedback; hole-filling as needed.
- Knowledge-based enhancements (KBEs)
  - Contextual data (terrain, soils, coastal/urban context, water) applied to reclassify parcels and improve thematic resolution.
  - KBEs affect roughly 20% of parcels; changes are recorded in vector attributes for auditability and reversion if needed.
- Final assembly and QA
  - UK-wide coverage ensured; QA includes ground reference validation (9127 points) with overall accuracy around 83%.

## Data products, access and provenance

- Primary products
  - Vector product: 23 land cover classes with 10 processing attributes.
  - 25 m raster product: 23 LCM2007 classes.
  - 1 km rasters: two summaries per class (percent cover and dominant class) for country-wide statistics.
- Access and licensing
  - 1 km rasters via CEH Information Gateway.
  - Full vector and 25 m rasters available on request under licence from CEH; licensing fees may apply.
  - Rich metadata for every polygon, including processing steps and KBEs, enabling reproducibility and audit trails.

## Quality assurance, accuracy and validation

- Validation
  - 9127 ground reference polygons used; overall accuracy approx. 83%.
  - Class-level producer’s and user’s accuracies vary; some classes show high producer’s accuracy but lower user’s accuracy due to spectral ambiguity and KBEs.
  - Notable variability across habitats (e.g., certain grasslands, bogs, montane habitats) due to spectral overlap and limited representative samples.
- Validation outputs
  - Results presented with producer’s vs user’s accuracy; KBEs and processing histories are retained in the vector product for audit and reclassification decisions.

## Comparison with Countryside Survey 2007

- Overall agreement
  - Broad Habitat (BH) correspondence GB-wide: about 62%.
  - Broad Habitat Association (BHA) correspondence: about 76%.
- Key drivers of differences
  - Differences in what CS defines as Arable and Horticulture, grassland classifications, and spatial boundaries.
  - Spectral confusion and the inclusion of boundary/linear features in LCM2007’s classifications.
  - Boundary and MMU differences: CS maps many small features that fall below LCM2007’s minimum mappable unit, causing field-boundary-field mappings in CS to translate into field-field mappings in LCM2007.
  - Fen, Marsh and Swamp discrepancies: CS records mosaics that LCM2007 often splits into Rough Grassland, Acid/Calcareous/Neutral Grassland; spectral mosaic complexity and patch size effects contribute to divergence.
- Implications
  - Grassland categories are particularly challenging due to one-to-many relationships with BH types; Broad Habitat Association rules were developed to improve cross-walk interpretation.
  - When comparing across products, consider aggregation (e.g., treating grasslands as broader groups) and the BHA framework to interpret correspondences.

## Change mapping and monitoring

- Challenges
  - Substantial methodological differences across LCM generations (1990, 2000, 2007) in spatial structure (parcels vs segments) and class definitions.
  - Classification errors (often ~20%) can obscure real changes.
- Practical stance
  - No definitive change-detection method established within this release.
  - Suggested approaches include focusing on aggregated classes, using the BHA framework, or reorganizing earlier maps into a common real-world spatial structure to enable robust change detection.

## Practical implications for GIS specialists

- Robust UK-wide data for habitat monitoring, biodiversity policy support, landscape planning, and ecosystem services assessments.
- Dual-format availability supports both map-based visualization (vector with metadata) and raster-based analysis (25 m and 1 km).
- KBEs can enhance thematic resolution but require attention to provenance and potential need to revert KBEs for transparency or bespoke analyses.
- Change detection requires careful handling of differing class definitions, spatial frameworks, and acknowledged classification uncertainties; consider cross-year reconciliation via the BHA framework and aggregated classes.

## Access points and quick references

- Access to 1 km rasters: CEH Information Gateway.
- Full vector and 25 m raster data: license-on-request from CEH (data portal via CEH website; licensing inquiries via spatialdata@ceh.ac.uk).
- Key outputs: vector product (23 classes with 10 attributes), 25 m raster, and 1 km summary rasters.
- Key performance indicator: ~83% overall accuracy; class-specific accuracies vary with spectral separability and KBEs.
- Core chapters for more detail: Introduction, classification and KBEs, QA, comparison with Countryside Survey, and product ranges.

Note: This summary synthesizes the provided content, including sections on dissimilar area estimates, discussion, UK land cover summaries, data products, QA, CS comparison, change mapping considerations, and practical GIS implications as they relate to LCM2007.