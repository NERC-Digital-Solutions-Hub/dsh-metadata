# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview and purpose
- Parcel-based UK land cover dataset using 23 classes aligned with UK Biodiversity Action Plan Broad Habitats.
- Provides both vector (polygons with rich metadata) and raster (25m and 1km) products to support diverse applications.
- Distinguishes land cover (not strictly land use); notes that some land use cannot be inferred from cover (e.g., grass recreation vs grazed grass).
- Aims to support a broad user community with multiple data formats and resolutions.

## Data products and structure
- Vector data set
  - Approximately 8.6 million polygons for Great Britain and 0.9 million for Northern Ireland.
  - Each polygon has 10 attributes (Table 1): Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (display class 1-23), KBE (Knowledge-Based Enhancement), ProbList (top 5 spectral class probabilities), CorePixels, Construct, TotPixels.
  - Parcel_ID provides a unique, persistent label for unambiguous communication.
  - Broad Habitat sub-classes (BHSub) provide additional detail but are not guaranteed to meet QA standards at sub-class level.
- Raster data sets
  - 25m and 1km products derived from the vector data.
  - 23-class (LCM2007) 25m raster; 1km rasters include Dominant cover, and Percentage cover for both LCM2007 classes and Aggregate classes.
  - 1km products allow UK-wide modeling and integration with other datasets (e.g., meteorology, species distribution).
- Data formats and scales
  - Vector: polygon features with extensive metadata; large file sizes.
  - Raster: 25m and 1km grids; GB and NI provided separately with respective projections.
- Color mapping and documentation
  - Appendix 3 provides a standard LCM2007 color mapping for visualization.
  - Appendix 2 documents relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
  - Appendix 1 lists detailed LCM2007 classes with brief definitions.

## Key classifications and decision rules
- 23 LCM2007 classes based on Broad Habitats (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Improved Grassland, Semi-natural grassland, Bog, Montane Habitats, Inland Rock, Saltwater, Freshwater, Urban, Suburban, etc.).
- Certain Broad Habitats are subdivided to improve interpretability (e.g., Built-up Areas into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Saltmarsh).
- The dataset maps land cover rather than definitive land use; some land-use distinctions may not be discernible spectrally.
- Minimum mappable unit: parcels <0.5 ha or linear features <20 m dissolved into surrounding landscape during production.

## Methodology and validation
- Source imagery: summer-winter composite satellite images at 20–30 m resolution; generally classified as land cover.
- Spatial framework: use of OS MasterMap/large-scale vector data to align parcel boundaries with real-world objects; segmentation enhances object-based mapping.
- Ground reference validation: average thematic accuracy of 83% against 9127 ground-reference polygons; local discrepancies can occur.
- Metadata and QA: vector products include a rich metadata history, KBE processing history, and a ProbList (top 5 spectral classes) to support user validation.
- Relationships and caveats
  - Broad Habitat sub-classes (BHSub) are informative but not guaranteed to be as accurate as the main LCM2007 class (INCODE/INTCODE).
  - Users are advised to perform own validation when using Broad Habitat sub-classes.

## Data access and licensing
- 1km raster data sets are available via the CEH Information Gateway.
- Full vector product and 25m raster product licenses are available on request; fees may apply.
- Access channels:
  - CEH Information Gateway (1km rasters)
  - CEH data contact (spatialdata@ceh.ac.uk) for licensing details
- Projections
  - Great Britain: British National Grid (OSGB36)
  - Northern Ireland: Irish National Grid (and moving toward ITM for NI)

## Practical considerations and use cases
- Data volume and management
  - Vector data: large files (~10 million polygons; 10 attributes each).
  - Raster data: 25m GB 1.36 GB; NI 46 MB; 1km products range 21 MB to 49 KB.
- Use cases
  - Regional/National land cover mapping and monitoring.
  - Integrating land cover with climate, meteorology, species distribution, or habitat suitability models.
  - Multi-resolution analyses: 25m for detailed area-level studies; 1km for UK-scale analyses; vector for rich attribute interrogation.
- Guidelines for use
  - Refer to the Final Report for LCM2007 (Morton et al., 2011) for production methodology and limitations.
  - When aggregating to Broad Habitat sub-classes, validate locally due to QA limitations at the subclass level.
  - Maintain Parcel_ID for clear communication and data traceability.

## Related authoritative materials
- Morton, D. et al. (2011) Final Report for LCM2007 – the new UK Land Cover Map (Countryside Survey Technical Report No. 11/07).
- Jackson, D.L. (2000) Guidance on interpretation of Biodiversity Broad Habitat Classification (JNCC Report 307).
- Appendices
  - Appendix 1: LCM2007 Classes (descriptions and Broad Habitat mapping)
  - Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes
  - Appendix 3: Colour mapping recipe for LCM2007 classes

## Summary for data-support workflows
- Start with 1km rasters for broad UK-scale analyses; use 25m rasters or vector for detailed, object-based investigations.
- Retain Parcel_ID in vector products to preserve traceability and enable precise cross-referencing across datasets.
- Use ProbList to guide validation of spectral class hypotheses; rely on INTCODE as the recommended display class and QA reference.
- When disseminating outputs, consider providing both aggregated 1km products and higher-resolution 25m or vector outputs for end users who require detail and metadata.
- Plan for licensing steps early if access to the full vector or 25m products is needed.